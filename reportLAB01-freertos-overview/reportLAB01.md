--
รูปการทดลอง ทั้งหมด
--
โครงสร้างโปรเจกต์
-
<img width="410" height="580" alt="image" src="https://github.com/user-attachments/assets/8ff004e5-9711-49bc-8732-544f83bdd826" />

Build โปรเจกต์สำเร็จ
-
<img width="1913" height="1014" alt="image" src="https://github.com/user-attachments/assets/344d9bd0-f283-4a87-a7b6-dafbf16e2b6a" />

---



Checklist การทำงาน
-
ผ่าน ตรวจสอบ ESP-IDF environment สำเร็จ

ผ่าน สร้างโปรเจกต์ใหม่ได้

ผ่าน เข้าใจโครงสร้างโปรเจกต์

ผ่าน Build โปรเจกต์สำเร็จ

ผ่าน แก้ไขโค้ดและ build ใหม่ได้

ผ่าน เข้าใจไฟล์ CMakeLists.txt

ทำแบบฝึกหัดครบ

คำถามทบทวหน

1. ไฟล์ใดบ้างที่จำเป็นสำหรับโปรเจกต์ ESP-IDF ขั้นต่ำ?

CMakeLists.txt (ของโปรเจกต์หลัก)  main/CMakeLists.txt main/main.c

 
2. ความแตกต่างระหว่าง hello_esp32.bin และ hello_esp32.elf คืออะไร?

มี symbol, debug info, address mapping, stack info, source line info

ไม่มี symbol / debug info


4. คำสั่ง idf.py set-target ทำอะไร?
   
เปลี่ยนตัวแปร TARGET ของโปรเจกต์


6. โฟลเดอร์ build/ มีไฟล์อะไรบ้าง?

ไฟล์ไบนารี output

Directory ที่สำคัญภายใน build

ไฟล์ config

BIN ทั้งหมด

build system

component


8. การใช้ vTaskDelay() แทน delay() มีความสำคัญอย่างไร?

ประหยัดทรัพยากร และ ทำให้ Multitasking ทำงานถูกต้อง
