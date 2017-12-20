6 chairs, each costing $35, totals $210

* Vimでは簡単な計算にアクセスすることができる`<Ctrl-R>=`で計算できる
* 文字コードによって入力することができる`<Ctrl-v>{number}`。文字コードは`ga`で取得することができる。

* Vimでは文字コードを指定することで文字コードごと入力が可能である
* `digraph-table`を用いることで複雑な特殊文字を入力できる（特殊文字を使いたくなるきっかけがあまり無いので微妙だが） 

## 置換モードで既存のテキストを上書き
```
Typing in Insert mode extends the line. But in Replace mode
the line length doesn't change.
```


* `R`で置換モードに入る。文字をどんどん置換することができるので、打ち間違えや修正時に消してから入力するというより早い

* `v`でヴィジュアルモードに入れる。`V`で行志向。`<Ctrl-v>`でブロック志向。`gv`で前回選択したものと同じ範囲を再度選択できる。

* `o`　ビジュアルモード中に別の端点に移動できる。

`Select from here to here`

* `e` 前方の単語の終わりに移動。`ge`は後方の単語の終わりに移動。`w`,`b`などと対比される。

```
def fib(n):
    a, b = 0, 1
    while a < n:
        print a,
        a, b = b, a+b
fib(42)
```

```
<a href="#">one</a>
<a href="#">two</a>
<a href="#">three</a>
```
* `vit`でタグの内部をビジュアルに選択できる
* 問題点は、vitだと三文字と固定されてしまうので、ここでは`gUit`とノーマルモードで処理を行う。

```
Chapter     |  Page
-------------------
Normal mode |    15
Insert mode |    31
Visual mode |    44
```

* `<Ctrl-v>`で矩形選択に入れる。
* `V`で行の選択になる

```
li.one   a{ background-image: url('/components/sprite.png'); }
li.two   a{ background-image: url('/components/sprite.png'); }
li.three a{ background-image: url('/components/sprite.png'); }
```
* 矩形選択モードを使うと実質複数カーソルのようなことができる

```
var foo = 1;
var bar = 'a';
var foobar = foo + bar;
```
* ビジュアルモードを利用することで複数行に同じ操作を行うこともできる

```
<html><head><title>Pragmatic Vim</title>

</head>
  <body><h1>Pragmatic Vim</h1>
</body></html>
```

* Exコマンド `:1`で先頭行に移動
* `:3d`で指定行を削除
* `:2,5p`で範囲指定
* vimでは範囲指定中に`:`を押すとその領域に対して処理が行える

```
Shopping list
    Hardware Store
        Buy new hammer
    Beauty Parlor
        Buy nail polish remover
        Buy nails
```

* `:<from>t<to>`で行を指定箇所にコピー
* `:<from>m<to>`で移動もできる

```
var foo = 1;
var bar = 'a';
var baz = 'z';
var foobar = foo + bar;
var foobarbaz = foo + bar + baz;
```

* `A;``j.`の繰り返しでもできるが、矩形選択し、`<area>normal .`でも同じことができる
* コマンドモードは補完機能がある

```
var counter;
for (counter=1; counter <= 10; counter++) {
  // do something with counter
};
```

* `<C-r><C-w>でカーソルが存在している場所の文字をインサートできる
* コマンドモードにはヒストリーが存在する

* `q:`でコマンドラインウィンドウになる。 `<C-f>`でコマンドラインモードとコマンドラインウィンドウを切り替え

* Vim上からShellを操作できるのはとても楽しい
* ~はvimのバックアップファイル。カレントを汚されて邪魔なので.vimrcに記載した
```
:set backupdir=/tmp
:set backupdir=~/.vim/tmp
:set backupdir=.
```
