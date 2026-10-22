# แผนพัฒนา KOMI AI 1

## ระยะ 0 — กำหนดผลิตภัณฑ์
- [ ] ตัดสินใจว่ารุ่นแรกเป็นต้นแบบภายในหรือผลิตจำหน่าย
- [ ] เลือกขนาดจอ งบประมาณ ภูมิภาค/เครือข่าย และเป้าหมายราคา
- [ ] เลือกว่าจะใช้ Android ที่มีอยู่, ODM phone reference design หรือ AOSP device port
- [ ] กำหนดนโยบายข้อมูลส่วนตัวและระยะเวลารองรับอัปเดต

## ระยะ 1 — ต้นแบบประสบการณ์ใช้งาน
- [ ] ทดสอบเว็บเดโมจาก `web-demo/index.html`
- [ ] ทำ design system: สี, typography, icon, animation, accessibility
- [ ] สร้าง KOMI Launcher สำหรับ Android
- [ ] สร้างแอป KOMI AI: chat UI, voice input/output, settings
- [ ] สร้าง backend สำหรับ AI พร้อมระบบยืนยันตัวตนและ rate limiting

## ระยะ 2 — เลือกฮาร์ดแวร์
ขอข้อมูลจากผู้ผลิต/ODM อย่างน้อย:
- SoC และรุ่นอ้างอิงที่แน่นอน
- BSP, kernel source และวิธีสร้าง image
- bootloader unlock/signing policy
- vendor blobs และไดรเวอร์กล้อง/โมเด็ม/GPU/Wi-Fi/Bluetooth
- แผน security patch, OTA, recovery และ warranty
- การทดสอบเครือข่าย/วิทยุและข้อกำหนดรับรองในประเทศเป้าหมาย

## ระยะ 3 — Android build
- [ ] ใช้เครื่อง Linux build host ตามข้อกำหนด AOSP รุ่นที่เลือก
- [ ] เริ่มจาก build guide ของอุปกรณ์ที่ผู้ผลิตรองรับ
- [ ] build และทดสอบบน emulator/บอร์ดพัฒนา ก่อนเครื่องต้นแบบ
- [ ] แยก product branding/app layer ออกจากการแก้ framework ที่ไม่จำเป็น
- [ ] ใช้ signed test build, verified boot และ OTA ที่ตรวจสอบลายเซ็นได้

## ระยะ 4 — AI และการสั่งงาน
- [ ] Chat: แสดงสถานะกำลังตอบ/ข้อผิดพลาด/ยกเลิกคำขอ
- [ ] Voice: ขอ permission อย่างชัดเจนและมีปุ่มปิดไมค์
- [ ] Actions: allowlist คำสั่งที่รองรับ และยืนยันก่อนการกระทำสำคัญ
- [ ] ไม่อ่านข้อมูลส่วนตัวหรือสั่งงานระบบโดยไม่มีสิทธิ์
- [ ] มีโหมดไม่ต่อเน็ตสำหรับหน้าจอพื้นฐานและข้อความสถานะ

## ระยะ 5 — Pilot
- [ ] ทดสอบในทีมเล็กด้วยอุปกรณ์สำรอง
- [ ] เก็บ log แบบลดข้อมูลส่วนบุคคล
- [ ] มี rollback/recovery plan และสำรองข้อมูล
- [ ] ตรวจสอบ crash, battery, thermal, connectivity, OTA และ accessibility
- [ ] อนุมัติปล่อยรุ่นหลังผ่านเกณฑ์ใน `TEST_PLAN_TH.md`
