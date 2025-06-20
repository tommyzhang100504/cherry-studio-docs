---
description: 暂时不支持Claude模型
---

{% hint style="warning" %}
此文件由 AI 從中文翻譯而來，尚未經過審閱。
{% endhint %}

# Vertex AI

## 教學概述

### 1. 獲取 API Key

* 獲取 Gemini API Key 前，您需要先建立一個 Google Cloud 專案（若已有專案可跳過此步驟）
* 前往 [Google Cloud](https://console.cloud.google.com/projectcreate) 建立專案，填寫專案名稱後點擊「建立專案」

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* 進入 [Vertex AI 控制台](https://console.cloud.google.com/vertex-ai)
* 在創建的專案中啟用 [Vertex AI API](https://console.cloud.google.com/apis/library/aiplatform.googleapis.com?inv=1\&invt=Ab0iBA)

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

## 2. 設定 API 訪問權限

* 開啟 [服務帳戶](https://console.cloud.google.com/iam-admin/serviceaccounts) 權限介面，建立服務帳戶

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

* 在服務帳戶管理頁面找到新建立的帳戶，點擊`金鑰`並建立新的 JSON 格式金鑰

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

* 建立成功後，金鑰檔案將以 JSON 格式自動儲存至您的電腦，請 **妥善保管**

## 3. 在 Cherry Studio 設定 Vertex AI

* 選擇 Vertex AI 服務供應商
* 將 JSON 檔案對應欄位填入

<figure><img src="../../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

點擊新增 [模型](https://console.cloud.google.com/vertex-ai/model-garden)，即可開始使用！