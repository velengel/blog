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
* draftをfalseにする

# ローカルで確認
```bash
hugo server
```

## Site Not Foundになるとき
* 多分themeがないので、submoduleのclone必要
* 参考: https://github.com/curegit/nagoya
```bash
git submodule update --init --recursive
```

# 自分用メモ

## サムネイルの設定
* `static/cover`に画像を配置
* 該当のmdファイル(ex. `content/posts/2025/0105.md`)のimagesのところに設定
