---
title: "Next.js 各レンダリング方法を例えつきで解説"
emoji: "💻️"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Next.js", "Vercel", "フロントエンド"]
published: true
publication_name: "desiennz" # ← ここにチームブログ名（URLスラッグ）を入れる
---

## この記事の目的

Next.js のレンダリング方法について知る。

## まず レンダリングとは？

ブラウザに表示するために、HTML・CSS・JS をもとに画面を作る処理。

## レンダリングの種類

Next.js には主に 4 つのレンダリング方法があります。

- CSR (Client Side Rendering)

- SSR (Server Side Rendering)

- SSG (Static Site Generation)

- ISR (Incremental Static Regeneration)

それぞれについて説明をしていきます。

## CSR (Client Side Rendering)

**CSR** とは **Client Side Rendering** の略になります。
CSR ではサーバーからほぼ空の HTML を返し、ブラウザ側で JS が実行され画面を生成。

### 特徴

- **初回表示は遅め**

- ぺージ全体をリロードせず、ユーザー操作ごとに必要な部分だけ更新可能（いいね、高評価など）

- ユーザーごとに表示内容が変わるサイト・アプリ向け（X、Instagram など）

### レストランで例えると

材料を渡してユーザーが自分で料理を作るイメージ

## SSR (Server Side Rendering)

**SSR** とは **Server Side Rendering** の略になります。
SSR ではリクエストごとにサーバーで HTML を生成。

### 特徴

- リクエストごとにサーバーで HTML を生成するため、**初回表示は遅め**

- **SEO にも強く**、リアルタイム更新系のサイトに効果的（ニュースサイト、株価など）

- リクエストごとに HTML を生成するので、アクセスが集中すると**サーバー負荷が増える**

### レストランで例えると

注文を受けてから料理を作って提供するイメージ

## SSG (Static Site Generation)

**SSG** とは **Static Site Generation** の略になります。
SSG ではビルド時に HTML を生成して事前に用意。

### 特徴

- ビルド時に HTML を生成するので **初回表示が高速**

- 事前に完成 HTML が用意されているため **SEO にも強い**

- サーバー負荷がほぼなく、更新頻度が低い静的サイトに向いている（LP、ブログなど）

### レストランで例えると

注文を受けてから既に作ってあるものをすぐ提供するイメージ

## ISR (Incremental Static Regeneration)

**ISR** とは **Incremental Static Regeneration** の略になります。
ISR ではビルド時に HTML を生成（SSG と同じ）＋アクセス後に一定時間ごとに更新可能。

### 特徴

- ビルド時に HTML を生成するので**初回表示が高速** (SSG と同じ)

- CDN から配信されるため、負荷も低い

- アクセス後一定時間ごとに HTML を更新可能

- ブログやニュースサイトなど、更新頻度はそこそこあるが、毎リクエスト SSR するほどではない場合

### レストランで例えると

注文を受けて作り置きの料理を提供 → ただし古くなった料理はこっそり厨房で作り直しておく → 次のお客さんには新しい料理を出せる

## 最後に

今回は Next.js のレンダリング方法についてまとめてみました。
ご参考になると幸いです。

📌 ご意見・ご感想などあればぜひコメントお願いします。
