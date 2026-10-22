# ความปลอดภัยและการปล่อยรุ่นทดลอง

- อย่าพยายามข้ามหน้าจอล็อกหรือระบบป้องกันของอุปกรณ์
- ใช้เฉพาะอุปกรณ์ทดสอบที่เป็นของทีมและได้รับอนุญาต
- ปลดล็อก bootloader เฉพาะตามเอกสารผู้ผลิต โดยเข้าใจว่าข้อมูลอาจถูกลบ
- ห้ามเผยแพร่ private signing keys, service credentials หรือ API keys ใน repository
- ใช้ backend สำหรับเรียก AI และเก็บ secrets ใน secret manager/environment ของเซิร์ฟเวอร์
- ปิด debug interface ในรุ่น release
- ใช้ signed builds, verified boot, OTA signing และ recovery ที่ตรวจสอบได้
- ทำ privacy notice และขอ consent สำหรับไมโครโฟน/ข้อมูลที่ส่งไป AI
- มีช่องทางรายงานบั๊กและขั้นตอนย้อนกลับรุ่นเมื่อพบปัญหา
