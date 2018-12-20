# How-to-install-laradock
How to install laradock . 如何安裝laradock

這是將Laradock的官方文件，經過實際安裝後，重新整理後的安裝說明與補充內容

[Laradock 官方安裝文件](https://laradock.io/getting-started/)

## 前置作業
* 安裝 Docker
* 安裝 Docker compose

## 目錄說明
	/project
	/Laradock
在/根目錄下有兩個目錄，分別是project (或任何你想命名的專案名稱)與 Laradock資料夾，這兩個都會在安裝步驟的實後實際安裝。  
Laradock為操作docker與各種設定的資料夾，容器的一切操作與服務的一切設定，像nginx、DB等設定都必須透過此資料夾執行，詳情請考 [官網說明](https://laradock.io/)。  
project 可以用任何你可以識別的專案名稱來命名它，這資料夾會被當成傳統架設Web server會產生的 `/var/www/` 資料夾，也就是網頁伺服器的網站根目錄。

## 安裝步驟

### 1. 在根目錄新增資料夾做為專案資料夾

	mkdir [projectname]

### 2. 將 Laradock 專案下載下來

	git clone https://github.com/laradock/laradock.git