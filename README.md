# This package is no longer maintained.

Supports using Dartium during development for projects using Dart v1.

For projects using Dart v2, this package is no longer needed.
See the [Dart 2 migration guide](https://webdev.dartlang.org/dart-2) for
details.

# dart.js

The dart.js file is used in Dart browser apps to check for native Dart support
and either (a) bootstrap Dartium or (b) load compiled JS instead.

1. Add the following to your pubspec.yaml:

    ```yaml
    dev_dependencies:
      browser: ^0.10.0
    ```

2. Run pub install.

3. Use a relative script tag in your html to the installed version:

    ```html
    <script src="packages/browser/dart.js"></script>
    ```

If you do not wish to use pub, you may host a copy of this file locally instead.
In this case, you will need to update it yourself as necessary.  We reserve the
right to move the old file in the repository, so we no longer recommend linking
to it directly.

# interop.js

This script was required for dart:js interop to work, but it is no longer
needed. The functionality is now supported by dart:js directly.

If you previously had a script such as this, please remove it:

```html
<script src="packages/browser/interop.js"></script>
```
