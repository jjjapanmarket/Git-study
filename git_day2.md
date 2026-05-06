# Git学習day2

# VS code　→ ターミナル　→ Github
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
・ git rm<ファイル名>
・ git rm -r<ディレクト名>
- ファイルを残したいとき
・ git rm --cached<ファイル名>

## ファイルの移動を記録する
- git mv <旧ファイル><新ファイル>

## リモートリポジトリ（Github）を新規追加する
- git remote add origin(URL)

## Gitのエイリアス（ショートカット）設定
- git st と打つだけで状況確認ができるようになる
・git config --global alias.st status
-  git cm "メッセージ" と打つだけでコミットできるようになる
・git config --global alias.cm "commit -m"
- git df と打つだけで差分が見れるようになる
・git config --global alias.df diff
- ブランチ（git branch）の基本
・ブランチは「履歴の枝分かれ」を作ること。
・役割：メインのコードを壊さずに、新機能の開発や実験ができる。

### 定番エイリアス一覧表
| 元のコマンド | エイリアス | 使う場面 |
| :--- | :--- | :--- |
| `git status` | `git st` | 「今どうなってる？」と確認する時 |
| `git commit -m` | `git cm` | 保存（セーブ）する時 |
| `git diff` | `git df` | 「何を書いたっけ？」と確認する時 |
| `git log --graph...` | `git graph` | 過去の履歴をグラフで見る時 |
