# Computer Network Labs & Practical Infrastructure

แหล่งรวบรวมผลงานการออกแบบและจำลองระบบเครือข่ายคอมพิวเตอร์ (Cisco Packet Tracer) และบันทึกประสบการณ์ปฏิบัติงานภาคสนามด้านโครงสร้างพื้นฐานใยแก้วนำแสง (Optical Fiber & FTTx) จากการฝึกประสบการณ์วิชาชีพ ณ บริษัท โทรคมนาคมแห่งชาติ จำกัด (มหาชน) — NT

---

## ประสบการณ์โครงสร้างพื้นฐานภาคสนาม (Physical Layer — NT Internship)

บันทึกการปฏิบัติงานในบทบาทช่างเทคนิคโครงข่ายโทรคมนาคม (รวมระยะเวลา 630 ชั่วโมง) ณ บมจ.โทรคมนาคมแห่งชาติ (NT) สาขานางรอง จังหวัดบุรีรัมย์ ครอบคลุมงานสายส่งสัญญาณใยแก้วนำแสง การต่อประสานสาย และการตรวจวัดคุณภาพสัญญาณด้วยเครื่องมือเฉพาะทางระดับผู้ให้บริการ (Carrier-Grade Equipment)

### 1. อุปกรณ์โครงข่ายหลัก (Carrier-Grade OLT)
การจัดคู่สายและดูแลการเชื่อมต่อสายใยแก้วนำแสง (Optical Patch Cord) บนตู้ **Huawei SmartAX MA5800 OLT (Optical Line Terminal)** เพื่อกระจายสัญญาณระบบ GPON/FTTx ไปยังโครงข่ายปลายทาง

![Huawei SmartAX MA5800 OLT](assets/olt-huawei-ma5800.jpg)

### 2. การเชื่อมต่อสายใยแก้วนำแสง (Fusion Splicing)
การปอกสาย ทำความสะอาด ตัดระนาบหน้าตัดแกนแก้วด้วย Fiber Cleaver และเชื่อมต่อสายใยแก้วนำแสงด้วย **เครื่อง Fusion Splicer** โดยตรวจสอบแนวแกน (Core Alignment) ผ่านหน้าจอแสดงผลก่อนปล่อยสัญญาณจริง

![Optical Fiber Fusion Splicing](assets/fusion-splicing-setup.png)

### 3. การตรวจวัดและวิเคราะห์คุณภาพคู่สาย (OTDR & Loss Diagnostics)
- **OTDR Testing:** การใช้งานเครื่อง **Optical Time-Domain Reflectometer (OTDR)** เพื่อตรวจวัดระยะทางของคู่สาย วิเคราะห์ตำแหน่งจุดบกพร่อง/สายหักขาด และตรวจสอบค่าลดทอนสัญญาณแสง (Attenuation) ตลอดเส้นทางโครงข่าย
- **Optical Power Meter:** การตรวจวัดกำลังแสง (Optical Power / dBm) ที่จุดแยกสัญญาณ (Splitter) และปลายสายก่อนเข้าอุปกรณ์ ONT/ONU เพื่อให้ค่าสัญญาณอยู่ในเกณฑ์มาตรฐาน

| การตรวจวัดคู่สายด้วยเครื่อง OTDR | การตรวจสอบกำลังสัญญาณแสงที่จุดต่อปลายทาง |
|:---:|:---:|
| ![OTDR Testing](assets/otdr-measurement.png) | ![Optical Power Meter](assets/optical-power-meter-test.png) |

---

## แบบจำลองระบบเครือข่ายคอมพิวเตอร์ (Logical Layer — Cisco Packet Tracer)

การฝึกปฏิบัติการออกแบบและตั้งค่าระบบเครือข่ายคอมพิวเตอร์ในระดับ Layer 2 (Data Link) และ Layer 3 (Network) ครอบคลุมการจัดการอุปกรณ์เครือข่าย การกำหนดหมายเลขไอพี และการกำหนดเส้นทาง

### หัวข้อและเนื้อหาที่ครอบคลุม
- **การจัดสรร IP Address & Subnetting:** การคำนวณ IPv4, Variable Length Subnet Masking (VLSM) และ Classless Inter-Domain Routing (CIDR)
- **การกำหนดค่าอุปกรณ์เครือข่าย:** การตั้งค่า Router, Switch, Host และ Server เบื้องต้นผ่าน CLI
- **Virtual LAN (VLAN) & Trunking:** การแบ่งกลุ่มเครือข่ายย่อย, 802.1Q Trunking และ Inter-VLAN Routing (Router-on-a-Stick)
- **Routing Protocols:** การตั้งค่า Static Routing และ Dynamic Routing
- **Network Services:** การตั้งค่าบริการพื้นฐาน เช่น DHCP Server, DNS และ Web Server

### รายการแบบฝึกหัดปฏิบัติการ

| ชุดแล็บ | ขอบเขตการทำงาน | รายการไฟล์ (.pkt) |
|---|---|---|
| **Lab 1: พื้นฐานเครือข่ายและการต่อสาย** | การเชื่อมต่ออุปกรณ์พื้นฐาน, Peer-to-Peer, การทดสอบการสื่อสาร และ IP Addressing เบื้องต้น | [LAB-1.1](labs/LAB-1.1.pkt) · [LAB-1.2](labs/LAB-1.2.pkt) · [LAB-1.3](labs/LAB-1.3.pkt) |
| **Lab 2: Subnetting & Device Config** | Switch Configuration, การแบ่งกลุ่มเครือข่ายเสมือน (VLAN), และ Trunking | [LAB-2.1](labs/LAB-2.1.pkt) · [LAB-2.2](labs/LAB-2.2.pkt) · [LAB-2.3](labs/LAB-2.3.pkt) |
| **Lab 3: Routing & Switching** | Router Configuration, IP Subnetting และการกำหนดเส้นทาง (Routing) | [LAB-3.1](labs/LAB-3.1.pkt) · [LAB-3.2](labs/LAB-3.2.pkt) |
| **Lab 4: Integrated Network Architecture** | แบบจำลองโครงข่ายคอมพิวเตอร์แบบบูรณาการ (Integrated Network Topology) | [LAB-4.1](labs/LAB-4.1.pkt) |

### วิธีเปิดใช้งาน
ดาวน์โหลดไฟล์นามสกุล .pkt แล้วเปิดด้วยโปรแกรม **Cisco Packet Tracer** (แนะนำเวอร์ชัน 8.0 ขึ้นไป) เพื่อดู Topology ผังการเชื่อมต่อ และการตั้งค่า Configuration ของอุปกรณ์แต่ละตัว
