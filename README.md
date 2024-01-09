# ChomCHOB QA Engineer Testing

## Section 1 - Manual Testing Skill and Testing Knowledge
1. หากต้องการ Design Test-case มี **Technique** อะไรบ้างที่สามารถช่วยให้การ Design Test-case เพื่อทดสอบระบบได้ครอบคลุม
2. Design Test-case จากโจทย์ต่อไปนี้อย่างน้อย 5 Case พร้อมระบุ **Technique** ที่ใช้ข้อนั้น ๆ
   - [โจทย์] : ผู้ใช้ต้องการโอน Point จากบัญชีตัวเอง ไปยังบัญชีปลายทาง โดยเงื่อนไขคือ
     - ขั้นต่ำในการโอน Point คือ 100 / การทำรายการ
     - สูงสุดในการโอน Point คือ 3,000 / การทำรายการ
     - หากโอน < ขั้นต่ำ ระบบคิดค่า Fee 8 Point โดยบวกเพิ่มจากค่าที่กรอก
     - ต้องกรอก Passcode 4 หลัก ให้ถูกต้องจึงทำรายการสำเร็จ
     - บัญชีปลายทางต้องถูกต้อง จึงจะสามารถกรอก Passcode ได้
                
3. หากทีมต้องการทดสอบ Feature ในข้อ 2 จะต้องมี Test Plan อย่างไร?
4. Software Testing มีความสำคัญอย่างไรในการพัฒนาระบบ
    
## Section 2: Automate Testing WEB Skills
จงใช้ Robot framework หรือ Selenium เพื่อพัฒนา Automate Test system ตาม test case ดังนี้
   - เปิด Browser และไปที่ Link [https://www.nejavu.com](https://www.nejavu.com/)
   - ถ้ามี Banner pop-up ขึ้นมาให้กดปิด Modal (แต่ถ้าไม่ทำข้อต่อไปได้เลย)
   - Click menu “การ์ตูน”
   - Get ชื่อหนังสือทุกเล่มในแถวที่หนึ่ง
   - กดปุ่ม “ใส่ตระกร้า” หนังสือทุกเล่มแถวที่หนึ่ง
   - กดปุ่ม “รถเข็น / ตระกร้า”
   - Verify ชื่อหนังสือทุกเล่ม ที่อยู่ในตระกร้า โดยใช้ชื่อที่ได้มาจากข้อที่แล้ว
   - ลบหนังสือทุกเล่มที่อยู่ในตระกร้า
   - Verify badge บนรถเข็นว่าเหลือหนังสือเท่ากับ 0

## Section 3: Automate Testing API Skills
จงใช้ Postman, Robot framework หรือ Selenium เพื่อพัฒนาระบบทดสอบ API โดยให้ส่ง Request และตรวจสอบ Response แบบ Automate Testing
    
1. GET - All Users : https://reqres.in/api/users [Status code : 200]
2. GET - User Info : https://reqres.in/api/users/1 [Status code : 200]
3. POST - Create User : https://reqres.in/api/users [Status code : 201]
                
    ```json
    //request body example
    {
        "name": "Yourname",
        "job": "Your Position"
    }
    ```             
4. PATCH - Update User : [https://reqres.in/api/users/](https://reqres.in/api/users/1)id [Status code : 200]
                
    ```json
    //Required id From Create User
    //request body example
    {
        "name": "Your nickname",
        "job": "Your Position"
    }
    ```
                
5. DELETE - Delete User : [https://reqres.in/api/users/](https://reqres.in/api/users/1)id [Status code : 204]
                
    ```json
    //Required id From Create User
    //request body example
    {
        "name": "Your nickname",
        "job": "Your Position"
    }
    ```
