# flutter_application_4

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

# Widget Dasar

- Void Main
    
    ```dart
    void main() {
      runApp(const MyApp());
    }
    ```
    
    Merupakan fungsi utama dan dijalankan paling pertama pada sebuah aplikasi flutter yang didalamnya terdapat fungsi runApp() yang menjalan kan sebuah class MyApp().

- Class MyApp
    
    Class yang memiliki inheritance atau perawisan dari class StatelessWidget yang memiliki constructor dan @overriding method Widget build() yang mengembalikan sebuah kelas widget beruapa MetarialApp() terdapat bebrapa field pada Material app seperti title, theme dan home. fokus pada home yang mengembalikan sebuah class MyHomePage.
    
    ```dart
    class MyApp extends StatelessWidget {
      const MyApp({super.key});
    
      // This widget is the root of your application.
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          title: 'Flutter Demo',
          theme: ThemeData(
            // This is the theme of your application.
            //
            // TRY THIS: Try running your application with "flutter run". You'll see
            // the application has a purple toolbar. Then, without quitting the app,
            // try changing the seedColor in the colorScheme below to Colors.green
            // and then invoke "hot reload" (save your changes or press the "hot
            // reload" button in a Flutter-supported IDE, or press "r" if you used
            // the command line to start the app).
            //
            // Notice that the counter didn't reset back to zero; the application
            // state is not lost during the reload. To reset the state, use hot
            // restart instead.
            //
            // This works for code too, not just values: Most code changes can be
            // tested with just a hot reload.
            colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
            useMaterial3: true,
          ),
          home: const MyHomePage(title: 'Flutter Demo Home Page'),
        );
      }
    }
    ```
    
    ![code-snapshot2.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/abcb1cf6-3200-4445-9cf9-e3c071b63f38/3aabe9b8-35e9-48a1-b7b3-fe52d437d25d/code-snapshot2.png)

- Class MyHomePage
    
    class MyHomePage memiliki inheritance dari class StatefulWidget agar class ini memiliki perbuhan pada sebuah screen dan lebih dinamis. StatefulWidget biasanya memiliki class turunan yang berheritance ke class State<MyHomePage> generic agar bisa melakukan sebuah perubahan pada screens pada class _MyHomePageState mengembalikan sebuah Widget Scaffold.
    
    ```dart
    class MyHomePage extends StatefulWidget {
      const MyHomePage({super.key, required this.title});
    
      // This widget is the home page of your application. It is stateful, meaning
      // that it has a State object (defined below) that contains fields that affect
      // how it looks.
    
      // This class is the configuration for the state. It holds the values (in this
      // case the title) provided by the parent (in this case the App widget) and
      // used by the build method of the State. Fields in a Widget subclass are
      // always marked "final".
    
      final String title;
    
      @override
      State<MyHomePage> createState() => _MyHomePageState();
    }
    
    class _MyHomePageState extends State<MyHomePage> {
      int _counter = 0;
    
      void _incrementCounter() {
        setState(() {
          // This call to setState tells the Flutter framework that something has
          // changed in this State, which causes it to rerun the build method below
          // so that the display can reflect the updated values. If we changed
          // _counter without calling setState(), then the build method would not be
          // called again, and so nothing would appear to happen.
          _counter++;
        });
      }
    
      @override
      Widget build(BuildContext context) {
        // This method is rerun every time setState is called, for instance as done
        // by the _incrementCounter method above.
        //
        // The Flutter framework has been optimized to make rerunning build methods
        // fast, so that you can just rebuild anything that needs updating rather
        // than having to individually change instances of widgets.
        return Scaffold(
          appBar: AppBar(
            // TRY THIS: Try changing the color here to a specific color (to
            // Colors.amber, perhaps?) and trigger a hot reload to see the AppBar
            // change color while the other colors stay the same.
            backgroundColor: Theme.of(context).colorScheme.inversePrimary,
            // Here we take the value from the MyHomePage object that was created by
            // the App.build method, and use it to set our appbar title.
            title: Text(widget.title),
          ),
          body: Center(
            // Center is a layout widget. It takes a single child and positions it
            // in the middle of the parent.
            child: Column(
              // Column is also a layout widget. It takes a list of children and
              // arranges them vertically. By default, it sizes itself to fit its
              // children horizontally, and tries to be as tall as its parent.
              //
              // Column has various properties to control how it sizes itself and
              // how it positions its children. Here we use mainAxisAlignment to
              // center the children vertically; the main axis here is the vertical
              // axis because Columns are vertical (the cross axis would be
              // horizontal).
              //
              // TRY THIS: Invoke "debug painting" (choose the "Toggle Debug Paint"
              // action in the IDE, or press "p" in the console), to see the
              // wireframe for each widget.
              mainAxisAlignment: MainAxisAlignment.center,
              children: <Widget>[
                const Text(
                  'You have pushed the button this many times:',
                ),
                Text(
                  '$_counter',
                  style: Theme.of(context).textTheme.headlineMedium,
                ),
              ],
            ),
          ),
          floatingActionButton: FloatingActionButton(
            onPressed: _incrementCounter,
            tooltip: 'Increment',
            child: const Icon(Icons.add),
          ), // This trailing comma makes auto-formatting nicer for build methods.
        );
      }
    }
    ```
    
    ![code-snapshot3.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/abcb1cf6-3200-4445-9cf9-e3c071b63f38/08be034d-aa46-404e-a20a-0d6a8897f8f0/code-snapshot3.png)

====================================================================================
![Capture.PNG](https://prod-files-secure.s3.us-west-2.amazonaws.com/abcb1cf6-3200-4445-9cf9-e3c071b63f38/1d3a1d8c-700f-4ddb-9c79-baffb67b7a9b/Capture.png)

![Capture2.PNG](https://prod-files-secure.s3.us-west-2.amazonaws.com/abcb1cf6-3200-4445-9cf9-e3c071b63f38/72248313-b623-43e6-b861-9adf29b92903/Capture2.png)

setiap detail atau ui tau desain atau bentuk pada flutter disebut Widget. pembuatan pertama kali sebuah dasar widget seperti di layar kita harus mengimport package matretial.dart

```dart
import 'package:flutter/material.dart';
```

lalu membuat main function dimana main ada fungsi yang akan di eksekusi pertama kali saat aplikasi dijalankan

```dart
void main(){
}
```

lalu menjalankan sebuah fungsi runApp yang berada pada package:flutter/meterial.dart.

```dart
import 'package:flutter/material.dart';

void main(){
	runApp();
}
```

didalam runApp() harus mengirimkan sebuah parameter berupa class yang akan di jalankan ketika aplikasi dijalankan akan tetpai class yang akan di jalankan harus extends class StatefulWidget atau StatefulWidget.

```dart
import 'package:flutter/material.dart'

void main(){
	runApp(MyApp());
}

class MyApp extends StatelessWidget{
}
```

di dalam class yang extends atau inheritance ke sebuah class StatelessWidget harus memiliki method overiding yaitu Widget build(BuildContext context){} yang mengembalikan sebuah Widget dasar yaitu MaterialApp();. MatrialApp merupakan Widget dasar ketika ingin membuat sebuah tampilan atau widget. didalam MaterapApp terdapat attribute home yaitu kesuluran tampilan yang membutuhkan sebuah parameter seperti Scaffold().

```dart
import 'package:flutter/material.dart'

void main(){
	runApp(MyApp());
}

class MyApp extends StatelessWidget{

	@override
	Widget build(BuildContext context){
		return const MaterialApp(
			home: Scaffold()
		);
	}
}
```

didalam Widget scaffold terdapat beberapa attribute seperti appBar yang memerlukan parameter berupa AppBar(). didalam widget AppBar() terdapat banyak attribute yang bisa digunakan untuk membangun widget untuk appBar pada bagian paling atas layar seperti attribute title: yang memerlukan parameter beruapa Widget kembali. attribute berikutnya yaitu body: yang merlukan parameter berupa widget kembali.

```dart
import 'package:flutter/material.dart'

void main(){
	runApp(MyApp());
}

class MyApp extends StatelessWidget{

	@override
	Widget build(BuildContext context){
		return const MaterialApp(
			home: Scaffold(
				appBar: AppBar(
					title: Text('Hello World');
				)
				body: Center(
					child: Text('Hello World');
				)
			)
		);
	}
}
```

![code-snapshot4.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/abcb1cf6-3200-4445-9cf9-e3c071b63f38/adf039d5-d6e6-44fa-92ac-fe7919f5e1ae/code-snapshot4.png)