# 綠界檢查碼與測試

## 1. 檢查碼生成步驟

1. 參數按鍵名排序
2. 將參數組裝成字串 `key1=value1&key2=value2...`
3. 在字串前後分別加上 `HashKey` 和 `HashIV`
4. URL 編碼整個字串
5. 使用 MD5 加密，並將字母轉大寫

[檢查碼詳細說明](https://developers.ecpay.com.tw/?p=2902)

## 2. 測試環境

**測試支付請求 URL**：
`https://payment-stage.ecpay.com.tw/Cashier/AioCheckOut/V5`

**常用測試參數**：
- `MerchantID`: 3002607
- `MerchantTradeNo`: 自訂唯一訂單編號
- `MerchantTradeDate`: yyyy/MM/dd HH:mm:ss
- `TotalAmount`: 1000
- `TradeDesc`: 訂單描述
- `ItemName`: 測試商品
- `ReturnURL`: 支付結果回傳的 URL

[綠界測試環境連結](https://payment-stage.ecpay.com.tw/Cashier/AioCheckOut/V5)
