# How-to-install-laradock
How to install laradock . 如何安裝laradock

這是將Laradock的官方文件，經過實際安裝後，重新整理後的安裝說明與補充內容

[Laradock 官方安裝文件](https://laradock.io/getting-started/)

## 前置作業
* 安裝 Docker
* 安裝 Docker compose

## 目錄說明

	/project
	/laradock

以上的內容的意思是，在根目錄下分別有 `project` 與 `laradock` 兩個資料夾，分別是project (或任何你想命名的專案名稱)與 Laradock資料夾，這兩個都會在安裝步驟的實後實際安裝。  

Laradock為操作docker與各種設定的資料夾，容器的一切操作與服務的一切設定，像nginx、DB等設定都必須透過此資料夾執行，詳情請考 [官網說明](https://laradock.io/)。  

project 可以用任何你可以識別的專案名稱來命名它，這資料夾會被當成傳統架設Web server會產生的 `/var/www/` 資料夾，也就是網頁伺服器的網站根目錄。  

## 安裝步驟

### 1. 在根目錄新增資料夾做為專案資料夾

	mkdir [projectname]

### 2. 將 Laradock 專案下載下來

使用git將Laradock下載到根目錄

	git clone https://github.com/laradock/laradock.git

進入 /laradock 目錄

	cd laradock

### 3. 修改 .env 檔

3-1. 將 env-example 複製並改名成 .env 檔  

	cp env-example .env

3-2. 開啟 .env檔(以下用vi示範，也可用nano或任何編輯器)  

	vi .env

3-3. 找到 APP_CODE_PATH_HOST 欄位  

	APP_CODE_PATH_HOST=../

若找不到以上欄位，在VI可以用 `/` 搜尋字元  

3-4. 指向專案資料夾 (取代/var/www)  

	APP_CODE_PATH_HOST=../projectname/

請將資料夾改成 `../projectname/` ，這將**指向位於根目錄的projectname資料夾**  

3-5 存檔
如果使用VIM請按 `ESC` 離開插入(編輯)模式，並輸入 `:wq` 存檔離開，如果使用其他編輯器，請依照該編輯器的操作方式存檔離開。
