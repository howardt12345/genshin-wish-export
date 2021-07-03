# 原神祈願記錄導出工具

中文 | [English](https://github.com/howardt12345/genshin-wish-export/blob/main/README.md)

一個使用 Electron 製作的小工具，需要在 Windows 64位操作系統上運行。

通過讀取遊戲日誌或者代理模式獲取訪問遊戲祈願記錄 API 所需的 authKey，然後再使用獲取到的 authKey 來讀取遊戲祈願記錄。

工具會在當前目錄下的 `userData` 文件夾裡保存數據，獲取到新的祈願記錄時，會與本地數據合併後保存。

需要更詳細的數據分析，可以在導出 Excel 文件後使用這個項目的網頁：[鏈接](https://github.com/voderl/genshin-gacha-analyzer)

## 從 Excel 恢復數據
https://genshin-gacha-export.danmu9.com

可以通過這個網頁從 Excel 文件導出 JSON 數據，也可以在網頁上選擇截止時間來去除重複數據。

將下載的JSON文件複製到工具的 userData 文件夾即可恢復數據。

使用網頁時一定要確保填寫正確的 UID， 選擇正確的 Excel 文件裡使用的語言。
## 其它語言

修改`src/i18n/`目錄下的 json 文件就可以翻譯到對應的語言。如果覺得已有的翻譯有不准確或可以改進的地方，可以隨時修改發 Pull Request。

## 使用說明

1. 下載工具後解壓 - [下載地址](https://github.com/biuuu/genshin-wish-export/releases/latest/download/Genshin-Wish-Export.zip)
2. 打開遊戲的祈願歷史記錄

   ![祈願歷史記錄](/docs/wish-history.png)
3. 點擊工具的“加載數據”按鈕

   ![加載數據](/docs/load-data.png)

   如果沒出什麼問題的話，你會看到正在讀取數據的提示，最終效果如下圖所示

   <details>
    <summary>展開圖片</summary>

   ![預覽](/docs/preview.png)

   </details>

如果需要導出多個賬號的數據，可以點擊旁邊的加號按鈕。

然後遊戲切換的新賬號，再打開祈願歷史記錄，工具再點擊“加載數據”按鈕。

## Devlopment

```
# 安裝模塊
yarn install

# 開發模式
yarn dev

# 構建一個可以運行的程序
yarn build
```

## License

[MIT](https://github.com/biuuu/genshin-wish-export/blob/main/LICENSE)