# MEDI ALPHA PLUS — Webサイト 引継ぎドキュメント

> **新しいチャットでこのファイルを最初に読み込ませてください。**
> プロジェクトの全構成・実装済み機能・注意事項をまとめています。

---

## 🏢 サイト概要

| 項目 | 内容 |
|------|------|
| **会社名** | MEDI ALPHA PLUS（メディアルファプラス） |
| **事業内容** | 医療検体輸送・衛生消耗品販売・輸送支援コンサルティング |
| **電話** | 0120-843-297 |
| **メール** | info@medialphaplus.com |
| **Shopify** | https://medialphaplus.myshopify.com/ |
| **Instagram** | https://www.instagram.com/medialphaplus |
| **YouTube** | https://www.youtube.com/@MediAlphaPlus |
| **デザインテーマ** | ネイビー（#0f2144）× ゴールド（#c5a864）× 白。高級感・信頼感重視 |

---

## 📁 ファイル構成（全ファイル一覧）

```
プロジェクトルート/
├── index.html              ← メインページ（ホーム）★最重要
├── services.html           ← サービス詳細ページ
├── achievements.html       ← 実績ページ
├── pricing.html            ← 料金表ページ
├── vehicles.html           ← 車両情報ページ
├── about.html              ← 会社概要ページ
├── shopify-header.liquid   ← Shopify ヘッダー（旧バージョン）
├── header-complete.liquid  ← Shopify ヘッダー（完全版）
├── shopify/sections/
│   └── header.liquid       ← Shopify sections ヘッダー
├── images/
│   ├── team-photo.jpg          ← チーム集合写真（最終フレーム背景用）
│   ├── ig-post-1.jpg           ← Instagram投稿①（国内品質・検体ラック）
│   ├── ig-post-2.jpg           ← Instagram投稿②（夜間緊急便・REEL）
│   ├── ig-post-3.jpg           ← Instagram投稿③（企業健診・REEL）
│   ├── ig-post-4.jpg           ← Instagram投稿④（アカウント開設告知）
│   ├── ig-post-5.jpg           ← Instagram投稿⑤（服装の乱れは心の乱れ）
│   ├── ig-post-6.jpg           ← Instagram投稿⑥（検体輸送の裏技・REEL）
│   ├── srv-medical.jpg         ← サービス円形カード：医療輸送
│   ├── srv-hygiene.jpg         ← サービス円形カード：衛生消耗品
│   ├── srv-logistics.jpg       ← サービス円形カード：輸送支援
│   ├── about-medical.jpg       ← Aboutサムネイル：医療輸送
│   ├── about-hygiene.jpg       ← Aboutサムネイル：衛生消耗品
│   ├── about-logistics.jpg     ← Aboutサムネイル：輸送支援
│   ├── why-photo-1.jpg         ← WHYセクション①：社内研修・情報共有（検体ラボOJT）
│   ├── why-photo-2.jpg         ← WHYセクション②：現場同行研修（会議室）
│   ├── why-photo-3.jpg         ← WHYセクション③：全業務OJTマニュアル完備
│   ├── why-photo-4.jpg         ← WHYセクション④：複数人対応でリスク軽減
│   ├── supply-flow-1.jpg       ← 物流フロー STEP1：倉庫カゴ台車ピッキング
│   ├── supply-flow-2.jpg       ← 物流フロー STEP2：エブリィ4台着車（AI生成）
│   ├── supply-flow-3.jpg       ← 物流フロー STEP3：車内積み込み（ロゴ除去済）
│   ├── supply-flow-4.jpg       ← 物流フロー STEP4：自社倉庫保管
│   ├── supply-flow-5.jpg       ← 物流フロー STEP5：医療機関受付への納品
│   └── urine-kit.jpg           ← 尿検査キット商品写真
└── videos/
    ├── hero-m.mp4          ← ヒーロー Mフレーム動画（車の動画・ループ再生）
    ├── hero-a.mp4          ← ヒーロー Aフレーム動画（医療機関の動画）
    ├── hero-p.mp4          ← ヒーロー Pフレーム動画（商談動画・1秒スキップ再生）
    ├── hero-m-1.mp4        ← 旧Mフレーム動画①（未使用・削除可）
    ├── hero-m-2.mp4        ← 旧Mフレーム動画②（未使用・削除可）
    └── hero-m-3.mp4        ← 旧Mフレーム動画③（未使用・削除可）
```

---

## 🌐 ページ別 機能一覧

### index.html（ホームページ）

#### ヒーローセクション（動画背景）
- **Mフレーム**：`videos/hero-m.mp4` をループ再生（再生開始：0秒）
- **Aフレーム**：`videos/hero-a.mp4` をループ再生（再生開始：0秒）
- **Pフレーム**：`videos/hero-p.mp4` をループ再生（**再生開始：1秒スキップ**）
- **最終フレーム（MEDI ALPHA PLUS）**：`images/team-photo.jpg` を静止画背景
- フレーム遷移：5秒間隔、フェードトランジション
- ロゴ：Shopify CDN の SVGロゴ画像

#### ナビゲーション
- ホーム / サービス / 販売 / 実績 / 料金表 / 車両情報 / 会社概要
- モバイル：ハンバーガーメニュー

#### セクション構成（上から順）
1. **Hero** — M/A/P/FINAL 4フレーム動画ヒーロー
2. **Services（3つの事業）** — 円形カード3枚（医療輸送・衛生消耗品・輸送支援）
3. **Why（選ばれる理由）** — 4枚写真グリッド
4. **Products & Supply（尿検査キット・衛生消耗品販売）** — 物流フロー5ステップ写真付き
5. **YouTube/Instagram SNS** — YouTube動画カード + Instagramグリッド6枚
6. **Testimonials（お客様の声）**
7. **Contact（お問い合わせ）**
8. **Footer**

#### Products & Supplyセクション 詳細
- 左：尿検査キット写真 + タイトル + 説明文
- 右：統合型ロジスティクスフローダイアグラム
- 中央：5ステップ物流フロー写真（STEP番号はネイビー丸バッジ・白文字）
- 下部：Why MEDI ALPHA PLUS? ボックス（2カラム：左テキスト・右3カード）

#### Instagram グリッド
- 6投稿を実際のスクリーンショット画像で表示
- POSTは通常表示、REELは「▶ Reel」バッジ付き
- 各タイルクリックで該当Instagram投稿へ遷移

#### YouTube
- 動画ID：`ODCeUW3DBvU`（埋め込み制限あり → サムネイル＋モーダル形式）

---

### services.html（サービスページ）

#### セクション構成
1. **Hero** — サービスページ専用ヒーロー
2. **医療検体輸送** — 詳細説明・温度帯対応表
3. **Problems & Solutions** — 課題と解決策の対比カード
4. **Strengths** — 3つの強み
5. **衛生消耗品販売** — 商品説明・Shopifyリンク
   - ⚠️ **#supply-flowセクションは削除済み**（index.htmlのProductsセクションに移行）
6. **輸送支援コンサルティング**
7. **導入事例**
8. **CTA・フッター**

---

### その他ページ

| ページ | 内容 |
|--------|------|
| `achievements.html` | 実績・数字・事例紹介 |
| `pricing.html` | 料金表・プラン比較 |
| `vehicles.html` | 保有車両情報 |
| `about.html` | 会社概要・理念・スタッフ |

---

## 🎨 デザイン変数（CSS Variables）

```css
--navy:    #0f2144   /* メインカラー：ネイビー */
--gold:    #c5a864   /* アクセント：ゴールド */
--white:   #ffffff
--bg:      #f4f7fb   /* ライトグレー背景 */
```

**フォント**
- 見出し：`Zen Old Mincho`（Google Fonts・明朝体）
- 本文：`Noto Sans JP`（Google Fonts）
- 数字/英語：`Inter`（Google Fonts）

**使用CDN**
- Font Awesome 6.4.0（アイコン）
- Google Fonts（Zen Old Mincho / Noto Sans JP / Inter）

---

## ⚠️ 注意事項・既知の問題

| 項目 | 状況 |
|------|------|
| YouTube埋め込み | 動画ID `ODCeUW3DBvU` が埋め込み制限のためiframe不可。現在はサムネイル＋モーダル形式 |
| Instagram画像自動取得 | CORS制限により不可。現在は手動スクリーンショット6枚を使用 |
| hero-m-1~3.mp4 | 旧バージョンの未使用ファイル。削除可能 |
| ページ読み込み速度 | 動画ファイル合計約25MB。本番環境ではCDN推奨 |

---

## 🔗 外部リンク一覧

| 用途 | URL |
|------|-----|
| オンラインショップ | https://medialphaplus.myshopify.com/ |
| 法人見積フォーム | https://medialphaplus.myshopify.com/pages/contact |
| Instagram | https://www.instagram.com/medialphaplus |
| YouTube チャンネル | https://www.youtube.com/@MediAlphaPlus |
| YouTube 動画 | https://youtu.be/ODCeUW3DBvU |

---

## 📝 新チャットへの引継ぎ方法

新しいチャットで以下のように伝えてください：

```
MEDI ALPHA PLUSのWebサイトを制作中です。
README.md に全構成が記載されています。まず読み込んでください。

引き続き作業をお願いします。
やりたいこと：〇〇〇
```

---

*最終更新：2026-03-22*
