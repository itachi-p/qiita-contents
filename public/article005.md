---
title: 'testing QiitaCLI: artuicue2023_01'
tags:
  - Gem
  - rbenv
  - CocoaPods
  - Flutter3
  - QiitaCLI
private: false
updated_at: '2023-10-07T16:22:40+09:00'
id: a14db39530af376f507d
organization_url_name: null
slide: false
ignorePublish: false
---
# new article body

QiitaCLIのテスト用記事

## new article body h2

後でタグに示した内容の記事を書く

### new article body h3

*hoge* _hoge_ **hoge** __hoge__ ***hoge***
~~huga~~

==huga==
h~2~SO~4~
sinθ^2^ + cosθ^2^ = 1

<details>
<summary>audio contents:</summary>
  
- [ゆるコンピュータ科学ラジオ](https://www.youtube.com/@yurucom)
- [ひまじんプログラマーの週末エンジニアリングレッスン](https://open.spotify.com/show/2uv9mONog0nr9q5YJJsvIt?si=e79fc99f3ecd4b8f)
- [エンジニアストーリー by Qiita](https://pitpa.jp/playlist/engineerstory)
- [PIVOT Growth Drivers](https://open.spotify.com/episode/4XoYSjNDuDrM8EMC1RqbPo)
</details>

#画像
![ビスカッチャ](https://livedoor.sp.blogimg.jp/karapaia_zaeega/imgs/c/6/c6fd2293.jpg)  

#リンク
[Markdown記法 チートシート](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)

#コードブロック(シンタックスハイライト)

```ruby:qiita.rb
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

```diff_javascript:hogehuga.js
function fancyAlert(arg) {
  if(arg) {
-   console.log('huga')
+   console.log('hoge')
    $.facebox({div:'#foo'})
  }
}
```

#数式
```math
\frac{1}{n} \sum_{i=1}^{n} x_{i}^{2}
```

#表
| hoge | huga | piyo |
|:----:|:----:|:----:|
|  1   |  2   |  3   |
|  4   |  5   |  6   |
|  7   |  8   |  9   |

#引用
> これは引用です
> > これは二重引用です
> 1. これは引用です
> 2. これは引用です
> * これは引用です

#水平線
---

#箇条書き
- 箇条書き1
- 箇条書き2
- 箇条書き3
  - 箇条書き3-1
  - 箇条書き3-2
- 箇条書き4

#番号付き箇条書き
1. 番号付き箇条書き1
2. 番号付き箇条書き2
3. 番号付き箇条書き3
   1. 番号付き箇条書き3-1
   2. 番号付き箇条書き3-2
4. 番号付き箇条書き4

#チェックボックス
- [ ] チェックボックス1
- [x] チェックボックス2

`#ffce44`
`rgb(255,0,0)`
`rgba(0,255,0,0.4)`
`hsl(100, 10%, 10%)`
`hsla(100, 24%, 40%, 0.5)`
