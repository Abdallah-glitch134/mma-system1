# بناء MMA System APK من الموبايل فقط

1. أنشئ حساب GitHub.
2. أنشئ Repository جديداً (يمكن أن يكون Private).
3. ارفع كل محتويات هذا المشروع إلى الـRepository، وليس ملف ZIP نفسه.
4. افتح تبويب Actions.
5. اختر **Build MMA System APK**.
6. اضغط **Run workflow**.
7. انتظر انتهاء البناء بنجاح.
8. افتح نتيجة التشغيل، ثم قسم **Artifacts**، ونزّل `MMA-System-debug-APK`.
9. فك الضغط عن الملف على الموبايل، ثم ثبّت `app-debug.apk`.

ملاحظة: GitHub Actions يبني التطبيق على خادم GitHub، لذلك لا تحتاج Android Studio أو كمبيوتر على جهازك.
