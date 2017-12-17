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
