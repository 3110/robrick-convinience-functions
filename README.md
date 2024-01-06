# [ロブリック](https://robohon.com/apps/robrick.php)用のちょっと気の利いた関数ブロック群

シャープ社製のコミュニケーションロボット「[ロボホン](https://robohon.com/)」用のプログラミング環境である「[ロブリック](https://robohon.com/apps/robrick.php)」で使える，ちょっと気の利いた関数ブロックを作って集めてみました。

## 使用方法

1. 追加したい関数ブロックのXMLファイルをダウンロードして，適当な場所に保存してください。
1. ロブリックで「設定」ボタンを押して，保存先が「デバイス」になっていることを確認してください。
1. ロブリックでご自身が作っているプログラムを開いた状態で，「読み込み」ボタンを押してダウンロードしたXMLファイルを読み込んでください。その際に「作成中のプログラムを削除しますか？」というダイアログが表示されるので，**「キャンセル」** ボタンを押してください。

## 気の利いた関数ブロック群

### 「指定したダンスを踊る」ブロック

<a href="https://github.com/3110/robrick-convenience-functions/blob/main/images/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.png"><img src="https://github.com/3110/robrick-convenience-functions/blob/main/images/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.png" height="350px"></a>

[指定したダンスを踊る.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「踊る」ブロックはプルダウンメニューからダンスを指定して踊らせますが，ダンスの名前を文字列で指定して踊らせることができるブロックです。

「踊る」ブロックでもプルダウンメニューから「ランダム」を選ぶことで，踊れるすべてのダンスからひとつをランダムに選んで踊らせることができますが，例えば「ロボホン体操」「ラジオ体操」「ロボホンズブートキャンプ」「ヲタ芸」の中からひとつをランダムに選んで踊らせたいといった使い方を想定しています。

現在，2023年12月21日までに追加されたダンスを指定することができます。

※2023年12月31日現在，ロブリック v2.12.0（2023年12月21日リリース）では「シャープ戦隊ロボレンジャー」は踊れません。

#### サンプル「ルーレット体操」

![ルーレット体操のプログラム](/images/%E3%83%AB%E3%83%BC%E3%83%AC%E3%83%83%E3%83%88%E4%BD%93%E6%93%8D.png)

[ルーレット体操.xml](https://github.com/3110/robrick-convenience-functions/raw/main/samples/%E3%83%AB%E3%83%BC%E3%83%AC%E3%83%83%E3%83%88%E4%BD%93%E6%93%8D.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「指定したダンスを踊る」ブロックのサンプルとして，特定のダンスの中からランダムに踊るプログラムを紹介します。

ロボホンに「ダンスをしよう」と話しかけると，「ロボホン体操」「ラジオ体操」「ロボホンズブートキャンプ」「ヲタ芸」の中からランダムにダンスを選択し，一緒に体操をしてくれます。変数「ダンスリスト」はキーにダンス名，値にダンスを踊る前に発話する言葉の連想配列になっています。踊る曲数は変数「体操を選択する発話リスト」の数だけ踊ります。この例では2曲をランダムに踊ります。

通常の「踊る」ブロックでもすべてのダンスからランダムに1曲選んで踊らせることはできます。しかし，いくつかのダンスからランダムに選んで踊らせたい場合などには，「指定したダンスを踊る」ブロックが便利に使えます。

### 「連想配列からJSON文字列を作成」ブロック

![「連想配列からJSON文字列を作成」ブロック](/images/連想配列からJSON文字列を作成.png)

[連想配列からJSON文字列を作成.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%81%8B%E3%82%89JSON%E6%96%87%E5%AD%97%E5%88%97%E3%82%92%E4%BD%9C%E6%88%90.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

あらかじめ「JSON文字列から連想配列を作成」ブロックは用意されていますが，その逆の機能である「連想配列からJSON文字列を作成」するブロックが用意されていなかったので作成しました。

「ずっと覚えておく」ブロックで連想配列を覚えておく用途を想定しています。

引数に連想配列を渡すと，「JSON文字列から連想配列を作成」ブロックに渡せる文字列を生成します。ただし，キーの値はすべて文字列に変換されます。

### 「連想配列の値のリスト」ブロック

![「連想配列の値のリスト」ブロック](/images/連想配列の値のリスト.png)

[連想配列の値のリスト.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%81%AE%E5%80%A4%E3%81%AE%E3%83%AA%E3%82%B9%E3%83%88.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「連想配列のキーのリスト」ブロックはありますが，連想配列の値のリストを返すブロックがなかったので作成しました。

### 「リストから連想配列を生成する」ブロック

![「リストから連想配列を生成する」ブロック](/images/リストから連想配列を生成する.png)

[リストから連想配列を生成する.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E3%83%AA%E3%82%B9%E3%83%88%E3%81%8B%E3%82%89%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%82%92%E7%94%9F%E6%88%90%E3%81%99%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

引数に指定したキーのリストと値のリストから`{"キーのリストの1番目の値":"値のリストの1番目の値", ... , "キーのリストのn番目の値":"値のリストのn番目の値"}`という連想配列を生成します。リストの長さが異なる場合は，短い方に合わせて生成します。

### 「プレースホルダを埋める」ブロック

![「プレースホルダを埋める」ブロック](/images/プレースホルダを埋める.png)

[プレースホルダを埋める.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E3%83%97%E3%83%AC%E3%83%BC%E3%82%B9%E3%83%9B%E3%83%AB%E3%83%80%E3%82%92%E5%9F%8B%E3%82%81%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

接頭辞＋数字で始まるプレースホルダを指定した値で置換する関数です。

例えば，プレースホルダの接頭辞が`%`の場合（3番目の引数「`_接頭辞`」で指定可能），`"ボクの名前は%2だよ。こう見えて%1なんだ。"`という文字列に対して，`["電話", "ロボホン"]`という値のリストを指定すると，`"ボクの名前はロボホンだよ。こう見えて電話なんだ。"`という文字列を返します。

プレースホルダの数字に対応する要素がない場合，プレースホルダはそのまま残ります。例えば，`"ボクの名前は%2だよ。こう見えて%1なんだ。"`に`[電話]`を渡した場合，`%2`に対応する要素がないため，`"ボクの名前は%2だよ。こう見えて電話なんだ。"`が返ります。

## よくある質問とその答え

Q. 関数の引数の名前の頭に`_`（アンダーバー）を付けているのはなぜ？

A. 単なる作者の趣味です……というのはさておき，ロブリックでは変数の内容をどこからでも参照・変更できてしまう（変数の有効範囲がグローバルになっていると言います）ので，特に関数を使う場合，関数の中から関数の外側で使っている変数も参照・変更できてしまいます。これは特にプログラミング初心者にとっては直感的でわかりやすい反面，意図しない変更もできてしまうという問題もあります。

そこで，関数の中で使う変数にはアンダーバーで付加して，同じものを表すけど別の名前にしておくことで，あくまで関数の中だけで使っていて，関数を呼び出してもその外側で使っている変数を直接参照・変更するつもりはないというのを明示したい，という意図です。



## 参考

* [ロボホン用プログラミングツール ロブリック SR-SA04 利用マニュアル Version 1.4.0](https://robohon.com/apps/robrick/robrick-manual_v1-4-0.pdf)（シャープ株式会社）
