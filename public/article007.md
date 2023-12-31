---
title: TOEIC399点のワイがUdemy教材を英語で学んでみた
tags:
  - 英語
  - ポエム
  - Flutter
  - プログラミング学習
  - Udemy
private: false
updated_at: '2023-10-27T01:18:17+09:00'
id: d2938db1495049214e9b
organization_url_name: null
slide: false
ignorePublish: false
---

## TL;DR

プログラミング学習の上でやっぱ英語力は高い方がいいよね、という話
と、 段階に合わせた学習方法の提案的なもの
(あくまで「英語学習法」ではなくプログラミング学習の付随)

## 注意

- この記事はほぼポエムです
- Flutterの技術的な話は一切ありません
- TOEIC399点は筆者が数年前(I myでーす)に無勉強で臨んだ際の得点[^1]
- 「その結果こんなに伸びたぜ！」という話でもない？
- 学習の効率性や手法には、合う合わないがあるのが前提

[^1]:べ、別に試験中に寝落ちたわけじゃないんだからね！

## 読んでほしい人

- 英語の技術情報やエラーメッセージを全文翻訳や検索に丸投げしてる
- 英語力あった方がいいとは思うけど、優先度は低いかなと思ってる
- 今日び翻訳ツールが優秀だから、英語力なくてもなんとかなるよね
- なんなら変数名やコミットメッセージだってAIが提案してくれるし[^2]？

[^2]:Gitのcommitメッセージはチーム・会社の文化次第では日本語でいいと思う

**そんな時代が私にもありました。**

## 概要

Udemyの外国人講師(ドイツ人)によるFlutter教材を、英語音声&英語字幕で受講**中**の所感

### この記事を書こうと思った経緯

最近最もよく聴いてるPodcast番組「**ひまじんプログラマーの週末エンジニアリングレッスン**」から受けた刺激もあり、*日常的に*プログラミング学習に英語学習を組み込もう
（からの）→　気づきを記事に書いてみようと思い立った。

https://podcastranking.jp/1601084785

学習中のFlutter教材 on(in?)[^3] Udemy
[^3]: onの方が適切 or どっちでもOK! な気がする  が、母語話者に聞いてみたい

https://www.udemy.com/course/learn-flutter-dart-to-build-ios-android-apps/

### 自己紹介

長いブランクからプログラミングを再開した、発生して半世紀が経とうとしてる現状無職。
異世界で無双する予定はない。
動物画像を見てニヤニヤするのが好き。蓼食う虫も愛づるいたち。
年齢的には限りなくシニアに近いジュニアエンジニア(未経験ではない)
最近はFlutterを学習中 & 今のところIT企業への応募は全滅中ﾋｬｯﾊｰ!

### 今回の流れ

今回の結論に至るまでのステップ。
なんなら丸々飛ばして「結論」に進んで可。
<details open>
<summary>よろしければどうぞ</summary>

Golangの学習を一旦中断し、Flutterの学習を3年ぶり（コロナ自粛騒動以来）で再開した。
Flutterのバージョンは1→一気に3になってた。
けど、書籍はそんなに良さげのが無いように思った。[^4]
[^4]: 筆者が知らないだけかもなので、むしろオススメしてほすい。

で、Udemyで動画教材を3本買った。
そのうちの1つが、ドイツ人講師による教材。
まぁ日本語字幕ついてるみたいだし、内容良さげなのでとりあえず買ってみようと思った。
~~しょっちゅうやってる~~セール価格も今夜までだし？

ところがである。
日本語字幕の質はお世辞にも良くはない。
「…あれ？今の長〜い英文まるまる翻訳飛んでるよね？」
「え？この日本語どう考えてもおかしくね？」
「いや、むしろそこは日本語訳しないでクレヨン」

```shell
(講師の発言) "questions_screen.dart"
 ↓
(日本語字幕) 「質問画面start」
```

**Oh...**

といった調子である。

**結果的に**、「コレなら英語字幕の方がまだコスト低いんじゃね？」と思い、**英語音声＆英語字幕**でちょっと進めてみることにした。（ダメ元で）

…あれ？
案外聴き取れるし、英語字幕もまぁまぁついていけてんぞ？
てか、英文字幕の方もけっこー間違ってんぞコレ…[^5]
[^5]:仮に英語の意味を勘違いしていたとしても、画面には講師のコードが見えてる&Gitにソースコードもあるので、最悪でも動かなくなることはない。

というわけで、途中から英語音声＆英語字幕(ときどき字幕を英語と日本語で切り替え)で学習中。
英語字幕だと消化にかかる時間が倍以上にもなるかと思ったけど、そこまでのコスト増でもなさげ。

なら、この機会にFlutterでアプリ作りながら、英語教材を英語のままで普通に消化できるようにもなれんじゃね？
なんならゆくゆくは再生速度上げたりもできんじゃね？
などと思い始めた。[^6]
[^6]:現状は逆に、再生速度を0.9~0.8倍に落としてもいいかもしれない。

最近特別「語学学習」にコストかけたつもりはないけど、なんか英語音声・英語字幕に案外ついてけてるぞワシ？！
もしかして今2度目のTOEIC受けたら500点台くらいには上がってんじゃね？
とも思った。

実際、翻訳ツールを介さずに英文のリーディング、さらには英語音声のヒアリング力が高まれば、ことプログラミング学習に絞った上でもいろんなコストが下げられる。[^7]
[^7]:基本的には日本人エンジニアに必須なのはリーディング力だが、ヒアリング力もあると便利。読む>>聴く,書く>>話す、の順だと思う。
もしかしたら向こう半世紀のうちにはもっと翻訳ツールが進化して、もはや誰も語学学習の必要なく世界各国の人とリアルタイムコミュニケーションできる時代が来るかもしれんけど。
</details>

### 結論

「英語を学習しよう」と考えなくても、プログラミング学習の過程で英語力は自然と(ある程度は)身につく気がする。
ただし、その時の自分の英語力に合わせた方法を選ぶ必要がある。

- 最低限「読む (&聴く)」力はある程度身に付いている
  - ときどき「英語の勉強をする」でなく、日常的に(適切な粒度で)英語に触れる機会を増やす
  - 主言語が英語の教材にチャレンジしてみる
    - 例えばUdemyの場合、外国人講師の教材を選ぶ
    - 英語音声＆英語字幕で学習する
  - 全文翻訳は極力しない。基本は単語単位で調べる。
  - 知らなかった単語はその時調べて終わりでなく、一定期間反復する
    - 人は忘れる。忘れるのだ…
    - 例えばスマホアプリの単語帳などに登録する
    - 例えばAnkiなどのSRSを使う　(なん・・・だと・・・！？)
      - 上の提案はGitHub Copilotによって書かれたもの
      - 筆者も今知ったので、これから試してみる

もしUdemyなどの動画教材はよく使うけど、英語音声・英語字幕はちょっと厳しい、読めるけど聴くのは全然無理…と感じる場合は、以下のような下準備から始めると良いかもしれない。

- 普段から英文や英語音声に日常的に触れる機会を増やす
  - ただ「聴き流すだけの英語教材」はオススメしない
- SVOCとかの文法は筆者は特に意識してない
- 英語を脳内で同時翻訳しようとせず、前から順番に理解するよう努める(日本語訳は語順が変わる)
  - ここが日本人にとっての一番のハードルなのかもしれない
- そのうち「いったん脳内インタプリタで日本語に翻訳して〜」ではなく、講師の発話＆英語字幕の前から順に理解が追い付くようになる
  - その状態になったら、以後は基本的に未知の単語を調べるだけ

---
上のリストは当初マインドマップの形で貼ろうかと思ったけどやめた。
でも、学習方針を決める上での現在地確認にはいいかもしれない。

### 謝辞的なもの

最近なんだかんだで一番よく聴く音声番組になった「**ひまじんプログラマーの週末エンジニアリングレッスン**」(長ぇ！) #ひまプロ #ひまじんプログラマー
「世の中に中堅エンジニアを増やそう」
「駆け出しエンジニアが中堅エンジニアになるための情報を発信する」
がコンセプト？のポッドキャスト。

最近読む本の多くはこの番組内で紹介されるものを買ったり、図書館で予約したりしてる。
Git内部の仕組みの話や著名なすご偉人エンジニャーの面白エピソード、変数の命名、設計やテスト、対人スキルや失敗談など、これからエンジニアを目指そうとする人〜中堅エンジニアに必要な知識やスキルを身につけるための情報が多い。
筆者もまだ最新話に追い付いていないが、「エンジニアならでは」の面白エピソードも、単純にクスッと笑える掛け合いも多く、おいしくてつよくなる番組。
非常に勉強になり、楽しみにもなっている。

三者三様に個性的で面白いメンバーの中でも、今回のエピソードはこの方の影響が強いかもしれない。
「エラーメッセージ全文丸投げする奴は粉末にする[^9]」という発言に恐れ慄き、身を粉にして頑張りました(？)

[^9]:もちろんギャグ。の筈。(旧)Twitter垢プロフィールの英文にも表れているとおり、非常にユーモアのある方。たぶん。

https://x.com/ittoku_ksm?s=20

### おわりに

英語に苦手意識のあるエンジニア、英語学習もやらなきゃ、とは思ってるものの、まぁ別に翻訳ツールでなんとかやってけてるしなぁ…といったエンジニアの参考になれば幸いです。

技術に関するシェアじゃないものの、久々のQiita投稿。
読んでいただいた方ありがとうございますた。
