# Review Judge Logs

## Format

- Situation:
- Judgment:
- Reason:

## Logs

- Situation: `outline.md` を同じ記事ディレクトリに置きたい。
  Judgment: `content/posts/2026/0418/index.md` の leaf bundle 形式にする。
  Reason: Hugo では `index.md` を持つディレクトリ内の Markdown を page resource として扱えるため、本文と執筆用メモを同じ場所で管理できる。

- Situation: これまでの記事は `content/posts/yyyy/mmdd.md` の単体ファイル形式が中心だった。
  Judgment: 今回は既存形式より `index.md` + `outline.md` のディレクトリ形式を優先する。
  Reason: 同じディレクトリに outline を置く要件があり、単体ファイル形式では自然に満たせないため。

- Situation: 骨子を本文化するとき、全項目を均等に肉付けするか迷った。
  Judgment: すべてを膨らませず、重要な学びに重点を置く。
  Reason: 記事の主題は実装内容の網羅ではなく、再現して初めて分かったことと AI との進め方だから。

- Situation: 初稿の本文が既存記事より説明文中心で長かった。
  Judgment: 箇条書き中心の構成に寄せる。
  Reason: 既存記事は `背景` `きっかけ` `学び・感想` を軸に、短い文と箇条書きで進む文体が多いため。

- Situation: 読者がガラケーゲームを知らない可能性がある。
  Judgment: i モード、月額課金、サイトとアプリの組み合わせ、通信要素を前提説明として入れる。
  Reason: ガラケーの制約や通信料の話が伝わらないと、この記事の背景が弱くなるため。

- Situation: 調査用リポジトリのローカルパスを受け取った。
  Judgment: 本文、outline、メモ本文にはローカルパスを記載しない。
  Reason: 記事に載せない情報であり、公開物や執筆メモに混ぜる必要がないため。

- Situation: ドラクエモンスターズ i / MOBILE の説明で `らしい` などの伝聞表現が入った。
  Judgment: 自分が遊んでいたゲームとして言い切れる表現に直す。
  Reason: 読者にとっては筆者の体験記事であり、過度な伝聞表現は距離感が出すぎるため。

- Situation: 外部資料の参考リンクが多くなった。
  Judgment: 参考リンクを最低限に絞る。
  Reason: 本文の補助として必要なリンクだけあればよく、リンク集が主役になると記事の焦点がぼやけるため。

- Situation: `npx textlint` が `node_modules` 不在で実行できなかった。
  Judgment: `npm install` を実行してから textlint をかける。
  Reason: README に textlint 運用が明記されており、本文を既存記事の品質ラインに合わせるため。

- Situation: `outline.md` も `content/**` 配下に置いた。
  Judgment: 公開本文ではないが `outline.md` も textlint 対象として確認する。
  Reason: README の lint 対象が `content/**` なので、後で全体 lint を実行したときに落ちないようにするため。

- Situation: `memo` ディレクトリを記事ディレクトリ内に作っていた。
  Judgment: リポジトリルート直下の `memo/review-judge-logs.md` に移す。
  Reason: 記事 bundle のリソースではなく、リポジトリ横断のレビュー判断ログとして管理するため。

- Situation: 箇条書きの中に、明確な順番がある手順が混ざっていた。
  Judgment: 手順や時系列があるものだけ `1. 2. 3.` の番号付きリストにする。
  Reason: 順番が意味を持つ項目は、ただの列挙より番号付きのほうが読み手に意図が伝わるため。

- Situation: `今回作ったもの` が調査で出てきた要素や実装要素の長い列挙になっていた。
  Judgment: 当時のゲーム体験と対応する基本ループにまとめ直す。
  Reason: 読者に必要なのは実装チェックリストではなく、どの体験を再現し、その結果何を学んだかだから。

- Situation: レビューで、スクショ、ADR/story の補足、DQM とヤンガスの対比、AI 開発全般への示唆を強めるとよいと判断した。
  Judgment: DQM のスクショを追加し、ADR/story の説明、2 作の対比、レガシー仕様復元にも通じる学びを本文に追記する。
  Reason: 高校生エンジニア、ゲーム業界エンジニア、非ゲーム業界のシニアエンジニアのどの読者にも、記事の入口と学びの接続が分かりやすくなるため。

- Situation: 追加レビューで、ヤンガス側のスクショ、楽しかった瞬間、記事冒頭の着地点があるとよいと判断した。
  Judgment: ヤンガスのスクショを追加し、意思決定が発生した瞬間の具体例と、冒頭に記事の着地点を追記する。
  Reason: 2 作の比較が視覚的にも内容的にも伝わりやすくなり、読者が記事の主題を早い段階で把握できるため。
