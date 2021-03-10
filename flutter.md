# Flutter
## Build beautiful applications for mobile



[![N|Solid](https://flutter.dev/assets/flutter-lockup-1caf6476beed76adec3c477586da54de6b552b2f42108ec5bc68dc63bae2df75.png)](https://flutter.dev/)

> Flutter is Google’s UI toolkit for
> beautiful, natively compiled applications for mobile,
> web, and desktop from a single codebase.

Made by[![Build Status](https://flutter.dev/assets/homepage/logo-google-fb903d829602dd356c500efc9dddf50b58f227ff1d88373c6caa64f997b663d3.svg)]()




[![Build Status](https://flutter.dev/assets/homepage/icon-development-02b120c5632de8bcfebaa9af8d93938c403217b5be8d40d596af576c4ed85aa6.svg)]()
##  Fast Development

- Paint your app to life in milliseconds with Stateful Hot Reload.
- Use a rich set of fully-customizable widgets to build native interfaces in minutes.
- Flutter's hot reload helps you quickly and easily experiment, build UIs, add features, and fix bugs faster. Experience sub-second reload times without losing state on emulators, simulators, and hardware.
[Learn More](https://flutter.dev/docs/development/tools/hot-reload)

[![Build Status](https://flutter.dev/assets/homepage/icon-ui-5917d09ef0d8f9538615b4281870960b865bba4c8b6926b5adaef91433af0b07.svg)]()
##  Expressive and Flexible UI

- Quickly ship features with a focus on native end-user experiences. 
- Layered architecture allows for full customization, which results in incredibly fast rendering and expressive and flexible designs.
- Delight your users with Flutter's built-in beautiful Material Design and Cupertino (iOS-flavor) widgets, rich motion APIs, smooth natural scrolling, and platform awareness.
[Browse the widget catalog](https://flutter.dev/docs/development/ui/widgets)

[![Build Status](https://flutter.dev/assets/homepage/icon-performance-680fb3687109ba7ea0c22627da3a9fa761944ae7b521468003b932aa9133ca5b.svg)]()
##  Native Performance

- Flutter’s widgets incorporate all critical platform differences such as scrolling, navigation, icons and fonts.
- your Flutter code is compiled to native ARM machine code using Dart's native compilers.
- Flutter’s widgets incorporate all critical platform differences such as scrolling, navigation, icons and fonts to provide full native performance on both iOS and Android.
[Examples of apps built with Flutter](https://flutter.dev/showcase)
Demo design inspired by [Aurélien Salomon](https://dribbble.com/aureliensalomon)'s [Google Newsstand Navigation Pattern](https://dribbble.com/shots/2940231-Google-Newsstand-Navigation-Pattern)
##  Learn from developers
- Watch these videos to learn from Google and developers as you build with Flutter.
[Visit our YouTube playlist](https://www.youtube.com/flutterdev)

##  Install Flutter today.
- It’s free and open source.
[Get Started](https://flutter.dev/docs/get-started/install)

# news
[![N|Solid](https://flutter.dev/assets/homepage/news-1-91bbb7b1f5fd7f145f357fe153b11b757f48f773823bb12efa3b2272ef7b2f67.png)]()
Announcing Flutter 2
[Read more](https://developers.googleblog.com/2021/03/announcing-flutter-2.html)

[![N|Solid](https://flutter.dev/assets/homepage/news-2-1cd501064a5a907ab1b66a67ab96b181040a4a19bea60395d614244fe06f72b0.png)]()
Announcing stable web
[Read more](https://medium.com/flutter/flutter-web-support-hits-the-stable-milestone-d6b84e83b425)




This text you see here is *actually- written in Markdown! To get a feel
for Markdown's syntax, type some text into the left window and
watch the results in the right.

## Try Flutter in your browser
```

## Code

import 'package:flutter/material.dart';

void main() async {
  runApp(
    MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: MyApp(),
      ),
    ),
  );
}

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp>
    with SingleTickerProviderStateMixin {
  AnimationController controller;
  Animation<double> animation;

  @override
  void initState() {
    super.initState();

    controller = AnimationController(
      duration: Duration(seconds: 1),
      vsync: this,
    );

    animation = CurvedAnimation(
      parent: controller,
      curve: Curves.easeInOutCubic,
    ).drive(Tween(begin: 0, end: 2));
  }

  @override
  void dispose() {
    controller.dispose();
    super.dispose();
  }

  @override
  Widget build(BuildContext context) {
    return GestureDetector(
      onTap: () {
        controller
          ..reset()
          ..forward();
      },
      child: RotationTransition(
        turns: animation,
        child: Stack(
          children: [
            Positioned.fill(
              child: FlutterLogo(),
            ),
            Center(
              child: Text(
                'Click me!',
                style: TextStyle(
                  fontSize: 60.0,
                  fontWeight: FontWeight.bold,
                ),
              ),
            ),
          ],
        ),
      ),
    );
  }
}
















  

