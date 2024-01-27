# [ロブリック](https://robohon.com/apps/robrick.php)用のちょっと気の利いた関数ブロック群

シャープ社製のコミュニケーションロボット「[ロボホン](https://robohon.com/)」用のプログラミング環境である「[ロブリック](https://robohon.com/apps/robrick.php)」で使える，ちょっと気の利いた関数ブロックを作って集めてみました。

## 使用方法

1. 追加したい関数ブロックのXMLファイルをダウンロードして，適当な場所に保存してください。
1. ロブリックで「設定」ボタンを押して，保存先が「デバイス」になっていることを確認してください。
1. ロブリックでご自身が作っているプログラムを開いた状態で，「読み込み」ボタンを押してダウンロードしたXMLファイルを読み込んでください。その際に「作成中のプログラムを削除しますか？」というダイアログが表示されるので，**「キャンセル」** ボタンを押してください。

## 1. 「指定したダンスを踊る」ブロック

<a href="https://github.com/3110/robrick-convenience-functions/blob/main/images/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.png"><img src="https://github.com/3110/robrick-convenience-functions/raw/main/images/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.png" height="350px"></a>

[指定したダンスを踊る.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E6%8C%87%E5%AE%9A%E3%81%97%E3%81%9F%E3%83%80%E3%83%B3%E3%82%B9%E3%82%92%E8%B8%8A%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「踊る」ブロックはプルダウンメニューからダンスを指定して踊らせますが，ダンスの名前を文字列で指定して踊らせることができるブロックです。

「踊る」ブロックでもプルダウンメニューから「ランダム」を選ぶことで，踊れるすべてのダンスからひとつをランダムに選んで踊らせることができますが，例えば「ロボホン体操」「ラジオ体操」「ロボホンズブートキャンプ」「ヲタ芸」の中からひとつをランダムに選んで踊らせたいといった使い方を想定しています。

現在，2024年1月23日までに追加されたダンスを指定することができます。

※2024年1月25日現在，ロブリック v2.12.0（2023年12月21日リリース）では最新のダンス（「まめまき」）が踊れない場合があります。

### サンプル「ルーレット体操」

![ルーレット体操のプログラム](/images/%E3%83%AB%E3%83%BC%E3%83%AC%E3%83%83%E3%83%88%E4%BD%93%E6%93%8D.png)

[ルーレット体操.xml](https://github.com/3110/robrick-convenience-functions/raw/main/samples/%E3%83%AB%E3%83%BC%E3%83%AC%E3%83%83%E3%83%88%E4%BD%93%E6%93%8D.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「指定したダンスを踊る」ブロックのサンプルとして，特定のダンスの中からランダムに踊るプログラムを紹介します。

ロボホンに「ダンスをしよう」と話しかけると，「ロボホン体操」「ラジオ体操」「ロボホンズブートキャンプ」「ヲタ芸」の中からランダムにダンスを選択し，一緒に体操をしてくれます。変数「ダンスリスト」はキーにダンス名，値にダンスを踊る前に発話する言葉の連想配列になっています。踊る曲数は変数「体操を選択する発話リスト」の数だけ踊ります。この例では2曲をランダムに踊ります。

通常の「踊る」ブロックでもすべてのダンスからランダムに1曲選んで踊らせることはできます。しかし，いくつかのダンスからランダムに選んで踊らせたい場合などには，「指定したダンスを踊る」ブロックが便利に使えます。

## 2. 「連想配列からJSON文字列を作成」ブロック

![「連想配列からJSON文字列を作成」ブロック](/images/連想配列からJSON文字列を作成.png)

[連想配列からJSON文字列を作成.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%81%8B%E3%82%89JSON%E6%96%87%E5%AD%97%E5%88%97%E3%82%92%E4%BD%9C%E6%88%90.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

あらかじめ「JSON文字列から連想配列を作成」ブロックは用意されていますが，その逆の機能である「連想配列からJSON文字列を作成」するブロックが用意されていなかったので作成しました。

「ずっと覚えておく」ブロックで連想配列を覚えておく用途を想定しています。

引数に連想配列を渡すと，「JSON文字列から連想配列を作成」ブロックに渡せる文字列を生成します。ただし，キーの値はすべて文字列に変換されます。

## 3. 「連想配列の値のリスト」ブロック

![「連想配列の値のリスト」ブロック](/images/連想配列の値のリスト.png)

[連想配列の値のリスト.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%81%AE%E5%80%A4%E3%81%AE%E3%83%AA%E3%82%B9%E3%83%88.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

「連想配列のキーのリスト」ブロックはありますが，連想配列の値のリストを返すブロックがなかったので作成しました。

## 4. 「リストから連想配列を生成する」ブロック

![「リストから連想配列を生成する」ブロック](/images/リストから連想配列を生成する.png)

[リストから連想配列を生成する.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E3%83%AA%E3%82%B9%E3%83%88%E3%81%8B%E3%82%89%E9%80%A3%E6%83%B3%E9%85%8D%E5%88%97%E3%82%92%E7%94%9F%E6%88%90%E3%81%99%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

引数に指定したキーのリストと値のリストから`{"キーのリストの1番目の値":"値のリストの1番目の値", ... , "キーのリストのn番目の値":"値のリストのn番目の値"}`という連想配列を生成します。リストの長さが異なる場合は，短い方に合わせて生成します。

## 5. 「プレースホルダを埋める」ブロック

![「プレースホルダを埋める」ブロック](/images/プレースホルダを埋める.png)

[プレースホルダを埋める.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E3%83%97%E3%83%AC%E3%83%BC%E3%82%B9%E3%83%9B%E3%83%AB%E3%83%80%E3%82%92%E5%9F%8B%E3%82%81%E3%82%8B.xml)（リンクを右クリックして「名前を付けてリンク先を保存」）

接頭辞＋数字で始まるプレースホルダを指定した値で置換する関数です。

例えば，プレースホルダの接頭辞が`%`の場合（3番目の引数「`_接頭辞`」で指定可能），`"ボクの名前は%2だよ。こう見えて%1なんだ。"`という文字列に対して，`["電話", "ロボホン"]`という値のリストを指定すると，`"ボクの名前はロボホンだよ。こう見えて電話なんだ。"`という文字列を返します。

プレースホルダの数字に対応する要素がない場合，プレースホルダはそのまま残ります。例えば，`"ボクの名前は%2だよ。こう見えて%1なんだ。"`に`[電話]`を渡した場合，`%2`に対応する要素がないため，`"ボクの名前は%2だよ。こう見えて電話なんだ。"`が返ります。

## 6. 「発話を聞きとる」ブロック

![「発話を聞きとる」ブロック](/images/%E7%99%BA%E8%A9%B1%E3%82%92%E8%81%9E%E3%81%8D%E3%81%A8%E3%82%8B.png)

[発話を聞きとる.xml](https://github.com/3110/robrick-convenience-functions/raw/main/%E7%99%BA%E8%A9%B1%E3%82%92%E8%81%9E%E3%81%8D%E3%81%A8%E3%82%8B.xml)

オーナーさんが話した内容をロボホンが聞きとる場合，違う答え方でも同じように扱いたい場合（OKなことを答えるのに「はい」「オッケー」「了解」でも良いようにしたい）や，聞き間違えた場合に備えて，聞き間違いも通るようにしたいということがあると思います。また，うまく聞きとれなかった場合に聞き直す必要もあります。

それをひとつのブロックで扱えるようにしたのが「発話を聞きとる」ブロックです。

![「発話を聞きとる」ブロック使用例その1](/images/%E3%80%8C%E7%99%BA%E8%A9%B1%E3%82%92%E8%81%9E%E3%81%8D%E3%81%A8%E3%82%8B%E3%80%8D%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E4%BD%BF%E7%94%A8%E4%BE%8B%E3%81%9D%E3%81%AE1.png)


「発話を聞きとる」ブロックの最初の引数「`_話しかける言葉`」は，ロボホンから最初に話しかける問い掛けの言葉です。

2番目の引数「`_聞きとる言葉一覧`」には連想配列を指定し，キーにはロボホンが聞いた言葉（＝音声認識した結果），値はその言葉を聞いたときに返す文字列です。この例では「いいよ」「はい」「おっけー」「了解」はすべてロボホンの問い掛けに対して肯定を意味する言葉なので，すべて共通で「OK」を返すようにしています。また，「だめだよ」「ダメだよ」「いいえ」は否定を意味する言葉なので，すべて共通で「NG」を返すようにしています。ここで「だめだよ」「ダメだよ」は，音声認識の揺れに対応している例です。

3番目の引数「`_聞き返す言葉一覧`」にはリストを指定し，聞き返す言葉を並べています。聞きとった結果，2番目の引数に指定した連想配列のキーに一致しない言葉が返ってきた場合，このリストに並んだ言葉を発話して，リストに指定した数だけ聞き返します。聞き返す必要がない場合は「空のリスト作成する」ブロックを渡します。この例の場合，聞きとれなかった場合に2回聞き返すことになります。

関数の返り値は，2番目の引数の連想配列のキーに指定した言葉を聞きとった場合は，その値に対応する連想配列の値，聞きとれなかった場合は「」（空の文字列）が返ります。この例では，「いいよ」「はい」「おっけー」「了解」が聞きとれば場合は「OK」，「だめだよ」「ダメだよ」「いいえ」が聞きとれた場合は「NG」，2回聞き返しても聞きとれなかった場合は「」（空の文字列）が返ります。

この「発話を聞きとる」ブロックの良いところは，聞きとった言葉のゆれを連想配列で吸収し，聞きとった言葉の意味で返ってくる文字列を共通化することで聞きとった後の処理をかんたんにできることと，聞き返す処理も含めてひとつのブロックで実現できることです。

ちなみに，2番目の引数「`_聞きとる言葉一覧`」に指定する連想配列は，上で紹介している「リストから連想配列を生成する」ブロックを使うとよりかんたんに指定できます。

![「発話を聞きとる」ブロック使用例その2](/images/%E3%80%8C%E7%99%BA%E8%A9%B1%E3%82%92%E8%81%9E%E3%81%8D%E3%81%A8%E3%82%8B%E3%80%8D%E3%83%96%E3%83%AD%E3%83%83%E3%82%AF%E4%BD%BF%E7%94%A8%E4%BE%8B%E3%81%9D%E3%81%AE2.png)


## 7. 「LINEに通知を送る」ブロック

![「LINEに通知を送る」ブロック（バグ回避版）](/images/LINE%E3%81%AB%E9%80%9A%E7%9F%A5%E3%82%92%E9%80%81%E3%82%8B%EF%BC%88%E3%83%90%E3%82%B0%E5%9B%9E%E9%81%BF%E7%89%88%EF%BC%89.png)

[LINEに通知を送る（バグ回避版）.xml](https://github.com/3110/robrick-convenience-functions/raw/main/LINE%E3%81%AB%E9%80%9A%E7%9F%A5%E3%82%92%E9%80%81%E3%82%8B%EF%BC%88%E3%83%90%E3%82%B0%E5%9B%9E%E9%81%BF%E7%89%88%EF%BC%89.xml)

[](/images/LINE%E3%81%AB%E9%80%9A%E7%9F%A5%E3%82%92%E9%80%81%E3%82%8B.png)

※ロブリックv2.10.0のWebAPIブロックにはバグがあり，引数のURLやHeadersに変数を渡せないので，このバグ回避版のブロックではテキストブロックで直接渡しています。バグが修正され次第，[LINEに通知を送る.xml](https://github.com/3110/robrick-convenience-functions/raw/main/LINE%E3%81%AB%E9%80%9A%E7%9F%A5%E3%82%92%E9%80%81%E3%82%8B.xml)に差し替えます。

[LINE Notify API](https://notify-bot.line.me/doc/ja/)を使ってLINEに通知を送るブロックです。LINE Notifyのパーソナル・アクセス・トークンの発行が必要です。発行したパーソナル・アクセス・トークンを「\[アクセストークンに書き換える\]」のところに入れてください。

### サンプル：ロボホンに話した内容をLINEに送る

![ロボホンに話した内容をLINEに送る](/images/%E3%83%AD%E3%83%9C%E3%83%9B%E3%83%B3%E3%81%AB%E8%A9%B1%E3%81%97%E3%81%9F%E5%86%85%E5%AE%B9%E3%82%92LINE%E3%81%AB%E9%80%81%E3%82%8B.png)

待ち受け起動のスクリプトになっているので，「LINE送って」と話しかけると起動します。ロボホンがLINEに送る内容を聞いてくれますので，送りたい内容を話しかけてください。話し終わるとロボホンが聞きとった内容を教えてくれるので，送ってよければ「いいよ」，送るのをやめる場合は「だめだよ」と言ってあげましょう。「いいよ」と言うとLINEに話した内容を送ってくれます。

![LINEに通知された様子](/images/LINE%E3%81%AB%E9%80%9A%E7%9F%A5%E3%81%95%E3%82%8C%E3%81%9F%E6%A7%98%E5%AD%90.jpg)

このスクリプトでは，ここで紹介している以下のブロックを使用しています。

* 「発話を聞きとる」ブロック
* 「リストから連想配列を生成する」ブロック

## よくある質問とその答え

Q. 関数の引数の名前の頭に`_`（アンダーバー）を付けているのはなぜ？

A. 単なる作者の趣味です……というのはさておき，ロブリックでは変数の内容をどこからでも参照・変更できてしまう（変数の有効範囲がグローバルになっていると言います）ので，特に関数を使う場合，関数の中から関数の外側で使っている変数も参照・変更できてしまいます。これは特にプログラミング初心者にとっては直感的でわかりやすい反面，意図しない変更もできてしまうという問題もあります。

そこで，関数の中で使う変数にはアンダーバーで付加して，同じものを表すけど別の名前にしておくことで，あくまで関数の中だけで使っていて，関数を呼び出してもその外側で使っている変数を直接参照・変更するつもりはないというのを明示したい，という意図です。

Q. ここにある関数ブロックを複数読み込んだりすると，`_キー_1`のように変数名の後ろに`_`（アンダーバー）と通し番号がついた名前に変わってしまう

A. 上のQでも説明しましたが，ロブリックでは変数の有効範囲がグローバルになっているため，後から読み込んだスクリプトに既に読み込まれているスクリプトで使っている変数名がある場合，同じ名前が重複しないように`_`（アンダーバー）と通し番号を付ける仕様になっています。

そのままでも問題はありませんが，名前が変わってしまった変数名の右に出ている▼をクリックして，「変数の名前を変える...」で一気に元の名前に戻すことができます。

## 参考

* [ロブリック](https://robohon.com/apps/robrick.php)（シャープ株式会社）
* [ロボホン用プログラミングツール ロブリック SR-SA04 利用マニュアル Version 1.4.0](https://robohon.com/apps/robrick/robrick-manual_v1-4-0.pdf)（シャープ株式会社）
* [ロボホン工房：ロブリックの部屋](https://robotomo.robohon.com/menus/gehvibwgpu4dg0bv/announcements)（[ロボホンともだち広場](https://robotomo.robohon.com/)）
