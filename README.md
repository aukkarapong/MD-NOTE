# IONIC-2023 @20230505

## Create ionic project ด้วย command line
```sh
ionic start ionic-login-demo blank
```

## เตรียม login form
```html
<ion-header [translucent]="true">
  <ion-toolbar>
    <ion-title>
      ionic-login-demo
    </ion-title>
  </ion-toolbar>
</ion-header>

<ion-content [fullscreen]="true">
  <ion-header collapse="condense">
    <ion-toolbar>
      <ion-title size="large">ionic-login-demo</ion-title>
    </ion-toolbar>
  </ion-header>

  <div id="container">
    <ion-grid>
      <ion-row>
        <ion-col>
          <ion-item>
            <ion-label position="floating">Email</ion-label>
            <ion-input placeholder="กรอกอีเมล์"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-item>
            <ion-label position="floating">Password</ion-label>
            <ion-input placeholder="กรอกรหัสผ่าน" type="password"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-button expand="block" fill="outline">
            Login (เข้าสู่ระบบ)
          </ion-button>
        </ion-col>
      </ion-row>
    </ion-grid>
  </div>
</ion-content>
```

## ใช้งาน data storage ใน ionic 6
https://ionicframework.com/docs/v6/angular/storage
https://github.com/ionic-team/ionic-storage

## install plugin
```sh
npm install @ionic/storage-angular
```

## src/app/app.module.ts
```ts
import { IonicStorageModule } from '@ionic/storage-angular'

@NgModule({
  declarations: [AppComponent],
  imports: [
    BrowserModule, 
    IonicModule.forRoot(), 
    AppRoutingModule,
    IonicStorageModule.forRoot()
  ],
  providers: [{ provide: RouteReuseStrategy, useClass: IonicRouteStrategy }],
  bootstrap: [AppComponent],
})
export class AppModule {}
```

## แก้ package.json
- ปรับ version "@angular***/***":"16.0.0" ไปเป็น "@angular/***":"15.0.0"
- "rxjs": "~7.8.0" ไปเป็น "rxjs": "~7.5.0"
- "zone.js": "~0.13.0" ไปเป็น "zone.js": "~0.11.4"
- "typescript": "~5.0.2" ไปเป็น "typescript": "~4.8.4"

## ลบไฟล์ package-lock.json

## ลบ folder node_module

## ลง package ใหม่ด้วยคำสั่ง npm i หรือ npm install


```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="utf-8" />
  <title>Ionic App</title>

  <base href="/" />

  <meta name="color-scheme" content="light dark" />
  <meta name="viewport" content="viewport-fit=cover, width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <meta name="format-detection" content="telephone=no" />
  <meta name="msapplication-tap-highlight" content="no" />

  <link rel="icon" type="image/png" href="assets/icon/favicon.png" />

  <!-- add to homescreen for ios -->
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="black" />
</head>

<body>
  <app-root></app-root>
</body>

</html>

```
