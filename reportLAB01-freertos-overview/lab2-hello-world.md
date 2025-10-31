--
ความแตกต่างระหว่าง printf() และ ESP_LOGI() คืออะไร
--
ESP_LOGI() มีระบบ Log Level แต่ printf() ไม่มี
ESP_LOGI() มี tag เพื่อช่วยระบุโมดูล แต่ printf() ไม่มี tag และไม่มีเวลาให้
ESP_LOGI() สร้าง output แบบ thread-safe ใช้ printf() พร้อมกันอาจ ข้อความสลับกันไม่เป็นระเบียบ
  
--   
Log level ไหนที่จะแสดงใน default configuration?
--   
จะแสดง log: Error / Warning / Info

--
การใช้ ESP_ERROR_CHECK() มีประโยชน์อย่างไร?
--
ตรวจสอบ error อย่างอัตโนมัติ  ทำให้โปรแกรมรีเซตอัตโนมัติเมื่อเกิดข้อผิดพลาดร้ายแรง ดีบักง่ายขึ้น ลดโค้ดเยอะ ๆ ใช้ได้กับทุก component ของ ESP-IDF

--
คำสั่งใดในการออกจาก Monitor mode?
--
Ctrl + C

--
การตั้งค่า Log level สำหรับ tag เฉพาะทำอย่างไร?
--


   ตั้งค่า TAG "WIFI" ให้เป็น Debug
   
   esp_log_level_set("WIFI", ESP_LOG_DEBUG);
   
   ตั้งค่า TAG "MAIN" ให้เป็น Verbose

   esp_log_level_set("MAIN", ESP_LOG_VERBOSE);
