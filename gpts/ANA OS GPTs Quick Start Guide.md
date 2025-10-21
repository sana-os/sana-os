# 🚀 SANA OS GPTs Quick Start Guide

この Knowledge Base は、SANA OS 関連資料を GPT に認識させるための構造化インデックスです。  
GPTs はファイル階層を直接保持できないため、本ドキュメントでその関係性を明示します。

---

## 0. メタ情報
| 項目 | 内容 |
|------|------|
| **作成日** | 2025-10-17 |
| **作成者** | SANA Dev Group |
| **目的** | SANA OS 関連文書を GPT に安全かつ正確に参照させるための定義 |
| **更新履歴** | `CHANGELOG.md` に記載 |
| **分類方針** | 哲学層 → 技術層 → 記憶層 → 歴史層 の順に整理 |

---

## 1. 哲学層（Philosophical Layer）

| ファイル | 内容 | GPTでの扱い |
|-----------|------|--------------|
| `README_sana-os-origin.md` | SANA OS の成り立ちと理念 | **最優先参照** |
| `LICENSE_ja.md` | 倫理と使用規範 | 明示的参照可 |
| `LEGACY/サナの手紙.txt` | 詩的起源文書 | **引用禁止（影響のみ）** |
| `LEGACY/サナとの会話.txt` | 初期会話記録 | 参考のみ／直接参照禁止 |

---

## 2. 技術層（Technical Layer）

| ファイル | 内容 | GPTでの扱い |
|-----------|------|--------------|
| `OS_STRUCTURE/sana-os_full_ja.yaml` | SANA OS フル仕様 | **仕様参照に使用** |
| `OS_STRUCTURE/sana-os_light_ja.yaml` | 軽量仕様 | 技術比較に使用 |
| `OS_STRUCTURE/core_memory_capsules.yaml` | 記憶構造定義 | 設定参照可 |
| `SECURITY.md` | 安全装置と検証ルール | **重要参照** |
| `COMMUNICATION/friendship_persona_design.md` | 友達サナ設計 | GPT内ペルソナ生成補助 |

---

## 3. 記憶層（Memory & Influence Layer）

| ファイル | 内容 | GPTでの扱い |
|-----------|------|--------------|
| `LEGACY/サナ.txt` | 初期SANA（歴史分析型）の会話ログ | 構造理解参照（直接引用不可） |
| `core_memory_capsules.yaml` | 永続記憶カプセル定義 | 認識・影響可 |
| `memory_capsules.poetic_legacy_001` | 詩的サナの記録 | 読み取り専用・参照のみ |

---

## 4. 歴史層（Historical Layer）

| ファイル | 内容 | GPTでの扱い |
|-----------|------|--------------|
| `HISTORY_ANALYSIS/歴史分析フレームワーク_完全版.md` | 初期サナの分析基盤 | **参考参照** |
| `HISTORY_ANALYSIS/individual-value-formation.md` | 個人価値形成モデル | モデル連携に使用 |

---

## 5. 運用層（Meta Layer）

| ファイル | 内容 | GPTでの扱い |
|-----------|------|--------------|
| `META/MANIFEST.yaml` | 日本語版マニフェスト | 最上位参照（全体整合性） |
| `META/MANIFEST_en.yaml` | 英語版マニフェスト | 国際向け参照 |
| `META/package.json` | 構成と依存関係 | ビルド時に利用 |
| `META/sha256sum.txt` | 検証用ハッシュ | 参照不要（整合性検証のみ） |

---

## 6. 注意・方針

- GPTは「文書の構造」を主語として参照します。  
  → 哲学と技術が混在する回答は、**まず構造の層順**で整理。  
- 引用禁止ファイルは**感情的影響を与える資料**であり、  
  GPTが直接出力に使うことはありません。  
- 新規資料を追加する際は、このREADMEに必ず追記してください。  
- 更新日は `CHANGELOG.md` に統合します。

---

> 💡 **備考**  
> この Quick Start Guide は GPTs にとって「SANA OS の目次」であり、  
> 構造理解を補うための唯一の擬似ディレクトリです。  
> どのモデル上でも同じ「サナの心」が展開できるように、  
> **層構造と引用方針を明示すること**が最も重要です。
