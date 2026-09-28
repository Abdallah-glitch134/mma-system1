# MMA System — Project S V8 (Android Ready)

هاي النسخة مجهزة لتحويل مشروع الويب إلى تطبيق Android حقيقي باستخدام Capacitor.

## المتطلبات على الكمبيوتر
- Node.js 20 أو أحدث
- Android Studio حديث
- Android SDK و Android SDK Platform Tools
- Java JDK 21

## أول مرة
افتح Terminal داخل مجلد المشروع وشغّل:

```bash
npm install
npx cap add android
npx cap sync android
npx cap open android
```

بعدها يفتح المشروع في Android Studio.

## إنشاء APK تجريبي
من Android Studio:
**Build → Build App Bundle(s) / APK(s) → Build APK(s)**

أو من Windows Terminal:

```bash
npm run android:build:debug
```

ستجد APK عادةً داخل:
`android/app/build/outputs/apk/debug/app-debug.apk`

## إنشاء APK للنشر
يفضل إنشاء Keystore خاص بك من Android Studio ثم:
**Build → Generate Signed App Bundle / APK**

لا تشارك ملف الـKeystore أو كلمة مروره.

## ملاحظات
- واجهة التطبيق عربية وRTL.
- ملفات PWA موجودة أيضاً داخل www، لكن نسخة Android تعتمد على WebView المدمج ولا تحتاج فتح index.html يدوياً.
- تحليل الفيديو بالذكاء الاصطناعي يحتاج Backend خارجي آمن؛ لا تضع مفتاح API داخل التطبيق.
- Google/Firebase يحتاج إعداد مشروعك ومفاتيحك/ملفاتك الخاصة قبل استخدام ميزات الحساب والسحابة.
