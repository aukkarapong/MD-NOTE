#Git

## reference

Practical DEVOPS and Clound Engineer โดย อ.ดร.ณัฐโชติ พรหมฤทธิ์

## Note

- ทำไมต้อง control version

## 1. Git คือ ?

Git เป็นเครื่องมือที่ช่วยจัดการเวอร์ชันของโค้ดให้กับเรา (Version Control)ในปัจจุบัน โดยจะเก็บประวัติว่าไฟล์แต่ละไฟล์ถูกสร้าง/ลบ/แก้ไขโดยใคร เมื่อไหร่ และอย่างไรเอาไว้ทั้งหมด ทำให้เราสามารถติดตามการเปลี่ยนแปลงของโค้ดได้ตลอด หรือแม้กระทั่งย้อน Version ของโค้ดกลับไปก่อนตอนที่จะทำการแก้ไขก็ได้

## 2. ความเป็นมาของ Version Control ก่อนที่จะมาเป็น Git

### 2.1 การจัดเก็บเวอร์ชั่นด้วยวิธีการก๊อปปี้ (Copy File & Folder)

![image-2.1.1](https://raw.githubusercontent.com/mozillascience/study-group-onboarding/master/images/gh04.png)

![image-2.1.2](https://raw.githubusercontent.com/mozillascience/study-group-onboarding/master/images/gh05.png)

![image-2.1.3](https://raw.githubusercontent.com/mozillascience/study-group-onboarding/master/images/gh06.png)

**ข้อดี**

- ง่าย

**ข้อเสีย**

- งง
- ไม่รู้ว่าไฟล์ไหนใหม่กว่ากัน
- ไม่สามารถบอกได้ว่าไฟล์ไหนถูกสร้างต่อยอดมาจากไฟล์ไหน
- เปลืองพื้นที่จัดเก็บ เนื่องจากต้อง Copy ไฟล์ทั้งไฟล์ หรือทั้ง Folder

### 2.2 การจัดเก็บเวอร์ชั่นด้วยวิธีแพตช์ (Patch)

![image-2.2.1](https://blog.pjjop.org/content/images/2019/12/Screen-Shot-2562-12-15-at-16.23.04.png)

จากภาพด้านบนแสดงตัวอย่างของ Patch ที่เกิดจากการเปรียบเทียบไฟล์เก่า (Original file) และ ไฟล์ใหม่ (Changed File) Patch ที่สร้างจะแสดงถึงบรรทัดที่มีการเปลี่ยนแปลง โดยใช้เครื่องหมาย < นำหน้าบรรทัดที่หายไป และ > นำหน้าบรรทัดที่เพิ่มมาแทน

**ข้อดี**

- ลดพื้นที่การจัดเก็บ

**ข้อเสีย**

- มีความเสี่ยงต่อการทำ Patch บาง Patch หาย จนทำให้ไม่สามารถประกอบร่าง Source Code เพื่อกลับไปยัง Version ต่างๆ ได้

### 2.3 Local Version Control System

เพื่อแก้ปัญหาจากการที่จัดเก็บแบบ Patch จึงมีการพัฒนา Version Control System ที่มี Database เฉพาะคอยจัดเก็บทุกการเปลี่ยนแปลงของ Source Code โดยเราจะเรียกการจัดเก็บ Version ของ Source Code ลง Database ว่าการ "Check-In" และการเรียกคืน Source Code จาก Database เพื่อทำงานต่อว่าการ "Check-Out"

![image-2.3.1](https://blog.pjjop.org/content/images/2019/12/Screen-Shot-2562-12-15-at-23.16.23.png)

Local Version Control System เป็น Version Control ในยุคแรกๆ ที่มีความสามารถในการจัดเก็บ Version (Check-In) พร้อมทั้งข้อความช่วยจำ (Log Message) ลง Database และเรียกคืน Version จาก Database (Check-Out) กลับมายังพื้นที่ทำงาน (Working Directory) เพื่อให้ Software developers แก้ไข Source Code ต่อไป โดยเราสามารถมอง Local Version Control System ได้อีกแบบดังภาพด้านล่าง

![image-2.3.2](https://blog.pjjop.org/content/images/2019/12/image.png)

แต่การ Check-Out จากผู้ใช้หลายคนพร้อมกันอาจทำให้เกิดปัญหาขึ้นดังภาพด้านล่าง

![image-2.3.3](https://blog.pjjop.org/content/images/2019/12/Screen-Shot-2562-12-16-at-21.15.26.png)

เมื่อวิธวินท์ และกันตพร Check-Out Source Code ออกจาก Database แต่วิธวินท์ทำงานเสร็จก่อนจึงได้ Check-In กลับเป็นคนแรก เมื่อกันตพร ทำงานของตนเองเสร็จจึง Check-In บ้าง ในกรณีนี้เนื้อหาที่เพิ่งถูกเพิ่มโดย วิธวินท์ใน Version ก่อนหน้าจะถูกลบทิ้ง

เพื่อแก้ปัญหาการสูญเสียข้อมูลเมื่อมีการ Check-Out จากผู้ใช้หลายคนจึงต้องมีการ Lock Database ไว้ ไม่ให้ผู้ใช้ที่ทำงานเสร็จช้ากว่า สามารถ Check-In ตามหลังได้ ซึ่งทำให้เป็นข้อจำกัดสำคัญของ Local Version Control System

### 2.4 Centralized Version Control System

Version Control ในยุคต่อมาจึงพยายามแก้ปัญหาการใช้งานหลายคน โดยเก็บ Database ไว้บน Server เมื่อผู้ใช้ Check-Out งาน version เดียวกัน แล้วกลับมา Check-In ระบบจะพยายามรวมเนื้อหาเข้าด้วยกัน (Merge) ถ้ารูปแบบการรวมเนื้อหามีความเรียบง่าย ระบบจะ Merge ให้อัตโนมัติ แต่ถ้าการรวมมีความซับซ้อน ระบบจะแจ้งให้ผู้ใช้ผู้ตัดสินใจแทน

![image-2.4.1](https://blog.pjjop.org/content/images/2019/12/Screen-Shot-2562-12-16-at-21.14.17-1.png)

โดยเราสามารถมอง Centralized Version Control System ได้ดังภาพด้านล่าง

![image-2.4.2](https://blog.pjjop.org/content/images/2019/12/image-1.png)

Centralized Version Control System ที่ได้รับความนิยมคือ Subversion (SVN)

### 2.5 Distributed Version Control System

อย่างไรก็ตาม Centralized Version Control System มีข้อเสียสำคัญคือมันเป็นการทำงานแบบรวมศูนย์ หาก Server ล่มไปชั่วขณะ ผู้ใช้งานจะไม่สามารถ Check-In หรือ Check-Out งานได้ ถ้า Server เสียหายถาวร Version ของ Source Code ทั้งหมดก็ได้รับผลกระทบด้วย

เพราะการดึงงานจาก Centralized Version Control System จะเป็นการ Check-Out เฉพาะเวอร์ชั่น แบบ Online ขณะที่ Distributed Version Control System จะแก้ปัญหาการทำงานแบบรวมศูนย์โดยการ Clone Database มาทั้งหมด (โดยเราจะเรียก Database ที่จัดเก็บ Version ของ Source Code ว่า Repository)

ซึ่งเมื่อ Clone มาแล้วเราสามารถ Check-In และ Check-Out ใน Local Host แบบ Offline ก่อนจะ Push ขึ้นสู่ Server ในภายหลัง

โดยเราสามารถมอง Distributed Version Control System ได้ดังภาพด้านล่าง

![image-2.5.1](https://blog.pjjop.org/content/images/2019/12/image-2.png)

Distributed Version Control System ที่สำคัญตัวหนึ่ง คือ BitKeeper ซึ่งเป็น Closed Source ไม่ใช่ Open Source โดย BitKeeper ได้ถูกนำมาใช้ในการเก็บ Source Code ของระบบปฏิบัติการ Linux ในปี 2002 แบบให้ใช้ฟรี อย่างไรก็ตามในปี 2005 BitKeeper ไม่ฟรีอีกต่อไป ถ้าเราเป็น Linus Torvalds ผู้ก่อตั้ง Linux เราจะแก้ปัญหานี้อย่างไร

สำหรับ Linus แล้ววิธีแก้ปัญหาของเขาคือการพัฒนา Distributed Version Control System ขึ้นมาเองในชื่อว่า Git และจากจุดนี้เอง Git จึงถือกำเนิดขึ้นมาในปี 2005 และเปิดให้ใช้งานแบบ Open Source และ Free Software ตั้งแต่นั้นเป็นต้นมา

## 3. หลักการพื้นฐานของ Git

### 3.1 Git vs other VCS

### 3.2 Git Work Flow

## 4. เริ่มต้นใช้งาน Git (Gitlab)

### 4.1 Register & Sign in Gitlab

### 4.2 สร้าง Project บน Gitlab

### 4.3 การเชื่อมโยงกับ Remote Repository

### 4.4 การติดตั้ง Git Client และการเรียกใช้งาน

### 4.5 การ Config Git ให้พร้อมใช้งาน

### 4.6 การ Check-in Source Code

### 4.7 การ Check-in Local Repository

### 4.8 การ Sync History กับ Gitlab Server

## 5. Git Branching

## 6. สรุป Git Command

[Reference. :: https://about.gitlab.com/images/press/git-cheat-sheet.pdf](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)

![1](git-cheat-sheet/git-cheat-sheet-1.png)
![2](git-cheat-sheet/git-cheat-sheet-2.png)
![3](git-cheat-sheet/git-cheat-sheet-3.png)
![4](git-cheat-sheet/git-cheat-sheet-4.png)

## 7. Git GUI Clients

- GitHub Desktop
- GitKraken
- Sourcetree
- Tortoise Git
- SmartGit
- GitForce
- Git Cola
- Aurees
- Magit
- Fork

### 7.1 การติดตั้ง Sourcetree

### 7.2 Create Repository

### 7.3 Clone Project

### 7.4 pull/push/staged/unstaged

### 7.5 branch

### 7.5 merge
