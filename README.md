# URL
https://www.velengel.com/blog/


# ビルド
```bash
hugo
```

# 新規追加
```bash
hugo new posts/2023/1015.md
```
* draft を false にする

# ローカルで確認
```bash
hugo server
```

## Site Not Foundになるとき
* 多分 theme がないので、submodule の clone 必要
* 参考: https://github.com/curegit/nagoya
```bash
git submodule update --init --recursive
```

# 自分用メモ

## サムネイルの設定
* `static/cover` に画像を配置
* 該当の md ファイル(ex. `content/posts/2025/0105.md`)の images のところに設定

## textlintのかけ方

```bash
# lint
npx textlint content/**
# fix
npx textlint --fix content/**
```
