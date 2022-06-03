# マストドンAccessToken再利用

　現状、アクセストークンは使い捨て。もしverifyで無効と判断されたら、`apps`から作り直している。たぶん`apps`は使い回せる。なるだけサーバ負荷をかけないような作りにしたいが、認証まわりが難しすぎて辛い。

　なお、アクセストークンに関しては流出した場合、削除したいことがある。なので無効化して再発行できるようにすべき。だったらもう最初から使いまわしたほうが楽なので、今のような実装になっている。

　XSS攻撃への対処をどうするか。ssesionStorageに登録しているが、かといってcookieにするにはサーバ側も自分でそれ用に設定・実装しなくちゃいけなくて不可能。あとはせいぜいトゥートしたらすぐにStorageから削除するくらいしかない。でもコメント一回ごとに認証が必要になる。どうせ一回しかしないだろうと見込めばそれでもいい。でも、どうせsessionStorageはブラウザを閉じたら消える。なら、べつに現状でも大した問題にはならないだろう。どちらにせよ、XSSされたら取られうる。どうしたものか。
