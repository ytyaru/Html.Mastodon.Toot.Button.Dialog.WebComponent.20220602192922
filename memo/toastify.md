# toastifyをdialogより手前に表示したい

　CSSのz-indexで値を大きくしたほうが手前に表示できる。が、toastifyで自由にz-indexをセットできていないっぽい。よくわからない。どうしたらいいんだ。

　dialogをshowModal()でなくshow()に変更することで解決した。

* toastifyがdialogの後ろに表示されてしまう問題の解決（dialogをshowModal()でなくshow()に変更した）
