# Rakuten RMS Fraud Detector

Client-side fraud detection tool for Rakuten RMS CSV data with IP analysis, duplicate detection, and heuristic risk scoring
楽天RMSの受注CSVをもとに、IP分析・重複チェック・独自ロジックによるリスクスコアリングで不正注文を検知するローカル実行型ツール

---

## 🔍 Overview

楽天RMSから出力した受注CSVを読み込むだけで、
不正注文のリスクを自動で可視化するブラウザツールです。

* データは外部に送信されません（※IP国判定のみ例外あり）
* インストール不要、HTMLファイルを開くだけで動作
* 非エンジニアでも使えるUI設計

---

## ✨ Features

* 📂 CSVドラッグ＆ドロップ対応（Shift-JIS / UTF-8）
* 🔴 不正リスクの自動分類（危険 / 要注意 / 正常）
* 🌍 IPアドレスから国名を自動取得
* ⚠️ 以下の条件でリスク判定

  * IPアドレス重複
  * 海外IPアクセス
  * 深夜注文（0〜4時）
  * 同時刻の複数注文
  * 同一IPの短時間連続注文
  * ランダムメールアドレス
* 📊 統計表示（件数・分類）
* 🧾 危険注文の一括コピー機能

---

## 🚀 Usage

1. 本リポジトリをクローン or ダウンロード
2. `rakuten_fraud_detector.html` を開く（Chrome推奨）
3. 楽天RMSから出力した受注CSVをドラッグ＆ドロップ

---

## ⚠️ Notes

* 必ずローカル環境で開いてください（file://）
* メール添付やクラウド上で開くと正常動作しない場合があります
* IPの国判定のみ外部API（ip-api.com）を使用します

---

## 💡 Use Case

* 不正注文の事前チェック
* チャージバック対策
* 楽天ショップ運営のリスク管理
* 社内業務の効率化

---

## 🛠 Tech Stack

* HTML
* CSS
* Vanilla JavaScript

---

## 📌 Future Improvements

* ブラックリスト管理機能
* CSVエクスポート機能
* スコアリングロジックのカスタマイズ
* UIのダーク/ライト切り替え

---

## 📄 License

MIT License

---

## 👤 Author

* GitHub: (your profile)

---

## 🔐 Privacy

本ツールは基本的にすべての処理をブラウザ内で完結させます。
個人情報が外部に送信されることはありません（IP国判定を除く）。


⚠️ Disclaimer / 免責事項

本ツールは不正注文の可能性を検知するための補助ツールであり、判定結果の正確性や完全性を保証するものではありません。
本ツールの利用によって生じたいかなる損害についても、作者は一切の責任を負いません。

This tool is intended to assist in detecting potentially fraudulent orders and does not guarantee the accuracy or completeness of its results.
The author shall not be held liable for any damages arising from the use of this tool.
