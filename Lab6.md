# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)
* วัตถุประสงค์
  * สร้างไวไฟขึ้นมาเอง เพื่อเชื่อมต่อกับโทรศัพท์มือถือได้
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. กล่องสัญญาณไวไฟ
* ศึกษาข้อมูลเบื้องต้น 
  [สร้างไวไฟ AP](https://www.ioxhop.com/article/71/esp32-%E0%B9%80%E0%B8%9A%E0%B8%B7%E0%B9%89%E0%B8%AD%E0%B8%87%E0%B8%95%E0%B9%89%E0%B8%99-%E0%B8%9A%E0%B8%97%E0%B8%97%E0%B8%B5%E0%B9%88-10-%E0%B8%81%E0%B8%B2%E0%B8%A3%E0%B9%83%E0%B8%8A%E0%B9%89%E0%B8%87%E0%B8%B2%E0%B8%99-wifi)
* วิธีการทำการทดลอง
 1. เข้าไปที่โปรแกรมที่ 6 : พิมพ์ใน cmd pwd enter vi src/main.cpp enter ![Screenshot 2021-03-24 161120](https://user-images.githubusercontent.com/80879651/112284283-a8945b00-8cbb-11eb-85d1-c6866129d9c6.png)
 2. ไมโครคอนโทรเลอร์มีไวไฟในตัวเองเป็น access point จะต้องกำหนดชื่อให้ ในตัวอย่างเราตั้ง username คือ TUENG-ESP-WIFI password คือ choompol ![Screenshot 2021-03-24 161607](https://user-images.githubusercontent.com/80879651/112284843-412adb00-8cbc-11eb-812c-e4b31a6dc86f.png)
 3. อัปโหลดโปรแกรมเข้าไปใน ไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio run -t upload พร้อมกับกดปุ่ม reset ![Screenshot 2021-03-24 161937](https://user-images.githubusercontent.com/80879651/112285305-beeee680-8cbc-11eb-9996-6850d8164faf.png)
 4. อัปโหลดเสร็จแล้ว ![Screenshot 2021-03-24 162123](https://user-images.githubusercontent.com/80879651/112285539-007f9180-8cbd-11eb-967a-8c983a9a838a.png)
 5. มอนิเตอร์ไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio device monitor enter ![Screenshot 2021-03-24 162504](https://user-images.githubusercontent.com/80879651/112286059-826fba80-8cbd-11eb-82ef-3ec392d16beb.png)
 6. เช็คในโทรศัพท์มือถือว่าเจอไวไฟหรือเปล่า จะเห็นได้ว่าเห็นไวไฟ TUENG-ESP-WIFI แปลว่าเราสร้างไวไฟสำเร็จ
![Screenshot 2021-03-24 162748](https://user-images.githubusercontent.com/80879651/112286425-e3978e00-8cbd-11eb-9ba6-304e04a1bc57.png)
* การบันทึกผลการทดลอง
  * เมื่อเช็คในโทรศัพท์มือถือแล้ว จะเห็นได้ว่าเห็นไวไฟ TUENG-ESP-WIFI แปลว่าสร้างไวไฟสำเร็จ ![Screenshot 2021-03-25 014707](https://user-images.githubusercontent.com/80879651/112367055-0c467480-8d0c-11eb-8bd7-d3fabfb22214.png)
* อภิปรายผลการทดลอง
  * เราต้องตั้ง username และ password ของไวไฟ เพราะเราจะนำไปเป็น wifi AP ของไมโครคอนโทรเลอร์ หลังจากนั้นอัปโหลดโปรแกรมเข้าไมโครคอนโทรเลอร์ พร้อมกับกดปุ่ม reset เมื่ออัปโหลดเสร็จแล้วก็เช็คสัญญาณไวไฟในโทรศัพท์มือถือ แล้วเราก็จะเห็น wifi AP ที่เราสร้างไว้
* คำถามหลังการทดลอง
  * ถ้าเราไม่กำหนด username กับ password ของไวไฟจะเป็นอย่างไร
    * Ans ไม่สามารถสร้างไวไฟได้ เพราะ wifi AP ต้องกำหนด username กับ password จึงจะสร้างได้
