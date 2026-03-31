---
name: lead-scoring
description: ให้คะแนน publisher ตามเกณฑ์ที่กำหนดเพื่อจัดลำดับความสำคัญ ใช้ skill นี้ทุกครั้งที่มีการวิเคราะห์ lead ใหม่ ค้นหา publisher ใหม่ หรือเมื่อถามว่า lead ไหนควรติดต่อก่อน
---

# Lead Scoring System (Publisher Edition)

สำหรับการหา Publishing Partner เกม PC/Steam

**คะแนนเต็ม 100 คะแนน**

## เกณฑ์การให้คะแนน

### 1. Platform Focus (25 คะแนน)

- **มีเกม PC/Steam ใน catalog เป็นหลัก** (เผยแพร่ PC/Steam เป็น main platform) = 25 คะแนน
- **มีเกม PC/Steam ใน catalog แต่ไม่ใช่หลัก** (console หรือ mobile มากกว่า) = 15 คะแนน
- **เน้น Console/Mobile เป็นหลัก** = 5 คะแนน
- **ไม่รับ PC/Steam** = 0 คะแนน (ตัดออก)

### 2. Genre Fit (20 คะแนน)

- **ตรงกับ genre ของเกมเราโดยตรง** (เช่น survival, RPG, strategy) = 20 คะแนน
- **Genre ใกล้เคียง / มีเกมคล้ายๆ ใน catalog** = 12 คะแนน
- **Genre ต่างกันแต่เปิดรับ cross-genre** = 8 คะแนน
- **Genre ไม่เกี่ยวข้องเลย** = 0 คะแนน

### 3. Track Record & Credibility (20 คะแนน)

- **มีเกมที่ประสบความสำเร็จบน Steam (top seller, good reviews)** = 20 คะแนน
- **มีประสบการณ์ publish หลายเกม ผลงานโดยเฉลี่ยดี** = 15 คะแนน
- **มีประสบการณ์ publish บ้าง แต่ยังใหม่ / น้อยเกม** = 10 คะแนน
- **เพิ่งเริ่มต้น / ไม่มี track record ชัดเจน** = 5 คะแนน

### 4. Market Reach (15 คะแนน)

- **มี presence ระดับ global (Steam global, multi-region)** = 15 คะแนน
- **มี presence ตลาดใหญ่ (US, EU หรือ Asia ชัดเจน)** = 12 คะแนน
- **ตลาดเฉพาะ niche / ภูมิภาคเดียว** = 8 คะแนน
- **ไม่ชัดเจนเรื่อง market reach** = 3 คะแนน

### 5. ความสามารถเข้าถึง (10 คะแนน)

- **มี contact ชัดเจน (publishing email, form submission มี response)** = 10 คะแนน
- **เข้าถึงได้ผ่าน LinkedIn หรือ network** = 7 คะแนน
- **มีแค่ general inquiry ไม่รู้ว่าติดต่อใคร** = 4 คะแนน
- **ไม่มีช่องทางติดต่อที่ชัดเจน** = 1 คะแนน

### 6. Publishing Terms & Flexibility (10 คะแนน)

- **เปิดรับ indie / ยืดหยุ่นเรื่อง terms** = 10 คะแนน
- **มี history ทำ indie deals บ้าง** = 7 คะแนน
- **เน้น mid-big budget เป็นหลัก** = 4 คะแนน
- **ไม่ชัดเจน / ไม่เคยรับ indie เลย** = 2 คะแนน

## การจัดระดับ

| คะแนน | ระดับ | การดำเนินการ |
|-------|-------|-------------|
| 75-100 | 🔥 Hot | Pitch ทันที ส่ง pitch deck + steam page |
| 55-74 | 🌡️ Warm | เก็บ research เพิ่ม หา contact ที่ใช่ แล้ว pitch |
| 35-54 | ❄️ Cool | เก็บไว้ใน list ติดตามยาว |
| < 35 | 📉 Low | เก็บไว้ใน database พอมี update |

## รูปแบบผลลัพธ์

เมื่อให้คะแนนเสร็จ ให้เพิ่มคอลัมน์ต่อไปนี้ในไฟล์ CSV:

- `score` - คะแนนรวม
- `grade` - ระดับ (Hot/Warm/Cool/Low)
- `score_breakdown` - รายละเอียดคะแนนแต่ละหมวด
- `recommended_action` - แนะนำขั้นตอนถัดไปสำหรับ lead รายนี้

## ข้อห้าม

- ห้ามสร้างข้อมูล publisher ที่ไม่มีอยู่จริง
- ห้ามเดาข้อมูลที่ไม่แน่ใจ ให้ระบุว่า "ไม่พบข้อมูล"
- คะแนนเป็นเพียงแนวทาง สุดท้ายต้องใช้วิจารณญาณของทีม

## แหล่งข้อมูลสำหรับ research

- Steam store pages ของเกมที่ publisher เคยทำ
- Publisher's website / press kit
- GameIndustry.biz, GamesIndustry.biz
- LinkedIn company pages
- Twitter/X ของ publisher
