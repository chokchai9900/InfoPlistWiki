
# ไฟล์ PLIST คืออะไร

ไฟล์ PLIST เป็นไฟล์การตั้งค่าหรือที่เรียกว่า "ไฟล์คุณสมบัติ" ที่ใช้โดยแอปพลิเคชัน macOS มันมีคุณสมบัติและการตั้งค่าการกำหนดค่าสำหรับโปรแกรมต่างๆ  ไฟล์ PLIST ได้รับการจัดรูปแบบเป็น XML และอ้างอิงจาก Core Core DTD ของ Apple

## ข้อมูลเพิ่มเติม

ไฟล์ PLIST ที่เปิดใน Apple Xcode 9
ไฟล์ PLIST สามารถบันทึกเป็นข้อความหรือรูปแบบไบนารี เอกสารที่เป็นข้อความและสามารถแก้ไขได้ด้วยโปรแกรมแก้ไขข้อความ อย่างไรก็ตามโดยทั่วไปผู้ใช้ไม่ควรแก้ไขเนื่องจากถูกดัดแปลงโดยโปรแกรมที่เกี่ยวข้อง
ไฟล์รายการคุณสมบัติที่มาพร้อมกับแอปพลิเคชันสามารถสร้างและแก้ไขโดยนักพัฒนาโดยใช้เครื่องมือแก้ไขรายการทรัพย์สินของ Apple ซึ่งมาพร้อมกับเครื่องมือสำหรับนักพัฒนาของ Apple พวกเขายังสามารถเปิดและแก้ไขได้โดยใช้โปรแกรมแก้ไข PLIST บุคคลที่สาม
หมายเหตุ: คุณสามารถแปลงไฟล์ PLIST ระหว่าง XML ได้ผ่าน tool ใน visual studio หรือเปิดเพื่ออ่านในรูปแบบ XML ได้เลยในโปรแกรม Visual studio code

# วิธีการหาไฟล์ info.plist ใน application ใน ios

1. ดาวน์โหลดโปรแกรมที่ชื่อ  iMazing  และเชื่อมต่ออุปกรณ์ ios ของคุณด้วยสาย ที่แถมมากับตัวเครื่อง เพื่อทำการเชื่อมต่อข้อมูล application ที่คุณมีในเครื่อง

![process 1](https://github.com/chokchai9900/InfoPlistWiki/blob/main/1.PNG)
![process 1](https://github.com/chokchai9900/InfoPlistWiki/blob/main/21.PNG)

2. เมื่อเชื่อมต่อเสร็จแล้ว หน้าจอจะแสดงเมนูต่างๆ ให้ไปที่เมานู Manage app และรอสักครู่เพื่อให้โปรแกรมเรียกข้อมูลของเครื่อง

![process 2](https://github.com/chokchai9900/InfoPlistWiki/blob/main/2.PNG)

3. เมื่อเสร็จแล้ว ให้เลือกที่แถบ library และเลือกแอปที่ต้องการจะดูข้อมุล จากนั้่นคลิกรูปไอคอนก้อนเมฆ เพื่อทำการดาวโหลด application และรอจนกว่าจะเสร็จสิ้น

![process 3](https://github.com/chokchai9900/InfoPlistWiki/blob/main/3.PNG)

4. จากนั้น ให้คลิกขวาที่แอปที่ต้เองการ และเลือก Export .IPA จากนั้นโปรแกรมจะให้เราเลือกสถานที่ที่จะเก็บ application ที่ดาวโหลด

![process 4](https://github.com/chokchai9900/InfoPlistWiki/blob/main/4.PNG)

5. จากนั้น ไปที่ folder ที่จัดเก็บ application ที่เลือกข้างต้น และทำการเปลี่ยนนามสกลุของไฟล์จาก .IPA > .zip

![process 5](https://github.com/chokchai9900/InfoPlistWiki/blob/main/5.png)

6. แล้วคลิกขวา และทำการแตกไฟล์ที่ได้

![process 6](https://github.com/chokchai9900/InfoPlistWiki/blob/main/6.png)

7. จากนั้นจะได้ folder ที่มีข้อมูลสำหรับ application ที่เลือกข้างต้น ให้ไปที่ ชื่อapplication > Payload > ชื่อapplication ใน folder นั้นจะมีไฟล์ info.plist อยู่

![process 7](https://github.com/chokchai9900/InfoPlistWiki/blob/main/7.png)

8. คลิกขวาที่ไฟล์ และเลือก open with visual studio code เพื่อทำการเปิดไฟล์นั้นๆ

![process 8](https://github.com/chokchai9900/InfoPlistWiki/blob/main/8.PNG)

9. ในไฟล์ info.plist จะมีข้อมุลเกี่ยวกับ application นั้นๆอยู่ เช่น URI Schema , packetname การอนุญาติการเข้าถึงต่างๆ รวมทั้งแอปที่สามารถถูกเรียกจากแอปที่เลือกได้

![process 9](https://github.com/chokchai9900/InfoPlistWiki/blob/main/9.PNG)
