# CLAUDE.md

ไฟล์นี้ให้คำแนะนำสำหรับ Claude Code เมื่อทำงานกับ repository นี้

## ภาพรวมโปรเจกต์

โปรเจกต์นี้สำหรับการ deploy n8n ซึ่งเป็นเครื่องมือสร้าง workflow อัตโนมัติที่ช่วยเชื่อมต่อบริการต่างๆ และทำให้งานเป็นอัตโนมัติ

## โครงสร้างโปรเจกต์

```
n8n-deolpy/
├── README.md          # เอกสารโปรเจกต์
└── CLAUDE.md          # คำแนะนำสำหรับ Claude Code
```

## แนวทางการพัฒนา

- ปฏิบัติตามหลัก infrastructure-as-code
- ใช้ชื่อที่สื่อความหมายสำหรับ workflow และการตั้งค่า
- บันทึก environment variables หรือ secrets ที่จำเป็น
- ทดสอบการ deploy ใน staging environment ก่อน production

## งานที่พบบ่อย

- **Setup**: ตั้งค่า environment และ dependencies สำหรับ deployment
- **Deploy**: Deploy n8n ไปยัง infrastructure เป้าหมาย
- **Update**: อัปเดตเวอร์ชัน n8n หรือการตั้งค่า
- **Backup**: สำรองข้อมูล workflows และ credentials

## Environment Variables

รายการ environment variables ที่จำเป็น:
- `N8N_HOST` - URL ของ n8n instance
- `N8N_PORT` - หมายเลข port (ค่าเริ่มต้น: 5678)
- `N8N_PROTOCOL` - http หรือ https

## หมายเหตุ

- เก็บข้อมูลที่เป็นความลับไว้นอก version control
- ใช้ระบบจัดการ secrets สำหรับ credentials
