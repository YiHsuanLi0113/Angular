# Angular路由器

### 路由(Routing) 

Angular提供了一個路由機制，讓我們可以方便抽**部分換區塊**，說是部分換區塊是因為在正常情況下，Angular的**根元件**(**起始模組**內所指定的**起始元件**)在一開始載入後便無法被抽換掉，只能替換根元件內的內容。

在建立Angular專案時，我們會透過指令`ng new newAppName --routing --style css`來建立專案，其中`--routing`參數讓CLI在建立專案的同時幫我們新增了一個具有路由功能的模組**AppRoutingModule**，並且將該模組註冊到**AppModule**中。
```typescript
app.module.ts

1   import { AppRoutingModule } from "./app-routing.module";
2      
3   @NgModule({
4      declarations: [AppComponent, ...],
5      imports: [
6        AppRoutingModule,
7        ...
8      ],
9      providers: [
10       ...
11     ],
12     bootstrap: [AppComponent]
13   })
```

※*將**Component**註冊到**Module**時是加在**NgModule**的**declaration**屬性中；**NgModule**要註冊到另一個**NgModule**時，則必須加到**import**屬性中。*

開啟`src\app\app-routing.module.ts`可以發現裡面宣告了一個`routes`的陣列變數，讓我們可以加入多個路由規則，最後`RouterModule.forRoot(routes)`則是將此路由變數宣告為根路由。
```typescript
1    import { NgModule } from "@angular/core";
2    import { Routes, RouterModule } from "@angular/router";
3    
4    const routes: Routes = [
5      {
6        path: "",
7        children: []
8      }
9    ];
10   
11   @NgModule({
12     imports: [RouterModule.forRoot(routes)],
13     exports: [RouterModule]
14   })
15   export class AppRoutingModule { }
```


***


### 路由插座(router-outlet) 

`<router-outlet></router-outlet>`  
我們可以將`<router-outlet>`看成**Component**的tag，因為Angular的路由機制運作結果會如同Component的tag，會以這個tag當作標記去插入指定的Component。
