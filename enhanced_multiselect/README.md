# enhanced_multiselect

### A simple multiselect dropdown but enhanced. It provide a concise way to create a Multi Selct ComboBox/SelectBox

![alt Demo](https://miro.medium.com/max/2548/1*94vYfiJSmzMaWIX0zfm9oA.gif "Demo")

# Usage

add it to `pubspec.yaml`

```yaml
dependencies:
  flutter:
    sdk: flutter
  enhanced_multiselect: # use latest version, currently is 0.1.0
```

import it

```dart
// Imports all Widgets included in [enhanced_multiselect] package
import 'package:enhanced_multiselect/enhanced_multiselect.dart';
```

Add the `DropDownMultiSelect` widget to your build method

```dart
// Import enhanced_multiselect
import 'package:enhanced_multiselect/enhanced_multiselect.dart';


class Home extends StatefulWidget {
  const Home({Key? key}) : super(key: key);

  @override
  _HomeState createState() => _HomeState();
}

class _HomeState extends State<Home> {

  List<String> selected = [];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: Center(
      child: Padding(
        padding: const EdgeInsets.all(20.0),
        // DropDownMultiSelect comes from multiselect
        child: DropDownMultiSelect(
          onChanged: (List<String> x) {
            setState(() {
              selected =x;
            });
          },
          options: ['a' , 'b' , 'c' , 'd'],
          selectedValues: selected,
          whenEmpty: 'Select Something',
        ),
      ),
    ));
  }
}

```

And that is it. You will have a working multiselect DropDown with no effort at all.  
\
&nbsp;
\
&nbsp;
\
&nbsp;

> PS: multiselect is planned to be a collection of multi-select widgets. I will add other functionality based on the needs of the community
