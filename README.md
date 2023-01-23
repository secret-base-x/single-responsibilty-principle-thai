# Single Responsibility Principle

แนวคิดในการเขียนโปรแกรม
ที่ทำให้ทักษะการวางโครงสร้างโค้ดของผมดีขึ้นมาก
คือ Single Responsibility Principle
Single Responsibility Principle หมายถึงว่า
Function นั้น ๆ หรือ Class นั้น ๆ รับผิดชอบเพียง 1 อย่าง
ถ้าต้องมีการเปลี่ยนแปลง ก็มีเพียงเหตุผลเดียวที่เปลี่ยน
Single Responsibility (ความรับผิดชอบเพียงอย่างเดียว)
นั้นอาจหมายถึง
- การดึงข้อมูลจากฐานข้อมูล (Data Access) ถ้าจะเปลี่ยน ก็เพราะรายละเอียดในการดึงข้อมูลมีการเปลี่ยน
- แสดงผล (Presentation) ถ้าจะเปลี่ยนก็เพราะรูปแบบการแสดงผลมีการเปลี่ยนแปลง
- เงื่อนไขทางธุรกิจ (Business Logic) ถ้าจะมีการเปลี่ยนแปลง ก็เพราะเงื่อนไขทางธุรกิจที่เกี่ยวข้องมีการเปลี่ยน
แต่ละส่วนจะแยกความรับผิดชอบกัน และจะมีโค้ดที่จับความรับผิดชอบเหล่านี้ให้มาทำงานร่วมกัน
ถ้าในสถาปัตยกรรมของ MVC 
(Model - View - Controller)
อาจจะเป็นแบบนี้
Controller เรียก Abstraction ของโค้ดที่รับผิดชอบส่วนของการต่อฐานข้อมูล
ได้ข้อมูลมาเอาข้อมูลที่ได้ไปส่งต่อไปให้ Abstraction ของ Business Logic ที่อาจจะเป็น Class หรือ Function ได้ข้อมูลบางอย่างที่มีความหมายออกมา
เอาข้อมูลที่มีความหมายนั้นส่งต่อไปให้ View เพื่อ แสดงผล
นี่เป็นแค่ตัวอย่างนึง
ของ Single Responsibility Principle
ในการทำงานจริง 
Implementation ของ การแยกโค้ดตามหลัก SRP
อาจจะขึ้นอยู่กับภาษาโปรแกรมมิ่งและ Framework ที่ใช้
ควรปรึกษาพูดคุยกับทีมโปรแกรมเมอร์
ที่ทำงานอยู่ด้วยเสมอ
