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


https://developers.ecpay.com.tw/?p=45895
https://developers.ecpay.com.tw/?p=7398


# 綠界測試環境特店資料

## 信用卡 3D 驗證特店資料

- **特店編號 (MerchantID)**: `3002607`
- **串接金鑰 HashKey**: `pwFHCqoQZGmho4w6`
- **串接金鑰 HashIV**: `EkRm7iFT261dpevs`

## 無信用卡 3D 驗證特店資料

- **特店編號 (MerchantID)**: `2000132`
- **串接金鑰 HashKey**: `5294y06JbISpM5x9`
- **串接金鑰 HashIV**: `v77hoKGq4kWxNNIS`

---

> 這些測試環境的特店資料僅適用於測試用途，請勿用於正式環境。正式環境中的相關資訊將由綠界分配，請參考綠界官方文件以獲取正式環境的資料。

資料來源：[ECPay 開發者中心](https://developers.ecpay.com.tw/)






