# Flutter Animation List

## Features

* Infinite scroll
* Custom child widgets

## Supported platforms

* Flutter Android
* Flutter iOS
* Flutter web
* Flutter desktop

## Installation

Add `flutter_animation_list: <later-version>` to your `pubspec.yaml` dependencies. And import it:

```
import 'package:flutter_animation_list/flutter_animation_list.dart';
```

#### How to Use ####

#Create List

```
final List<String> data = List<String>.generate(100, (int index) => "Index $index").toList();

```

# Animation List

```          
AnimationList(
          duration: 10000,
          reBounceDepth: 10.0,
          children: data.map((item) {
            //return widget
             return _buildTile(item);
          }).toList(),
        ),
```

# Return Widget

```
Widget _buildTile(String title) {
    return Container(
        height: 100,
        margin: const EdgeInsets.symmetric(horizontal: 10, vertical: 5),
        decoration: BoxDecoration(
          borderRadius: const BorderRadius.all(Radius.circular(8)),
          color: Colors.blue.shade100,
          border: Border.all(color: Colors.grey.shade50)
        ),
      child: Center(
        child: Text(
          title
        ),
      ),
    );
  }
```

## Screenshot

![prefetch](animation_list.gif)