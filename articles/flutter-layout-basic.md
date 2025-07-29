---
title: "Flutterでの基本的なレイアウト:ColumnとRow"
emoji: "💻️"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["Flutter", "Dart"]
published: true
publication_name: "desiennz" # ← ここにチームブログ名（URLスラッグ）を入れる
---

## この記事の目的

Flutter の学習を始めたので自分のアウトプットと同じように Flutter を学習し始めた人に参考になればいいと思ったから。

## 私の経歴

工業高校 電気科卒
デザイン系専門学校 WEB 専攻卒
新卒で WEB で制作会社のスタートアップにコーダーとして入社
(スキルは デザイン力少し,HTML,CSS,JS が読める程度,CMS も少し)
会社の意向でフロントエンドエンジニアになるため Next React を学習

8 月から開発中のアプリのデスクトップ版にアサインされる予定が
モバイル版の開発が遅れており、Flutter 触ったこと無いのにいきなる実務にアサインされる ← なう

※9 月から SES として派遣さる予定なのでそれまでの間

## Column とは？

`Column` は複数のウィジェットを縦方向に並べるためのウィジェットです。

`````dart
Column(
  children: [
    Text('ゴリラ'),
    Text('キリン'),
    Text('ワニ'),
  ],
)
```
---

縦方向のウィジェットの配置を変えたいときは、mainAxisAlignment を使う。

---

### **中央寄せ・下寄せ・均等配置**

```dart
Column(
  // 中央寄せ
  mainAxisAlignment: MainAxisAlignment.center,
  children: <Widget>[],
)
Column(
  // 下寄せ
  mainAxisAlignment: MainAxisAlignment.end,
  children: <Widget>[],
)
Column(
  // 均等配置
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  children: <Widget>[],
)
```

### **左寄せ・右寄せ**

```dart
Column(
  // 左寄せ
  crossAxisAlignment: CrossAxisAlignment.start,
  children: <Widget>[],
)
Column(
  // 右寄せ
  crossAxisAlignment: CrossAxisAlignment.end,
  children: <Widget>[],
)
```






## Row とは？

`Row` は複数のウィジェットを横方向に並べるためのウィジェットです。

````dart
Row(
  children: [
    Text('ゴリラ'),
    Text('キリン'),
    Text('ワニ'),
  ],
)
```
---

横方向のウィジェットの配置を変えたいときも、mainAxisAlignment を使う。

---

### **中央寄せ・下寄せ・均等配置**

```dart
Row(
  // 中央寄せ
  mainAxisAlignment: MainAxisAlignment.center,
  children: <Widget>[],
)
Row(
  // 右寄せ
  mainAxisAlignment: MainAxisAlignment.end,
  children: <Widget>[],
)
Row(
  // 均等配置
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  children: <Widget>[],
)
```

### **上寄せ・下寄せ**

```dart
Row(
  // 左寄せ
  crossAxisAlignment: CrossAxisAlignment.start,
  children: <Widget>[],
)
Row(
  // 右寄せ
  crossAxisAlignment: CrossAxisAlignment.end,
  children: <Widget>[],
)
```


## 最後に

縦にならべたいときは Columnを使う。
横にならべたいときは Rowを使う。
基本的に ColumnとRowを変えるだけ！

---

📌 ご意見・ご感想などあればぜひコメントください！
`````
