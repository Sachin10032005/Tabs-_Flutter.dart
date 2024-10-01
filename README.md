# Tabs-_Flutter.dart

This Flutter app demonstrates the usage of tabs with a `TabBar` and `TabBarView`. The app has three tabs: Home, Search, and Profile, each represented by an icon and corresponding text.

## Code:

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return DefaultTabController(
      length: 3, // Number of tabs
      child: Scaffold(
        appBar: AppBar(
          title: Text('Flutter Tabs Example'),
          bottom: TabBar(
            tabs: [
              Tab(icon: Icon(Icons.home), text: 'Home'),
              Tab(icon: Icon(Icons.search), text: 'Search'),
              Tab(icon: Icon(Icons.person), text: 'Profile'),
            ],
          ),
        ),
        body: TabBarView(
          children: [
            Icon(Icons.home, size: 100),
            Icon(Icons.search, size: 100),
            Icon(Icons.person, size: 100),
          ],
        ),
      ),
    );
  }
}
```
## Features:
1.TabBar: Displays three tabs (Home, Search, Profile) with icons and text.

2.TabBarView: Provides different content for each tab.

3.DefaultTabController: Manages the state and switching between tabs automatically.


