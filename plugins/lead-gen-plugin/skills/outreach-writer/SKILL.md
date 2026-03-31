---
name: outreach-writer
description: ร่างอีเมล pitch หรือข้อความติดต่อ publisher แบบ personalized ใช้เมื่อต้องการเขียนอีเมล pitch publisher, LinkedIn message
---

# Outreach Writer (Publisher Edition)

## ขั้นตอน

1. อ่านข้อมูล lead จากไฟล์ enriched CSV
2. อ่าน Communication Style จาก CLAUDE.md (English, professional)
3. เลือก template ที่เหมาะสมจาก outreach/templates/:
   - `pitch-to-publisher.md` — สำหรับอีเมลแรกที่ pitch
   - `follow-up-1-publisher.md` — สำหรับติดตามครั้งที่ 1
   - `follow-up-2-publisher.md` — สำหรับติดตามครั้งที่ 2
   - `linkedin-message.md` — สำหรับ LinkedIn outreach
4. สำหรับแต่ละ publisher ให้ personalize ข้อความโดย:
   - อ้างอิงเกมที่ publisher เคยทำมา (ที่ตรงกับเกมของเรา)
   - ใช้ชื่อผู้ติดต่อและตำแหน่ง (ถ้าหาได้)
   - เน้นจุดที่ตรงกับ publisher คนนั้นๆ
5. สร้างไฟล์ร่างอีเมลสำหรับแต่ละราย เก็บไว้ใน outreach/sent/drafts/ และย้าย lead ที่ร่างอีเมลแล้วไป prospects/4-contacted/

## ข้อห้าม

- ห้ามส่งอีเมลโดยไม่ผ่านการตรวจสอบจากมนุษย์
- ผลลัพธ์คือร่างเท่านั้น ต้องรอ approve ก่อนส่ง
- ห้ามใช้ข้อมูลที่ไม่ยืนยันแล้วในอีเมล
