# 🍨 بستنی سنتی زعفرونی — لندینگ پیج

لندینگ پیج تک‌صفحه‌ای، مدرن و کاملاً واکنش‌گرا برای یک کارگاه کوچک خانوادگی تولید بستنی سنتی.

## ✨ امکانات

- **RTL کامل** با فونت فارسی [وزیرمتن](https://github.com/rastikerdar/vazirmatn)
- پالت رنگی برند: کرم، زعفرانی/طلایی، قهوه‌ای گرم
- بخش‌ها: هدر چسبان، هیرو، درباره کارگاه، محصولات (۵ طعم)، چرا ما، نظرات مشتریان، **سفارش خرده و عمده**، تماس و فوتر
- **سیستم سفارش‌گیری**: سبد خرید با حالت خرده/عمده، تخفیف پلکانی عمده (۵٪ / ۱۰٪ / ۱۵٪) و ارسال خودکار متن سفارش به **واتساپ**
- انیمیشن‌های ملایم هنگام اسکرول (IntersectionObserver) و احترام به `prefers-reduced-motion`
- آیکون‌های دست‌ساز SVG، بدون هیچ کتابخانه‌ی آیکون
- بهینه برای موبایل و سئوی محلی (JSON-LD)

## 🛠 تکنولوژی

- HTML + Tailwind CSS (CDN) + JavaScript خالص — بدون بیلد و بدون وابستگی نصب‌شدنی
- تصاویر محصولات در `assets/img/`

## 🚀 اجرا

کافی است `index.html` را در مرورگر باز کنید، یا یک سرور استاتیک ساده بگیرید:

```bash
python3 -m http.server 8000
# سپس: http://localhost:8000
```

## 🌍 انتشار روی GitHub Pages

ورک‌فلو `.github/workflows/pages.yml` با هر push روی شاخه‌ی `main` (یا اجرای دستی از تب Actions) سایت را به‌صورت خودکار منتشر می‌کند.

### فعال‌سازی یک‌باره (در تنظیمات مخزن)

1. **Settings → Pages → Build and deployment → Source → GitHub Actions**
2. **Settings → Actions → General → Workflow permissions → Read and write permissions**

> اگر این دو مورد تنظیم نشده باشند، ورک‌فلو با پیام راهنمای فارسی شکست می‌خورد و دقیقاً می‌گوید چه چیزی را فعال کنید.

نشانی نهایی: `https://<username>.github.io/<repository>/`

### عیب‌یابی

| پیام خطا | راه‌حل |
| --- | --- |
| `GitHub Pages هنوز روی این مخزن فعال نیست` | مورد ۱ بالا را انجام دهید و ورک‌فلو را Re-run کنید |
| `Resource not accessible by integration` در مرحله‌ی deploy | مورد ۲ بالا (مجوز Read and write) را انجام دهید و Re-run کنید |

## ⚙️ شخصی‌سازی

| مورد | محل |
| --- | --- |
| شماره واتساپ | ثابت `WHATSAPP_NUMBER` در `assets/js/main.js` |
| قیمت محصولات | آبجکت `PRODUCTS` در `assets/js/main.js` |
| پله‌های تخفیف عمده | ثابت `WHOLESALE_TIERS` در `assets/js/main.js` |
| آدرس، تلفن، ساعات کاری | بخش تماس در `index.html` |
| پالت رنگی | پیکربندی `tailwind.config` داخل `index.html` |
