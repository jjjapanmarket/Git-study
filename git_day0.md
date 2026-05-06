# Day 0 のファイル作成と編集

1.  **Day 4 用のファイルを作成**
    ```bash
    touch `git_day0.md`
    ```
2.  **VS Codeで編集**
    *   `git_day0.md` を開き、今日学んだこと

---

###  保存とアップロード（コミット＆プッシュ）

1.  **ステージング（全部の変更を載せる）**
    ```bash
    git add .
    ```
    *   （エイリアスを作っているなら `git aa` でもOK）
2.  **記録（コミット）**
    ```bash
    git commit -m "day4: originの正体とリモート名の仕組みを学習"
    ```
3.  **世界へ公開（プッシュ）**
    ```bash
    git push origin main
    ```

---

## VS Code用チェックリスト
## Git手順まとめ
1. `git fetch origin`（GitHubに変化がないか見に行く）
2. `git merge origin/main`（手元を最新にする）
3. `touch git_day4.md`（新しい日のファイル作成）
4. 編集・学習
5. `git add .` -> `git commit` -> `git push origin main`