# การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์
* วัตถุประสงค์
 1. เพื่อให้เข้าใจว่าไมโครคอนโทรเลอร์คืออะไร
 2. เพื่อให้เขียนโปรแกรมลงบนไมโครคอนโทรเลอร์เป็น
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
* ศึกษาข้อมูลเบื้องต้น 
 [การเขียนโปรแกรมเบื้องต้นกับ arduino c+](https://www.myarduino.net/article/5/%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%80%E0%B8%82%E0%B8%B5%E0%B8%A2%E0%B8%99%E0%B9%82%E0%B8%9B%E0%B8%A3%E0%B9%81%E0%B8%81%E0%B8%A3%E0%B8%A1%E0%B9%80%E0%B8%9A%E0%B8%B7%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%95%E0%B9%89%E0%B8%99%E0%B8%81%E0%B8%B1%E0%B8%9A-arduino-c-%E0%B9%82%E0%B8%84%E0%B8%A3%E0%B8%87%E0%B8%AA%E0%B8%A3%E0%B9%89%E0%B8%B2%E0%B8%87%E0%B9%82%E0%B8%9B%E0%B8%A3%E0%B9%81%E0%B8%81%E0%B8%A3%E0%B8%A1%E0%B8%82%E0%B8%AD%E0%B8%87-arduino)
* วิธีการทำการทดลอง
 1. เสียบสาย  USB Type C กับ usb to serial converter ซึ่ง USB Type C จะต้องเสียบกับคอมพิวเตอร์ด้วย ![Screenshot 2021-03-23 170103](https://user-images.githubusercontent.com/80879651/112130563-30666080-8bfb-11eb-992b-63e670a0a90b.png)
 2. เสียบ serial converter กับ ไมโครคอนโทรเลอร์ ESP-01 ![Screenshot 2021-03-23 171845](https://user-images.githubusercontent.com/80879651/112131305-02cde700-8bfc-11eb-8b15-c8921da5ceea.png)
 3. พิมพ์ใน CMD เข้าไปใน cd pattani enter cd 01_Serial-Monitor enter vi src/main.cpp enter  จะได้ค่าตามหน้านี้ ![Screenshot 2021-03-23 210625](https://user-images.githubusercontent.com/80879651/112159364-aa0e4680-8c1b-11eb-8436-4b6175be50f7.png)
 4. พิมพ์ใน CMD vi platformio.ini ซึ่งมันจะบอกว่าบอร์ดชื่ออะไร ใช้ platform framework แบบไหน enter 
![Screenshot 2021-03-23 211045](https://user-images.githubusercontent.com/80879651/112159995-4f291f00-8c1c-11eb-9e81-dbbb1a52458e.png)
 5. อัปโหลดโปรแกรม 01_Serial-Monitor ลงในไมโครคอนโทรเลอร์ ESP-01 พิมพ์ใน CMD pio run -t upload 
 6. กดปุ่มที่ตัวไมโครคอนโทรเลอร์ ESP-01 เพื่อรับโปรแกรม แล้วก็กดปุ่ม set 
 7. pio device monitor enter
![Screenshot 2021-03-23 213228](https://user-images.githubusercontent.com/80879651/112163446-a086dd80-8c1f-11eb-83fa-5d72b628303d.png)
 8. แล้วมันก็จะแสดงผลทีละ 1 วินาที 
![Screenshot 2021-03-23 213922](https://user-images.githubusercontent.com/80879651/112164184-420e2f00-8c20-11eb-802e-3b9903ed6200.png)
 9. กดปุ่ม reset ที่ไมโครคอนโทรเลอร์ ESP-01 มันก็จะเริ่มนับใหม่ ![พ](https://user-images.githubusercontent.com/80879651/112164565-91545f80-8c20-11eb-9e22-37a61bc2bb36.png)
* การบันทึกผลการทดลอง
  * ไมโครคอนโทรเลอร์สามารถรับโปรแกรมที่เขียนได้ ซึ่งมันจะแสดงผลทีละ 1 วินาที ![Screenshot (12)](https://user-images.githubusercontent.com/80879651/112289503-f2cc0b00-8cc0-11eb-8238-0f6e7cb42bc3.png)
* อภิปรายผลการทดลอง
  * ในตอนแรกนำเสียบสาย usb เข้ากับ usb to serial converter แล้วนำไมโครคอนโทรเลอร์ ESP-01 เสียบกับ usb to serial converter หลังจากนั้นกดค้นหาในโปรแกรมที่ 1 ซึ่งในโปรแกรมนั้นมันจะเป็นโปรแกรมที่ตัวเลขเพิ่มขึ้นทีละ 1 และจะเปลี่ยนเลขทีละ 1 ms หลังจากนั้นพิมพ์ platformio.ini ซึ่งมันจะบอกว่าไมโครคอนโทรเลอร์คือยี่ห้ออะไร รุ่นอะไร ใช้วิธีเขียนโปรแกรมแบบไหน หลังจากเสร็จสิ้นทุกอย่างเราก็ทำการรันโปรแกรมเข้าไปในไมโครคอนโทรเลอร์ ESP-01 โดยพิมพ์ว่า pio run -t upload พร้อมกับกดปุ่ม boost กับ reset หลังจากที่อัปโหลดโปรแกรมเสร็จแล้ว  ก็มาลองทดสอบโดยพิมพ์ว่า pio device monitor ซึ่งมันจะเริ่มนับเลขจาก 0 และเพิ่มเลขขึ้นทีละ 1 และเปลี่ยนทุก 1 ms แต่ถ้าเรากดปุ่ม reset ที่ usb to serial converter มันก็จะเริ่มนับเลขใหม่
* คำถามหลังการทดลอง
  * บอร์ดของการทดลองนี้ใช้ framework อะไร
  '<Ans arduino>'


