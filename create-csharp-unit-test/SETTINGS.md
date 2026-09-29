# create-csharp-unit-test の設定

このファイルは利用者が手動で編集できます。値を変更した場合、次回のスキル起動から反映します。

## コーディング規約書

- `path`: `未設定`
- `status`: `pending`
- `use`: `no`

## ユニットテストガイドライン

- `path`: `未設定`
- `status`: `pending`
- `use`: `no`

## 検索記録

- `searched`: `no`
- `search-duration-ms`: `未計測`
- `search-duration-over-60-seconds`: `no`
- `search-disabled`: `no`

## 設定値の意味

- `path`: 採用する文書のリポジトリ相対パス、絶対パス、または URL。未採用の場合は `未検出` とします。
- `status`: `pending`、`approved`、`rejected`、`not-found` のいずれかです。
- `use`: 次回以降のテスト生成で文書を使うかどうかです。`yes` または `no` を指定します。
- `search-duration-ms`: 文書の所在を検索した実測時間をミリ秒で記録します。
- `search-duration-over-60-seconds`: 検索に1分以上かかった場合は `yes` にします。
- `search-disabled`: `yes` の場合、設定された文書が利用できなくても再検索しません。

`status: approved` と `use: yes` の文書は、テスト生成のたびに必ず最新内容を読み込みます。`status: rejected` の場合は、別の所在を利用者に確認します。
