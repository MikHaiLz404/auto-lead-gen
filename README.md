# Auto Lead Gen — Game Studio Publisher Outreach

ระบบหาลูกค้า (Publishing Partner) อัตโนมัติด้วย Claude Cowork สำหรับ Game Studio ที่ต้องการหา Publisher สำหรับเกม PC/Steam

---

## 🎮 Context

- **ธุรกิจ:** Game Studio (พัฒนาเกม PC/Steam)
- **เป้าหมาย:** หา Publisher ร่วมงาน
- **ตลาด:** ต่างประเทศ (English)
- **งบ:** ~10M THB
- **Stage:** Ready to Publish

---

## โครงสร้าง

```
auto-lead-gen/
├── CLAUDE.md                    # คู่มือโปรเจกต์ (กรอกข้อมูล studio + เกม)
├── README.md
├── prospects/                   # ข้อมูล publisher (Pipeline 8 สถานะ)
│   ├── 1-new/
│   ├── 2-enriched/
│   ├── 3-scored/
│   ├── 4-contacted/
│   ├── 5-replied/
│   ├── 6-meeting-booked/
│   ├── 7-closed-won/
│   └── 8-closed-lost/
├── outreach/
│   ├── templates/               # Email & LinkedIn templates
│   └── sent/drafts/            # ร่างอีเมลรอ approve
├── research/
│   ├── company-notes/           # ข้อมูล publisher เป็นรายราย
│   ├── industry-reports/        # รายงานอุตสาหกรรมเกม
│   └── game-assets.md          # ข้อมูลเกมที่จะ pitch
├── reports/
│   ├── weekly/
│   └── monthly/
├── skills/
│   └── lead-scoring/           # Publisher scoring criteria
└── plugins/
    └── lead-gen-plugin/        # Claude Cowork plugin
```

---

## 🚀 Quick Start

### 1. เตรียมข้อมูลเกม
แก้ไขไฟล์ `research/game-assets.md` ใส่ข้อมูล:
- ชื่อเกม, genre, platform
- Steam page (ถ้ามีแล้ว)
- Trailer / gameplay video
- Unique selling points
- Target audience
- Competitive analysis

### 2. แก้ไข CLAUDE.md
เปลี่ยน:
- ชื่อ Studio
- รายละเอียดเกม
- งบประมาณ
- Genre ที่ตรงกับเกม

### 3. เชื่อม MCP Connectors
Claude Desktop → Settings → Connectors:
- **Gmail** — ส่งและติดตามอีเมล
- **Google Drive** — เก็บ pitch deck, press kit
- **Google Calendar** — ตาราง call กับ publisher
- **HubSpot Free** — CRM สำหรับติดตาม pipeline

### 4. เริ่มหา Publisher
ใน Claude Cowork ให้คำสั่ง:

```
"ค้นหา publishers ที่รับ indie PC/Steam games ที่ตรงกับ genre [ของเกมคุณ] สร้าง list 10 รายพร้อมข้อมูลเบื้องต้นใน prospects/1-new/"
```

### 5. ตั้ง Scheduled Tasks
พิมพ์ `/schedule` ใน Claude Cowork:

| Task | ความถี่ | สิ่งที่ทำ |
|------|---------|----------|
| Publisher Research | ทุก 2 สัปดาห์ | หา publisher ใหม่ 10 ราย |
| Follow-up Check | ทุกวัน | เช็คอีเมลตอบกลับ, ติดตาม lead ที่รอ |
| Weekly Report | ทุกวันศุกร์ | สรุป pipeline + ความคืบหน้า |

---

## 📊 Lead Scoring (Publisher)

| คะแนน | ระดับ | การดำเนินการ |
|-------|-------|-------------|
| 75-100 | 🔥 Hot | Pitch ทันที |
| 55-74 | 🌡️ Warm | Research เพิ่ม + หา contact แล้ว pitch |
| 35-54 | ❄️ Cool | เก็บไว้ติดตาม |
| < 35 | 📉 Low | เก็บใน database |

---

## 📁 Outreach Templates

| Template | ใช้เมื่อ |
|----------|----------|
| `pitch-to-publisher.md` | อีเมล pitch แรก |
| `follow-up-1-publisher.md` | ติดตามครั้งที่ 1 (3-5 วัน) |
| `follow-up-2-publisher.md` | ติดตามครั้งที่ 2 (10 วัน) |
| `linkedin-message.md` | LinkedIn outreach |
| `pitch-first-contact.md` | Alternative first contact |

---

## ⚠️ กฎสำคัญ

- **ทุกอีเมลต้องผ่านมนุษย์ตรวจก่อนส่ง** — AI ร่าง คน approve
- **ข้อมูล publisher ต้องยืนยันจากแหล่งที่เชื่อถือได้** — Steam pages, เว็บไซต์, press kits
- **ห้ามเดา contact info** — ถ้าไม่แน่ใจ ใช้ LinkedIn outreach แทน
- **Claude Desktop ต้องเปิดอยู่** สำหรับ scheduled tasks

---

## 💰 ต้นทุน

| แพลน | ราคา | เหมาะกับ |
|------|------|----------|
| Claude Pro | ~700 บ./เดือน | เริ่มต้น |
| Claude Max | ~3,500 บ./เดือน | ใช้งานหนัก |
| HubSpot Free | ฟรี | CRM |

---

## 🔍 แหล่งข้อมูล Publisher

- **Steam Store** — ดูเกมที่คล้าย → publisher page
- **GameIndustry.biz** — ข่าว publishing deals
- **Indie Publisher Lists** — Raw Fury, Devolver, Team17, etc.
- **LinkedIn** — Publishing managers
- **Twitter/X** — Publisher announcements
