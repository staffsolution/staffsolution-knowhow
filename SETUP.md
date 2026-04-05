# GitHub Pages セットアップ手順（ノウハウサイト）

> **このフォルダがマスター（正本）です。**
> `docs-knowhow/` 内のファイルを直接編集して push するだけでサイトに反映されます。

---

## 公開URL

```
https://staffsolution.github.io/staffsolution-knowhow/
```

---

## ノウハウを更新するとき

1. `docs-knowhow/` 内の該当 MD ファイルを Cursor で直接編集する
2. push する：

```bash
cd "/Volumes/OWC Envoy Pro FX/w-work/s-スタッフソリューション/staffsolution_cursor/docs-knowhow"
git add .
git commit -m "ノウハウ更新：○○○"
git push https://【GitHubトークン】@github.com/staffsolution/staffsolution-knowhow.git main
```

---

## 新しいカテゴリを追加するとき

1. `docs-knowhow/` 配下に新フォルダと MD ファイルを追加する
2. `_includes/nav.html` にリンクを追記する
3. `index.md` にカテゴリのリンクを追記する
4. push する

---

## GitHub Pages の初回セットアップ手順（参考）

リポジトリを作り直す場合などに使用。

```bash
cd "/Volumes/OWC Envoy Pro FX/w-work/s-スタッフソリューション/staffsolution_cursor/docs-knowhow"
git init
git add .
git commit -m "初回：スタッフソリューション ノウハウサイト"
git branch -M main
git remote add origin https://github.com/staffsolution/staffsolution-knowhow.git
git push -u origin main
```

GitHub → Settings → Pages → Source：Deploy from a branch → main / root → Save
