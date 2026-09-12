# Computer Network Labs & Field Experience

คลังรวบรวมไฟล์ปฏิบัติการจำลองระบบเครือข่ายคอมพิวเตอร์ (Cisco Packet Tracer) ควบคู่กับบันทึกประสบการณ์ปฏิบัติงานจริงภาคสนามด้านโครงข่ายใยแก้วนำแสง (บมจ.โทรคมนาคมแห่งชาติ - NT)

เนื้อหาภายใน Repository นี้แบ่งออกเป็น 2 ส่วนหลัก:
- [ส่วนที่ 1: ปฏิบัติการจำลองระบบเครือข่าย (Cisco Packet Tracer Labs)](#ส่วนที่-1-ปฏิบัติการจำลองระบบเครือข่าย-cisco-packet-tracer-labs)
- [ส่วนที่ 2: ประสบการณ์ภาคสนามโครงข่ายโทรคมนาคม (FTTx & Fiber Optic)](#ส่วนที่-2-ประสบการณ์ภาคสนามโครงข่ายโทรคมนาคม-fttx--fiber-optic)

---

## ส่วนที่ 1: ปฏิบัติการจำลองระบบเครือข่าย (Cisco Packet Tracer Labs)

> [!NOTE]
> ส่วนนี้เป็นงานทดลองและแบบฝึกหัดในรายวิชาเครือข่ายคอมพิวเตอร์ โดยเน้นการออกแบบ จำลองผังเครือข่าย และตั้งค่าอุปกรณ์ในระดับ Logical Network (Layer 2 & Layer 3)

### ขอบเขตและทักษะที่ปฏิบัติในแลป
- **IP Address & Subnetting:** คำนวณ IPv4, ออกแบบวงเครือข่ายด้วย VLSM (Variable Length Subnet Mask)
- **Device Configuration:** ตั้งค่าอุปกรณ์ Router, Switch, Host PC และ Server ผ่าน Command Line Interface (CLI)
- **VLAN & Switching:** แบ่ง Virtual LAN บน Switch, ตั้งค่า 802.1Q Trunking และทำ Inter-VLAN Routing (Router-on-a-Stick)
- **Routing Protocols:** กำหนดเส้นทางการรับส่งข้อมูลทั้งแบบ Static Route และ Dynamic Route
- **Network Services:** จำลองและทดสอบบริการพื้นฐานของระบบเครือข่าย เช่น DHCP Server และ DNS Server

### รายการไฟล์แลป (.pkt)
| ชุดแลป | วัตถุประสงค์และเนื้อหาการทดลอง | ดาวน์โหลดไฟล์งาน |
| :--- | :--- | :--- |
| **Lab 1** | การเชื่อมต่ออุปกรณ์พื้นฐาน, การต่อสาย LAN, และการกำหนดหมายเลข IP ให้คอมพิวเตอร์ | [LAB-1.1](labs/LAB-1.1.pkt) · [LAB-1.2](labs/LAB-1.2.pkt) · [LAB-1.3](labs/LAB-1.3.pkt) |
| **Lab 2** | การตั้งค่า Switch ขั้นพื้นฐาน, การสร้าง VLAN และการทำ Trunking ลิงก์ข้ามสวิตช์ | [LAB-2.1](labs/LAB-2.1.pkt) · [LAB-2.2](labs/LAB-2.2.pkt) · [LAB-2.3](labs/LAB-2.3.pkt) |
| **Lab 3** | การตั้งค่า Router, การแบ่ง Subnet และการกำหนดเส้นทาง (Routing) ข้ามโครงข่าย | [LAB-3.1](labs/LAB-3.1.pkt) · [LAB-3.2](labs/LAB-3.2.pkt) |
| **Lab 4** | การจำลองระบบเครือข่ายรวมหลายอุปกรณ์และเปิดใช้งานบริการเครือข่าย (Integrated Topology) | [LAB-4.1](labs/LAB-4.1.pkt) |

### ข้อกำหนดและวิธีเปิดใช้งาน
1. ติดตั้งโปรแกรม Cisco Packet Tracer (แนะนำเวอร์ชัน 8.0 ขึ้นไป)
2. ดาวน์โหลดไฟล์ `.pkt` จากตารางด้านบน
3. เปิดไฟล์เพื่อตรวจสอบ Topology, Running Configuration และทดสอบการส่ง Packet (Ping / Simulation Mode)

---

## ส่วนที่ 2: ประสบการณ์ภาคสนามโครงข่ายโทรคมนาคม (FTTx & Fiber Optic)

> [!NOTE]
> ส่วนนี้เป็นบันทึกการฝึกปฏิบัติงานจริงด้าน Physical Layer & Optical Infrastructure เพื่อศึกษาโครงข่ายสื่อสัญญาณกายภาพหน้างานจริงในระดับผู้ให้บริการโทรคมนาคม

บันทึกจากการฝึกงานตำแหน่งช่างเทคนิค ณ บมจ.โทรคมนาคมแห่งชาติ (NT) สาขานางรอง จ.บุรีรัมย์ (พ.ค. – ก.ย. 2565 รวม 630 ชั่วโมง) โดยได้ปฏิบัติงานหน้างานจริงเกี่ยวกับระบบโครงข่ายใยแก้วนำแสง FTTx ดังนี้:

### 1. ชุมสายและตู้กระจายสัญญาณ OLT (Huawei SmartAX MA5800)
- ศึกษาโครงสร้างตู้ชุมสาย Optical Line Terminal (OLT) สำหรับระบบ FTTx
- ตรวจสอบคู่สาย PON และจัดระเบียบสาย Patch Cord บนตู้กระจายสัญญาณหลักเพื่อจ่ายสัญญาณไปยังพื้นที่บริการ

![Huawei SmartAX MA5800 OLT](assets/olt-huawei-ma5800.jpg)

### 2. การตัดต่อและเชื่อมสายใยแก้วนำแสง (Fusion Splicing)
- ปฏิบัติการเตรียมเส้นใยแก้ว (Stripping & Cleaving) ทำความสะอาดปลายสาย
- ใช้งานเครื่องเชื่อมต่อสายอัตโนมัติ (Fusion Splicer) เพื่อต่อสายใยแก้วนำแสงเข้ากับกล่องพักสาย (Closure / Terminal Box)

![Optical Fiber Fusion Splicing](assets/fusion-splicing-setup.png)

### 3. การตรวจวัดและทดสอบคุณลักษณะสัญญาณแสง (OTDR & Optical Power Meter)
- **OTDR (Optical Time Domain Reflectometer):** ตรวจหาพิกัดตำแหน่งสายขาด จุดโค้งงอ (Macro-bending) หรือจุดที่มีการสูญเสียกำลังแสงสูงเกินมาตรฐานในเส้นทาง
- **Optical Power Meter:** ตรวจวัดค่าความแรงสัญญาณแสง (dBm) ที่จุดแยกสัญญาณ (Splitter) และหน้างานบ้านลูกค้าก่อนต่อเข้ากับอุปกรณ์ ONU/Router ปลายทาง

| การทดสอบหาจุดชำรุดด้วยเครื่อง OTDR | การวัดค่ากำลังแสงด้วย Power Meter |
| :---: | :---: |
| ![OTDR Testing](assets/otdr-measurement.png) | ![Optical Power Meter](assets/optical-power-meter-test.png) |

---

## สรุปความสอดคล้องของเนื้อหา (Correlation)

| ขอบเขตงาน | ส่วนที่ 1: Packet Tracer Labs | ส่วนที่ 2: NT Field Experience |
| :--- | :--- | :--- |
| **OSI Layer** | Data Link & Network Layer (Layer 2 & 3) | Physical Layer (Layer 1) |
| **ทักษะหลัก** | Network Logic, Subnetting, CLI Config, Routing Protocols | Fiber Splicing, OLT Maintenance, Optical Signal Testing |
| **เครื่องมือที่ใช้** | Cisco Packet Tracer | Fusion Splicer, OTDR, Optical Power Meter |
