### สวัสดีจ้า 👋

<!--
**Chutani09/Chutani09** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
OAuth

ในการใช้การเรียก pCloud api ก่อนอื่นคุณต้องรับโทเค็นจากผู้ใช้โดยใช้โปรโตคอล OAuth

ตั้งค่า pCloud ของคุณ [แอปพลิเคชัน OAuth] (https://docs.pcloud.com/oauth/index.html) และจดบันทึกรหัสแอปในหน้าหลักของแอปพลิเคชันเมื่อคุณสร้าง

(ฝั่งไคลเอ็นต์เท่านั้น) ตั้งค่า URL เปลี่ยนเส้นทางที่คุณสามารถเข้าถึงได้และสามารถวางหน้า html แบบคงที่ได้

โฟลว์ฝั่งไคลเอ็นต์

ใช้ข้อมูลโค้ดต่อไปนี้ในการดำเนินการที่ผู้ใช้เริ่มต้น (คลิก):

 

pCloudSdk.oauth.initOauthToken ({

  client_id: "YOUR_CLIENT_ID",

  redirect_uri: "YOUR_REDIRECT_URL",

  response_type: "โทเค็น" | "รหัส",

  รับโทเค็น: ฟังก์ชัน (access_token, locationid) {

    // ทำอะไรบางอย่างกับโทเค็น

  }

});

 

ซึ่งจะเปิดหน้าต่างป๊อปอัปที่ผู้ใช้สามารถอนุญาตการใช้แอปของคุณได้ หลังจากนี้ เขาจะถูกเปลี่ยนเส้นทางไปยังหน้า  redirect_uri  ซึ่งต้องเป็น html ธรรมดาที่โหลด SDK และรันสิ่งต่อไปนี้:

 

pCloudSdk.oauth.popup();

 

ประทัดข้อมูลด้านบนสุดจะและคุณจะ "access_token" สุด oauth ตัวอย่างสำหรับข้อมูลเพิ่มเติม

โฟลว์ซีพียู

แหล่งข้อมูลที่ท่องเีขียนเพื่อท่องเ...

อาจใช้งานได้ SDK เยียมเยาะเย้ยเยี่ยงเย้ย "เยาะเย้ย" ของเยาะเย้ยเยาะเย้ยเยาะเย้ยเยาะเย้ยเยาะเย้ยเย้... :

`` เจสัน

{

"client_id": "",

"app_secret": ""

}

 

ง่ายมาก `node Example/node/token.js` และเป้าหมาย เป้าหมายจะบันทึก `access_token` และปรับปรุง `userid` ของผู้ใช้ใน `app.json` (อาจกล่าวล่วงหน้า)

* (**ฝั่งเรือพร้อมโพลเท่านั้น**)

  ใช้ข้อมูลโค้ดต่อไปนี้ในการดำเนินการที่ผู้ใช้เริ่มต้น (คลิก):

```js

pCloudSdk.oauth.initOauthPollToken ({

  client_id: "YOUR_CLIENT_ID",

  รับโทเค็น: ฟังก์ชัน (access_token) {

    // ทำอะไรบางอย่างกับโทเค็น

  },

  onError: ฟังก์ชั่น (ผิดพลาด) {}

});

 
