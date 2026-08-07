<div dir="rtl">

# فیدل USA (Fiddel USA) — اشتراک رایگان کانفیگ VPN فقط آمریکا

یک اشتراک VPN رایگان و به‌روزرسانی‌شونده که **هر روز ساعت ۰۴:۳۴ به وقت تهران** ساخته می‌شود؛ فقط با **۸ کانفیگ برتر آمریکا (🇺🇸)**. هر کانفیگ پیش از انتشار با پروسه‌های واقعی Xray / sing-box / Hysteria2 به‌صورت زنده تست می‌شود.

نسخه: **۳.۰.۰-usa**

## ✨ تفاوت با نسخه اصلی

- **فقط آمریکا**: خروجی فقط شامل کانفیگ‌های کشور آمریکا (US) است
- **۸ کانفیگ برتر**: به جای ۲ کانفیگ در اشتراک اصلی، اینجا ۸ کانفیگ برتر آمریکا نگه داشته می‌شوند
- **زمان‌بندی**: هر روز ساعت **۰۴:۳۴** به وقت تهران (Asia/Tehran)
- **فایل‌های جداگانه**: خروجی هم در `felfelconfig.txt` و هم در `felfelconfig-US.txt` منتشر می‌شود

## لینک‌های مستقیم اشتراک

| نوع | لینک مستقیم (Raw) |
|-----|-------------------|
| **Base64 (همه اپلیکیشن‌ها)** | `https://raw.githubusercontent.com/sinahosseini379/VPN-Subscription-Tester-USA/main/felfelconfig.txt` |
| **فقط آمریکا (فایل جداگانه)** | `https://raw.githubusercontent.com/sinahosseini379/VPN-Subscription-Tester-USA/main/felfelconfig-US.txt` |

> **نکته:** همه اپلیکیشن‌های مدرن VPN (SFA، sing-box، NekoBox، Clash Meta، v2rayNG، Shadowrocket، Streisand، Hiddify و…) یک URL اشتراک Base64 را می‌پذیرند. کافیست همین یک لینک را وارد کنید.

## نحوه افزودن به اپلیکیشن‌ها

### اندروید (Android)
| اپلیکیشن | روش افزودن |
|----------|------------|
| **SFA / Sing-box** | `Profiles` ← `Add` ← `Remote` ← لینک را بچسبانید |
| **NekoBox** | `Profile` ← `Import from URL` ← لینک را بچسبانید |
| **v2rayNG** | `+` ← `Import from clipboard` (پس از کپی لینک) |
| **Kitsunebi** | `+` ← `Import from URI` ← لینک را بچسبانید |
| **Hiddify** | `Config` ← `Add Subscription` ← لینک را بچسبانید |

### iOS / macOS
| اپلیکیشن | روش افزودن |
|----------|------------|
| **Shadowrocket** | `+` ← `Subscribe` ← لینک را بچسبانید |
| **Streisand** | `Subscriptions` ← `Add` ← لینک را بچسبانید |
| **FoXray** | `Configuration` ← `Add Subscription` ← لینک را بچسبانید |
| **Quantumult X** | `Subscription` ← `Add` ← لینک را بچسبانید |

### ویندوز / لینوکس (Windows / Linux)
| اپلیکیشن | روش افزودن |
|----------|------------|
| **NekoRay** | `Server` ← `Add from URL` ← لینک را بچسبانید |
| **v2rayN** | `Subscription` ← `Add` ← لینک را بچسبانید |
| **Clash Verge / Verge Rev** | `Profiles` ← `New` ← `Remote` ← لینک را بچسبانید |
| **کلاینت‌های گرافیکی (v2rayA و…)** | لینک اشتراک را در تنظیمات وارد کنید |

## چه چیزی درون اشتراک است؟

- **پروتکل‌ها:** VLESS، VMess، Trojan، Shadowsocks، Hysteria2
- **ترنسپورت‌ها:** TCP، WebSocket، gRPC، HTTP/2، HTTPUpgrade، SplitHTTP
- **امنیت:** TLS، Reality، none
- **کشور خروجی:** فقط **آمریکا 🇺🇸**
- **تست‌شده:** هر کانفیگ از طریق فیلتر TCP، تشخیص کشور خروجی و چند دور تست URL زنده عبور می‌کند.
- **به‌روزرسانی روزانه:** هر روز ساعت **۰۴:۳۴ به وقت `Asia/Tehran`**.

## به‌روزرسانی خودکار

اشتراک یک راهنمای به‌روزرسانی خودکار به کلاینت اعلام می‌کند (`SUBSCRIPTION_INTERVAL_HOURS`، پیش‌فرض ۲۴ ساعت). اپلیکیشن‌های سازگار هر ۲۴ ساعت خودشان اشتراک را دوباره می‌گیرند. اگر اپلیکیشن شما به‌روزرسانی خودکار ندارد، روزی یک‌بار همان لینک را دوباره وارد کنید.

> هدرهای پروفایل (`profile-title`، `subscription-userinfo`، `profile-update-interval`) فقط از مسیر داشبورد `/subscription` ارائه می‌شوند؛ فایل خام گیت‌هاب این هدرها را ندارد اما همان محتوا را دارد.

## راه‌اندازی شخصی (Self-Hosting) — شروع سریع

```bash
git clone https://github.com/sinahosseini379/VPN-Subscription-Tester-USA
cd VPN-Subscription-Tester-USA
pip install -e ".[dev]"
# config.env همیشه با توکن و تنظیمات USA موجود است
vpn-tester
```

- به‌صورت پیش‌فرض یک حلقه زمان‌بندی‌شده به‌همراه داشبورد وب روی `http://0.0.0.0:30445` اجرا می‌شود.
- برای یک اجرای تکی: `vpn-tester --once`
- برای رد کردن مرحله‌ی ارسال به گیت‌هاب: `vpn-tester --no-push`
- نیازمندی‌ها: **پایتون ۳.۹ به بالا**. هسته‌های Xray / sing-box / Hysteria به‌صورت خودکار دانلود و به‌روزرسانی می‌شوند.

## تنظیمات پیشرفته (config.env)

| متغیر | پیش‌فرض USA | توضیح |
|--------|-------------|-------|
| `CONFIGS_PER_COUNTRY` | `8` | تعداد کانفیگ در **اشتراک اصلی** |
| `PER_COUNTRY_OUTPUT_COUNT` | `8` | تعداد کانفیگ در **فایل جداگانه‌ی کشور** |
| `SCHEDULE_TIME` | `04:34` | زمان اجرای روزانه (HH:MM) |
| `TIMEZONE` | `Asia/Tehran` | منطقه زمانی برای زمان‌بندی |
| `STEALTH_MODE` | `prefer` | `off` \| `prefer` \| `strict` — کنترل امتیازدهی Stealth |
| `STEALTH_MIN_SCORE` | `0.4` | حداقل امتیاز (فقط در حالت `strict`) |
| `ALLOWED_COUNTRIES` | `US:United States:🇺🇸` | فقط آمریکا مجاز است |

**پیشنهاد برای سرورهای ایران (سازگاری همه اپراتورها):**
```env
STEALTH_MODE=strict
STEALTH_MIN_SCORE=0.5
CONFIGS_PER_COUNTRY=8
PER_COUNTRY_OUTPUT_COUNT=8
```

این تنظیمات باعث می‌شود کانفیگ‌های با Security ضعیف (plaintext، TCP خام، Shadowsocks ساده) قبل از تست‌های وقت‌گیر حذف شوند و فقط کانفیگ‌های پرامتیاز (VLESS+Reality+WS، VLESS+TLS+WS، Trojan+TLS+WS) در خروجی باقی بمانند.

## داشبورد

داشبورد پیشرفت زنده، لاگ‌های جاری، کانفیگ‌های منتشرشده، مدیریت لیست اشتراک‌ها و ویرایش زمان‌بندی را نشان می‌دهد.
دسترسی: `http://<server-ip>:30445`

## حریم خصوصی

- **بدون لاگ ترافیک:** تستر فقط اتصال‌پذیری را می‌سنجد؛ هیچ ترافیک کاربری از سرورهای ما عبور نمی‌کند.
- **بدون ردیابی:** نه آنالیتیکس، نه شناسه کاربر، نه تلِمتری.
- **متن‌باز:** کل کد در گیت‌هاب موجود است.

## سلب مسئولیت

این پروژه صرفاً کانفیگ‌های **عمومیِ در دسترس** پروکسی را برای پژوهش و استفاده شخصی گردآوری و تست می‌کند. ما هیچ سرور پروکسی‌ای را میزبانی، کنترل یا تأیید نمی‌کنیم. استفاده بر عهده کاربر و مطابق قوانین محلی است.

## حمایت

اگر این پروژه برایتان مفید بود، لطفاً به مخزن گیت‌هاب ⭐ بدهید:
[github.com/sinahosseini379/VPN-Subscription-Tester-USA](https://github.com/sinahosseini379/VPN-Subscription-Tester-USA)

</div>

---

# Fiddel USA — Free VPN Config Subscription (USA Only)

A free, daily-rebuilt VPN subscription with **only 8 best USA configs (🇺🇸)**, updated daily at **04:34 Asia/Tehran**. Every config is **live-tested** through real Xray / sing-box / Hysteria2 processes before it is published.

Version: **3.0.0-usa**

## ✨ Differences from Main Version

- **USA only**: Only United States exit country
- **8 top configs**: Instead of 2 per country in main subscription, keeps 8 best USA configs
- **Schedule**: Daily at **04:34 Asia/Tehran**
- **Dual output**: Both `felfelconfig.txt` and `felfelconfig-US.txt` published

## Quick Subscription Links

| Type | Direct (raw) link |
|------|-------------------|
| **Base64 (all apps)** | `https://raw.githubusercontent.com/sinahosseini379/VPN-Subscription-Tester-USA/main/felfelconfig.txt` |
| **USA only (separate file)** | `https://raw.githubusercontent.com/sinahosseini379/VPN-Subscription-Tester-USA/main/felfelconfig-US.txt` |

> **Tip:** Every modern VPN app (SFA, sing-box, NekoBox, Clash Meta, v2rayNG, Shadowrocket, Streisand, Hiddify, …) accepts a single base64 subscription URL. Just paste this one link.

## What's Inside

- **Protocols:** VLESS, VMess, Trojan, Shadowsocks, Hysteria2
- **Transports:** TCP, WebSocket, gRPC, HTTP/2, HTTPUpgrade, SplitHTTP
- **Security:** TLS, Reality, none
- **Exit country:** **United States 🇺🇸 only**
- **Tested:** every config passes a TCP filter, exit-country check, and several rounds of live URL tests.
- **Daily updates:** on schedule (default 04:34 `Asia/Tehran`).

## Auto-Update

The subscription advertises an auto-update hint to clients (`SUBSCRIPTION_INTERVAL_HOURS`, default 24). Compatible apps re-fetch the subscription every 24 hours on their own. If your app does not auto-update, just re-import the same URL once a day.

> Profile headers (`profile-title`, `subscription-userinfo`, `profile-update-interval`) are served from the dashboard's `/subscription` route. The raw GitHub file carries the same content but cannot carry those headers.

## Self-Hosting Quick Start

```bash
git clone https://github.com/sinahosseini379/VPN-Subscription-Tester-USA
cd VPN-Subscription-Tester-USA
pip install -e ".[dev]"
# config.env already configured for USA
vpn-tester
```

- By default this runs a scheduled loop plus a web dashboard at `http://0.0.0.0:30445`.
- Single run: `vpn-tester --once`
- Skip the GitHub push step: `vpn-tester --no-push`
- Requirements: **Python 3.9+**. Xray / sing-box / Hysteria cores are downloaded and updated automatically.

## Advanced Configuration (config.env)

| Variable | USA Default | Description |
|----------|-------------|-------------|
| `CONFIGS_PER_COUNTRY` | `8` | Configs in **main subscription** |
| `PER_COUNTRY_OUTPUT_COUNT` | `8` | Configs in **per-country file** |
| `SCHEDULE_TIME` | `04:34` | Daily run time (HH:MM) |
| `TIMEZONE` | `Asia/Tehran` | IANA timezone for schedule |
| `STEALTH_MODE` | `prefer` | `off` \| `prefer` \| `strict` — stealth scoring control |
| `STEALTH_MIN_SCORE` | `0.4` | Minimum score (only in `strict` mode) |
| `ALLOWED_COUNTRIES` | `US:United States:🇺🇸` | Only USA allowed |

**Recommended for Iran servers (cross-ISP compatibility):**
```env
STEALTH_MODE=strict
STEALTH_MIN_SCORE=0.5
CONFIGS_PER_COUNTRY=8
PER_COUNTRY_OUTPUT_COUNT=8
```

This drops configs with weak security (plaintext, raw TCP, basic Shadowsocks) before expensive tests, keeping only high-score configs (VLESS+Reality+WS, VLESS+TLS+WS, Trojan+TLS+WS).

## Dashboard

The dashboard shows live progress, streaming logs, published configs, subscription-list management, and schedule editing.
Access: `http://<server-ip>:30445`

## Privacy

- **No traffic logs:** the tester only checks connectivity; no user traffic passes through our servers.
- **No tracking:** no analytics, no user IDs, no telemetry.
- **Open source:** all code is on GitHub.

## Disclaimer

This project only collects and tests **publicly available** proxy configurations for research and personal use. We do not host, control, or endorse any proxy server. Use at your own risk and in accordance with local laws.

## Support / Star

If this helped you, please ⭐ the GitHub repository:
[github.com/sinahosseini379/VPN-Subscription-Tester-USA](https://github.com/sinahosseini379/VPN-Subscription-Tester-USA)