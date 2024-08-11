# Coraline-Interview-Challenge-Data-Engineer

**Candidate Name:** Tanakit Gittibahnpachaa (Get)

## Project Structure
```
Coraline-Interview-Challenge-Data-Engineer/
│
├── README.md
│ # เอกสารที่อธิบายโปรเจกต์
│
├── [For Candidate] Challenge - DE.pdf
│ # เอกสารที่เกี่ยวข้องกับ Interview Challenge (Data Engineer)
│
├── [For candidate] de_challenge_data.xlsx
│ # ไฟล์ Excel ที่มีข้อมูลสำหรับ Challenge นี้
│
├── config.ini
│ # ไฟล์การตั้งค่าการเชื่อมต่อฐานข้อมูล
│
├── cat_reg.sql
│ # SQL Query สำหรับแสดงผลลัพธ์ของ Challenge นี้
│
├── clean_code.py
│ # Python Source code ที่มีเฉพาะโค้ด
│
├── code_with_explanations.py
│ # Python Source code ที่มีคำอธิบายอย่างละเอียด
```

## Structure and Main Functions of Python Source code
โค้ดนี้ถูกออกแบบมาเพื่อนำเข้าข้อมูลจากไฟล์ Excel ไปยังฐานข้อมูล PostgreSQL โดยแบ่งออกเป็นฟังก์ชันย่อยต่างๆ ได้แก่
### Database Connection
ฟังก์ชัน ```connect_to_db``` ใช้ไลบรารี ```psycopg2``` เพื่อเชื่อมต่อกับฐานข้อมูล PostgreSQL โดยอ่านค่าการตั้งค่าจากไฟล์ config.ini
### Load Data from Excel File
ฟังก์ชัน ```load_excel_data``` ใช้ไลบรารี ```pandas``` เพื่ออ่านข้อมูลจากไฟล์ Excel และแปลงเป็น DataFrame
### Process Data
ฟังก์ชัน ```process_data``` ทำการตรวจสอบข้อมูล เช่น ตรวจสอบชื่อคอลัมน์, กรองข้อมูลที่ขาดหาย, และแปลงชนิดข้อมูลให้เหมาะสมก่อนนำไปใส่ในฐานข้อมูล
### Create Table in Database
ฟังก์ชัน ```create_table``` สร้างตารางในฐานข้อมูล โดยก่อนสร้างจะทำการลบตารางเก่าที่มีชื่อเดียวกันออก เพื่อป้องกัน error ในระหว่างการทดสอบโค้ด
### Insert Data into Table
ฟังก์ชัน ```insert_data``` แทรกข้อมูลจาก DataFrame ลงในตารางที่สร้างขึ้น โดยใช้คำสั่ง SQL เพื่อเพิ่มประสิทธิภาพและความปลอดภัย

## Project Results





