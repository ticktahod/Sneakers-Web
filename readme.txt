ส่วนที่ 1 โครงสร้างไฟล์ในโฟลเดอร์

firstweb ใช้เก็บข้อมูลการตั้งค่าต่างๆและ path urls
migrations เป็นการย้ายข้อมูลจากระบบฐานข้อมูลหนึ่งไปยังฐานข้อมูลหนึ่ง
static ใช้เก็บรูปพื้นหลัง
template รวมเก็บข้อมูลของ html ในเเต่ละหน้า
venv ใช้ตัว virtualenv ใช้แยก environment ของแต่ละงาน Python ออกจากกัน
media ใช้เก็บรูปภาพสินค้าและรูปโปรไฟล์
myapp จัดเก็บข้อมูลในส่วนของฟังก์ชันการทำงานต่างๆเเละฐานข้อมูลต่างๆ
requirements.txt ใช้เก็บข้อมูลทุกอย่างก่อนจะย้ายโปรเจค

ส่วนที่ 2 การติดตั้งโครงงาน

*********  ก่อนย้ายข้อมูล ************
1.สร้างไฟล์ requirements.txt ขึ้นมาใน Floder Project 
2.cd เข้าไปที่ตัวโปรเจค firstweb เเล้วพิม pip freeze > requirements.txt จากนั้นเช็คดูที่ไฟล์ว่ามีเขียนไรไหม ถ้ามีก็คือสำเร็จ
3.ทำโฟลเดอร์ firstweb ให้เป็นไฟล์ zip

********* ติดตั้งโปรเจค ************
1.ต้องติดตั้ง Python โดยดาวโหลดผ่านเว็บ https://www.python.org/ เเนะนำให้เป็นเวอร์ชั่น 3.8 ขึ้นไป (กรณีที่เคยติดตั้งและตั้งค่าใน enviromentเเล้วไม่จำเป็นต้องทำ)
2.สร้าง  Floder ขึ้นมาที่ไดร์ฟไหนก้ได้ เช่น ไดรฟ์ D โฟลเดอร์ชื่อ New_Project
3.ย้าย Floder โปรเจคจากเครื่องเก่ามาไว้ในโฟลเดอร์นี้ก่อน
4.เปิด cmd เเล้ว cd ไปยังโฟลเดอร์ที่เราสร้าง เช่น D:\New_Project
5.ติดตั้ง virtualenv ด้วยคำสั่ง pip install virtualenv เช่น D:\New_Project>pip install virtualenv
6.ติดตั้งตัว venv ด้วยคำสั่ง python -m virtualenv venv เช่น D:\New_Project>python -m virtualenv venv
7.พิม dir เพื่อเช็คว่ามีโฟลเดอร์หลักตามนี้ไหม ถ้ามีคือถูกต้อง
	11/09/2021  03:58 PM    <DIR>          .
	11/09/2021  03:58 PM    <DIR>          ..
	11/09/2021  03:41 PM    <DIR>          firstweb
	11/09/2021  04:07 PM    <DIR>          venv
8.cd เข้าไปที่ firstweb เเล้วพิม pip install -r requirements.txt เช่น D:\New_Project\firstweb>pip install -r requirements.txt
9.จากนั้นพิม cd .. เพื่อกลับมาที่  New_project เช่น D:\New_Project
10.ลอง activate ด้วยคำสั่ง .\venv\scripts\activate เช่น D:\New_Project>.\venv\scripts\activate
	ผลลัพธ์ (venv) D:\New_Project
11.cd เข้าไปที่ firstweb เพื่อติดตั้ง Django ด้วยคำสั้ง  pip install django==3.0 เช่น (venv) D:\New_Project\firstweb> pip install django==3.0
12.ติดตั้งตัว Pillow ด้วยคำสั่ง python -m pip install Pillow เช่น  (venv) D:\New_Project\firstweb>python -m pip install Pillow
*** กรณีมี markdown ด้วยให้ติดตั้ง pip install django-markdown เช่น  (venv) D:\New_Project\firstweb>pip install django-markdown ***
13.พิม python manage.py runserver เช่น  (venv) D:\New_Project\firstweb>python manage.py runserver
14.เปิด browser ขึ้นมาเเล้วพิม http://localhost:8000/ จะขึ้นหน้าเว็บไซต์มา

ถ้าหากต้องการเเก้ไขตัว code ก็สามารถเปิดโปรเจคใน Eiditor ได้ เช่น ใช้ Visual Studio Code เเล้วเลือก path floder ไปยัง firstweb

ถ้าหากต้องการเปิดดู database ก็ใช้โปรเเกรม DB Browser (SQLite) เปิดไฟล์ db.sqlite3 ที่อยู่ในโฟลเดอร์โปรเจคขึ้นมาก็จะสามารถเห็นฐานข้อมูลได้ โดยโปรเเกรมสามารถดาวโหลดได้ผ่านเว็บไซต์  https://sqlitebrowser.org/