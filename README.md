# Firedragon Frontend

這是一個基於 React 的聊天應用，使用 Flask 作為後端服務器。該應用允許用戶與 ChatGPT 進行對話，並支持 Markdown 格式的訊息顯示。

## 目錄

* [安裝](#安裝)
* [運行項目](#運行項目)
* [解決依賴衝突](#解決依賴衝突)
* [後端設置](#後端設置)
* [功能](#功能)
* [文件結構](#文件結構)
* [聯繫方式](#聯繫方式)

## 安裝

首先，克隆這個倉庫到你的本地機器：

```bash
git clone https://github.com/yourusername/firedragonfrontend.git
cd firedragonfrontend
```

然後，安裝項目的依賴包：

### 使用 npm

```bash
npm install
```

### 使用 yarn

如果你更喜歡使用 yarn，可以運行以下命令：

```bash
yarn install
```

## 運行項目

在安裝完所有依賴包後，你可以運行以下命令來啟動開發服務器：

### 使用 npm

```bash
npm start
```

### 使用 yarn

```bash
yarn start
```

## 解決依賴衝突

在安裝依賴包時，你可能會遇到以下錯誤：

```
ERESOLVE unable to resolve dependency tree
```

這是由於 `react-markdown` 需要 `react@>=18`，而你的項目目前使用的是 `react@17.0.2`。有幾種方法可以解決這個問題：

### 方法一：升級 React 到版本 18

1. 在你的項目根目錄中運行以下命令來升級 React 和 ReactDOM：

   ```bash
   npm install react@18 react-dom@18
   ```

2. 然後安裝 `react-scripts`：

   ```bash
   npm install react-scripts
   ```

### 方法二：使用 `--legacy-peer-deps` 選項

1. 在你的項目根目錄中運行以下命令來安裝 `react-scripts`，忽略 peer 依賴衝突：

   ```bash
   npm install react-scripts --legacy-peer-deps
   ```

### 方法三：使用 yarn 來安裝依賴

1. 首先，安裝 `yarn`：

   ```bash
   npm install -g yarn
   ```

2. 然後，在你的項目根目錄中運行以下命令來安裝所有依賴：

   ```bash
   yarn install
   ```

## 後端設置

後端使用 Flask 作為服務器。以下是後端的設置步驟：

1. 安裝 Python 和 pip。
2. 創建虛擬環境並激活它：

   ```bash
   python -m venv venv
   source venv/bin/activate  # 對於 Windows，運行 `venv\Scripts\activate`
   ```

3. 安裝後端依賴：

   ```bash
   pip install -r requirements.txt
   ```

4. 運行後端服務器：

   ```bash
   python app.py
   ```

## 功能

* 與 ChatGPT 進行對話
* 支持 Markdown 格式的訊息顯示
* 重新整理按鈕可以清除所有聊天訊息並通知後端清除所有線程

## 文件結構

```
firedragonfrontend/
├── public/
│   ├── index.html
│   └── ...
├── src/
│   ├── components/
│   │   ├── Chat.js
│   │   ├── Chat.css
│   │   └── ...
│   ├── App.js
│   ├── index.js
│   └── ...
├── .env
├── package.json
├── README.md
└── ...
```

## 聯繫方式

如果你有任何問題或建議，請隨時聯繫我。  
DC: firedragonz