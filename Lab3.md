# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล
* วัตถุประสงค์
 1. เขียนโปรแกรมในไมโครคอนโทรเลอร์ ESP-01 เพื่อให้ Adapter ต่อสาย port0 port1 ส่องสว่าง
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. Adapter ต่อสาย port0 port1
* ศึกษาข้อมูลเบื้องต้น 
* วิธีการทำการทดลอง
 1. ดูตัวอย่างในเนื้อหาที่ 3 พิมพ์ใน cmd 1s enter pwd enter vi src/main.cpp enter ![Screenshot 2021-03-24 004936](https://user-images.githubusercontent.com/80879651/112193883-e7ce9780-8c3a-11eb-8a12-97640d11565c.png)
 2. โปรแกรมจะ set ให้ port เป็นเลข 0 เป็นโหมด output แล้วก็วนลูปตลอดไป ทุกๆครึ่งวินาที 500ms ถ้า count เป็นเลขคี่ให้ on ถ้า count เป็นเลขคู่ให้ off ![Screenshot 2021-03-24 005518](https://user-images.githubusercontent.com/80879651/112194647-ae4a5c00-8c3b-11eb-8836-903b60b6b335.png)
 3. อัปโหลดโปรแกรมเข้าไปใน ไมโครคอนโทรเลอร์ ESP-01 พิมพ์ใน cmd pio run -t upload 
 4. กดปุ่ม boost แล้วกดปุ่ม reset ที่ usb to serial converter หลังจากนั้นจะมีไฟติด ![Screenshot 2021-03-24 010124](https://user-images.githubusercontent.com/80879651/112195465-93c4b280-8c3c-11eb-8d47-2747f79769c7.png)
 5. ผลลัพธ์ของการรันโปรแกรม พิมพ์ใน cmd pio device monitor enter มันจะ on off ทุกครึ่งวินาที ซึ่งก็คือไฟ LED สีเขียว ที่ port0 จะสว่างแล้วก็ดับต่ไฟ LED สีน้ำเงิน ที่ port1 ไม่เกี่ยวเพราะไม่ได้ต่อกับไมโครคอนโทรเลอร์ ESP-01 ![Screenshot (9)](https://user-images.githubusercontent.com/80879651/112202485-05ecc580-8c44-11eb-9f23-12d8d9290104.png)
![Screenshot 2021-03-24 011721](https://user-images.githubusercontent.com/80879651/112197478-b788f800-8c3e-11eb-9677-d94f1fcbe7d4.png)
* การบันทึกผลการทดลอง
* อภิปรายผลการทดลอง
* คำถามหลังการทดลอง
