# How-to-install-laradock
How to install laradock . 如何安裝laradock

這是將Laradock的官方文件，經過實際安裝後，重新整理後的安裝說明與補充內容

[Laradock 官方安裝文件](https://laradock.io/getting-started/)

## 前置作業
* 安裝 Docker
* 安裝 Docker compose

## 目錄說明
	/home
	* project
	* Laradock
在/根目錄下有兩個目錄，Laradock為操作docker與各種設定的資料夾，容器的一切操作與服務的一切設定，像nginx、DB等設定都必須透過此資料夾執行，詳情請參考 [官網說明](https://laradock.io/)

## 安裝步驟

### 1. 在根目錄新增資料夾做為專案資料夾

	mkdir [projectname]

### 2. 將 Laradock 專案下載下來

	git clone https://github.com/laradock/laradock.git