# React 部落格

使用 React 實作的簡易部落格，並以 Redux 儲存 state 與執行 action dispatch，其中有基本的文章 CRUD 功能，以及使用者的註冊與登入機制。

[部落格連結](https://ericcch24.github.io/w24-react-redux-blog/)

![](https://i.imgur.com/TEj0XcP.png)

## 部落格架構

```
- 首頁: 顯示所有文章 - 分頁頁碼
    |      |
    |      *-- 點選文章標題
    |                  |
    |                  *-- 單篇文章
    |
    *---- 關於我
    |
    *---- 註冊 / 登入 - 使用者註冊 / 登入
    |         |
    |         *-- 發布文章
    |         *-- 點選首頁文章標題
    |                  |
    |                  *-- 單篇文章
    |                          |
    |                          *-- 編輯文章
    |                          *-- 刪除文章
    |
    *-- 登出

```

## 頁面與功能說明

- 未登入訪客：

  - 登入頁面：輸入帳號密碼後可以登入。
  - 註冊頁面：使用者可以註冊，**因後端密碼為明碼儲存，註冊後密碼將強制轉換為 `Lidemy`**。
  - About 頁面：顯示關於這個部落格的描述。
  - 文章列表頁面：可以看到所有文章，一頁只會顯示 5 筆，有分頁功能可以換頁。
  - 單篇文章頁面：點選文章標題可以看到文章完整內容。

- 註冊 / 登入後：
  - 發表文章頁面：登入後可以輸入標題與內文發布文章。
  - 編輯文章：登入後可以在單篇文章頁面編輯文章。
  - 刪除文章：登入後可以在單篇文章頁面刪除文章。

## 使用工具

- React: 以 function component + hooks 的方法實作。
- Redux: 儲存 user 與 post 相關的 state 與 dispatch action。
- Redux toolkit: 整合 action 與 reducer。
- Redux thunk: 處理 API 串接的函式執行。
- React-router-dom: 處理分頁連結。
- styled components: React component 的樣式製作。
