# GainenThesis

## ローカルで編集する方法
1. GainenThesisディレクトリの下で git branch を実行
2. この時に以下のように出力され、 * が developOgawaにあることを確認する （これはオガワマン専用作業場所にいることを示している）
  develop
* developOgawa
  master
3. 編集したいものを編集し、最終的にコンパイルできることを確認しておく

変更点をリモートに取り入れるときは
4. git status
5. git add <④で表示されたファイル名1> <④で表示されたファイル名2>　・・・
6. git commit -m "変更点を示すログメッセージ"
7. git pull
8. git push -u origin developOgawa:developOgawa

以上でリモートに取り入れれました。あとは developOgawa での変更点を更に最終的な master に取り入れる必要があって、それはまぁまた落ち着いたらで(´_ゝ｀)笑

## 各ファイルの説明
main.tex
- メインファイル。新しい章を追加するときは¥input{section/<新しい章>}の記述を記入する。

config/setting.tex
- 設定ファイル。新しい章を追加したときには¥graphicpath{}を記入例に倣って追記する。そうすれば、各章のtexファイルで画像を読み込むときは¥includegraphics{画像名}だけでコンパイルできる。

section/
- 各セクションに該当するdirectoryを置く。
