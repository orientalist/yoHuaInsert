# AWS SNS and S3 Integration with Node.js

## 簡介
這是一個用於處理 AWS Lambda 函數的 Node.js 範例應用程式，該應用程式從傳入事件中提取資料，透過指定的 API 獲取調查數據，並根據返回的結果將數據存入 AWS S3。當特定的優惠券類型被選擇時，程式還會透過 AWS SNS 發送短信通知。

## 功能
- 接收 HTTP 請求並解析請求主體中的參數。
- 通過調用外部 API 獲取調查數據。
- 根據調查結果將電話號碼分類存儲到 AWS S3。
- 根據不同的優惠券類型選擇發送短信通知。

## 安裝與使用方式
1. 確保已安裝 Node.js 和 NPM。
2. 克隆這個專案到本地：
   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository
   ```
3. 安裝必要的依賴模組：
   ```bash
   npm install aws-sdk node-fetch
   ```
4. 配置 AWS 賬戶的訪問鍵及區域設定，將 `accessKeyId`、`secretAccessKey` 和 `region` 替換為您的 AWS 設定。
5. 配置 S3 資料桶名稱和鍵。
6. 將程式碼部署到 AWS Lambda 並設置適當的事件觸發器。

## 必要的依賴模組清單
- `aws-sdk`: 用於與 AWS 服務進行交互。
- `node-fetch`: 用於發送 HTTP 請求。

## 授權條款
本專案採用 MIT 授權條款。詳細信息請參閱 [LICENSE](LICENSE) 檔案。