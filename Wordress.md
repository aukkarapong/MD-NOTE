# Wordpress

- [Wordpress](#wordpress)
  - [Wordpress คืออะไร?](#wordpress-คืออะไร)
  - [รูปแบบของ Wordpress](#รูปแบบของ-wordpress)
    - [1. wordpress.com](#1-wordpresscom)
    - [2. wordpress.org](#2-wordpressorg)
  - [ข้อดีของ Wordpress](#ข้อดีของ-wordpress)
  - [ตัวอย่างเว็บที่ทำด้วย wordpress สวย ๆ](#ตัวอย่างเว็บที่ทำด้วย-wordpress-สวย-ๆ)
  - [การติดตั้ง WordPress](#การติดตั้ง-wordpress)
    - [Requirements](#requirements)
    - [การ Install XAMPP](#การ-install-xampp)
    - [การ Install Wordpress](#การ-install-wordpress)
    - [การเข้าดูหน้า website wordpress](#การเข้าดูหน้า-website-wordpress)
    - [การเข้าใช้งานระบบจัดการเนื้อหาเว็บไซต์ (CMS)](#การเข้าใช้งานระบบจัดการเนื้อหาเว็บไซต์-cms)
  - [ตั้งค่าเริ่มต้นใช้งาน WordPress](#ตั้งค่าเริ่มต้นใช้งาน-wordpress)
    - [วิธีเข้าสู่ระบบหลังบ้าน WordPress (Dashboard)](#วิธีเข้าสู่ระบบหลังบ้าน-wordpress-dashboard)
    - [การกลับสู่หน้าบ้านเว็บ](#การกลับสู่หน้าบ้านเว็บ)
    - [การออกจากระบบ WordPress](#การออกจากระบบ-wordpress)
    - [ติดตั้งปลั๊กอิน classic editor](#ติดตั้งปลั๊กอิน-classic-editor)
    - [เปลี่ยนมาใช้ธีม Twenty Seventeen](#เปลี่ยนมาใช้ธีม-twenty-seventeen)
    - [ตั้งค่า General Settings](#ตั้งค่า-general-settings)
    - [Permalink Settings (ตั้งค่าลิงค์ถาวร)](#permalink-settings-ตั้งค่าลิงค์ถาวร)
    - [การตั้งค่าความสวยงามของ url](#การตั้งค่าความสวยงามของ-url)
  - [ใช้งาน Page/Post](#ใช้งาน-pagepost)
    - [การสร้าง Page](#การสร้าง-page)
    - [การสร้าง post](#การสร้าง-post)
  - [ตั้งค่าหน้า Home/Blog](#ตั้งค่าหน้า-homeblog)
  - [การสร้างเมนู (Menu)](#การสร้างเมนู-menu)
  - [Sidebar Footer และ Widget](#sidebar-footer-และ-widget)
  - [การเพิ่ม plugin (ปลั๊กอิน)](#การเพิ่ม-plugin-ปลั๊กอิน)
  - [การเปลี่ยนธีม (Theme)](#การเปลี่ยนธีม-theme)
  - [Woocommerce](#woocommerce)

https://codex.wordpress.org/Database_Description

[![วิธีการติดตั้ง xampp บน windows 10](https://codex.wordpress.org/images/2/25/WP4.4.2-ERD.png)


## Wordpress คืออะไร?

Wordpress เป็นโปรแกรมสำเร็จรูปที่ใช้สร้างและจัดการเนื้อหาเว็บไซต์ประเภท Contents Management System หรือเรียกย่อๆ ว่า "CMS" ซึ่งเขียนด้วยภาษา PHP และใช้ระบบจัดการฐานข้อมูล MySQL โดยมีส่วนประกอบหลักๆ คือ

1. **WordPress Core** เป็นซอฟแวร์หลัก ที่ใช้ในการจัดการเว็บไซต์ เนื้อหาและบทความต่างๆ
2. **Theme** เป็นส่วนที่กำหนดหน้าตาเว็บไซต์ ดีไซน์ หรือรูปแบบการแสดงผล
3. **Plugin** เป็นส่วนที่ช่วยเพิ่มความสามารถให้กับ WordPress เช่น ระบบสร้างหน้าเว็บไซต์ ระบบสินค้า ระบบสั่งซื้อสินค้า เป็นต้น

## รูปแบบของ Wordpress

มี 2 รูปแบบ

### 1. wordpress.com

เป็นบริการเว็บไซต์ที่เหมาะสำหรับผู้ที่ต้องการมี Blog เป็นของตัวเอง หรือผู้ที่เริ่มต้นทดลองใช้งานเว็บไซต์ โดยจะต้องสมัครสมาชิกกับทาง Wordpress.com มีทั้งใช้ฟรีและเสียตังค์ (รายเดือน/รายปี)

โดยเวอร์ชั่นฟรีจะมีความยืดหยุ่นน้อย ทั้ง Theme และ Plugin ไม่สามารถนำจากภายนอกมาติดตั้งได้ ส่วนชื่อของเว็บไซต์ จะสามารถตั้งได้ในรูปแบบซัพโดเมน คือ "ชื่อบล็อกของเรา.wordpress.com"

เวอร์ชั่นเสียตังค์ ซึ่งมีให้เลือกหลายแพลนตามความต้องการและตอบโจทย์การใช้งานมากขึ้น เช่น จดชื่อโดเมนเป็นของตัวเอง, ปรับเปลี่ยน Theme ให้มีลูกเล่นมากขึ้น, เพิ่มพื้นที่ในการจัดเก็บข้อมูล, ลง Plugin เพิ่ม เป็นต้น

### 2. wordpress.org

เป็นซอฟต์แวร์ที่ให้เราดาวน์โหลดได้ฟรี เพื่อมาติดตั้งที่ Hosting สามารถนำไปสร้างเว็บไซต์ได้อย่างอิสระ ไม่ว่าจะเป็นการปรับแต่งหน้าเว็บ หรือการนำ Theme และ Plugin จากภายนอกมาติดตั้ง หรือการทำเว็บไซต์แบบ E-commerce ที่มีระบบตะกร้าสินค้า เป็นต้น

## ข้อดีของ Wordpress

- ประหยัดเวลาและค่าใช้จ่าย
- มีดีไซน์หน้าเว็บให้เลือกหลากหลาย
- อัพเดทสะดวกและสม่ำเสมอ
- เป็นแหล่งรวมนักพัฒนา
- สามารถสร้างเว็บไซต์ได้อย่างรวดเร็ว และสวยงาม โดยไม่ต้องเสียเวลาออกแบบ หรือตกแต่งธีมให้วุ่นวาย
- WordPress มี Plugins (โปรแกรมเสริม) มากมาย ช่วยให้เว็บไซต์มีประสิทธิภาพมากขึ้น สวยงามยิ่งขึ้น และตอบ โจทย์ตรงตามความต้องการของเราได้
- ง่ายต่อการเรียนรู้สำหรับผู้เริ่มต้น เพราะมีเมนูที่เรียบง่าย เข้าใจง่าย เหมาะแก่การศึกษา และต่อยอดได้ในอนาคต
- มีการอัพเดต Version ให้มีความทันสมัยและน่าใช้อยู่เสมอ
- WordPress มีประสิทธิภาพในการทำให้เว็บไซด์ติดอันดับหน้าแรกๆ ในการค้นหาด้วย Search Engine อย่าง Google หรือที่เรียกว่า การทำ SEO (Search engine optimization) เพราะมีโครงสร้างต่างๆ รวมถึงเครื่องมือ ที่มีมาให้นั้นช่วยให้ผู้ใช้งานปรับแต่งได้สะดวกมากยิ่งขึ้น

## ตัวอย่างเว็บที่ทำด้วย wordpress สวย ๆ

https://wordpress.org/showcase/

## การติดตั้ง WordPress

ติดตั้งได้ 2 แบบ คือ

1. ติดตั้งบน web hosting (เพื่อใช้งานจริง)
2. ติดตั้งบนเครื่องเราเอง (เพื่อเรียนรู้)

### Requirements

- PHP version 7.4 ขึ้นไป
- Mysql version 5.6 ขึ้นไป or MariaDB version 10.1 ขึ้นไป
- Web server Apache หรือ Nginx

ทั้งหมดทั้งมวลที่กล่าวมามีอยู่ใน **XAMPP** ซึ้งสามารถ Download ได้จาก https://www.apachefriends.org/index.html

และที่ขาดไม่ได้เลย Highlight ของงานคือ **Wordpress** ซึ่ง Download ได้จาก https://wordpress.org/download/

### การ Install XAMPP

1. Download XAMPP ได้ที่ https://www.apachefriends.org/index.html
2. ติดตั้ง XAMPP (บน windows 10)

   [![วิธีการติดตั้ง xampp บน windows 10](https://img.youtube.com/vi/-f8N4FEQWyY/0.jpg)](https://www.youtube.com/watch?v=-f8N4FEQWyY)

### การ Install Wordpress

- Download Wordpress ได้ที่ https://wordpress.org/download/
- แตก zip ไฟล์เตรียมไว้
- เข้าไปที่ phpMyAdmin สร้าง database
- สร้าง folder ที่จะ install wordpress ใน XAMPP
- นำ code wordpress ไปวางที่ XAMPP (folder htdocs)
- เริ่มต้น install wordpress โดยการเข้าไปที่ http://localhost/ชื่อ-folder-ที่วางไฟล์-wordpress/

### การเข้าดูหน้า website wordpress

http://localhost/ชื่อ-folder-ที่วางไฟล์-wordpress/

### การเข้าใช้งานระบบจัดการเนื้อหาเว็บไซต์ (CMS)

http://localhost/ชื่อ-folder-ที่วางไฟล์-wordpress/wp-admin

## ตั้งค่าเริ่มต้นใช้งาน WordPress

### วิธีเข้าสู่ระบบหลังบ้าน WordPress (Dashboard)

http://localhost/ชื่อ-folder-ที่วางไฟล์-wordpress/wp-admin

### การกลับสู่หน้าบ้านเว็บ

ให้คลิกที่รูปสัญลักษณ์บ้าน

### การออกจากระบบ WordPress

ดูที่มุมบนขวา เอาเมาส์ไปชี้ แล้วจะเจอคำสั่ง Logout

### ติดตั้งปลั๊กอิน classic editor

เนื่องจาก WordPress เวอร์ชั่น 5.0+ มีการเปลี่ยน Editor (เครื่องมือสำหรับการเขียนข้อมูล) จากเวอร์ชั่นเก่าที่เป็น Classic Editor มาเป็น Gutenberg ซึ่งทำให้การใช้งานเปลี่ยนไปทั้งหมด

เข้าไปที่ `Plugin` > `Add New` > `ค้นหาปลั๊กอินชื่อ Classic Editor` > `คลิก Install` และ `Activate`

ถ้าหน้าจอเด้งให้เรากรอก FTP ให้เราทำดังนี้ (ในกรณีที่ลงเครื่องตัวเองและไม่มี FTP)

- เปิดไฟล์ wp-config.php
- เพิ่ม code

  ```php
  define('FS_METHOD','direct');
  ```

- ถ้าขึ้น error `Installation failed: Could not create directory.` ให้ทำการแก้ไข permission folder /wp-content/plugins/ ให้สามารถ write ได้

  ```sh
  #เครื่อง Mac
  cd /Applications/XAMPP/htdocs/wp-01
  chmod -R 777 wp-content
  ```

### เปลี่ยนมาใช้ธีม Twenty Seventeen

ไปที่ `Appearance` > `Themes` > `คลิก Add new` > `ค้นหา Twenty Seventeen` > `คลิก Install`

### ตั้งค่า General Settings

ดูที่เมนูด้านซ้าย ไปที่ Settings > คลิก General

- เปลี่ยน Site Language --> ไทย
- เปลี่ยน Timezone --> UTC+7
- เปลี่ยน Date Format --> 07/09/2021 [d/m/Y]
- เปลี่ยน Time Format --> 18:32 [H:i]

### Permalink Settings (ตั้งค่าลิงค์ถาวร)

ไปที่ `Settings` > `Permalink` แล้วให้ติ๊กที่ช่อง `Post name (หรือ ชื่อเรื่อง)`

### การตั้งค่าความสวยงามของ url

สร้างไฟล์ .htaccess ไปวางไว้ใน folder

```.htaccess
# BEGIN WordPress
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /wp-01/
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /wp-01/index.php [L]
</IfModule>
# END WordPress
```

## ใช้งาน Page/Post

**`Page (หน้า)`** คือ หน้าที่ไม่จำเป็นต้องแบ่งหมวดหมู่เนื้อหา ไม่ต้องเรียงลำดับของวันที่ว่าใครจะมาก่อนมาหลัง โดยมากเราจะใช้ Page กับหน้าเว็บที่เป็นข้อมูลนิ่งๆ เช่น หน้า Home, About, Contact เป็นต้น

**`Post (เรื่อง หรือ บทความ)`** คือ หน้าข้อมูลที่เราต้องการแบ่งเนื้อหาตาม category เช่น ตามชนิดสินค้า ตามประเภทความรู้ ตามภาค ตามจังหวัด ตามกลุ่ม ตามเวลา (ใหม่/เก่า) ฯลฯเมื่อเราเขียน Post หรือบทความเสร็จ (รวมถึงสินค้าที่เราจะขายด้วย) เราต้องสร้าง Category เพื่อทำเป็นหมวดหมู่ให้เขาอยู่นั้นเองเมื่อถึงเวลาก็แสดงผลเป็นหมวดหมู่ ตามสไตล์บล็อก คือ เรียงบทความตามหมวดหมู่ โดยดึง Post ล่าสุดขึ้นมาแสดงด้านบนเสมอ

### การสร้าง Page

ไปที่ `Page` > `add new` > แล้วให้`ใส่ชื่อหน้า กับเนื้อหา` ลงไป แล้ว`กด Publish เผยแพร่ข้อมูล`

### การสร้าง post

ก่อนจะเริ่มต้นเขียน post จะต้องวางโครงสร้าง category ก่อน ว่าเว็บเราจะแบ่งหมวดหมู่เป็นประเภทอะไรบ้าง

เช่น เว็บขายรองเสื้อผ้าแฟชั่นอาจจะแบ่งหมวดหมู่ ได้เป็นด้งนี้

- เทรนแฟชั่น (fashion-trends)
- แฟชั่นดารา (celebrity-fashion)
- โซนเกาหลี (korean-fashion-zone)
- โซนญี่ปุ่น (japanese-fashion-zone)
- เทคนิคการแต่งตัว (dressing-technique)
- เคล็ดลับการ mix & match (mix-and-match-tips)
- ฯลฯ

การสร้าง Category

    ไปที่ `post` > `คลิก Categories`

การสร้าง Post

    ไปที่ post > add new จากนั้นให้ใส่เนื้อหาของบทความลงไป

การสร้างหน้า Blog เพื่อเอาไว้เข้าอ่าน post ต่าง ๆ

## ตั้งค่าหน้า Home/Blog

set home page

    ไปที่ settings > reading > ติ๊กที่ A static page > แล้วเลือกชื่อหน้าที่เราต้องการให้เป็นหน้า Homepage

set blog page

    ไปที่ settings > reading > ติ๊กที่ A static page > แล้วเลือกชื่อหน้าที่เราต้องการให้เป็นหน้า Posts page

## การสร้างเมนู (Menu)

ไปที่ `Appearance` > `menu` > `ตั้งชื่อเรียกชุดเมนู` > คลิก `Create Menu`

## Sidebar Footer และ Widget

ปลั๊กอิน Classic Widgets

## การเพิ่ม plugin (ปลั๊กอิน)

ไปที่ `Plugins `> คลิก `add new`

ทดสอบการเปลี่ยน font web ด้วย plugin `seed font`

ไปที่ `Appearance` > `Fonts` แล้วคลิก `Enable`

## การเปลี่ยนธีม (Theme)

**`Theme`** คืออะไร???

Theme คือ เครื่องมือที่ใช้สำหรับออกแบบ และจัดวาง layout หน้าตาเว็บไซต์ WordPress ของเราให้สวยงามในแบบที่เราต้องการ หากเราใช้งานธีมได้เก่งๆ เราจะสามารถออกแบบหน้าเว็บของเราอย่างไรก็ได้ ทุกไอเดีย หรือออกแบบเว็บเลียนแบบหน้าตาของเว็บที่เราชอบก็ได้

Theme มีอยู่ 2 ประเภท คือ

- ฟรี
- เสียตังค์ซื้อ (หรือเรียกกันว่า Premium Theme)
  - https://themeforest.net/
  - https://seedthemes.com/

ตัวอย่าง theme ฟรี พร้อม demo content https://wpastra.com/pricing/

## Woocommerce

WooCommerce คือ ปลั๊กอินที่ช่วยแปลงร่างเว็บ WordPress ให้กลายเป็นเว็บร้านค้าออนไลน์เต็มรูปแบบ สามารถโหลดตัวปลั๊กอินนี้มาใช้ฟรีๆ
