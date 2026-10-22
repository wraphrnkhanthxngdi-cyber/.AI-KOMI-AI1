# Hardware brief — KOMI AI 1

ยังไม่กำหนดสเปกตายตัวจนกว่าจะทราบงบประมาณและผู้ผลิต ใช้เอกสารนี้คุยกับ ODM/ผู้ผลิต

## ข้อมูลที่ต้องขอ
1. SoC: ผู้ผลิตและหมายเลขรุ่นเต็ม พร้อมเอกสาร BSP
2. RAM/Storage: ความจุและชนิดหน่วยความจำ
3. Display: ขนาด ความละเอียด refresh rate และ touch controller
4. Camera: sensor IDs และ camera HAL support
5. Cellular: bands, modem firmware, SIM/eSIM และการรับรองเครือข่าย
6. Connectivity: Wi-Fi, Bluetooth, GNSS, NFC (ถ้าต้องการ)
7. Security: secure boot, hardware-backed keystore, biometric support
8. Power: battery capacity, charging, thermal design
9. Software: Android baseline, vendor image, kernel source, update support
10. Lifecycle: ระยะผลิตชิ้นส่วนและระยะ security updates
11. Factory: วิธีลง serial/build, test jig, recovery และ RMA
12. Compliance: การรับรองวิทยุ/ความปลอดภัยที่ต้องใช้ในตลาดเป้าหมาย

## เกณฑ์คัดเลือกเบื้องต้น
- เลือกแพลตฟอร์มที่ผู้ผลิตยืนยันว่ารองรับ AOSP/Android build
- ต้องมีเอกสาร BSP และเส้นทางอัปเดตความปลอดภัยชัดเจน
- ต้องมี recovery และวิธีกู้คืนอุปกรณ์ที่ทดสอบได้
- หลีกเลี่ยงการเลือกชิปจากคะแนน benchmark อย่างเดียว
- ขอ development kit/reference device ก่อนสั่งผลิตจำนวนมาก

## คำถามสำหรับผู้ใช้ผลิตภัณฑ์
- งบประมาณต่อเครื่องโดยประมาณ?
- เน้นราคาประหยัด แบตอึด กล้อง หรือประสิทธิภาพ AI?
- จะจำหน่ายในประเทศไทยเท่านั้นหรือหลายประเทศ?
- ต้องการ Android app/launcher หรือ system image ของตัวเอง?
