# Angular如何運作

## 起於index.html

   - `angular.json` Angular專案的相關設定

```json
"architect": {
        "build": {
          "builder": "@angular-devkit/build-angular:browser",
          "options": {
            "outputPath": "dist/demo1",
            "index": "src/index.html",
            "main": "src/main.ts",
            "polyfills": "src/polyfills.ts",
            "tsConfig": "tsconfig.app.json",
            "aot": true,
            "assets": [
              "src/favicon.ico",
              "src/assets"
            ],
            "styles": [
              "src/styles.css"
            ],
            "scripts": []
          },
```

從`angular.json`可以看到`option`底下的`index`屬性設定為`index.html`，此為起始頁面，亦是Angular專案中的唯一頁面。因為Angular是SPA(Single Page Application)網站，所有的頁面切換與介面內容的改變都是透過JavaScript做即時動態切換。

## Angular專案進入點`main.ts`

- Angular如何知道AppModule是應用程式的入口呢? 打開`angular.json`看到`options`底下`main`屬性設定`main.ts`。這支程式在Angular CLI編譯打包程式實，會做為主要的程式進入點。
- 開啟src/main.ts可以發現Angular將AppModule當作起始模組載入：
 
 ```
 platformBrowserDynamic().bootstrapModule(AppModule)
  .catch(err => console.error(err));
 ```
