# mobasher
### إعداد صفحة البث المباشر لشبكات المايكروتك

هذا المشروع يتيح لك إضافة صفحة بث مباشر لجميع قنوات بين سبورت والقنوات الرياضية والتلفزيونية العربية والعالمية والإخبارية والأطفال والمشفرة إلى شبكتك. يمكن استخدام هذا الشرح من قبل أصحاب شبكات المايكروتك لتهيئة الصفحة بشكل صحيح.

#### الملفات المطلوبة
1. **mobasher.html** - صفحة البث المباشر.
2. **tv.html** - صفحة القنوات التلفزيونية.

### خطوات الإعداد

1. **تحميل الملفات**
   - قم بتحميل الملفين `mobasher.html` و `tv.html` من [هذا الرابط](https://github.com/Goody-Code/Hotspot/archive/refs/heads/main.zip).

2. **نقل الملفات إلى مجلد صفحة الهوتسبوت**
   - انسخ الملفين `mobasher.html` و `tv.html` إلى المجلد الذي يحتوي على ملفات صفحة الهوتسبوت في جهاز المايكروتك الخاص بك.

3. **تعديل ملف config.js**
   - افتح ملف `config.js` الموجود في مجلد صفحة الهوتسبوت باستخدام أي محرر نصوص.
   - ابحث عن القيمة `"redirect-to-mobasher"` وقم بتعديلها لتصبح كما يلي:
     ```json
     "redirect-to-mobasher": "mobasher.html"
     ```

#### مثال على config.js المعدل
```json
{
  // إعدادات أخرى...
  "redirect-to-mobasher": "mobasher.html"
}
```

### لأصحاب الشبكات الذين ليس لديهم ملف config.js

إذا لم يكن لديك ملف `config.js`، يمكنك عرض زر البث المباشر في صفحتك عن طريق تعديل ملف `status.html` كما يلي:

1. **فتح ملف status.html**
   - ابحث عن ملف `status.html` في مجلد صفحة الهوتسبوت.
   - افتح الملف باستخدام أي محرر نصوص.

2. **إضافة كود زر البث المباشر**
   - أضف الكود التالي في نهاية كود الصفحة:
     ```html
     ```css
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            background-color: #f4f4f9;
        }
        .popup {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 320px;
            background: rgba(255, 255, 255, 0.9);
            box-shadow: 0 8px 32px rgba(31, 38, 135, 0.37);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.18);
            overflow: hidden;
            transition: transform 0.6s ease-in-out;
            transform: translateY(100%);
        }
        .popup-header {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: #ffffff;
            padding: 15px;
            text-align: center;
            font-size: 18px;
            font-weight: bold;
            position: relative;
        }
        .popup-header i {
            margin-right: 10px;
        }
        .popup-body {
            padding: 20px;
            text-align: center;
            font-size: 16px;
            color: #333333;
        }
        .popup-body i {
            font-size: 22px;
            color: #ff5f6d;
            margin-bottom: 10px;
        }
        .popup-button {
            display: block;
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, #36d1dc, #5b86e5);
            color: #ffffff;
            text-align: center;
            font-size: 16px;
            font-weight: bold;
            text-decoration: none;
            border: none;
            cursor: pointer;
            border-radius: 0 0 20px 20px;
            transition: background 0.3s, transform 0.3s;
        }
        .popup-button:hover {
            background: linear-gradient(135deg, #2bb4c8, #5077c7);
            transform: scale(1.05);
        }
        .popup-close {
            position: absolute;
            top: 10px;
            right: 10px;
            background: none;
            border: none;
            color: #ffffff;
            font-size: 20px;
            cursor: pointer;
        }
        @keyframes slideUp {
            0% {
                transform: translateY(100%);
            }
            100% {
                transform: translateY(0);
            }
        }
        .show-popup {
            animation: slideUp 1s forwards;
        }
        @keyframes pulse {
            0% {
                box-shadow: 0 0 0 0 rgba(31, 38, 135, 0.7);
            }
            70% {
                box-shadow: 0 0 0 20px rgba(31, 38, 135, 0);
            }
            100% {
                box-shadow: 0 0 0 0 rgba(31, 38, 135, 0);
            }
        }
        .popup-button {
            animation: pulse 2s infinite;
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    ```
    ```html
    <div class="popup" id="liveStreamPopup">
        <div class="popup-header">
            <i class="fas fa-video"></i> بث مباشر
            <button class="popup-close" id="popupClose">&times;</button>
        </div>
        <div class="popup-body">
            
🎥! انضم إلينا الآن لمشاهدة البث المباشر
        </div>
        <a href="mobasher.html" class="popup-button">مشاهدة البث المباشر</a>
    </div>
    ```
    ```js
    <script>
        window.onload = function() {
            document.getElementById('liveStreamPopup').classList.add('show-popup');
        };
        document.getElementById('popupClose').addEventListener('click', function() {
            document.getElementById('liveStreamPopup').style.transform = 'translateY(100%)';
        });
    </script>

     ```
   ```
### شكر وتقدير

تم تطوير هذا المشروع من قبل المهندس والمطور خالد الغيلي، الذي يقدم هذا الحل لأصحاب الشبكات بكل فخر وتفاني. نقدم له ألف شكر وتحية على مساهمته وجهوده.

### صورة توضيحية
![قناة اليمن](https://mj.bald-news.com/wp-content/uploads/2023/07/%D9%82%D9%86%D8%A7%D8%A9-%D8%A7%D9%84%D9%8A%D9%85%D9%86.jpg)

### ملاحظات
- تأكد من صحة المسارات والأسماء عند نقل وتعديل الملفات.
- يُفضل أخذ نسخة احتياطية من ملفاتك الحالية قبل إجراء أي تعديلات.

### خاتمة

يهدف هذا الشرح إلى تسهيل عملية إعداد صفحة البث المباشر لشبكات المايكروتك بوضوح ودقة. نتمنى أن تجد هذه الإرشادات مفيدة وتساهم في تحسين تجربتك. إذا كان لديك أي استفسارات أو تحتاج إلى مساعدة إضافية، فلا تتردد في التواصل معنا.

---

رخصه MTV
---

**روابط التحميل:**
- [تحميل الملفات](https://github.com/Goody-Code/Hotspot/archive/refs/heads/main.zip)
