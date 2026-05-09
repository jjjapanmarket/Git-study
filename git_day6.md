# Git学習day6

##　タグ
- コミットを参照しやすくするためにわかりやすい名前をつけるのがタグ。
- git tag 
### タグを作成する（注釈付き）
- git tag -a [タグ名]　（注釈付きタグを作成する）
　　　　　　-m [メッセージ]　　（メッセージをつけられる）
### タグを作成する（軽量版）
- git tag [タグ名]
### タグのデータを表示する
- git show [タグ名]

##　タグをリモートリポジトリに送信する
- git push [リモート名][タグ名]
- git push origin --tags (--tagsをつけるとローカルにあってリモートリポジトリに存在しないタグを一斉に送信する)

##　作業を一次避難する
- git stash
- git stash save
## 避難した作業を確認する
- git stash list
## 避難した作業を復元する
- git stash apply (最新の作業を復元する)
- git stash apply --index(ステージの状況も復元する)
