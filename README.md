### การสร้าง HTML ตามแบบที่กำหนดให้

ตลิก link [Figma](https://www.figma.com/design/cLKdrG7KzQB65UygvLbNSu/Dev-Test?node-id=0-1&t=uEazXJLpPeHycSv3-0) เพื่อดู Design

โดยกำหนดเป้าหมายดังนี้
* Input ราคาอสังหาฯ
  * Format เมื่อพิมพ์ตัวเลขจะต้องเป็นไปตาม Format number ตัวอย่าง 1,000,000
  * กรอกได้แค่ตัวเลขเท่านั้น
  * ไม่สามารถใส่ทศนิยม
  * ไม่สามารถใส่ 0 ได้ในตัวแรก
  * ในกรณี copy text จากที่อื่น มาวาง จะต้องเข้าเงื่อนข้างต้นด้านบนทั้งหมด
  * เมื่อลบข้อมูล input ทั้งหมดจะต้องมี Error message ตาม Design และเมื่อ on input border จะต้องเปลี่ยนสีตาม Design พร้อมกับ Error message จะต้องหายไป
* Input อัตราดอกเบี้ย
  * รองรับการใส่ทศนิยมได้แค่ 2 ตำแหน่ง
