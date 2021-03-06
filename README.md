# What's "savlog"?
'save(保存する)' + 'blog(ブログ)' の造語。  
[乃木坂46のメンバーのブログ](http://blog.nogizaka46.com/)を、画像含め1から保存したかったのですが、人力でやるのは明らかに非効率であるため、自分のために作りました。  
メンバーが卒業してしまうため過去のブログのアーカイブを取りたい際にでもご使用ください。  
***
3期生の個人ブログに対応し，更新時点での卒業メンバーを整理しました(2018.4.26)

## 使い方
`python main.py -n 好きなメンバーのフルネーム`で実行するだけ。  
memberフォルダの中に好きなメンバーのフォルダが作成され、日付ごとのブログをtxt形式で、そのブログで登場した画像もまとめて保存します。

## 課題
* 一部収集漏れがある
  * **1日に複数回ブログを更新している**時に、最初のブログの文章が保存できていませんでした。
  * また、それに際して画像の保存も一部うまくいっていないようです。取得はできているので、保存処理に関するコード(125行目以降)を修正すればうまくいく…はず。
* 昔の記事では絵文字を多用しているメンバーがいます。メンバーが基本的にgif形式のファイルを画像として貼らないことから、絵文字を排除するため、gifは全て除きました(例外は無視ですがおそらくありません)。
  * しかし、当然ながら絵文字はgifだけではなく、jpegも存在します。本来取得したい画像もjpegが多く、それらとの識別が面倒だったので、その処理は割愛しました(あなたの推しが絵文字を多用していないことを願います)。
* メンバーによって収集度に違いがある
  * 例をいくつか...
    * 西野七瀬： 2016年6月10日の記事の5枚目の画像で403エラー
    * 生田絵梨花：2012年6月以前で画像&テキストが保存されていない日がある
  * 成功メンバー：白石麻衣、橋本奈々未、伊藤万理華、生田絵梨花etc(興味のあるメンバーしか試しておりませんが、基本的にどのメンバーでも問題無いはずです)