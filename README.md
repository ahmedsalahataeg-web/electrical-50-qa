# POWER ACADEMY — Classic Control Interview Challenge

React + TypeScript، بيتبني بـ esbuild. الموقع RTL كامل ومتجاوب، وتقدّمك بيتحفظ في localStorage.

## التشغيل
```bash
npm install
npm run build        # بيطلّع dist/ + dist/power-academy.single.html (ملف واحد)
npx serve dist       # أو افتح dist/index.html من أي استضافة static
npm run validate     # بيفحص الـ 50 سؤال (4 اختيارات، إجابة صحيحة، تحليل، نصيحة...)
```

## إضافة أسئلة جديدة
كل الأسئلة في `src/data/level1.ts … level6.ts`. انسخ أي سؤال وعدّل فيه، أو أضف ملف جديد وسجّله في `src/data/index.ts`.
الحقول: `id, level, difficulty, category, tags, question, options[4] (text + why), correct, analysis[], flow?, trap?, tip`.
الاختيارات الأربعة كل واحد فيهم معاه شرحه (`why`) علشان Interview Mode يخلط الترتيب من غير ما الشرح يتلخبط.

## الهيكل
- `src/data` الأسئلة والأنواع
- `src/logic` الجلسة، التخزين، الفلاتر والبحث، النتائج
- `src/components` الواجهة
- `public/` اللوجو الرسمي (متقصوص الهوامش وبأحجام محسّنة، بدون أي تعديل في التصميم)
