# tabler_sass.dart

This package contains the [Tabler](https://github.com/tabler/tabler) sass source files to make it easy to import tabler ui components.

## Usage

1\. In the `pubspec.yaml` file add the `tabler_sass.dart` and `sass_builder` dependencies.

```yaml
...
depencencies:
  ...
  tabler_sass.dart: ^0.0.32 # change for the latest version
  ...
dev_dependencies:
  # place sass_builder before any other builder
  sass_builder: ^2..1.1 # change for the latest version
  ...
```

2\. Create a `style.scss` in your `web` directory, change the variables you want and import `package:tabler_sass.dart/scss/tabler`

```scss
@import 'variables';
@import 'package:tabler_sass.dart/scss/tabler';
```

>Importing `package:tabler_sass.dart/scss/tabler` imports everything, including bootstrap.

In your `index.html` add this to `<head>` tag

```html
<link rel="stylesheet" href="style.css">
```

3\. Run `webdev serve` or `webdev build`, No configs required.  

## Importing component required styles

In `avatar_component.dart`

```dart
...
@Component(
    selector: 'avatar_component',
    // Notice how we're pointing to .css and not .scss,
    // This is because sass_builder automatically builds it for us.
    styleUrls: ['avatar_component.css'],
    templateUrl: 'avatar_component.html',
)
class AvatarComponent {
...
```

In `avatar_component.scss`

```scss
@import 'variables'
@import 'package:tabler_sass.dart/scss/dashboard/avatar';
...
```

In `avatar_component.html`

```html
<span class="avatar" style="background-image: url(<URL>)"></span>
```

## Credits

Inspired by: [bootstrap_sass](https://github.com/dart-league/bootstrap_sass)  
Tabler Dashboard UI kit: the [Tabler Authors](https://github.com/tabler/tabler/graphs/contributors) and [codecalm.net](codecalm.net)

## Bugs and feature requests

Have a bug or a feature request to [tabler_sass.dart](https://github.com/devkabiir/tabler_sass.dart)?  
Please open a new issue [here](https://github.com/devkabiir/tabler_sass.dart/issues/new)

## Copyright and license

Code and documentation Copyright 2018 Dinesh Ahuja ([devkabiir](https://dev.kabiir.me))  
Code released under the [MIT License](https://github.com/devkabiir/tabler_sass.dart/blob/master/LICENSE).

Code and documentation copyright 2018 the [Tabler Authors](https://github.com/tabler/tabler/graphs/contributors) and [codecalm.net](codecalm.net). Code released under the MIT License.
