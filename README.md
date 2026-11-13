# My First Flutter App

Lab 1 by Elisabeth(I): a Flutter counter app, built and pushed to Git.

## What I did
- Installed the toolchain. `flutter doctor` shows no red X.
- Ran the app on a device.
- Changed the text to "Hello Elisabeth!", changed the theme colour and the app title.
- Added a second `Text` in the `Column`. After pressing `r`, it appeared and the counter kept its value (hot reload keeps state).
- Printed the screen width with `debugPrint`: **411.43 dp** on my phone.

## Screenshots
See the `docs/` folder: the running app and the `flutter doctor` output.

## What I learned and what blocked me
I learned how hot reload works and that dp is a logical unit that varies between phones. My main problem was that I first put the `MediaQuery` lines in the `build` method of `MyApp`. They belong in `_MyHomePageState`, the `build` that returns `Scaffold`, because `MediaQuery` is only available below `MaterialApp`.