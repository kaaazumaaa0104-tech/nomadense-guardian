# NOMADENSE Guardian

全クライアントBotの中央監視・自動復旧システム。

## 監視対象クライアント

| # | クライアント | サービス |
|---|---|---|
| 1 | よしこBot（ミライ工務店） | LINE経費管理Bot |

## 新規クライアント追加手順

`.github/workflows/guardian.yml` の `matrix.client` に1エントリ追加するだけ。

```yaml
- name: 〇〇Bot（△△会社）
  url: https://your-railway-url.up.railway.app
  railway_service: your-railway-service-name
```

## シークレット一覧

| シークレット名 | 内容 |
|---|---|
| `RAILWAY_TOKEN` | RailwayアカウントAPIトークン（全サービス共通） |
| `MONITORING_LINE_TOKEN` | 監視通知用LINEボットトークン |
| `SAIKI_LINE_UID` | 才木さんのLINE User ID |
