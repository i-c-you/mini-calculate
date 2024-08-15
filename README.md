### การสร้าง HTML ตามรูปแบบที่กำหนดให้

คลิก link \[ [Figma](https://www.figma.com/design/cLKdrG7KzQB65UygvLbNSu/Dev-Test?node-id=0-1&t=uEazXJLpPeHycSv3-0) \] เพื่อดู Design
> Library : Boostrap | jQueury | Javascript | etc.

> Default value
>
> ราคาอสังหาฯ = 1,800,000
>
> อัตราดอกเบี้ย = 6.5
>
> จำนวนปี = 30
>
> รายได้ขั้นต่ำต่อเดือน คำนวนจาก ( ราคาอสังหาฯ / 650,000 ) * 10,000
>
> ยอดผ่อนต่อเดือน คำนวนจาก
> 1. หาดอกเบี้ยทั้งหมด วงเงินกู้ * ( ดอกเบี้ย / 100) * จำนวนปี
> 2. ดอกเบี้ยต่อเดือน  หาดอกเบี้ยทั้งหมด / ( จำนวนปี * 12 )
> 3. เงินต้นต่อเดือน  วงเงินกู้ / ( จำนวนปี * 12 )
> 4. จำนวนเงินที่ต้องผ่อนชำระต่อเดือน  ดอกเบี้ยต่อเดือน + เงินต้นต่อเดือน
>    
---
โดยกำหนดเป้าหมายดังนี้
* Input ราคาอสังหาฯ
  * Format เมื่อพิมพ์ตัวเลขจะต้องเป็นไปตาม Format number ตัวอย่าง 1,000,000
  * ใส่จำนวนได้ไม่เกิน 99,999,999,999
  * กรอกได้แค่ตัวเลขเท่านั้น
  * ไม่สามารถใส่ทศนิยม
  * ไม่สามารถใส่ 0 ได้ในตัวแรก
  * ในกรณี copy text จากที่อื่น มาวาง จะต้องเข้าเงื่อนข้างต้นด้านบนทั้งหมด
  * เมื่อลบข้อมูล input ทั้งหมดจะต้องมี Error message ตาม Design และเมื่อ on input border จะต้องเปลี่ยนสีตาม Design พร้อมกับ Error message จะต้องหายไป
* Input อัตราดอกเบี้ย
  * รองรับการใส่ทศนิยมได้แค่ 2 ตำแหน่ง
  * ใส่จำนวนได้ไม่เกิน 99.99
  * กรอกได้แค่ตัวเลขเท่านั้น
  * ไม่สามารถใส่ 0 ได้ในตัวแรก
  * ในกรณี copy text จากที่อื่น มาวาง จะต้องเข้าเงื่อนข้างต้นด้านบนทั้งหมด
  * เมื่อลบข้อมูล input ทั้งหมดจะต้องมี Error message ตาม Design และเมื่อ on input border จะต้องเปลี่ยนสีตาม Design พร้อมกับ Error message จะต้องหายไป
* Input จำนวนปี
  * กรอกได้แค่ตัวเลขเท่านั้น
  * ใส่จำนวนได้ไม่เกิน 99 ปี
  * ขั้นต่ำคือ 3 ปี
  * ไม่สามารถใส่ 0 ได้ในตัวแรก
  * ในกรณี copy text จากที่อื่น มาวาง จะต้องเข้าเงื่อนข้างต้นด้านบนทั้งหมด
  * เมื่อลบข้อมูล input ทั้งหมดจะต้องมี Error message ตาม Design และเมื่อ on input border จะต้องเปลี่ยนสีตาม Design พร้อมกับ Error message จะต้องหายไป

* ล้างข้อมูล
  * Input ต่างๆ กลับสู่ default ทั้งหมด
  * Error message จะต้องหายไป
* ปุ่มคำนวณสินเชื่อ
  * เมื่อทั้ง 3 input ผิดไปจากเงื่อนไข หรือ ไม่มีค่าใดๆ ต้อง disabled ไว้
