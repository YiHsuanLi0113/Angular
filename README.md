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

## 補充

- 如何將npm升級到最新版本
  1. 安裝npm-windows-upgrade套件
    ```
    npm install --global --production npm-windows-upgrade
    ```
  2. 執行升級動作
     ```
     npm-windows-upgrade --npm-version latest
     ```
- How to End `ng serve`
  - `ctrl` + `C`

- Open Project with Visual Studio Code
  - 開啟cmd `code .`
