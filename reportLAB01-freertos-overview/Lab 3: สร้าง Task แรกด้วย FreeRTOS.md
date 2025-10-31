--
คำถามทบทวน
-
เหตุใด Task function ต้องมี infinite loop?
-
เพราะ Task คือ “งานที่ต้องทำต่อเนื่อง
กระพริบ LED ตลอดเวลา
อ่าน sensor ซ้ำ ๆ
รับข้อมูล UART
ทำงาน background เช่น WiFi, MQTT

ความหมายของ stack size ใน xTaskCreate() คืออะไร?
-
ขนาดของหน่วยความจำ Stack ที่ Task จะใช้สำหรับเก็บข้อมูลขณะทำงาน
เช่น ตัวแปรภายในฟังก์ชัน, ค่า return address, register, local array ฯลฯ
โดยแต่ละ Task ใน FreeRTOS จะมี “Stack ของตัวเองแยกจากกัน”

ความแตกต่างระหว่าง vTaskDelay() และ vTaskDelayUntil()?
-
vTaskDelay() = หน่วงจากตอนนี้ ไม่แม่นยำ
vTaskDelayUntil() = หน่วงตามรอบเวลา แม่นยำ ควบคุมคาบได้


การใช้ vTaskDelete(NULL) vs vTaskDelete(handle) ต่างกันอย่างไร?
-
vTaskDelete(NULL) ลบตัวเอง (self-delete) Task หยุดทำงานทันที Scheduler จะลบ stack และ resource ที่เกี่ยวข้อง

vTaskDelete(handle) ลบ task อื่น โดยใช้ TaskHandle_t
 
Priority 0 กับ Priority 24 อันไหนสูงกว่า?
-
24 คือค่าที่ “สูงสุด” ที่ Task จะชิง CPU จาก task อื่นได้ทันที
