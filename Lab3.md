# การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล
* วัตถุประสงค์
  * เขียนโปรแกรมในไมโครคอนโทรเลอร์ ESP-01 เพื่อให้ Adapter ต่อสาย port0 port1 ส่องสว่าง
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. Adapter ต่อสาย port0 port1
* ศึกษาข้อมูลเบื้องต้น 
  [การควบคุมเอาท์พุตสัญญาณดิจิตัล](https://www.ioxhop.com/article/67/esp32-%E0%B9%80%E0%B8%9A%E0%B8%B7%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%95%E0%B9%89%E0%B8%99-%E0%B8%9A%E0%B8%97%E0%B8%97%E0%B8%B5%E0%B9%88-6-%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B8%84%E0%B8%A7%E0%B8%9A%E0%B8%84%E0%B8%B8%E0%B8%A1%E0%B8%AD%E0%B8%B4%E0%B8%99%E0%B8%9E%E0%B8%B8%E0%B8%95%E0%B9%80%E0%B8%AD%E0%B8%B2%E0%B8%95%E0%B9%8C%E0%B8%9E%E0%B8%B8%E0%B8%95%E0%B8%9E%E0%B8%B7%E0%B9%89%E0%B8%99%E0%B8%90%E0%B8%B2%E0%B8%99)
* วิธีการทำการทดลอง
 1. เสียบ Adapter ต่อสาย port0 port1 กับ usb to serial converter แล้วเสียบไมโครคอนโทรเลอร์ ESP-01 กับ Adapter ต่อสาย port0 port1 ![Screenshot 2021-03-25 003455](https://user-images.githubusercontent.com/80879651/112357304-f764e380-8d01-11eb-9263-a965919880b4.png)
 2. ดูตัวอย่างในเนื้อหาที่ 3 พิมพ์ใน cmd 1s enter pwd enter vi src/main.cpp enter ![Screenshot 2021-03-24 004936](https://user-images.githubusercontent.com/80879651/112193883-e7ce9780-8c3a-11eb-8a12-97640d11565c.png)
 3. โปรแกรมจะ set ให้ port เป็นเลข 0 เป็นโหมด output แล้วก็วนลูปตลอดไป ทุกๆครึ่งวินาที 500ms ถ้า count เป็นเลขคี่ให้ on ถ้า count เป็นเลขคู่ให้ off ![Screenshot 2021-03-24 005518](https://user-images.githubusercontent.com/80879651/112194647-ae4a5c00-8c3b-11eb-8836-903b60b6b335.png)
 4. อัปโหลดโปรแกรมเข้าไปใน ไมโครคอนโทรเลอร์ ESP-01 พิมพ์ใน cmd pio run -t upload 
 5. กดปุ่ม boost แล้วกดปุ่ม reset ที่ usb to serial converter หลังจากนั้นจะมีไฟติด ![Screenshot 2021-03-24 010124](https://user-images.githubusercontent.com/80879651/112195465-93c4b280-8c3c-11eb-8d47-2747f79769c7.png)
 6. ผลลัพธ์ของการรันโปรแกรม พิมพ์ใน cmd pio device monitor enter มันจะ on off ทุกครึ่งวินาที ซึ่งก็คือไฟ LED สีเขียว ที่ port0 จะสว่างแล้วก็ดับทุกครึ่งวินาที ส่วนไฟ LED สีน้ำเงิน ที่ port1 ไม่เกี่ยวเพราะไม่ได้ต่อกับไมโครคอนโทรเลอร์ ESP-01 ![Screenshot (9)](https://user-images.githubusercontent.com/80879651/112202485-05ecc580-8c44-11eb-9f23-12d8d9290104.png)
![Screenshot 2021-03-24 011721](https://user-images.githubusercontent.com/80879651/112197478-b788f800-8c3e-11eb-9677-d94f1fcbe7d4.png)
* การบันทึกผลการทดลอง
  * ไมโครคอนโทรเลอร์จะ on off ทุกครึ่งวินาที ซึ่งก็คือไฟ LED สีเขียว ที่ port0 จะสว่างแล้วก็ดับทุกครึ่งวินาที ส่วนไฟ LED สีน้ำเงิน ที่ port1 ไม่เกี่ยวข้องกันเพราะไม่ได้ต่อกับไมโครคอนโทรเลอร์ 
  * ![Screenshot 2021-03-25 002218](https://user-images.githubusercontent.com/80879651/112355635-6e997800-8d00-11eb-9870-497c63c2e625.png)
![Screenshot 2021-03-25 002246](https://user-images.githubusercontent.com/80879651/112355652-71946880-8d00-11eb-92df-76da527a4707.png)
* อภิปรายผลการทดลอง
  * ในตอนแรกเสียบ Adapter ต่อสาย port0 port1 กับ usb to serial converter แล้วเสียบไมโครคอนโทรเลอร์ ESP-01 กับ Adapter ต่อสาย port0 port1 หลังจากนั้นกดค้นหาโปรแกรมที่ 3 มันก็จะขึ้นค่า set ให้ port เป็นเลข 0 เป็นโหมด output แล้วก็วนลูปตลอดไป ทุกๆครึ่งวินาที 500ms ถ้า count เป็นเลขคี่ให้ on ถ้า count เป็นเลขคู่ให้ off หลังจากนั้นอัปโหลดโปรแกรมเข้าไปในไมโครคอนโทรเลอร์ พร้อมกับกดปุ่ม boost แล้วกดปุ่ม reset ที่ usb to serial converter หลังจากนั้นจะมีไฟติด หลังจากนั้นไมโครคอนโทรเลอร์จะ on off ทุกครึ่งวินาที ซึ่งก็คือไฟ LED สีเขียว ที่ port0 จะสว่างแล้วก็ดับทุกครึ่งวินาที ส่วนไฟ LED สีน้ำเงิน ที่ port1 ไม่เกี่ยวข้องกันเพราะไม่ได้ต่อกับไมโครคอนโทรเลอร์ 
* คำถามหลังการทดลอง 
  * ถ้าไมโครคอนโทรเลอร์อยู่ในโหมด off แปลว่ามัน count ได้เลขอะไร
    * Ans เลขคู่
