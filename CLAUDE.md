# CLAUDE.md

## リポジトリ概要
- LoNalogy 統一理論の Marp スライド資料
- ライセンス: CC0 1.0 (パブリックドメイン)

## ファイル構成
- `LoNalogy_marp_rewritten.md` — Marp スライド本体（KaTeX 数式）

## 公開手順

### 初回セットアップ（済）
```bash
gh repo create LoNalogy --public --source=. --push \
  --description "LoNalogy: unified theory treating i (rotation) and j (visible/invisible separation) on equal footing."
```

### 更新時
```bash
# ローカルで編集後
cp ~/Desktop/dualcomplex/LoNalogy_marp_rewritten.md /tmp/lonalogy-publish/
cd /tmp/lonalogy-publish
git add LoNalogy_marp_rewritten.md
git commit -m "Update slides"
git push
```

### Marp でスライド表示
```bash
# CLI
npx @marp-team/marp-cli LoNalogy_marp_rewritten.md --html

# PDF 出力
npx @marp-team/marp-cli LoNalogy_marp_rewritten.md --pdf

# VS Code: Marp for VS Code 拡張でプレビュー可
```

## 注意
- 数式は KaTeX 記法（`math: katex` 指定）
- `j := σ₃` は内部作用素（split-complex の数ではない）
