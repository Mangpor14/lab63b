# การทดลองที่ 5 เรื่อง การเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซิร์ฟเวอร์
* วัตถุประสงค์
 1. สร้างเว็บเซิร์ฟเวอร์ผ่านไวไฟ
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
* ศึกษาข้อมูลเบื้องต้น 
 [การเชื่อมต่อไวไฟและเว็ปเซิร์ฟเวอร์](https://lovecodingblogger.blogspot.com/2018/01/web-server-sensor-2-nodemcu-web-server.html)
* วิธีการทำการทดลอง
 1. เข้าไปที่โปรแกรมที่ 5 : พิมพ์ใน cmd cd05_Wifi-Web-Server enter 1s enter vi src/main.cpp enter ![Screenshot 2021-03-24 122504](https://user-images.githubusercontent.com/80879651/112260155-0618af80-8c9c-11eb-89f4-a1a4a1fb03f8.png)
 2. โปรแกรมต่อกับไวไฟ จึงต้องรู้ username และ password ของไวไฟ
 3. อัปโหลดโปรแกรมเข้าไปใน ไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio run -t upload พร้อมกับเสียบ ไมโครคอนโทรเลอร์ ESP-01 เข้ากับ usb to serial converter ![Screenshot 2021-03-24 123024](https://user-images.githubusercontent.com/80879651/112260561-ba1a3a80-8c9c-11eb-8d6d-4ee65abed5fb.png)
 4. ระหว่างรอโปรแกรมอัปโหลด ก็ไปค้นหาเว็ปเบราเซอร์ ![Screenshot 2021-03-24 124027](https://user-images.githubusercontent.com/80879651/112261276-2184ba00-8c9e-11eb-81e0-c72be828722b.png)
 5. เมื่ออัปโหลดเสร็จแล้ว ก็เข้าไปเช็คในเว็ปเบราเซอร์ที่เปิดรอไว้
 6. เมื่อให้มันทำงานใหม่ กดปุ่ม reset ที่ usb to serial converter เว็ปสามารถทำงานได้
 7. ใส่เป็น html
 8. แก้โปรแกรม ให้ตัวอักษรใหญ่ขึ้น Hello cnt ใส่ #h1 enter เพื่อให้ตัวอักษรใหญ่ขึ้น 
 9. อัปโหลดโปรแกรมลงในไมโครคอนโทรเลอร์ pio run -t upload enter
 10. ผลลัพธ์ของการรันโปรแกรม พิมพ์ใน cmd pio device monitor enter สามารถสร้างเว็บเซิร์ฟเวอร์ผ่านไวไฟได้ และแก้เป็นอักษรตัวใหญ่
* การบันทึกผลการทดลอง
* อภิปรายผลการทดลอง
* คำถามหลังการทดลอง

