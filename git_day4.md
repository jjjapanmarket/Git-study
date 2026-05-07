# Git学習day4

## ブランチとは
- 並行して複数機能を開発するためにあるのがブランチ
- コミットしたらブランチが指すコミットファイルが変わる

## HEAD
- 現在作業中のブランチへのポインタ。

## ブランチを新規追加する
- git branch<ブランチ名>
### ブランチの一覧を表示する
- git branch (-a 全てのブランチを表示する)

## ブランチを切り替える
- git checkout<既存ブランチ名>
### ブランチを新規作成して切り替える
- git checkout -b<新ブランチ名>

##　 マージとは
- 他の人の変更内容を取り込む作業のこと
- git merge<ブランチ名>

### マージには３種類ある
1. Fast Foward : 早送りになるマージ
- Github上で編集をし、commit→　git pull origin main→ cat<Githubでciしたファイル>→ git log --onelineで確認　

2. Auto Merge : 枝分かれを合体させるマージ
- main と feature の両方で作業が進んでいたり、マージした事実を記録に残したい時の合体。
- 移動: git checkout main（本流のブランチに戻る）
- 合体: git merge feature（featureの成果をmainに取り込む）
- 確認: ls で feature.md が出現しているか確認
- 中身: cat feature.md で中身が正しいか確認
- ログ: git log --oneline --graph で枝が合流した図を確認

3. コンフリクトとは
- 同じファイルの同じ箇所を、別々のブランチで同時に書き換えた時に発生する「どっちを優先すればいいの？」というエラー。
- 状況: main で 1行目を「A」に変え、feature で 1行目を「B」に変えてマージしようとした時に起こる。
### 解決の手順:
1. 合体: git merge feature → エラー（Conflict）が出る。
2. 確認: VS Codeで該当ファイルを開くと、<<<< HEAD などの記号で「どっちにする？」と表示される。
3. 修正: 手動でコードを書き直し、不要な記号（<<<<, ==== など）を消す。
4. 完了: git add . → git commit で「衝突を解決したよ」と記録する。

## コンフリクト関連の事故が起きにくい運用ルール
- 複数人で同じファイルを変更しない
- pullやmergeする前に変更中の状態をなくしておく（commitやstashをしていく）
- pullする時は、pullするブランチに移動してからpullする
- コンフリクトしても慌てない

## ブランチを変更・削除する
### ブランチを変更する
- git branch -m <ブランチ名>
- git branch -m new_branch
### 削除する
- git branch -d <ブランチ名>
- git branch -D <ブランチ名>　（強制削除する）

