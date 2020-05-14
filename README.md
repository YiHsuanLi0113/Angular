# Angular 9

## 開發工具

- Visual Studio Code
  - Angular 擴充套件
    - Angular Extension Pack (Will保哥)
    - Prettier-Code formatter
    
## 安裝Node.js工具

 - [Node.js](https://nodejs.org/en/) (建議v12.16.1 LTS以上，至少需要v10.13以上版本)
 
 - 驗證安裝結果的指令
   - `node -v`
     - 確認為`v12.16.1`或以上版本
   - `npm -v`
     - 確認為`v6.13.4`以上版本
   
## 安裝Angular CLI工具

開啟cmd執行以下命令

```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
```
npm install -g @angular/cli
```
  - 驗證安裝結果指令
    - `ng version`
      - 確認`9.0.5`以上版本
      
## 驗證Angular CLI
 
- 建立demo1專案資料夾與Angular專案骨架
  ```
  ng new demo1 --routing --style css
  ```
  - 這個過程會建立Angular專案檔案並自動安裝所有npm相依套件

- 進入demo1目錄
  ```
  cd demo1
  ```
  
- 啟動Angular開發伺服器並自動開啟網頁(http://localhost:4200)
  ```
  ng serve --open
  ```

## 建立新專案

1. 開啟cmd，輸入指令

 注意：切換磁碟需輸入`/D`參數
```
C:\Users\em2542>>cd /D E:
E:\>cd work\Practice\Angular //移至建立專案的位置
```


