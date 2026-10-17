# History

[English](#english) | [日本語](#日本語)

## English

SANA has two lineages that share this repository's history.

| Lineage | Period | License | Where |
|---|---|---|---|
| Character SANA (v2.0) | 2025-10 – 2026-01 | SANA Ethical Open License (SEOL) v1.7 | archived at [sana-os/sana-character](https://github.com/sana-os/sana-character); tag `character-v2.0-final` (commit `64a7fa7`) in this repository |
| SANA OS (v1.0 –) | 2026-04 – | SANA OS License v1.0 | this repository; tag `os-v1.0` (commit `96f08c4`) |

### Why there are two lineages

The first lineage was built when AI was used mainly as a chat partner, and it put the character of SANA in front.

SANA was later rewritten as **SANA OS**, an operating system for premise alignment. In April 2026 the rewrite replaced the earlier files in place (commit `96f08c4`, "Full replace — SANA OS v1.0"), because the author was not yet familiar with GitHub. Today it would have been published as a separate repository.

The version number therefore restarts at 1.0. SANA OS v1.0 is a different system from Character SANA v2.0, not a downgrade of it. The license also differs by lineage: SEOL v1.7 applies to the character lineage, SANA OS License v1.0 to SANA OS.

### What the replacement removed, and where it is now

Nothing was lost; it moved out of the current tree. All of the following remain in this repository's history (up to `64a7fa7`) and in the archived repository:

- Japanese editions (`README_ja.md`, `LICENSE_ja.md`, the Japanese knowledge files)
- the seven SANA personas, including SANA the Friend (`docs/Meet_the_SANAs.md`)
- the YAML editions of the OS, full and light, in English and Japanese (`src/`)
- the GPTs instructions and manifests (`gpts/`)
- the original `CHANGELOG.md` and `SECURITY.md`

### Later changes

From here on, changes are recorded with what changed, why, and the observation that prompted them — in commit messages and in `CHANGELOG.md`.

---

## 日本語

SANA には二つの系統があり、このリポジトリの履歴を共有しています。

| 系統 | 期間 | ライセンス | 場所 |
|---|---|---|---|
| キャラクターの SANA（v2.0） | 2025年10月〜2026年1月 | SANA Ethical Open License (SEOL) v1.7 | [sana-os/sana-character](https://github.com/sana-os/sana-character) にアーカイブ。このリポジトリではタグ `character-v2.0-final`（コミット `64a7fa7`） |
| SANA OS（v1.0〜） | 2026年4月〜 | SANA OS License v1.0 | このリポジトリ。タグ `os-v1.0`（コミット `96f08c4`） |

### 系統が二つある理由

最初の系統は、AI が主に会話の相手として使われていた時期に作られ、SANA のキャラクターを前面に出していました。

その後 SANA は、前提を整列させるための OS「**SANA OS**」として作り直されました。2026年4月、作者がまだ GitHub の使い方に慣れていなかったため、作り直した版が以前のファイルをそのまま置き換えています（コミット `96f08c4`「Full replace — SANA OS v1.0」）。今なら別のリポジトリとして公開するところです。

そのため、版番号は 1.0 から始まり直しています。SANA OS v1.0 は、キャラクターの SANA v2.0 を格下げしたものではなく、別のシステムです。ライセンスも系統ごとに異なり、キャラクターの系統には SEOL v1.7、SANA OS には SANA OS License v1.0 が適用されます。

### 置き換えで消えたものと、その所在

失われたものはありません。今のファイル一覧から外れただけです。次のものは、このリポジトリの履歴（`64a7fa7` まで）と、アーカイブしたリポジトリに残っています。

- 日本語版（`README_ja.md`、`LICENSE_ja.md`、日本語のナレッジファイル）
- SANA FRIEND を含む7人の SANA（`docs/Meet_the_SANAs.md`）
- OS の YAML 版（full と light、英語と日本語。`src/`）
- GPTs 用の指示とマニフェスト（`gpts/`）
- 当時の `CHANGELOG.md` と `SECURITY.md`

### これからの変更

これからの変更は、何を変えたか、なぜ変えたか、きっかけになった観察は何かを、コミットメッセージと `CHANGELOG.md` に残します。
