## スライドを作ろう

* Author: か
* Twitter: [@ka_](https://twitter.com/ka_)
* GitHub: [@kaosf](https://github.com/kaosf)
* Homepage: [http://kaosfield.net](http://kaosfield.net)


reveal.js の紹介


"reveal.js" でググって下さい


Markdown で書く方法


[GitHub kaosf reveal.js-2.5.0-customized](https://github.com/kaosf/reveal.js-2.5.0-customized) を参考にして下さい

index.markdown を編集すればいいようになっています


確認方法ですが index.html をブラウザで開くだけでは多分ダメです

オススメは

```
python -m SimpleHTTPServer
```

で簡易 Web サーバ立ててブラウザから `http://localhost:8000` にアクセスする方法


ソース見せます

[https://raw.githubusercontent.com/kaosf/20140712-ksgstudy-lt/gh-pages/index.markdown](https://raw.githubusercontent.com/kaosf/20140712-ksgstudy-lt/gh-pages/index.markdown)


簡単！


デモスライド


# 見出し1だよ

## 見出し2だよ

### 見出し3だよ

```
# 見出し1だよ

## 見出し2だよ

### 見出し3だよ
```


普通の文章だよ

```
普通の文章だよ
```


* 順序無しリストアイテム1だよ
* 順序無しリストアイテム2だよ
* 順序無しリストアイテム3だよ

```
* 順序無しリストアイテム1だよ
* 順序無しリストアイテム2だよ
* 順序無しリストアイテム3だよ
```


1. 順序付きリストアイテム1だよ
1. 順序付きリストアイテム2だよ
1. 順序付きリストアイテム3だよ

```
1. 順序付きリストアイテム1だよ
1. 順序付きリストアイテム2だよ
1. 順序付きリストアイテム3だよ
```

とりあえず全部 ``1.`` って書いておくの順序入れ替えに強いのでオススメ


```
<div>
  <p>This is a paragraph.</p>
</div>
```

    ```
    <div>
      <p>This is a paragraph.</p>
    </div>
    ```

ハイライトを賢くする方法募集中


Pandoc とか使う方法もあるよ


Ubuntu の場合

```
sudo apt-get install haskell-platform
```

```
echo 'export PATH=$HOME/.cabal/bin:$PATH' >> $HOME/.bash_profile
source $HOME/.bash_profile
```

`.bash_profile` の代わりに `.zshenv` とかにするのは適宜

```
cabal update
cabal install pandoc
```

```
pandoc index.markdown -t revealjs > slide.html
```

これで後は `slide.html` を reveal.js の `index.html` の

```
      <div class="slides">
        <!-- ここ -->
      </div>
```

に挿入すればOK


LT時に本当に言いたかったことを改めて補足します


## かつて思っていたこと

* PowerPoint とか Impress とか起動してマウスをちまちま動かしながらスライド作るのってダルい
* Vim だけでスライド作れたらいいのに
* スライドだって大別すれば構造化文書の一つだし Markdown 書くだけでスライドが作れてもいいじゃないか


それ reveal.js で出来るよ(2013年に知った)


参考

[JavaScript - なんかかっこいいプレゼンテーションテンプレートを探しているならreveal.js使ってみろって - Qiita](http://qiita.com/ryurock/items/9c6de36b9d6a716e7992)


テキストファイルでスライドが作れることで得られた利点

* バージョン管理しやすい


つまり以下の利点が得られることでもあります

* ミスを PullRequest で修正してもらえる


## HTML になることの利点

* ブラウザさえあれば見える(※でもさすがにIE8とかでは動かないみたいです)
  * SlideShare や SpeakerDeck のようにモッサリしない
* ハンズオン時に使いやすい
  * 公開しておいて URL を示しておけば講師のスライドのページ送りにいちいち合わせる必要がない
  * スマホでも割と綺麗に見える


今までスライド作成に対して非常に重かった腰が90%くらい軽くなりました


## 目標

今って Twitter Bootstrap デザインの Web ページを見ると「また Bootstrap か(笑)」みたいになりますよね

それと同じように「また reveal.js か(笑)」みたいになって欲しいです


そりゃ当然不便なこともあるけどテキストエディタだけでスライドが作れるのってマジお手軽嬉しい


ということでどんどん皆さんも文字書いていってスライド作ってLTしましょう

画像貼り付けも普通に出来ます

ていうか HTML で出来ることは理論上何でも出来ますね


おわり

当然このスライドも [GitHub 上に公開されてます](https://github.com/kaosf/20140712-ksgstudy-lt) ので誤字脱字の指摘から内容の追加まで任意のご意見を Issues と PullRequest でお待ちしております
