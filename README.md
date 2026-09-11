# نظام كاشير المحل — تطبيق PWA

## الملفات
- `index.html` — التطبيق نفسه
- `manifest.json` — إعدادات التثبيت على الهاتف
- `sw.js` — تشغيل بدون إنترنت
- `icons/` — أيقونات التطبيق

---

## خطوات الرفع على GitHub (مرة واحدة فقط)

1. أنشئ حساب على https://github.com (لو ما عندك)
2. اضغط **New repository** → اعطه اسم مثل `cashier-app` → اجعله **Public** → **Create repository**
3. على جهازك، افتح Terminal / Git Bash داخل مجلد المشروع (بعد فك الضغط) ونفّذ:

```bash
git remote add origin https://github.com/USERNAME/cashier-app.git
git branch -M main
git push -u origin main
```

(بدّل `USERNAME` باسم حسابك على GitHub. المشروع مهيأ مسبقًا بـ git، فقط أضف الرابط وارفع.)

---

## ربط GitHub بـ Netlify (تحديث تلقائي)

1. اذهب إلى https://app.netlify.com وسجل دخول (يمكن بحساب GitHub مباشرة)
2. اضغط **Add new site** → **Import an existing project**
3. اختر **GitHub** ثم اختر مستودع `cashier-app`
4. اترك إعدادات البناء فارغة (لا يوجد build command، فقط اضغط **Deploy**)
5. بعد ثوانٍ سيعطيك رابط مثل `xxxx.netlify.app`

من الآن فصاعدًا: أي تعديل تعمله على `index.html` (أو أي ملف) وترفعه بـ:

```bash
git add -A
git commit -m "وصف التعديل"
git push
```

سيتحدث الموقع تلقائيًا خلال ثوانٍ بدون أي رفع يدوي.

---

## تثبيت التطبيق على الهاتف
افتح رابط Netlify من هاتفك:
- **أندرويد (كروم):** ⋮ ← "تثبيت التطبيق"
- **آيفون (سفاري):** زر المشاركة ← "إضافة إلى الشاشة الرئيسية"

## كود الدخول الافتراضي
`STORE-4872` (يمكن تعديله من داخل السكربت في `index.html`، المتغير `VALID_CODES`)
