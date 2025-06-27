[**English**](README.md) | [**فارسی**](README_fa.md) | [**简体中文**](README-ch.md) | [**Русский**](README_ru.md)

# 🧱 تور پلاس برای OpenWrt با Passwall و Passwall2

> ⚡️ **دستور نصب تنها با یک خط**:

```bash
rm -f *.sh && wget https://raw.githubusercontent.com/peditx/opnwrt-torplus/refs/heads/main/.Files/install.sh && chmod +x install.sh && sh install.sh
```

---

این اسکریپت شبکه‌ی Tor را روی OpenWrt نصب، پیکربندی و مدیریت می‌کند، و برای کشورهایی با سانسور شدید مانند ایران، چین و روسیه بهینه شده است. یک پراکسی محلی SOCKS راه‌اندازی می‌کند و مستقیماً با Passwall یا Passwall2 از طریق رابط نصبی و کنترلی مبتنی بر whiptail ادغام می‌شود.


---

🛠️ قابلیت‌ها

نصب آسان با رابط whiptail

نصب خودکار بسته‌های مورد نیاز

پشتیبانی از سه نوع پل: snowflake، obfs4، meek — یا تشخیص خودکار

تنظیم پورت SOCKS تور روی 9050

ادغام با Passwall یا Passwall2 از طریق ایجاد نود SOCKS5 فعال

کنترل‌پنل خط فرمان از طریق tor-control:

شروع / توقف / ریستارت تور

بررسی وضعیت Tor

تست اتصال با check.torproject.org

تغییر تعاملی نوع پل




---

📡 استفاده از کنترل تور

بعد از نصب، از اسکریپت کنترل استفاده کنید:

tor-control

شما می‌توانید:

تور را شروع/توقف کنید

آن را ریستارت کنید

وضعیت اتصال را ببینید

از طریق پراکسی تور پینگ بگیرید

نوع پل را دوباره انتخاب کرده و مجدداً پیکربندی کنید



---

📂 خلاصه فایل‌ها

مسیر	کاربرد

/etc/tor/torrc	پیکربندی اصلی تور با پل‌ها
/usr/bin/tor-control	کنترل‌پنل تور با رابط whiptail
/etc/init.d/tor	اسکریپت راه‌اندازی سرویس تور



---

🔁 ادغام با Passwall

اگر Passwall یا Passwall2 شناسایی شود، یک نود SOCKS به نام "Tor" با آدرس 127.0.0.1:9050 ساخته می‌شود.

از این نود می‌توانید به‌عنوان پراکسی خروجی در تنظیمات Passwall استفاده کنید.


---

🧪 تست اتصال تور

برای اطمینان از اتصال از طریق Tor:

tor-control → Ping (check.torproject.org)

یا دستی:

curl --socks5-hostname 127.0.0.1:9050 https://check.torproject.org


---

🧾 لایسنس

منتشر شده تحت لایسنس PeDitX
📢 کانال تلگرام: https://t.me/peditx
