---
icon: book-bookmark
---

{% hint style="warning" %}
このドキュメントはAIによって中国語から翻訳されており、まだレビューされていません。
{% endhint %}

# 知識解説

## トークンとは？

トークンはAIモデルがテキストを処理する際の基本単位であり、モデルが「思考」する最小単位と理解できます。これは私たちが理解する文字や単語と完全には一致せず、モデル独自の特殊なテキスト分割方法です。

#### 1. 中国語の分かち書き
* 1つの漢字は通常1-2トークンに符号化されます
* 例：`"你好"` ≈ 2-4トークン

#### 2. 英語の分かち書き
* 一般的な単語は通常1トークン
* 長い単語や一般的でない単語は複数のトークンに分割されます
* 例：
  * `"hello"` = 1トークン
  * `"indescribable"` = 4トークン

#### 3. 特殊文字
* スペースや句読点などもトークンを消費します
* 改行文字は通常1トークンです

{% hint style="info" %}
ベンダーごとにTokenizerは異なり、同じベンダーの異なるモデル間でも違いがあります。この解説はトークンの概念を明確にするためのみです。
{% endhint %}

***

## Tokenizer（トークナイザー）とは？

Tokenizer（トークナイザー）はAIモデルがテキストをトークンに変換するツールです。入力テキストをモデルが理解可能な最小単位に分割する方法を決定します。

### なぜモデルごとにTokenizerが異なるのか？

#### 1. 学習データの違い
* 異なるコーパスが最適化方向に差異を生む
* 多言語サポートの程度差
* 医療・法律など特定分野向けの最適化

#### 2. 分かち書きアルゴリズムの違い
* BPE (Byte Pair Encoding) - OpenAI GPTシリーズ
* WordPiece - Google BERT
* SentencePiece - 多言語シナリオに適応

#### 3. 最適化目標の違い
* 圧縮効率を重視するケース
* 意味保存を重視するケース
* 処理速度を重視するケース

### 実際の影響
同じテキストでもモデルによってトークン数が異なる場合があります：

```
入力："Hello, world!"
GPT-3: 4 tokens
BERT: 3 tokens
Claude: 3 tokens
```

***

## 埋め込みモデル（Embedding Model）とは？

**基本概念:** 埋め込みモデルは高次元の離散データ（テキスト・画像など）を低次元の連続ベクトルに変換する技術で、機械が複雑なデータをより良く理解・処理できるようにします。複雑なパズルを簡素な座標点に変換すると考えてください。この点にはパズルの主要な特徴が保持されています。大規模モデルエコシステムにおいて、人間が理解可能な情報をAIが計算可能な数値形式に変換する「翻訳者」として機能します。

**動作原理:** 自然言語処理の例では、埋め込みモデルは単語をベクトル空間内の特定位置にマッピングします。この空間では意味的に近い語が自動的に集まります。例えば：

* 「王様」と「女王」のベクトルは近くなります
* 「猫」と「犬」といったペット関連語も距離が近くなります
* 「車」と「パン」のように無関係な語は距離が遠くなります

**主な応用シナリオ：**
* テキスト分析：文書分類、感情分析
* 推薦システム：パーソナライズドコンテンツ推薦
* 画像処理：類似画像検索
* 検索エンジン：意味検索最適化

**中核的利点：**
1. 次元削減効果：複雑なデータを扱いやすいベクトル形式に簡素化
2. 意味保持：元データの重要な意味情報を保持
3. 計算効率：機械学習モデルの学習・推論効率を大幅向上

**技術的価値：** 埋め込みモデルは現代AIシステムの基礎コンポーネントであり、機械学習タスクに高品質なデータ表現を提供します。自然言語処理、コンピュータビジョンなどの分野発展を推進する重要技術です。

***

## 知識検索におけるEmbeddingモデルの動作原理

**基本ワークフロー：**

1. **知識ベース前処理段階**
* ドキュメントを適切なサイズのchunk（テキスト塊）に分割
* 各chunkを埋め込みモデルでベクトルに変換
* ベクトルと原文をベクトルデータベースに保存

2. **クエリ処理段階**
* ユーザーの質問をベクトルに変換
* ベクトルデータベースから類似内容を検索
* 検索された関連コンテンツをLLMにコンテキストとして提供

***

## **MCP（Model Context Protocol）とは？**

MCPはオープンソースプロトコルで、大規模言語モデル（LLM）に標準化された方法でコンテキスト情報を提供することを目的としています。

* **比喩的理解：** MCPはAI分野の「USBメモリ」と想像できます。USBメモリは様々なファイルを保存でき、コンピュータに挿入すると直接使用可能です。同様に、MCPサーバーにはコンテキストを提供する様々な「プラグイン」を「挿入」でき、LLMは必要に応じてMCPサーバーにこれらのプラグインを要求し、より豊富なコンテキスト情報を得て能力を強化します。
* **Function Toolとの対比：** 従来のFunction Tool（関数ツール）もLLMに外部機能を提供しますが、MCPはより高次元の抽象化と言えます。Function Toolは具体的なタスク向けのツールであるのに対し、MCPはより汎用的でモジュール化されたコンテキスト取得メカニズムを提供します。

### **MCPの中核的利点**

1. **標準化：** MCPは統一されたインターフェースとデータフォーマットを提供し、異なるLLMとコンテキスト提供者がシームレスに連携可能
2. **モジュール化：** コンテキスト情報を独立したモジュール（プラグイン）に分解でき、管理・再利用が容易
3. **柔軟性：** LLMは自身の必要に応じて動的にコンテキストプラグインを選択可能で、よりスマートでパーソナライズされたインタラクションを実現
4. **拡張性：** MCPの設計は将来の様々なタイプのコンテキストプラグイン追加に対応し、LLMの能力拡張に無限の可能性を提供

***