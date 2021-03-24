# การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล
* วัตถุประสงค์
 1. เพื่อนำสัญญาณอินพุทจากภายนอกเข้ามาในไมโครคอนโทรเลอร์
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. Adapter ต่อสาย port0 port2
 6. LED 
* ศึกษาข้อมูลเบื้องต้น 
* วิธีการทำการทดลอง
 1. source code : พิมพ์ใน cmd vi src/main.cpp enter setup ![Screenshot 2021-03-24 112201](https://user-images.githubusercontent.com/80879651/112254474-40318380-8c93-11eb-84d7-9d262b2a39a9.png) ให้ port0(สายสีขาว) เป็น input port2(สายสีเหลือง) เป็น output digital read ดึงเนื้อหาจาก port0 ซึ่งจะมี 2 ค่า คือ 0 1 ถ้าอ่านค่าออกมาเป็น 1 ไฟที่ port2 จะดับ แต่ถ้าอ่านค่าออกมาเป็น 0 ไฟที่ port2 จะติด ดังนั้นตัว port0 จึงเป็นตัวควบคุม port2
 2. อัปโหลดลงในไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio run -t upload และกดปุ่ม boost ที่ usb to serial converter ![Screenshot 2021-03-24 112813](https://user-images.githubusercontent.com/80879651/112254993-0c0a9280-8c94-11eb-9d5c-5ac4b9918c31.png)
 3. อัปโหลดเสร็จสิ้น ถ้า input เป็น 0 จะมีไฟติดที port2 แต่ถ้า input เป็น 1 ไฟจะดับที่ port2 ![Screenshot 2021-03-24 113013](https://user-images.githubusercontent.com/80879651/112255195-51c75b00-8c94-11eb-8770-9de60afbe67b.png)
 4. ผลลัพธ์ของการรันโปรแกรม พิมพ์ใน cmd pio device monitor enter ซึ่งค่าที่อ่านได้ อ่านเป็น 1 คือไฟดับ ![Screenshot 2021-03-24 114209](https://user-images.githubusercontent.com/80879651/112256060-0746de00-8c96-11eb-8591-c182fa2e2b8c.png)
 5. นำสายสีขาวไปจิ้มสายสีดำจะมีไฟติดขึ้นมา เพราะ port0 อ่านค่าได้ 0 ![Screenshot (10)](https://user-images.githubusercontent.com/80879651/112255978-dcf52080-8c95-11eb-9cb9-8eb7bd4df8ac.png)
 6. แต่ถ้าเราจะไม่เอาสายสีขาวไปจิ้มสายสีดำก็ได้ เราไปกดปุ่ม boost ที่ usb to serial converter ก็จะมีไฟติดเหมือนกัน เพราะ usb to serial converter ต่ออยู่กับ port0 ![Screenshot 2021-03-24 114641](https://user-images.githubusercontent.com/80879651/112256599-a1a72180-8c96-11eb-8c28-50f122fa2f96.png)
 7. ทดสอบกับเซ็นเซอร์ นำตัวต้านทานที่ต่อกับเซ็นเซอร์ ไปต่อกับสายสีแดงที่เป็นไฟเลี้ยงมาจาก Adapter ต่อสาย port0 port2 แล้วขาอีกด้านหนึ่งต่อกับสายสีดำ หรือกราวด์ แล้วสายตรงกลางที่พันระหว่างตัวต้านทานกับเซ็นเซอร์ต่อกับสายสีขาวของ port0 ![Screenshot 2021-03-24 115817](https://user-images.githubusercontent.com/80879651/112258215-acfb4c80-8c98-11eb-88b2-0db805321106.png)
![Screenshot 2021-03-24 115929](https://user-images.githubusercontent.com/80879651/112258248-bf758600-8c98-11eb-81ee-6d2456946ef0.png)
 8. ซึ่งสายสีขาวคือ input ก็เหมือนการนำให้ไฟติดโดยอัตโนมัต port0 จะอ่านค่าได้ 0 ![Screenshot 2021-03-24 120313](https://user-images.githubusercontent.com/80879651/112258437-1aa77880-8c99-11eb-93f3-26b7041c4f48.png)
 9. แต่เมื่อนำนิ้วไปบังแสงตรงเซนเซอร์ port0 จะอ่านค่าได้ 1 ก็คือไฟดับ ![Screenshot (11)](https://user-images.githubusercontent.com/80879651/112258611-593d3300-8c99-11eb-817e-134a735e659a.png)

* การบันทึกผลการทดลอง
* อภิปรายผลการทดลอง
* คำถามหลังการทดลอง
