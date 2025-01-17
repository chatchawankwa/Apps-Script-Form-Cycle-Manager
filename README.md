# Apps-Script-Form-Cycle-Manager
ระบบสร้างฟอร์มอัตโนมัติจาก Google Sheet โดยใช้ Apps Script สุ่มสร้างข้อสอบตามจำนวนที่กำหนด เมื่อผู้ใช้ส่งคำตอบ ระบบจะประมวลผลและตรวจสอบความถูกต้อง หากไม่ผ่าน 100% จะสร้าง Trigger ใหม่และส่ง URL ทาง Email ให้ผู้ใช้ทำซ้ำเฉพาะส่วนที่ผิด โดยจำกัด 15 คิวต่อการทำงานพร้อมกัน

# 🎯 Google Form Auto-Generation System

ระบบสร้างและจัดการแบบทดสอบอัตโนมัติผ่าน Google Forms โดยใช้ Apps Script ในการสุ่มสร้างข้อสอบ ตรวจสอบ และจัดการการทำซ้ำจนกว่าจะผ่านเกณฑ์

## 📋 คุณสมบัติหลัก
- สร้างฟอร์มอัตโนมัติจาก Google Sheet
- สุ่มข้อสอบตามจำนวนที่กำหนด
- ตรวจสอบและประมวลผลอัตโนมัติ
- สร้างฟอร์มใหม่เฉพาะข้อที่ผิด
- ส่ง URL ทาง Email อัตโนมัติ
- รองรับการทำงานพร้อมกัน 15 คิว

## 🔄 กระบวนการทำงาน
1. **การสร้างฟอร์ม**
   - ดึงข้อมูลจาก Google Sheet
   - สุ่มสร้างข้อสอบตามเงื่อนไข
   - สร้าง Google Form อัตโนมัติ

2. **การรับข้อมูล**
   - บันทึกคำตอบลงใน Google Sheet
   - ประมวลผลความถูกต้อง
   - ตรวจสอบเกณฑ์ผ่าน (100%)

3. **การจัดการ Trigger**
   - สร้าง Trigger ใหม่สำหรับการทำซ้ำ
   - ลบ Trigger เก่าโดยอัตโนมัติ
   - จำกัดจำนวน Trigger ที่ทำงานพร้อมกัน

## ⚙️ การติดตั้ง
1. เตรียม Google Sheet สำหรับเก็บข้อมูล
2. เปิดใช้งาน Apps Script ในโปรเจค
3. คัดลอกโค้ดไปยัง Apps Script Editor
4. ตั้งค่า Trigger เริ่มต้น
5. กำหนดสิทธิ์การเข้าถึงที่จำเป็น

## 📝 การใช้งาน
1. **การเตรียมข้อมูล**
   - จัดเตรียมข้อสอบใน Google Sheet
   - กำหนดรูปแบบข้อมูลตามที่กำหนด

2. **การสร้างฟอร์ม**
   - รัน Script เพื่อสร้างฟอร์มอัตโนมัติ
   - ระบบจะสุ่มข้อสอบตามเงื่อนไข

3. **การทำแบบทดสอบ**
   - ผู้ใช้รับ URL ผ่าน Email
   - ทำแบบทดสอบและส่งคำตอบ

4. **การทำซ้ำ**
   - ระบบส่ง URL ใหม่หากไม่ผ่านเกณฑ์
   - ทำซ้ำเฉพาะข้อที่ผิด

## ⚠️ ข้อจำกัด
- รองรับการทำงานพร้อมกันสูงสุด 15 คิว
- จำกัดจำนวน Trigger ตาม Google Apps Script quota
- ต้องมีการเชื่อมต่ออินเทอร์เน็ต
- ต้องมีสิทธิ์เข้าถึง Google Services ที่เกี่ยวข้อง

## 🛠️ การแก้ไขปัญหาเบื้องต้น
- ตรวจสอบการเชื่อมต่ออินเทอร์เน็ต
- ยืนยันสิทธิ์การเข้าถึง Google Services
- ตรวจสอบรูปแบบข้อมูลใน Sheet
- ตรวจสอบ Quota ของ Trigger

## 📊 โครงสร้างข้อมูล
1. **Google Sheet**
   - Sheet1: ข้อมูลข้อสอบ
   - Sheet2: บันทึกคำตอบ
   - Sheet3: ประวัติการทำแบบทดสอบ

2. **Apps Script**
   - Main.gs: ฟังก์ชันหลัก
   - FormCreation.gs: สร้างฟอร์ม
   - TriggerManagement.gs: จัดการ Trigger
   - EmailService.gs: ส่งอีเมล

## 🔒 ความปลอดภัย
- ตรวจสอบสิทธิ์ผู้ใช้งาน
- เข้ารหัสข้อมูลสำคัญ
- จำกัดการเข้าถึง API
- บันทึกประวัติการใช้งาน
