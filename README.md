# GainenThesis

## ローカルで編集する方法
1. GainenThesisディレクトリの下で git branch を実行し * が developOgawaにあることを確認する （これはオガワマン専用作業場所にいることを示している）  
  1. もし * が masterの前に表記されていたら、 `git checkout developOgawa`を実行する！
1. 編集したいものを編集し、最終的にコンパイルできることを確認しておく  
  
変更点をリモートに取り入れるときは   
1. git status   
1. git add <④で表示されたファイル名1> <④で表示されたファイル名2>　・・・  
1. git commit -m "変更点を示すログメッセージ(日本語OK)"  
1. git pull  
1. git push -u origin developOgawa:developOgawa   

以上でリモートに取り入れれました。あとは developOgawa での変更点を更に最終的な master に取り入れる必要があって、それはまぁまたやっとく(´_ゝ｀)笑
1. Web上でマージリクエストを出す
1. マージリクエストを許可する

## リモートの変更をローカルで見る
まずローカルで、
1. git branch -a で master が表示の中にあることを確認する
1. git status で "nothing to commit, working tree clean" と表示されることを確認する
  1. 表示されなかったら、git add, commit を実行してコミットする
1. git checkout master を実行する
1. git pull -u origin master を実行する
これで最終版(master)の変更点をローカルに持ってこれたので、あとはコンパイルすればよい。

## 各ファイルの説明
main.tex
- メインファイル。新しい章を追加するときは¥input{section/<新しい章>}の記述を記入する。  

config/setting.tex
- 設定ファイル。新しい章を追加したときには¥graphicpath{}を記入例に倣って追記する。そうすれば、各章のtexファイルで画像を読み込むときは¥includegraphics{画像名}だけでコンパイルできる。

section/
- 各セクションに該当するdirectoryを置く。
