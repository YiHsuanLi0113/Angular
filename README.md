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
- ※若出現如下錯誤
  ```
  npm ERR! code SELF_SIGNED_CERT_IN_CHAIN
  npm ERR! self signed certificate in certificate chain
  ```
  則輸入
  ```
  npm set strict-ssl false
  ```
  即可正常安裝
      
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
  - 若啟動出現以下訊息
    ```
    An unhandled exception occurred: Cannot find module '@angular-devkit/build-angular/package.json'
    Require stack:
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\node_modules\@angular-      devkit\architect\node\node-modules-architect-host.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\node_modules\@angular-devkit\architect\node\index.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\models\architect-command.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\commands\serve-impl.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\node_modules\@angular-devkit\schematics\tools\export-ref.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\node_modules\@angular-devkit\schematics\tools\index.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\utilities\json-schema.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\models\command-runner.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\lib\cli\index.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\lib\init.js
    - C:\Users\ez4577\AppData\Roaming\npm\node_modules\@angular\cli\bin\ng
    See "C:\Users\ez4577\AppData\Local\Temp\ng-zS1CrO\angular-errors.log" for further details.
    npm ERR! code ELIFECYCLE
    npm ERR! syscall spawn
    npm ERR! file C:\Windows\system32\cmd.exe
    npm ERR! errno ENOENT
    npm ERR! smartadmin-angular-seed@0.8.1 start: `ng serve --port 4300`
    npm ERR! spawn ENOENT
    npm ERR!
    npm ERR! Failed at the smartadmin-angular-seed@0.8.1 start script.
    npm ERR! This is probably not a problem with npm. There is likely additional logging output above.
    npm WARN Local package.json exists, but node_modules missing, did you mean to install?

    npm ERR! A complete log of this run can be found in:
    npm ERR!     C:\Users\ez4577\AppData\Roaming\npm-cache\_logs\2020-05-20T10_13_48_699Z-debug.log
    PS D:\TeamProject\SKG建議書升級建置專案\Development\Source\AngularWeb>
    ```
    則輸入以下指令
    ```
    npm install --save-dev @angular-devkit/build-angular
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
  
- 在Visual Studio Code中開啟Terminal
  - `ctrl` + `~`
