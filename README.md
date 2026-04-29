# Rakuten RMS Fraud Detector

Client-side fraud detection tool for Rakuten RMS CSV data with IP analysis, duplicate detection, and heuristic risk scoring
楽天RMSの受注CSVをもとに、IP分析・重複チェック・独自ロジックによるリスクスコアリングで不正注文を検知するローカル実行型ツール

---

## 🔍 Overview

楽天RMSから出力した受注CSVを読み込むだけで、
不正注文のリスクを自動で可視化するブラウザツールです。

* インストール不要（HTMLを開くだけ）
* データは基本的に外部送信されません
* 非エンジニアでも使えるシンプルUI

---

## ✨ Features

* 📂 CSVドラッグ＆ドロップ対応（Shift-JIS / UTF-8）
* 🔴 不正リスクの自動分類（危険 / 要注意 / 正常）
* 🌍 IPアドレスから国名を取得
* ⚠️ リスク判定ロジック

  * IPアドレス重複
  * 海外IPアクセス
  * 深夜注文（0〜4時）
  * 同時刻の複数注文
  * 同一IPの短時間連続注文
  * ランダムメールアドレス検知
* 📊 統計表示
* 🧾 危険注文のコピー機能

---

## 🚀 Usage

1. 本リポジトリをダウンロード
2. `rakuten_fraud_detector.html` を開く（Chrome推奨）
3. 楽天RMSから出力した受注CSVをドラッグ＆ドロップ

---

## 🌐 IPデータについて

IPアドレスの国判定には外部API（ip-api.com）を使用しています。
無料プランにはレート制限および利用制限があります。

※ アクセスが増加した場合、別APIへの切り替えを検討してください

---

## ⚠️ Notes

* ローカル環境での使用を推奨します（file://）
* クラウド上やメール添付から開くと正常動作しない場合があります

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

* ブラックリスト管理
* CSVエクスポート
* スコアリングカスタマイズ
* UI改善

---

## ⚠️ Disclaimer / 免責事項

本ツールは不正注文の可能性を検知するための補助ツールであり、判定結果の正確性や完全性を保証するものではありません。
本ツールの利用によって生じたいかなる損害についても、作者は一切の責任を負いません。

本ツールの判定結果は参考情報としてご利用ください。最終的な判断は利用者自身の責任において行ってください。

This tool is intended to assist in detecting potentially fraudulent orders and does not guarantee the accuracy or completeness of its results.
The author shall not be held liable for any damages arising from the use of this tool.

---

## 📄 License

MIT License

---

## 👤 Author

* GitHub: chi-papa

---

## 🔐 Privacy

本ツールは基本的にすべての処理をブラウザ内で完結させます。
個人情報が外部に送信されることはありません（IP国判定を除く）。
