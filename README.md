# Dart Basic Instructions

```dart
void main() {
    String nombre = 'Camilo';
    print('Hola $nombre');
}
```

# Flutter Basic Tutorial

## Step 1

```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: Text('Hello World'),
        ),
      ),
    );
  }
}
```

## Step 2

```dart
        body: Counter(),
      ),
    );
  }
}

class Counter extends StatefulWidget {
  _CounterState createState() => _CounterState();
}

class _CounterState extends State<Counter> {
  
  Widget build(BuildContext context) {
    return Text('Hello World');
  }
}
```

## Step 3

```dart
Widget build(BuildContext context) {
    return Center(
      child: Column(
        children: <Widget>[
          Text('Hello Word'),
        ],
      ),
    );
  }
```

## Step 4
```dart
children: <Widget>[
    Image.network('https://raw.githubusercontent.com/caev03/LabMovilesFlutter/master/TAs/###.jpg'),
]
```


## Final Step

```dart
import 'package:flutter/material.dart';

class Counter extends StatefulWidget {
  _CounterState createState() => _CounterState();
}

class _CounterState extends State<Counter> {
  int val;

  void initState() {
    super.initState();
    val = 0;
  }

  void change() {
    setState(() {
      val += 1;
      val = val%4;
    });
  }

  Widget build(BuildContext context) {
    return Center(
        child: Column(
          children: <Widget>[
            Image.network('https://raw.githubusercontent.com/caev03/LabMovilesFlutter/master/TAs/$val.jpg'),
            MaterialButton(
              color: Theme.of(context).primaryColor,
              child: Text(
                'Add',
                style: TextStyle(color: Colors.white),
              ),
              onPressed: () => change(),
            ),
          ],
        ),
      );
  }
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Counter(),
      );
  }
}

void main() {
  runApp(MyApp());
}
```