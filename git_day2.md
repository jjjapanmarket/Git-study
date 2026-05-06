# Git学習day2

## VS code　→ ターミナル　→ Github
- VS Code: メモをしっかり書く
- ターミナル で git status を打って、ファイルが赤字で出ている。
- git add . で一括登録
- git commit -m "..." 
- git push origin main でGitHubに公開。

## 管理しないファイルをGitの管理から外す「.gitignore」
- .gitignoreファイルに指定することで、ファイルをGitの管理から外すことができる。（自動生成されるファイル、パスワードが記載されているファイル）
- ファイルの削除（git rm）
- 取り消し（git reset）(HEAD = 「今のブランチの最新コミット」)
- git checkout -- は、作業ディレクトリの変更を捨てて、ファイルを元の状態に戻すコマンド

##　変更差分を確認する
- git addする前の変更分「git diff」
- git addした後の変更分「git diff --staged」

##　変更履歴を確認する
- git log
- git log --oneline （一行で表示する）
- git log -n <コミット数>

## ファイルの削除を記録する
- ファイルごと削除
・　git rm<ファイル名>
・　git rm -r<ディレクト名>
- ファイルを残したいとき
・　git rm --cached<ファイル名>




