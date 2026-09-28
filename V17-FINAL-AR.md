# MMA System V17.0 — Final Game/Competition Layer

أضيفت طبقة اللعبة فوق V16.1 بدون إزالة نظام التدريب.

## الجديد
- Arena / ساحة المقاتلين.
- Seasons ربع سنوية مع Season Points.
- Rating + Divisions: Bronze / Silver / Gold / Platinum / Diamond.
- Daily Challenges + Weekly Challenges.
- Coins ومكافآت.
- Badges/إنجازات قابلة للجمع.
- Training Arena rating للمواجهات التدريبية.
- Global leaderboard عبر Firestore عند تفعيل Firebase.
- نشر بيانات الترتيب مع UID فقط والاسم المختصر.
- Offline-first: اللعبة والتقدم الأساسي يعملان محلياً.

## ملاحظة إنتاجية
الترتيب المركزي يحتاج Firebase حقيقي وتفعيل Authentication/Firestore ونشر FIREBASE-RULES-V17.txt.
ولمنع الغش في الترتيب التنافسي على مستوى الإنتاج، الأفضل لاحقاً نقل احتساب Season Points/Rating الحساس إلى Cloud Functions أو backend موثوق، بدلاً من الاعتماد على جهاز اللاعب وحده.

## النسخة
17.0.0
