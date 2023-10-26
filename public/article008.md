---
title: hideCurrentSnackBar()の使いどころ
tags:
  - 'Flutter3'
  - 'SnackBar'
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: true
---
## hideCurrentSnackBarの使いどころがわからなかったので調べてみた

```dart
ScaffoldMessenger.of(context).hideCurrentSnackBar();
```

と

```dart
ScaffoldMessenger.of(context).hideCurrentSnackBar();
```

の違いがよーわからん…。

**私、気になります！**

**よろしい、ならば検証だ。**

と、いうわけで、検証してみました。

## まずは公式の定義を見てみよう

[公式APIドキュメント](https://api.flutter.dev/flutter/material/ScaffoldMessengerState-class.html)

clearSnackBars method

Removes all the snackBars currently in queue by clearing the queue and running normal exit animation on the current snackBar.

Implementation

```dart
void clearSnackBars() {
  if (_snackBars.isEmpty || _snackBarController!.status == AnimationStatus.dismissed) {
    return;
  }
  final ScaffoldFeatureController<SnackBar, SnackBarClosedReason> currentSnackbar = _snackBars.first;
  _snackBars.clear();
  _snackBars.add(currentSnackbar);
  hideCurrentSnackBar();
}
```

…お？
clearSnackBars()の最後でhideCurrentSnackBar()呼び出しとるやんけ

一方、hideCurrentSnackBar()はこうなってる

---

hideCurrentSnackBar method

Removes the current SnackBar by running its normal exit animation.

The closed completer is called after the animation is complete.

Implementation

```dart
void hideCurrentSnackBar({ SnackBarClosedReason reason = SnackBarClosedReason.hide }) {
  if (_snackBars.isEmpty || _snackBarController!.status == AnimationStatus.dismissed) {
    return;
  }
  final Completer<SnackBarClosedReason> completer = _snackBars.first._completer;
  if (_accessibleNavigation!) {
    _snackBarController!.value = 0.0;
    completer.complete(reason);
  } else {
    _snackBarController!.reverse().then<void>((void value) {
      assert(mounted);
      if (!completer.isCompleted) {
        completer.complete(reason);
      }
    });
  }
  _snackBarTimer?.cancel();
  _snackBarTimer = null;
}
```

どうやら、hideCurrentSnackBar()は現在のSnackBarを非表示にするだけで、SnackBar自体はキューに残っているようだ。
（というか、素直にメソッドの命名通り）
