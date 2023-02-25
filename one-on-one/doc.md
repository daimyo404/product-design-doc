## プロダクト概要

1on1 のログを残すための Web サービス

## 画面一覧

- ログイン画面
- 受け手一覧表示画面
- 受け手詳細表示画面

## 機能一覧

- 認可機能（認可エンドポイント）
- トークン発行機能（トークエンドポイント）
- 受け手一覧表示機能
- 受け手詳細表示機能

## アーキテクチャ、採用技術について

- 全て Azure 上に構築
- FE <-> BFF <-> BE <-> DB の構成とする
- FE は Next.js を採用し、BFF との通信は SSR で行うものとする
  また、BFF とは GraphQL クライアント（Apollo Client）にてデータのやり取りを行う
- BFF は NestJS（Express）、GraphQL サーバー（Apollo Server）を利用する
- BE は NestJS（Express）を利用し、通信は gRPC にて行う
- DB は Azure Database for MySQL を利用
