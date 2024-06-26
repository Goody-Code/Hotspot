# mobasher
#### البث المباشر
 - لمشاهدة ومعاينة صفحة البث من هنا [مشاهدة](https://goody-code.github.io/Hotspot/mobasher.html).
### إعداد صفحة البث المباشر لشبكات المايكروتك

هذا المشروع يتيح لك إضافة صفحة بث مباشر لجميع قنوات بين سبورت والقنوات الرياضية والتلفزيونية العربية والعالمية والإخبارية والأطفال والمشفرة إلى شبكتك. يمكن استخدام هذا الشرح الموجة الى أصحاب شبكات المايكروتك لتهيئة الصفحة بشكل صحيح.

#### الملفات المطلوبة
1. **mobasher.html** - صفحة البث المباشر.

### خطوات الإعداد

1. **تحميل الملف**
   - قم بتحميل الملف `mobasher.html` من [هذا الرابط](https://github.com/Goody-Code/Hotspot/archive/refs/heads/main.zip).

2. **نقل الملف إلى مجلد صفحة الهوتسبوت**
   - انسخ الملف `mobasher.html` إلى المجلد الذي يحتوي على ملفات صفحة الهوتسبوت في جهاز المايكروتك الخاص بك.
- ![أنسخ الملف الى مجلد الصفحه بهاذا الشكل](https://i.postimg.cc/xTTk352Z/Screenshot-My-Files.jpg)
- 
3. **تعديل ملف config.js**

   - افتح ملف `config.js` الموجود في مجلد صفحة الهوتسبوت باستخدام أي محرر نصوص.
   -![بهاذا الشكل](https://i.postimg.cc/Gtb2s7F4/Screenshot-My-Files.jpg)
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
-![بهاذا الشكل](https://i.postimg.cc/yd4W7YWX/IMG-20240606-WA0065.jpg)

- بعد ذالك سيضهر زر الدخول الى البث في الصفحة بهاذا الشكل.
![زر البث](https://i.postimg.cc/Gh7vnmGb/Screenshot-Chrome.jpg)



### لأصحاب الشبكات الذين ليس لديهم ملف config.js

إذا لم يكن لديك ملف `config.js`، يمكنك اضافه نافذه منبثقه لعرض البث المباشر في صفحتك عن طريق تعديل ملف `status.html` كما يلي:

حمل الكود من هنا .[تحميل](https://raw.githubusercontent.com/Goody-Code/live/main/mobasher-pop.html).
بعد تحميل الملف افتح الملف وانسخ الكود الذي بداخلة ثم قم بالخطوات التاليه :
1. **فتح ملف status.html اذا لم تجده يمكنك البحث عن ملف index.html**
   - ابحث عن ملف `status.html` او اذا لم تجده ابحث عن ملف index.html  في مجلد صفحة الهوتسبوت.
   - افتح الملف باستخدام أي محرر نصوص.

2. **إضافة كود نافذه زر البث المباشر**
   - أضف الكود الذي قمت بنسخه في نهاية كود الصفحة:
   - وستظهر بهاذا الشكل.
   -![ستظهر نافذه لدخول البث بهاذا الشكل](https://i.postimg.cc/vThNZNft/Screenshot-Chrome.jpg)
     

### شكر وتقدير

تم تطوير هذا المشروع من قبل المهندس والمطور خالد الغيلي، الذي يقدم هذا الحل لأصحاب الشبكات بكل فخر وتفاني. نقدم له ألف شكر وتحية على مساهمته وجهوده.

### صورة توضيحية للبث المباشر 
![البث المباشر](https://i.postimg.cc/d1rh7qhZ/Screenshot-Chrome.jpg)

![البث المباشر](https://i.postimg.cc/13NPmv38/chrome-GMT-03-00.png)

![البث المباشر](https://i.postimg.cc/wvGf1Z8V/Screenshot-Chrome.jpg)

### ملاحظات
- تأكد من صحة المسارات والأسماء عند نقل وتعديل الملفات.
- يُفضل أخذ نسخة احتياطية من ملفاتك الحالية قبل إجراء أي تعديلات.

### خاتمة

يهدف هذا الشرح إلى تسهيل عملية إعداد صفحة البث المباشر لشبكات المايكروتك بوضوح ودقة. نتمنى أن تجد هذه الإرشادات مفيدة وتساهم في تحسين تجربتك. إذا كان لديك أي استفسارات أو تحتاج إلى مساعدة إضافية، فلا تتردد في التواصل معنا.

## هدف المشروع
هدف مشروعنا هو تقديم حلاً شاملاً لأصحاب الشبكات، يتيح لهم إضافة صفحة بث مباشر لمختلف القنوات، بما في ذلك الرياضية، الإخبارية، والترفيهية. نسعى من خلال ذلك إلى توفير تجربة مشاهدة مميزة ومتنوعة للمستخدمين، وتوفير الراحة والسهولة في الوصول إلى محتوى البث المباشر.

---

## الرخصة
- هذا المشروع مرخص بموجب ترخيص MIT.
---

**روابط التحميل:**
- [تحميل ملفات البث](https://github.com/Goody-Code/Hotspot/archive/refs/heads/main.zip)
- [تحميل ملف كود نافذه عرض زر البث في الصفحة](https://raw.githubusercontent.com/Goody-Code/live/main/mobasher-pop.html)
