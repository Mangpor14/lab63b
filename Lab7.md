# การทดลองที่ 7 เรื่อง การเพิ่ม variety เข้าไปในแลป 4
  ## วัตถุประสงค์
  1. เพื่อวัดความเข้มของแสงที่อยู่ในห้อง หรือสิ่งแวดล้อมรอบตัวเรา
  2. เพื่อทดสอบเซ็นเซอร์แสง
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. Adapter ต่อสาย port0 port2
 6. LED 
 7. LDR Photoresistor
 8. ตัวต้านทาน
* ศึกษาข้อมูลเบื้องต้น 
 1. [วัดความเข้มแสง](https://www.myarduino.net/article/211/%E0%B8%AA%E0%B8%AD%E0%B8%99%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99-nodemcu-esp8266-%E0%B9%80%E0%B8%8B%E0%B9%87%E0%B8%99%E0%B9%80%E0%B8%8B%E0%B8%AD%E0%B8%A3%E0%B9%8C%E0%B8%A7%E0%B8%B1%E0%B8%94%E0%B8%84%E0%B8%A7%E0%B8%B2%E0%B8%A1%E0%B8%AA%E0%B8%A7%E0%B9%88%E0%B8%B2%E0%B8%87%E0%B8%84%E0%B8%A7%E0%B8%B2%E0%B8%A1%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%A1%E0%B9%81%E0%B8%AA%E0%B8%87-%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B9%84%E0%B8%9F%E0%B8%95%E0%B8%B2%E0%B8%A1%E0%B9%81%E0%B8%AA%E0%B8%87) , [BH1750](http://127.0.0.1:8010/session/3f2a8d5865cd1dafc753cc22bba82ce7efb06094/?start=%2F&theme=dark&utm_source=platformio&utm_medium=piohome)
 2. [lightsensor](https://github.com/choompol-boonmee/lab63b/blob/master/examples/04_Input-Port/src/main.cpp)
* วิธีการทำการทดลอง
  1. เปิดโปรแกรม Visual studio code
     * ![Screenshot 2021-03-31 110836](https://user-images.githubusercontent.com/80879651/113090609-649dda80-9214-11eb-93be-24d68d1e5967.png)
  2. กดที่หน้าเอเลี่ยน หรือ รูปบ้าน แล้วเพิ่มโปรเจ็กใหม่
     * ![Screenshot 2021-03-31 113138](https://user-images.githubusercontent.com/80879651/113090876-f7d71000-9214-11eb-881b-c2aab3eb8d40.png)
  3. ตั้งชื่อโปรเจ็ก และเลือกบอร์ดที่ใช้ แล้วกด finish
     * ![Screenshot 2021-03-31 113228](https://user-images.githubusercontent.com/80879651/113092969-3a9ae700-9219-11eb-8a7d-ee512ceacde4.png)
  4. หลังจากนั้นโปรแกรมก็จะสร้างโฟลเดอร์ของไฟล์นี้ ซึ่งเวลาเขียนโค้ดก็จะเขียนใน main.cpp
     * ![Screenshot 2021-03-31 122027](https://user-images.githubusercontent.com/80879651/113094304-9c5c5080-921b-11eb-935d-70b7a10c6da0.png) 
![Screenshot 2021-03-31 121923](https://user-images.githubusercontent.com/80879651/113094433-dcbbce80-921b-11eb-8957-8394c1fb4749.png)
  5. บอร์ดที่เราสร้าง หรือข้อมูลของบอร์ดก็จะอยู่ใน platformio.ini
     * ![Screenshot 2021-03-31 135921](https://user-images.githubusercontent.com/80879651/113103327-58704800-9229-11eb-8771-5956c8de9f05.png)
  6. เริ่มเขียนโค้ด





* การบันทึกผลการทดลอง
* อภิปรายผลการทดลอง
* คำถามหลังการทดลอง
