
{% hint style="warning" %}
このドキュメントはAIによって中国語から翻訳されており、まだレビューされていません。
{% endhint %}

# カスタムプロバイダー

Cherry Studio は主要なAIモデルサービスを統合しているだけでなく、強力なカスタマイズ機能も提供します。**カスタムAIプロバイダー**機能を使用することで、必要なあらゆるAIモデルを簡単に接続できます。

## なぜカスタムAIプロバイダーが必要なのか？

* **柔軟性：** 事前設定されたプロバイダーリストに制限されず、ニーズに最適なAIモデルを自由に選択可能
* **多様性：** 様々なプラットフォームのAIモデルを試し、それぞれの特徴を活用できる
* **制御性：** APIキーやアクセスアドレスを直接管理し、セキュリティとプライバシーを確保
* **カスタマイズ性：** プライベートデプロイメントのモデルを接続し、特定の業務要件に対応

## カスタムAIプロバイダーの追加方法

Cherry StudioにカスタムAIプロバイダーを追加するのは簡単な数ステップで完了します：

<figure><img src="../../.gitbook/assets/image (2) (5).png" alt=""><figcaption></figcaption></figure>

1. **設定を開く：** Cherry Studioの左サイドバーで「設定」（歯車アイコン）をクリック
2. **モデルサービスに移動：** 設定ページで「モデルサービス」タブを選択
3. **プロバイダーを追加：** 「モデルサービス」ページで既存プロバイダーリストを確認し、下部の「＋追加」ボタンクリック
4. **情報を入力：** ポップアップで以下の情報を入力：
   * **プロバイダー名：** 識別しやすい名前（例：MyCustomOpenAI）
   * **プロバイダータイプ：** ドロップダウンから選択（現在対応：OpenAI, Gemini, Anthropic, Azure OpenAI）
5. **設定を保存：** 「追加」ボタンをクリックして設定を保存

## カスタムAIプロバイダーの設定

<figure><img src="../../.gitbook/assets/image (3) (5) (1).png" alt=""><figcaption></figcaption></figure>

追加後、リストからプロバイダーを選択して詳細設定を実施：

1. **有効化状態：** リスト右端のトグルスイッチでサービスの有効/無効を切り替え
2. **APIキー：**
   * AIプロバイダーから提供されたAPIキーを入力
   * 右側の「チェック」ボタンでキーの有効性を確認
3. **APIアドレス：**
   * AIサービスのベースURLを入力
   * 公式ドキュメントを参照し正確なアドレスを入力
4. **モデル管理：**

    * 「＋追加」ボタンで使用したいモデルIDを入力（例：`gpt-3.5-turbo`, `gemini-pro`）

    <figure><img src="../../.gitbook/assets/image (4) (5).png" alt=""><figcaption></figcaption></figure>

    * モデル名が不明な場合は公式ドキュメントを参照
    * 「管理」ボタンで既存モデルの編集・削除を実施

## 利用開始

上記設定完了後、チャットインターフェースでカスタムAIプロバイダーとモデルを選択し、AIとの対話を開始できます！

## vLLMをカスタムAIプロバイダーとして使用

vLLMはOllamaのような高速で使いやすいLLM推論ライブラリです。Cherry Studioとの統合手順：

1. **vLLMをインストール：** 公式ドキュメント（[https://docs.vllm.ai/en/latest/getting_started/quickstart.html](https://docs.vllm.ai/en/latest/getting_started/quickstart.html)）に従いインストール

    ```sh
    pip install vllm # pipを使用する場合
    uv pip install vllm # uvを使用する場合
    ```
2. **vLLMサービスを起動：** OpenAI互換インターフェースで起動（2種類の方法）：
    * `vllm.entrypoints.openai.api_server`での起動
    ```sh
    python -m vllm.entrypoints.openai.api_server --model gpt2
    ```
    * `uvicorn`での起動
    ```sh
    vllm --model gpt2 --served-model-name gpt2
    ```
    デフォルトポート`8000`で起動を確認（`--port`パラメータでポート変更可）

3. **Cherry StudioにvLLMプロバイダーを追加：**
   * 前述の手順で新規プロバイダーを追加
   * **プロバイダー名：** `vLLM`
   * **プロバイダータイプ：** `OpenAI`を選択
4. **vLLMプロバイダーを設定：**
   * **APIキー：** vLLMはキー不要なので空欄または任意の値を入力
   * **APIアドレス：** vLLMサービスのアドレス（例：`http://localhost:8000/`）
   * **モデル管理：** vLLMでロードしたモデル名を入力（例：`gpt2`）
5. **対話開始：** vLLMプロバイダーとモデルを選択し、LLMとの対話を開始

## ヒントとテクニック

* **ドキュメントを精読：** プロバイダー追加前に公式ドキュメントでAPIキー・アドレス・モデル名を確認
* **APIキーチェック：** 「チェック」ボタンでキーの有効性を検証
* **APIアドレス注意：** プロバイダーやモデルによりアドレスが異なるので正確に入力
* **モデル選択：** 実際に使用するモデルのみ追加し、無用な追加を避ける