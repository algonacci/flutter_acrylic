<h1 align="center"><a href="https://github.com/alexmercerind/flutter_acrylic">flutter_acrylic</a></h1>
<h4 align="center">Acrylic & aero blur effect on Flutter Windows.</h4>


## Installation

Mention in your `pubspec.yaml`.
```yaml
dependencies:
  ...
  flutter_acrylic: ^0.0.1
```

## Example

You can [download](https://github.com/alexmercerind/flutter_acrylic/releases/download/v0.0.1/flutter_acrylic_example.zip) & try out the example application.

<img src='https://github.com/alexmercerind/flutter_acrylic/blob/assets/acrylic.jpg' height='512'></img>

## Documentation

### Acrylic

Initialize the plugin inside the main method.

```dart
void main() {
  WidgetsFlutterBinding.ensureInitialized();
  Acrylic.initialize();
  runApp(MyApp());
}
```

Apply the effect to Flutter window.

```dart
Acrylic.setEffect(
  effect: AcrylicEffect.aero,
  gradientColor: this.color
);
```

Following effects are available.
- `AcrylicEffect.disabled`.
- `AcrylicEffect.solid`.
- `AcrylicEffect.transparent`.
- `AcrylicEffect.aero`.
- `AcrylicEffect.acrylic`.

### Window

Other utility features offered by the plugin.

Enter fullscreen.

```dart
Window.enterFullscreen();
```

Exit fullscreen.

```dart
Window.exitFullscreen();
```

More features coming soon.

## Notes

This plugin exposes the undocumented `SetWindowCompositionAttribute` API from `user32.dll` on Windows 10.
Learn more at [Rafael Rivera](https://github.com/riverar)'s amazing blog post about this [here](https://withinrafael.com/2015/07/08/adding-the-aero-glass-blur-to-your-windows-10-apps).

In most cases, you might wanna render custom window frame because the blur effect might leak outside the window boundary.
You can use [bitsdojo_window](https://github.com/bitsdojo/bitsdojo_window) to make a custom window for your Flutter application.

Currently `AcrylicEffect.acrylic` causes lag on window drag, this is a bug in Windows itself. Latest Windows 11 build appears to be fixing this issue.

You can see the [example](https://github.com/alexmercerind/flutter_acrylic/blob/master/example/lib/main.dart) application for further details.

## License

MIT License. Contributions welcomed. 

## More

#### Checkout other awesome projects for Flutter on Windows
(Irrespective of order)
- [bitsdojo_window](https://github.com/bitsdojo/bitsdojo_window)
  - A Flutter package that makes it easy to customize and work with your Flutter desktop app window.
- [fluent_ui](https://github.com/bdlukaa/fluent_ui)
  - Implements Microsoft's Fluent Design System in Flutter.

<img src='https://github.com/alexmercerind/flutter_acrylic/blob/assets/aero.jpg' height='512'></img>

Aero blur effect.

<img src='https://github.com/alexmercerind/flutter_acrylic/blob/assets/transparent.jpg' height='512'></img>

Transparent Flutter window.
