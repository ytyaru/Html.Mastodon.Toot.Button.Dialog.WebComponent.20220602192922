# statusの取得方法

* `<tood-dialog>`のshadow内にある`<textarea id="status">`の`value`
* `<toot-button status="これ">`の`status`属性値

　とりあえず後者にしておいた。

　本当は前者に変えたかったが、shadow要素のためか取得できなかった。

　イベントとの絡みでどう実装すればいいかわからない。

  toot-dialog側でやるべきか、それともtoot-button側でやるべきか。それをどう実装すべきか。toot-buttonが押されたとき、toot-dialog内のtextareaの値を取得したい。
