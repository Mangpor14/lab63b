# การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)
* วัตถุประสงค์
 1. สร้างไวไฟขึ้นมาเอง เพื่อเชื่อมต่อกับโทรศัพท์มือถือได้
* อุปกรณ์ที่ใช้
 1. ไมโครคอนโทรเลอร์ ESP-01
 2. สาย USB Type C
 3. usb to serial converter
 4. คอมพิวเตอร์ 
 5. กล่องสัญญาณไวไฟ
* ศึกษาข้อมูลเบื้องต้น 
* วิธีการทำการทดลอง
 1. เข้าไปที่โปรแกรมที่ 6 : พิมพ์ใน cmd pwd enter vi src/main.cpp enter ![Screenshot 2021-03-24 161120](https://user-images.githubusercontent.com/80879651/112284283-a8945b00-8cbb-11eb-85d1-c6866129d9c6.png)
 2. ไมโครคอนโทรเลอร์มีไวไฟในตัวเองเป็น access point จะต้องกำหนดชื่อให้ ในตัวอย่างเราตั้ง username คือ TUENG-ESP-WIFI password คือ choompol ![Screenshot 2021-03-24 161607](https://user-images.githubusercontent.com/80879651/112284843-412adb00-8cbc-11eb-812c-e4b31a6dc86f.png)
 3. อัปโหลดโปรแกรมเข้าไปใน ไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio run -t upload พร้อมกับกดปุ่ม reset ![Screenshot 2021-03-24 161937](https://user-images.githubusercontent.com/80879651/112285305-beeee680-8cbc-11eb-9996-6850d8164faf.png)
 4. อัปโหลดเสร็จแล้ว ![Screenshot 2021-03-24 162123](https://user-images.githubusercontent.com/80879651/112285539-007f9180-8cbd-11eb-967a-8c983a9a838a.png)
 5. มอนิเตอร์ไมโครคอนโทรเลอร์ : พิมพ์ใน cmd pio device monitor enter ![Screenshot 2021-03-24 162504](https://user-images.githubusercontent.com/80879651/112286059-826fba80-8cbd-11eb-82ef-3ec392d16beb.png)
 6. เช็คในโทรศัพท์มือถือว่าเจอไวไฟหรือเปล่า จะเห็นได้ว่าเห็นไวไฟ TUENG-ESP-WIFI 
![Screenshot 2021-03-24 162748](https://user-images.githubusercontent.com/80879651/112286425-e3978e00-8cbd-11eb-9ba6-304e04a1bc57.png)


* การบันทึกผลการทดลอง
* อภิปรายผลการทดลอง
* คำถามหลังการทดลอง
