# measurements

A package providing basic classes for working with measurements such as Length and Mass. All provided classes provide
the means to perform conversions, calculations and comparisons using objects.

## Example

Conversions:
```dart
import 'package:measurements/measurements.dart';

void main(List<String> arguments) async {
  Length heightOfEverest = Length.fromMetres(8848);
  print("Height of Everest (in metres): ${heightOfEverest.inMetres}.");
  print("Height of Everest (in kilometres): ${heightOfEverest.inKilometres}.");
  print("Height of Everest (in yards): ${heightOfEverest.inYards}.");
  print("Height of Everest (in miles): ${heightOfEverest.inMiles}.");
}
```

Calculations:
```dart
import 'package:measurements/measurements.dart';

void main(List<String> arguments) async {
  Length a = Length.fromCentimetres(87);
  Length b = Length.fromCentimetres(43);
  print("a + b is ${(a + b).inCentimetres} centimetres");//130
  print("a - b is ${(a - b).inCentimetres} centimetres.");//44
  print("a * b is ${(a * b).inCentimetres} centimetres.");//3741
  print("a / b is ${(a / b).inCentimetres} centimetres.");//2.02325581395
}
```

Comparisons:
```dart
import 'package:measurements/measurements.dart';

void main(List<String> arguments) async {
  Mass elephantWeight = Mass.fromKilograms(5400);
  Mass zebraWeight = Mass.fromKilograms(380);
  if (elephantWeight == zebraWeight) {
    print("An elephant and a Zebra have the same weight.");
  } else if (zebraWeight < elephantWeight) {
    Mass difference = elephantWeight - zebraWeight;
    print("An elephant is ${difference.inPounds} pounds heavier than a zebra.");
  } else {
    Mass difference = zebraWeight - elephantWeight;
    print("A Zebra is ${difference.inPounds} pounds heavier than an elephant.");
  }
}
```

## Available Measurements

The available classes as well as those that will hopefully be implemented soon are listed below. If you are willing to 
speed up the process of implementing missing functionality, [contributions](#Contributing) are most welcome.

- [x] Length
- [x] Mass
- [ ] Area
- [ ] DataTransferRate
- [ ] DigitalStorage
- [ ] Energy
- [ ] Frequency
- [ ] Pressure
- [ ] Speed
- [ ] Temperature
- [ ] Volume

## Contributing

There are couple of ways in which you can contribute.

- Propose any feature, enhancement
- Report a bug
- Fix a bug
- Participate in a discussion and help in decision making
- Write and improve some **documentation**. Documentation is super critical and its importance
  cannot be overstated!
- Send in a Pull Request :-)