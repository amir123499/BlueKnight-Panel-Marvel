# 🛡️ Marvel Panel — BlueKnight Panel Mod

English | [فارسی](#-فارسی)

---

## ⚠️ Credit First

**This panel is 100% BlueKnight's work.** This repo is a **UI mod** — I did not write any of the proxy, security, or core logic. I only changed the appearance (Marvel-inspired themes), added Persian translation, and integrated new features.

- 🛡️ **Original panel:** BlueKnight Panel by **BlueKnight**
- 🔗 **Original repo:** https://github.com/BlueKnightNet/Blue-Knight-Panel
- 📡 **Author's Telegram:** https://t.me/BlueKnight_Net
- 🎨 **This mod:** arblant

If you use this panel, please credit the original author. 🙏

---

## What's in this version

### My changes
- 🖥️ **3 independent UI designs** — pick from Appearance (saved per device):
  - `Aurora Glass` (default — floating glass sidebar)
  - `Command Deck` (sharp HUD rail)
  - `Floating Dock` (calm bottom dock)
- 🎬 **9 dynamic Marvel-inspired themes** — each with adaptive light & dark glass palettes:
  - `Arc Reactor`, `Scarlet Street`, `Chaos Red`, `Ten Rings Gold`, `Autumn Rooftops`, `Crescent Moon`, `Variant Green`, `Mystic Multiverse`, `Cosmic Outlaws`
- 🇮🇷 **Full Persian translation engine** — built-in dictionary, EN/فا toggle with RTL layout
- 📷 **Local QR generation** — no external requests (more private than the original)
- ✍️ **Clear credit inside the panel** — footer, login, and setup pages link to the original repo
- 🔒 **Security hardening** — login brute-force protection (429 after 8 fails), `PANEL_KEY` access key, decoy 404, CSRF check, security headers, IPv6 disabled
- 👥 **User Management** — per-user VLESS with quota (GB) and expiry (days)
- 📈 **Traffic Dashboard** — usage stats with per-user progress bars
- ⚡ **ISP Preset Builder** — Irancell → Fragment+Fingerprint; MCI → ECH
- 💾 **Backup & Restore** — export/import all panel data as JSON
- 🔗 **Per-user subscriptions** — `/sub/u/:uuid` returns the user's config

### From BlueKnight (unchanged)
- VLESS, Trojan, Shadowsocks over WebSocket
- Subscription links for v2rayNG, Hiddify, Clash, sing-box
- Built-in encrypted DNS (DoH)
- Fragmentation and Chain Proxy
- Hashed admin password (PBKDF2) + secure sessions

> Base version: BlueKnight Panel **v5.2.7**

---

## 📦 Download

Get `worker.js` from the **[Releases](../../releases)** page.

| File | What |
|---|---|
| **`worker.js`** | Standard version — panel at `/panel` |
| **`worker-stealth.js`** | Stealth version — panel at `/telemetry`, disguised paths |

> ⚠️ Subscription links differ between versions — copy fresh links from the Subscriptions tab after switching.

## ⚡ 3-Minute Install (Cloudflare Workers — free)

1. Download **`worker.js`** from [Releases](../../releases)
2. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** → **Create** → **Hello World** → **Deploy**
3. **Edit code** → delete the sample → paste the downloaded file → **Deploy**
4. **Storage & Databases** → **KV** → create a namespace
5. Back to the worker → **Settings** → **Bindings** → **Add** → **KV namespace** → variable name exactly **`BK_KV`**
6. **Settings** → **Runtime** → compatibility date `2026-10-20` or newer → **Deploy** (do NOT enable `nodejs_compat`)
7. Open `https://<your-worker>.workers.dev/panel` — set an admin password on first visit. **Use a long password.**

> Without `BK_KV` the panel has nowhere to store the password and login won't work.

---

## 🔒 Security notes

- Login has brute-force protection (429 after 8 failed attempts), but a long password is still best.
- Treat subscription links like passwords — rotate the token in settings if leaked.
- Keep the panel behind HTTPS (Workers is HTTPS by default).

---

## 📄 License

MIT — per the original BlueKnight Panel license. Full text in [LICENSE](LICENSE).
Copyright of the original code belongs to BlueKnight; UI changes in this version are by arblant.

---

---

# 🇮🇷 فارسی

<div dir="rtl">

## ⚠️ اول از همه: کردیت سازنده‌ی اصلی

**اصل این پنل، صددرصد متعلق به BlueKnight است.**
این ریپو فقط یک **تغییر ظاهری (UI Mod)** روی پنل BlueKnight است — من هیچ‌کدام از منطق پروکسی، امنیت یا قابلیت‌های اصلی را ننوشته‌ام؛ فقط ظاهرش را با تم‌های الهام‌گرفته از دنیای مارول عوض کرده‌ام، ترجمه‌ی فارسی اضافه کرده‌ام و چند قابلیت جدید گذاشته‌ام.

- 🛡️ **پنل اصلی:** BlueKnight Panel — ساخته‌ی **BlueKnight**
- 🔗 **ریپوی اصلی:** https://github.com/BlueKnightNet/Blue-Knight-Panel
- 📡 **کانال تلگرام سازنده:** https://t.me/BlueKnight_Net
- 🎨 **این نسخه (تغییرات):** arblant

اگر از این پنل استفاده می‌کنید، لطفاً حق سازنده‌ی اصلی را فراموش نکنید. 🙏

---

## این نسخه چی داره؟

### تغییراتی که من دادم
- 🖥️ **سه طراحی کامل و مستقل** — از بخش Appearance انتخاب کن:
  - `Aurora Glass` (پیش‌فرض)
  - `Command Deck`
  - `Floating Dock`
- 🎬 **۹ تم سینمایی با الهام از مارول** — هر تم حالت روشن و تیره‌ی خودش را دارد
- 🇮🇷 **ترجمه‌ی فارسی کامل داخل خود پنل** — دکمه‌ی EN/فا با چیدمان راست‌به‌چپ
- 📷 **ساخت QR کاملاً محلی** — هیچ درخواستی به بیرون نمی‌رود
- ✍️ **کردیت واضح داخل پنل** — فوتر، لاگین و setup لینک به ریپوی اصلی دارند
- 🔒 **سخت‌افزاری امنیتی** — محافظت لاگین (۸ بار اشتباه → 429)، کلید `PANEL_KEY`، صفحه‌ی ۴۰۴ جعلی، محافظت CSRF، هدرهای امنیتی، غیرفعال‌سازی IPv6
- 👥 **مدیریت یوزر** — VLESS اختصاصی با حجم (گیگ) و انقضا (روز)
- 📈 **داشبورد ترافیک** — آمار مصرف با نوار پیشرفت هر یوزر
- ⚡ **ISP Preset Builder** — ایرانسل → Fragment+Fingerprint؛ همراه اول → ECH
- 💾 **بکاپ و ریستور** — خروجی/ورودی همه‌ی داده‌ها به‌صورت JSON
- 🔗 **سابسکریپشن per-user** — مسیر `/sub/u/:uuid` کانفیگ یوزر را برمی‌گرداند

### چیزهایی که از BlueKnight اومده (بدون تغییر)
- پروتکل‌های VLESS و Trojan و Shadowsocks روی WebSocket
- لینک سابسکریپشن برای v2rayNG، Hiddify، Clash، sing-box
- سرور DNS رمزنگاری‌شده (DoH) داخلی
- Fragmentation و Chain Proxy
- پسورد ادمین هش‌شده (PBKDF2) و سشن امن

> نسخه‌ی پایه: BlueKnight Panel **v5.2.7**

---

## 📦 دانلود

فایل `worker.js` را از صفحه‌ی **[Releases](../../releases)** بگیر.

| فایل | چیه؟ |
|---|---|
| **`worker.js`** | نسخه‌ی عادی — پنل روی `/panel` |
| **`worker-stealth.js`** | نسخه‌ی استتار — پنل روی `/telemetry`، مسیرهای مخفی |

> ⚠️ لینک‌های سابسکریپشن بین دو نسخه فرق دارد — بعد از تعویض نسخه، لینک‌های جدید را از تب Subscriptions کپی کن.

## ⚡ نصب در ۳ دقیقه (Cloudflare Workers — رایگان)

۱. فایل **`worker.js`** را از [Releases](../../releases) دانلود کن
۲. برو به [dash.cloudflare.com](https://dash.cloudflare.com) ← **Workers & Pages** ← **Create** ← **Hello World** ← **Deploy**
۳. **Edit code** ← کد نمونه را پاک کن ← محتوای فایل دانلودشده را پیست کن ← **Deploy**
۴. **Storage & Databases** ← **KV** ← یه namespace بساز
۵. برگرد به ورکر ← **Settings** ← **Bindings** ← **Add** ← **KV namespace** ← اسم متغیر دقیقاً **`BK_KV`**
۶. **Settings** ← **Runtime** ← compatibility date روی `2026-10-20` یا جدیدتر ← **Deploy** (فلگ `nodejs_compat` را فعال نکن)
۷. باز کن: `https://< اسم-ورکرت >.workers.dev/panel` — بار اول پسورد ادمین می‌خواهد. **یه پسورد طولانی بذار.**

> بدون `BK_KV` پنل جایی برای نگه‌داشتن پسورد ندارد و لاگین کار نمی‌کند.

---

## 🔒 چند نکته‌ی امنیتی

- لاگین محافظت brute-force دارد (۸ بار اشتباه → 429)، ولی پسورد طولانی هنوز بهترین است.
- لینک سابسکریپشن مثل پسورد است — اگر لو رفت، از تنظیمات توکن را عوض کن.
- پنل را پشت HTTPS نگه دار (روی Workers خودش HTTPS است).

---

## 📄 لایسنس

MIT — طبق لایسنس پنل اصلی BlueKnight. متن کامل در فایل [LICENSE](LICENSE).
حق کپی‌رایت کد اصلی برای BlueKnight محفوظ است؛ تغییرات این نسخه از arblant است.

</div>
