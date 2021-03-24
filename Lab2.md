# การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ
* วัตถุประสงค์
 1. เพื่อให้ไมโครคอนโทรเลอร์ ESP-01 ค้นหาไวไฟได้
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. กล่องสัญญาณไวไฟเพื่อทดสอบว่า ไมโครคอนโทรเลอร์ ESP-01 ค้นหาได้ไหม
* ศึกษาข้อมูลเบื้องต้น 
 [ค้นหาไวไฟ](https://www.ioxhop.com/article/71/esp32-%E0%B9%80%E0%B8%9A%E0%B8%B7%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%95%E0%B9%89%E0%B8%99-%E0%B8%9A%E0%B8%97%E0%B8%97%E0%B8%B5%E0%B9%88-10-%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99-wifi)
* วิธีการทำการทดลอง
 1. พิมพ์ใน cmd 1s enter vi src/main.cpp enter ส่วน setup คือ ส่วน set wifi ให้พร้อมทำงาน และ loop คือ สแกนหาไวไฟว่ามี  access point ไหนบ้าง
![Screenshot 2021-03-23 233133](https://user-images.githubusercontent.com/80879651/112182926-4fcbb080-8c30-11eb-9379-3caeb2fefd72.png)
 2. อัพโหลดโปรแกรมข้าสู่ไมโครคอนโทรเลร์ pio run -t upload enter 
![Screenshot 2021-03-23 233858](https://user-images.githubusercontent.com/80879651/112183661-0af44980-8c31-11eb-9548-5d241f30cfdc.png)
 3. กดปุ่ม boost แล้วกดปุ่ม reset เพื่อให้รันข้อมูลเข้าไปในไมโครคอนโทรเลอร์ได้ ![Screenshot (6)](https://user-images.githubusercontent.com/80879651/112184728-1005c880-8c32-11eb-80c5-92b8a133edef.png)
 4. เมื่อโปรแกรมค้นหาไวไฟเขียนเสร็จแล้ว ![Screenshot 2021-03-23 234845](https://user-images.githubusercontent.com/80879651/112184967-56f3be00-8c32-11eb-8e5f-11c9bef4c709.png)
 5. ลองรันค้นหาไวไฟ pio device monitor enter ![Screenshot (7)](https://user-images.githubusercontent.com/80879651/112185720-147eb100-8c33-11eb-83ed-02facd08a7b6.png)
 6. เจอไวไฟ ซึ่งขึ้นอยู่กับความแรงของไวไฟ
![Screenshot 2021-03-23 235606](https://user-images.githubusercontent.com/80879651/112186064-5c053d00-8c33-11eb-94ae-52131c5e25d9.png)
 7. กดปุ่ม reset เพื่อให้ไมโครคอนโทรเลอร์ทำงานหนักกว่าเดิม หรือค้นหาไวไฟได้มากขึ้น ![Screenshot 2021-03-23 235936](https://user-images.githubusercontent.com/80879651/112186788-1137f500-8c34-11eb-95a8-85a5cb1ba60c.png) ![Screenshot (8)](https://user-images.githubusercontent.com/80879651/112186767-0aa97d80-8c34-11eb-9489-0401539ffe55.png)
* การบันทึกผลการทดลอง
  * ไมโครคอนโทรเลอร์ ESP-01 สามารถค้นหาไวไฟได้ ซึ่งในผลการทดลองไมโครคอนโทรเลอร์เห็นไวไฟ 4 ตัว ![Screenshot 2021-03-24 175740](https://user-images.githubusercontent.com/80879651/112299601-86eea000-8cca-11eb-9842-d865683c05cf.png)
* อภิปรายผลการทดลอง
  * 
* คำถามหลังการทดลอง

