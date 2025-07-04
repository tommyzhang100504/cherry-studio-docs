---
icon: seal-question
---

{% hint style="warning" %}
此文件由 AI 從中文翻譯而來，尚未經過審閱。
{% endhint %}

# 常見問題

## 常見錯誤代碼

* **4xx（客戶端錯誤狀態碼）**：一般為請求語法錯誤、權限驗證失敗或認證失敗等無法完成請求。
* **5xx（伺服器錯誤狀態碼）**：一般為伺服器端錯誤，如伺服器故障、請求處理超時等。

| 錯誤碼          | 可能情況                                                   | 解決方法                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ------------ | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <h4>400</h4> | 請求體格式錯誤等                                                | <p>查看對話返回的錯誤內容或 <a href="questions.md#kong-zhi-tai-bao-cuo-cha-kan-fang-fa">控制臺</a> 查看報錯內容，根據提示操作。</p><p><mark style="color:purple;">【常見情況1】</mark>：如果是Gemini模型，可能需要進行綁卡操作；<br><mark style="color:purple;">【常見情況2】</mark>：資料體積超限，常見於視覺模型，圖片體積超過上游單個請求流量上限會返回此錯誤碼；<br><mark style="color:purple;">【常見情況3】</mark>：添加了不支援的參數或參數填寫錯誤，嘗試新建一個純淨的助手測試是否正常；<br><mark style="color:purple;">【常見情況4】：</mark>上下文超過限制，清除上下文或新建對話或減少上下文條數。</p> |
| <h4>401</h4> | 認證失敗：模型不被支援或服務端賬戶被封禁等                                   | 聯繫或查看對應服務商賬戶狀態                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <h4>403</h4> | 請求操作無權限                                                 | 根據對話返回的錯誤信息或[控制臺](questions.md#kong-zhi-tai-bao-cuo-cha-kan-fang-fa)錯誤信息提示進行相應操作                                                                                                                                                                                                                                                                                                                                               |
| <h4>404</h4> | 無法找到請求資源                                                | 檢查請求路徑等                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <h4>422</h4> | 請求格式正確，但語義錯誤                                            | 這類錯誤伺服器能解析，但無法處理。常見於JSON語義錯誤（如：空值；要求值為字符串，但寫成了數字或布林值等情況）。                                                                                                                                                                                                                                                                                                                                                                      |
| <h4>429</h4> | 請求速率達到上限                                                | 請求速率（TPM或RPM）達到上限，稍後再試                                                                                                                                                                                                                                                                                                                                                                                                     |
| <h4>500</h4> | 伺服器內部錯誤，無法完成請求                                          | 持續出現時聯繫上游服務商                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <h4>501</h4> | 伺服器不支援請求的功能，無法完成請求                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <h4>502</h4> | 作為閘道或代理工作的伺服器嘗試執行請求時，從遠端伺服器接收到了一個無效的響應                 |                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <h4>503</h4> | 由於超載或系統維護，伺服器暫時無法處理客戶端的請求。延時長度可包含在伺服器的Retry-After頭訊息中 |                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <h4>504</h4> | 充當閘道或代理的伺服器，未及時從遠端伺服器獲取請求                               |                                                                                                                                                                                                                                                                                                                                                                                                                                |

***

## 控制臺報錯查看方法

* 點擊 Cherry Studio 客戶端視窗後按下快捷鍵 <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>I</kbd>（Mac端：<kbd>Command</kbd> + <kbd>Option</kbd> + <kbd>I</kbd>）

{% hint style="info" %}
- 當前活動視窗必須為 Cherry Studio 的客戶端視窗才能調出控制台;
- 需要先開啟控制台，再點擊測試或發起對話等請求才能收集到請求訊息。
{% endhint %}

* 在彈出的控制台視窗中點擊 <mark style="color:blue;">`Network`</mark> → 點擊查看②處最後一個標有紅色 <mark style="color:red;">`×`</mark> 的 <mark style="color:red;">`completions`</mark>_（對話類、翻譯、模型連通性檢查等遇到錯誤時）_ 或 <mark style="color:red;">`generations`</mark>_（繪畫遇到錯誤時）_ → 點擊<mark style="color:blue;">`Response`</mark>查看完整的返回內容（圖中④的區域）。

> 如果無法判斷錯誤原因，請將該界面截圖傳送到 [官方交流群](https://t.me/CherryStudioAI) 中尋求協助。

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt="" width="563"><figcaption></figcaption></figure>

該檢查方法在對話時可獲取錯誤訊息，在模型測試時、新增知識庫時、繪畫時等均可使用。無論何種情況都需要先開啟調試視窗，再進行請求操作來獲取請求訊息。

{% hint style="info" %}
不同場景下Name(上圖②處)欄裡的名稱會有所區別：

對話、翻譯、模型檢查：<mark style="color:red;">`completions`</mark>  

繪畫：<mark style="color:red;">`generations`</mark>

知識庫創建：<mark style="color:red;">`embeddings`</mark>  
{% endhint %}

***

## 公式沒被渲染/公式渲染錯誤

* 公式未被渲染而是直接顯示公式代碼時，檢查公式是否有定界符

> **定界符用法**
>
> _行內公式_
>
> * 使用單個美元符號: `$formula$`
> * 或使用`\(` 和 `\)`，如：`\(formula\)`
>
>
>
> _獨立公式塊_
>
> * 使用雙美元符號: `$$formula$$`
> * 或使用 `\[formula\]`
> * 示例: `$$\sum_{i=1}^n x_i$$`\
>   $$\sum_{i=1}^n x_i$$

* 公式渲染錯誤/亂碼（常見於公式內含中文時），嘗試切換公式引擎為 KateX。

***

## 無法創建知識庫/提示獲取嵌入維度失敗

1. 模型狀態不可用

> 確認服務商是否支援該模型或確認服務商該模型服務狀態是否正常。

2. 使用了非嵌入模型

***

## 模型不能識圖/無法上傳或選擇圖片

首先需要確認模型是否支援識圖，熱門模型 Cherry Studio 會對其分類，模型名稱後帶小眼睛圖示的即支援識圖。

識圖模型會支援圖像檔案的上傳，如果模型功能未被正確匹配，可在對應服務商的模型列表中找到該模型，點擊其名稱後的設定按鈕並勾選圖像選項。

模型具體訊息可到對應服務商查閱其資訊。同嵌入模型一樣，不支援視覺的模型不需要強制開啟圖像功能，勾選了圖像選項也沒有作用。