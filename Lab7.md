# การทดลองที่ 7 เรื่อง การเพิ่ม variety เข้าไปในแลป 4
  ## วัตถุประสงค์
   1. เพื่อวัดความเข้มของแสงที่อยู่ในห้อง หรือสิ่งแวดล้อมรอบตัวเรา
   2. เพื่อทดสอบเซ็นเซอร์แสง
  ## อุปกรณ์ที่ใช้
   1. ไมโครคอนโทรเลอร์ ESP-01
   2. สาย USB Type C
   3. usb to serial converter
   4. คอมพิวเตอร์ 
   5. Adapter ต่อสาย port0 port2
   6. LED 
   7. LDR Photoresistor
   8. ตัวต้านทาน
  ## ศึกษาข้อมูลเบื้องต้น 
   1. [วัดความเข้มแสง](https://www.myarduino.net/article/211/%E0%B8%AA%E0%B8%AD%E0%B8%99%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99-nodemcu-esp8266-%E0%B9%80%E0%B8%8B%E0%B9%87%E0%B8%99%E0%B9%80%E0%B8%8B%E0%B8%AD%E0%B8%A3%E0%B9%8C%E0%B8%A7%E0%B8%B1%E0%B8%94%E0%B8%84%E0%B8%A7%E0%B8%B2%E0%B8%A1%E0%B8%AA%E0%B8%A7%E0%B9%88%E0%B8%B2%E0%B8%87%E0%B8%84%E0%B8%A7%E0%B8%B2%E0%B8%A1%E0%B9%80%E0%B8%82%E0%B9%89%E0%B8%A1%E0%B9%81%E0%B8%AA%E0%B8%87-%E0%B9%80%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B8%9B%E0%B8%B4%E0%B8%94%E0%B9%84%E0%B8%9F%E0%B8%95%E0%B8%B2%E0%B8%A1%E0%B9%81%E0%B8%AA%E0%B8%87) , [BH1750](https://github.com/claws/BH1750)
   2. [lightsensor](https://github.com/choompol-boonmee/lab63b/blob/master/examples/04_Input-Port/src/main.cpp)
  ## วิธีการทำการทดลอง
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
  6. เริ่มแรก เราจะดึงค่าตัวแปรต้นแบบที่เราจะนำมาใช้เขียนโค้ดก่อน กดรูปบ้าน แล้วกดที่ Libraries 
     * ![Screenshot 2021-03-31 181345](https://user-images.githubusercontent.com/80879651/113135931-f1fd2100-924c-11eb-8bae-7c79963237b0.png)
  7. พิมพ์สิ่งเราต้องการค้นหา แต่ในตัวอย่างเราพิมพ์ BH1750FVI(คือ การหาความเข้มแสง)
     * ![Screenshot 2021-03-31 182130](https://user-images.githubusercontent.com/80879651/113136777-f413af80-924d-11eb-895f-1d849cecfbd7.png)
  8. เลือกโค้ดที่เราสนใจ ซึ่งเลือกอันบนสุด แล้วกด Add to project
     * ![Screenshot 2021-03-31 182740](https://user-images.githubusercontent.com/80879651/113137515-d430bb80-924e-11eb-8f3a-b5dd46693d68.png)
  9. ใน platformio.ini ก็จะมีสิ่งที่เราเพิ่มเข้ามา
     * ![Screenshot 2021-03-31 183031](https://user-images.githubusercontent.com/80879651/113137931-5f11b600-924f-11eb-97f8-b9e4b18dd4e3.png)
 10. หลังจากนั้นก็มาเขียนโค้ด ซึ่งเขียนใน main.cpp
     * ![Screenshot 2021-03-31 183404](https://user-images.githubusercontent.com/80879651/113138266-c4fe3d80-924f-11eb-9f8e-f5cdd158373d.png)
![Screenshot 2021-03-31 183645](https://user-images.githubusercontent.com/80879651/113138513-127aaa80-9250-11eb-9cf4-6d037eb2dfd3.png)
 11. แล้วรันโค้ดออกมาสำเร็จ จึงสามารถใช้ได้
     * ![Screenshot 2021-03-31 183858](https://user-images.githubusercontent.com/80879651/113138840-8452f400-9250-11eb-9c14-22876acc72d9.png)
![Screenshot 2021-03-31 183923](https://user-images.githubusercontent.com/80879651/113138848-874de480-9250-11eb-917e-ab75ec150945.png)
  ## การบันทึกผลการทดลอง
   * ในที่นี้เราไม่มีอุปกรณ์ที่จะรันโค้ดเข้าไปในบอร์ดจริงได้ จึงขอยืมรูปจากเว็ปไซต์ที่อ้างอิง และรูปจากแลปอิเล็กทรอนิกส์มาใช้เป็นตัวอย่างผลการทดลอง
     * ![Screenshot 2021-03-31 184551](https://user-images.githubusercontent.com/80879651/113154231-00a20300-9262-11eb-829f-8bd2be06da0d.png) 
     * ![Screenshot 2021-03-31 205858](https://user-images.githubusercontent.com/80879651/113156726-74450f80-9264-11eb-89bf-134a6e917166.png)
     * ![Screenshot 2021-03-31 205923](https://user-images.githubusercontent.com/80879651/113156743-78712d00-9264-11eb-9078-218357df8347.png)


  ## อภิปรายผลการทดลอง
  ## คำถามหลังการทดลอง
