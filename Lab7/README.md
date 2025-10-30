1. เมื่อใดควรสร้าง component ใหม่ แทนที่จะเขียนโค้ดใน main application?

  เมื่อโค้ดเริ่มมีขนาดใหญ่ แก้ไขยาก หรือมีส่วนที่สามารถใช้งานซ้ำได้ เช่น driver, library, หรือฟังก์ชันเฉพาะ

  เพื่อให้แยกความรับผิดชอบแต่ละส่วนชัดเจน จัดการง่าย และสามารถ reuse ได้ในโปรเจกต์อื่น

2. ความแตกต่างระหว่าง REQUIRES และ PRIV_REQUIRES ส่งผลต่อการ compile อย่างไร?

  REQUIRES คือ dependency แบบ public ที่ component อื่นสามารถเข้าถึงได้ด้วย

  PRIV_REQUIRES คือ dependency แบบ private ใช้เฉพาะภายใน component นั้นเท่านั้น

  ต่างกันที่ขอบเขตของ include path และลำดับการ build — REQUIRES จะส่งต่อ dependency ให้ component อื่นเห็นด้วย ในขณะที่ PRIV_REQUIRES ไม่ส่งต่อ

3. การเลือกใช้ local component vs managed component ขึ้นอยู่กับปัจจัยใดบ้าง?

  Local Component
  ใช้เมื่อโค้ดยังอยู่ระหว่างพัฒนา แก้ไขบ่อย และใช้เฉพาะในโปรเจกต์เดียว ไม่ต้องจัดการเวอร์ชันหรือแชร์ให้ผู้อื่น

  Managed Component
  ใช้เมื่อโค้ดต้องการแชร์ให้หลายโปรเจกต์หรือหลายทีม ต้องการควบคุมเวอร์ชัน และสามารถอัปเดตผ่าน component manager ได้อัตโนมัติ

4. ในทีมงานขนาดใหญ่ จะจัดการ component dependencies อย่างไรให้มีประสิทธิภาพ?

  กำหนดขอบเขตและหน้าที่ของแต่ละ component ให้ชัดเจน

  ใช้ REQUIRES และ PRIV_REQUIRES ให้ถูกต้อง

  หลีกเลี่ยงการพึ่งพาวนกัน (circular dependency)

  ใช้ version control สำหรับ component ที่แชร์

  มีเอกสารประกอบและระบบทดสอบอัตโนมัติสำหรับทุก component

5. การทดสอบ component ที่มีการพึ่งพา hardware ทำได้อย่างไร?

  ใช้ mock หรือจำลอง hardware เพื่อแยกส่วน logic ออกจาก hardware layer

  ทดสอบ logic ได้โดยไม่ต้องใช้บอร์ดจริง

  ใช้บอร์ดจริงเฉพาะช่วง integration test

  ในบางกรณีอาจใช้ hardware-in-the-loop หรือ test rig เพื่อรันการทดสอบอัตโนมัติ
