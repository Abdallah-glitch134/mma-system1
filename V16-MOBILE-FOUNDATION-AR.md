# MMA System V16 — Mobile Foundation

هذه النسخة هي الانتقال من V15 إلى أساس تطبيق موبايل حقيقي، مع الحفاظ على محرك V15 وبيانات اللاعب.

## الموجود الآن
- تطبيق Web/PWA جاهز للعمل داخل Capacitor.
- إعداد Capacitor Android موجود، وGitHub Actions ينشئ مشروع Android تلقائياً عند البناء.
- حسابات اللاعبين وFirestore موجودة في المحرك، مع تخزين اللاعب تحت `fighters/{uid}`.
- الخطة الذكية اليومية موجودة: الجاهزية، نقاط الضعف، المهارات التالية، التدريب الخفيف/القوي والتعافي.
- Onboarding وXP/Rank والمهارات والاختبارات والإصابات والتعافي والتصدير/الاستيراد موجودة.
- تمت ترقية هوية المشروع إلى V16.

## الخطوة التالية التي سننفذها
1. إنشاء مشروع Firebase الإنتاجي وربط Auth + Firestore.
2. تثبيت قواعد Firestore من `FIREBASE-RULES-V16.txt`.
3. تحسين تسجيل الدخول على Android/iOS ليكون Native-friendly بدلاً من الاعتماد على popup فقط.
4. فصل بيانات التطبيق عن إعدادات Firebase السرية/البيئية.
5. إضافة مكتبة التمارين والفيديوهات كبيانات منظمة.
6. تطوير محرك التدريب الذكي إلى توصيات يومية قابلة للتفسير.
7. اختبار APK على جهاز حقيقي.

## بناء APK من GitHub
الـworkflow الموجود في `.github/workflows/` ينفذ:
- Node 20
- Java 21
- Android SDK 35
- npm install
- `npx cap add android`
- `npx cap sync android`
- `./gradlew assembleDebug`

ثم يرفع `app-debug.apk` كـArtifact.

## مهم
لا نضع أي مفتاح API سري للذكاء الاصطناعي داخل التطبيق. Firebase Web config يمكن تضمينه، لكن الحماية الفعلية تعتمد على Authentication وFirestore Rules.
