# Flutter.js Transpile JSX to dart widgets

[![NPM Version][npm-image]][npm-url]


## Install

```
npm i -g flutterjsx
```


> Coming soon ... (on development)

Hello Home !

As you know <a href='https://flutter.dev'>Flutter</a> comes with dirty syntax, therefore I decided to start developing jsx transpiler for flutter.

## Usage

> cd to your flutter app path

and Run: 

> $ flutterjx

1 - Flutter Widget (flutter_app/lib/HomePage.dart):
```
import 'package:flutter/material.dart';
class HomePageView extends StatelessWidget {
  static final jsxView = "HomePageView.jsx";
  static final spaces = "  ";

  build(BuildContext context) {
  }
  // afterBuild
}

```
jsxView is required.
spaces is optional.
// afterBuild is required.

2 -JSX (flutter_app/lib/HomePageView.jsx):
```
const style = {
  wrapper: {
    padding: "32.0",
    margin: { top: 30, bottom: 10 },
    color: "#000000",
  },
  text: {
    fontSize: 20,
  },
};

export default (
  <Container {...style.wrapper}>
    <Text style={style.text} text={"This is a simple text"} />
  </Container>
);
```

3 - Output

> I wish to make it prettier in future.

```
import 'package:flutter/material.dart';

class HomePageView extends StatelessWidget {
  static final jsxView = "HomePageView.jsx";
  static final spaces = "  ";

  build(BuildContext context) {
    return Container(
      child: Text("This is a simple text",
          style: TextStyle(
            fontSize: 15,
            color: Color(0xFF111111),
          )),
      padding: EdgeInsets.all(32.0),
      margin: EdgeInsets.only(top: 30, bottom: 10),
      color: Colors.red,
    );
  }
  // afterBuild
}

```

That's it Javascript + Flutter will kill it.


[npm-image]: https://img.shields.io/npm/v/flutterjsx.svg?style=flat
[npm-url]: https://www.npmjs.com/package/flutterjsx

## License

WTF.
