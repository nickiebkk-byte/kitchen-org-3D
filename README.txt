จัดระเบียบตู้ครัว 3D — ไฟล์ทั้งหมด
====================================

วิธีใช้
- อัปโหลดทั้งโฟลเดอร์นี้ขึ้นเว็บโฮสต์ (Firebase Hosting / GitHub Pages / เว็บของร้าน) ได้ทันที
  ไฟล์หน้าเว็บคือ index.html ไม่ต้อง build
- ต้องต่ออินเทอร์เน็ต เพราะโหลดไลบรารี 3D (three.js) และฟอนต์จาก CDN

โครงสร้าง
- index.html              หน้าเว็บทั้งหมด (ข้อมูลสินค้า + รูปย่อ ฝังอยู่ในไฟล์แล้ว)
- manifest.webmanifest    ตั้งค่าแอปสำหรับ Android/Chrome (เพิ่มลงหน้าจอหลัก)
- favicon.ico             ไอคอนแท็บเบราว์เซอร์ (16–256 px)
- icons/
    icon-16/32/48.png      ไอคอนเบราว์เซอร์
    icon-192/512.png       ไอคอน Android / PWA (พื้นใส)
    maskable-192/512.png   ไอคอน Android แบบ adaptive (พื้นน้ำเงิน มีขอบปลอดภัย)
    apple-touch-icon.png   ไอคอน iPhone / iPad (180 px)
    mstile-150.png         ไอคอน Windows
    icon-master.png        ต้นฉบับความละเอียดสูง (พื้นใส)
- data/
    products.csv           รายการสินค้า 28 SKU (เปิดใน Excel ได้)
    products.json          ข้อมูลสินค้า + ของใช้ประกอบภาพ 15 รายการ
    images/                รูปสินค้าที่ดึงจากไฟล์ PowerPoint (ตั้งชื่อตาม SKU)

แก้ไขสินค้า
- ข้อมูลสินค้าที่หน้าเว็บใช้อยู่ใน index.html ส่วน "const P=[" แต่ละบรรทัดคือ
  [SKU, ชื่อ, กลุ่ม, กว้าง, ลึก, สูง, 'โซน'] — โซน: upper / lower / sink / drawer
