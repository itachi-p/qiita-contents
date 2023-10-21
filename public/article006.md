---
title: 'Flutter 1 -> 3で躓いたCocoaPodsのアップデート'
tags:
  - Flutter3
  - iOS
  - CocoaPods
  - Gem
  - rbenv
private: false
updated_at: ''
id: null
organization_url_name: null
slide: false
ignorePublish: true # 執筆中断(記事執筆に必要なログや画像の保存ミス)
---

## Flutterのバージョンを1から一気に3へ

### やったこと

Flutter3をインストール後、`flutter doctor` の結果がオールグリーンになるまで

- 2020年を最後に更新してなかった**Flutter**をバージョン1から間の2を飛ばして3にバージョンアップ
- 依存関係にある諸々を一旦アンイストールはせず全てバージョンアップした
- その際、何ヶ所かで詰まった
  - 特にiOS(Xcode)とAndroidStudio
  - 最後に残ったCocoaPods1.9.1->1.13.0のエラーではRuby、Gem、rbenvも関わってきた
  - rbenvを介してGemでActive Supportのバージョンを7.1.0から7.0.8に下げて解決

[参考記事]
[CocoaPodsのバージョンアップの方法](https://qiita.com/Yuta/items/a20f4ea3207635b4ef9e)
[After updating Cocoapods to 1.13.0 it throws error](https://stackoverflow.com/questions/77236339/after-updating-cocoapods-to-1-13-0-it-throws-error)

![事後](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/342237/59ae0c6c-4c90-32f7-1e0b-2b6ad441e4b2.png)

Syntax highlighting:

```dart:main.dart
void main() {
  print('Hello, World!');
}
```
