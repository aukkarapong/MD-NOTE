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
            <ion-input placeholder="กรอกอีเมล์" [(ngModel)]="loginEmail"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-item>
            <ion-label position="floating">Password</ion-label>
            <ion-input placeholder="กรอกรหัสผ่าน" [(ngModel)]="loginPassword" type="password"></ion-input>
          </ion-item>
        </ion-col>
      </ion-row>
      <ion-row>
        <ion-col>
          <ion-button expand="block" fill="outline" (click)="onClickLoginButton()">
            Login (เข้าสู่ระบบ)
          </ion-button>
        </ion-col>
      </ion-row>
    </ion-grid>
  </div>
</ion-content>
```
