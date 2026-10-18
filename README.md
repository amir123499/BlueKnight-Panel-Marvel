<div dir="rtl">

# 🛡️ پنل arblant — نسخه‌ی مارولِ BlueKnight Panel

![بنر](docs/banner.webp)

---

## ⚠️ اول از همه: کردیت سازنده‌ی اصلی

**اصل این پنل، صددرصد متعلق به BlueKnight است.**
این ریپو فقط یک **تغییر ظاهری (UI Mod)** روی پنل BlueKnight است — من هیچ‌کدام از منطق پروکسی، امنیت یا قابلیت‌های اصلی را ننوشته‌ام؛ فقط ظاهرش را با تم‌های الهام‌گرفته از دنیای مارول عوض کرده‌ام و ترجمه‌ی فارسی و چند بهبود کوچک ظاهری اضافه کرده‌ام.

- 🛡️ **پنل اصلی:** BlueKnight Panel — ساخته‌ی **BlueKnight**
- 🔗 **ریپوی اصلی:** https://github.com/BlueKnightNet/Blue-Knight-Panel
- 📡 **کانال تلگرام سازنده:** https://t.me/BlueKnight_Net
- 🎨 **این نسخه (تغییرات ظاهری):** arblant

اگر از این پنل استفاده می‌کنید، لطفاً حق سازنده‌ی اصلی را فراموش نکنید. 🙏

---

## این نسخه چی داره؟

### تغییراتی که من دادم (فقط ظاهری)
- 🎬 **۹ تم سینمایی با الهام از دنیای مارول** — هر تم پالت رنگ و حال‌وهوای خودش را دارد:
  - `Arc Reactor` ،`Scarlet Street` ،`Chaos Red` ،`Ten Rings Gold` ،`Autumn Rooftops` ،`Crescent Moon` ،`Variant Green` ،`Mystic Multiverse` ،`Cosmic Outlaws`
- 🇮🇷 **ترجمه‌ی فارسی داخل خود پنل** — متن‌های انگلیسی به‌صورت خودکار فارسی می‌شوند
- ✍️ **کردیت واضح داخل پنل** — در فوتر، صفحه‌ی ورود و صفحه‌ی ساخت پسورد نوشته شده که پنل اصلی از BlueKnight است (با لینک به ریپوی اصلی)

### چیزهایی که از BlueKnight اومده (بدون هیچ تغییری)
- پروتکل‌های VLESS و Trojan و Shadowsocks روی WebSocket
- لینک سابسکریپشن برای v2rayNG، Hiddify، Clash، sing-box و بقیه
- سرور DNS رمزنگاری‌شده (DoH) داخلی
- Fragmentation و Chain Proxy برای شبکه‌های سخت
- پسورد ادمین هش‌شده (PBKDF2) و سشن امن

> نسخه‌ی پایه: BlueKnight Panel **v5.2.4**

---

## ⚡ نصب در ۳ دقیقه (Cloudflare Workers — رایگان)

۱. از صفحه‌ی **Releases** همین ریپو فایل **`worker.js`** را دانلود کن
۲. برو به [dash.cloudflare.com](https://dash.cloudflare.com) ← بخش **Workers & Pages** ← **Create** ← **Start from Hello World** ← **Deploy**
۳. **Edit code** ← کل کد نمونه را پاک کن ← محتوای `worker.js` را پیست کن ← **Deploy**
۴. بخش **Storage & Databases** ← **KV** ← یه namespace بساز (مثلاً `blueknight`)
۵. برگرد به ورکر ← **Settings** ← **Bindings** ← **Add** ← **KV namespace** ← اسم متغیر دقیقاً **`BK_KV`**
۶. **Settings** ← **Runtime** ← compatibility date روی `2024-09-23` یا جدیدتر + فلگ **`nodejs_compat`** را فعال کن ← **Deploy**
۷. باز کن: `https://< اسم-ورکرت >.workers.dev/panel` — بار اول ازت پسورد ادمین می‌خواهد. **یه پسورد طولانی بذار.**

> بدون `BK_KV` پنل جایی برای نگه‌داشتن پسورد ندارد و لاگین کار نمی‌کند.

---

## 🔒 چند نکته‌ی امنیتی

- صفحه‌ی لاگین **rate limit ندارد**؛ پسوردت هرچه طولانی‌تر، امن‌تر.
- لینک سابسکریپشن مثل پسورد است — اگر لو رفت، از تنظیمات توکن را عوض کن.
- پنل را پشت HTTPS نگه دار (روی Workers خودش HTTPS است).

---

## 📄 لایسنس

MIT — طبق لایسنس پنل اصلی BlueKnight. متن کامل در فایل [LICENSE](LICENSE).
حق کپی‌رایت کد اصلی برای BlueKnight محفوظ است؛ تغییرات ظاهری این نسخه از arblant است.

</div>
