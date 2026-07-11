# 🤍

صفحة عربية هادئة فيها مقدمة + كم سؤال بسيط لطيف. الجواب دايمًا "نعم"، وزر «لأ» بيهرب — ومحمد بيزعل 😄. وكل حركة تنسجّل مباشر لمحمد.

A calm mobile-first Arabic page: a friendly intro, then a few gentle, low-pressure questions. The **No** button dodges, the **Mohammad** avatar reacts (angry face + speech bubble on every No attempt), and everything is logged **live** to Firebase.

## الصفحتان / Two pages
- **`index.html`** — صفحة أسيل (the page she opens).
- **`watch.html`** — لوحة محمد المباشرة (Mohammad's live dashboard).

## المميزات / Features
- 🕊️ **مقدمة** تشرحلها كيف تشتغل، بدون ضغط.
- 💬 أسئلة **غير مباشرة وخفيفة** (تعارف على مهل، خطوة خطوة).
- 🏃 زر **«لأ» يهرب** يمين ويسار، ووجه محمد **يزعل** ويطلع فقاعة كلام.
- 👀 شارة **«محمد يشاهد الآن»** تظهر لأسيل لما محمد يفتح لوحته (زي سناب).
- 📡 **تسجيل مباشر**: كل «نعم» وكل محاولة «لأ» + وين واصلة تظهر عند محمد لحظيًا.

## كيف يشتغل مباشر / How live works
Uses **Firebase Realtime Database**:
- `presence/aseel` & `presence/mohammad` → online status (auto-removed on disconnect).
- `events` → the live activity log (start / yes / no_attempt / final).

> ملاحظة: قاعدة البيانات حاليًا **بوضع تجريبي مفتوح** (أي حد بيقدر يقرأ/يكتب). لو بدك أمان أكتر، فعّل قواعد Firebase.

## التشغيل / Run locally
```bash
python3 -m http.server 8000
```
- افتحي صفحة أسيل: `http://localhost:8000/index.html`
- افتح لوحة محمد: `http://localhost:8000/watch.html`

## النشر / Deploy (GitHub Pages)
Settings → Pages → Branch `main` → `/ (root)`.
- صفحة أسيل: `https://mohammad00197.github.io/aseel/`
- لوحة محمد: `https://mohammad00197.github.io/aseel/watch.html`
