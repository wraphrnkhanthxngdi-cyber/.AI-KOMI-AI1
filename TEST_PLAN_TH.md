# แผนทดสอบ KOMI AI 1

ทดสอบบน emulator ก่อน แล้วทดสอบบน development device ที่ผู้ผลิตรองรับ ใช้เครื่องสำรองและสำรองข้อมูลก่อนทดสอบระบบระดับ OS

## เว็บ/UX
- [ ] หน้า Home อ่านได้ทั้งจอเล็กและใหญ่
- [ ] ปุ่มหลักมีสถานะและข้อความอธิบาย
- [ ] keyboard navigation, contrast และ text scaling
- [ ] offline fallback ของหน้าเดโม

## AI
- [ ] แชตไทย/อังกฤษและข้อความยาว
- [ ] network timeout, retry, cancel และ server error
- [ ] rate limit และการป้องกัน prompt/input ที่ไม่เหมาะสม
- [ ] ไม่มี API secret อยู่ใน client
- [ ] ผู้ใช้ลบประวัติได้ หากมีการบันทึกประวัติ

## เสียงและสิทธิ์
- [ ] ขอไมโครโฟนเฉพาะเมื่อผู้ใช้กดใช้งาน
- [ ] ปฏิเสธ permission แล้วแอปยังใช้งานแชตได้
- [ ] มีสถานะกำลังฟัง/หยุดฟังชัดเจน
- [ ] ทดสอบเสียงรบกวนและภาษาไทย
- [ ] ไม่มีการบันทึกเสียงเบื้องหลังโดยไม่แจ้ง

## คำสั่งอุปกรณ์
- [ ] จำกัดคำสั่งเป็น allowlist
- [ ] ขอการยืนยันก่อนส่งข้อความ โทรออก ซื้อของ หรือลบข้อมูล
- [ ] ปฏิเสธคำสั่งที่ไม่มีสิทธิ์
- [ ] บันทึก audit event โดยไม่เก็บข้อมูลส่วนตัวเกินจำเป็น

## อุปกรณ์จริง
- [ ] boot/reboot และ recovery
- [ ] Wi-Fi, Bluetooth, GPS, cellular, SIM
- [ ] camera, microphone, speaker, sensors
- [ ] sleep/wake, charging, battery drain, thermal throttling
- [ ] OTA update, interrupted update, rollback
- [ ] factory reset และการลบข้อมูลผู้ใช้
- [ ] verified boot/signature และการควบคุม debug builds
