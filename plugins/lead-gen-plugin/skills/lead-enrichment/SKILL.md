---
name: lead-enrichment
description: เพิ่มข้อมูลรายละเอียดให้กับ publisher ใช้เมื่อมี list publisher แล้วต้องการข้อมูลเพิ่มเติมเกี่ยวกับผู้ติดต่อ, track record, publishing terms
---

# Lead Enrichment (Publisher Edition)

## ขั้นตอน

1. อ่านไฟล์ CSV ของ lead ที่ต้อง enrich
2. สำหรับแต่ละ publisher ค้นหาข้อมูลเพิ่มเติม:
   - **ชื่อและตำแหน่งผู้ติดต่อด้าน publishing** (Publishing Manager, Business Development)
   - **อีเมลติดต่อ** (ถ้าเป็นข้อมูลสาธารณะบนเว็บไซต์หรือ LinkedIn)
   - **เกมที่เพิ่งประกาศรับ** (เช็คเว็บไซต์หรือ Twitter ล่าสุด)
   - **ข่าวล่าสุดของ publisher** ในรอบ 6 เดือน
   - **Publishing terms โดยประมาณ** (จาก press kit หรือ interview)
   - **ความสนใจใน SEA games** (มีประวัติรับเกมจาก SEA หรือไม่)
3. สร้างไฟล์ enriched CSV ใหม่วางใน prospects/2-enriched/

## ข้อห้าม

- ห้ามเดาอีเมลที่ไม่แน่ใจ ให้ระบุว่า "ต้องยืนยัน" หรือ "LinkedIn outreach"
- ข้อมูลทุกชิ้นต้องระบุแหล่งที่มา
- ถ้าไม่พบ contact info ให้ระบุว่า "หาข้อมูลไม่ได้ — ใช้ LinkedIn outreach แทน"
