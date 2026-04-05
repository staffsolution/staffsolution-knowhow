# GitHub Pages セットアップ手順（ノウハウサイト）

## 1. GitHubでリポジトリを作る

1. https://github.com/new を開く（staffsolution アカウントでログイン済みの状態で）
2. 以下の設定で作成：
   - **Repository name**: `staffsolution-knowhow`
   - **Visibility**: Public
   - Initialize README：チェックしない
3. 「Create repository」をクリック

## 2. このフォルダ（docs-knowhow）を push する

Cursor のターミナルで以下を実行：

```bash
cd "/Volumes/OWC Envoy Pro FX/w-work/s-スタッフソリューション/staffsolution_cursor/docs-knowhow"
git init
git add .
git commit -m "初回：スタッフソリューション ノウハウサイト"
git branch -M main
git remote add origin https://github.com/staffsolution/staffsolution-knowhow.git
git push -u origin main
```

## 3. GitHub Pages を有効にする

1. https://github.com/staffsolution/staffsolution-knowhow を開く
2. **Settings → Pages**
3. Source：「Deploy from a branch」
4. Branch：`main` / Folder：`/ (root)`
5. 「Save」

## 4. 公開URL

```
https://staffsolution.github.io/staffsolution-knowhow/
```

設定後 1〜2 分で公開されます。

---

## ノウハウを更新するときのルール

### ノウハウ本体（マスター）を更新する

1. `ノウハウ/9ステップメソッド/` の該当 MD ファイルを Cursor で編集する
2. `docs-knowhow/9ステップメソッド/` の同名ファイルにも同じ内容をコピーする
3. push する：

```bash
cd "/Volumes/OWC Envoy Pro FX/w-work/s-スタッフソリューション/staffsolution_cursor/docs-knowhow"
git add .
git commit -m "ノウハウ更新：○○○"
git push
```

### 新しいカテゴリを追加するとき

1. `docs-knowhow/` 配下に新フォルダと MD ファイルを追加する
2. `_includes/nav.html` にリンクを追記する
3. `index.md` にカテゴリのリンクを追記する
4. push する

---

> **注意**：`ノウハウ/9ステップメソッド/` がマスター（正本）。
> `docs-knowhow/9ステップメソッド/` はサイト公開用のコピー。
> 必ずマスター側を先に更新してから、docs-knowhow 側に反映する。
