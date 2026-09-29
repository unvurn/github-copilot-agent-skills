# create-csharp-unit-test の設定

このファイルは利用者が手動で編集できます。値を変更した場合、次回のスキル起動から反映します。

## コーディング規約書

- `path`: `unset`
- `status`: `pending`
- `use`: `no`
- `searched`: `no`
- `search-duration-ms`: `not-measured`
- `search-duration-over-60-seconds`: `no`
- `search-disabled`: `no`

## ユニットテストガイドライン

- `path`: `unset`
- `status`: `pending`
- `use`: `no`
- `searched`: `no`
- `search-duration-ms`: `not-measured`
- `search-duration-over-60-seconds`: `no`
- `search-disabled`: `no`

## 設定値の意味

- `path`: 採用する文書のリポジトリ相対パス、絶対パス、または URL。未決定の場合は `unset`、検索して候補が見つからなかった場合は `not-found` とします。
- `status`: `pending`、`approved`、`rejected`、`not-found` のいずれかです。`pending` は未判断、`not-found` は検索済みで候補がなく利用者の判断待ち、`rejected` は文書を使わない判断が確定した状態です。
- `use`: 次回以降のテスト生成で文書を使うかどうかです。`yes` または `no` を指定します。
- `searched`: 文書の所在検索を実行した場合は `yes`、まだ実行していない場合は `no` にします。
- `search-duration-ms`: 文書の所在を検索した実測時間をミリ秒で記録します。未計測の場合は `not-measured` とします。
- `search-duration-over-60-seconds`: 検索に1分以上かかった場合は `yes` にします。
- `search-disabled`: `yes` の場合、自動検索しません。文書の所在を利用者に確認します。利用者が明示的に再検索を選んだ場合は検索できます。

`status: approved` と `use: yes` の文書は、テスト生成のたびに必ず最新内容を読み込みます。登録済みの `path` から読み込めない場合、または検索候補・利用者指定の文書を新たに確認する場合は、内容の概要と文書種別への適合性を利用者に示し、明示的な承認を得るまでは使用・登録しません。`status: not-found` の場合は自動検索せず、文書が見つからなかったことを伝えて利用者の判断を確認します。`status: rejected` と `use: no` の場合は検索・再確認をせず、文書種別ごとの代替資料を参考にします。コーディング規約書の代替資料はこのプロジェクト内の関連するC#ファイル、ユニットテストガイドラインの代替資料は関連する既存テストファイルとテストプロジェクト設定です。再検討する場合は、利用者が該当項目の `status` を `pending` に戻します。
