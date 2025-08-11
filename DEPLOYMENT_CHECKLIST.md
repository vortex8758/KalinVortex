# چک‌لیست آماده‌سازی استقرار Kalin AI Assistant

## ✅ فایل‌های ایجاد شده

### فایل‌های اصلی
- [x] `package.json` - بروزرسانی شده با اطلاعات پروژه
- [x] `README.md` - راهنمای کامل پروژه
- [x] `LICENSE` - مجوز MIT
- [x] `CONTRIBUTING.md` - راهنمای مشارکت
- [x] `DEPLOYMENT.md` - راهنمای استقرار

### فایل‌های استقرار
- [x] `liara.json` - تنظیمات Liara
- [x] `.github/workflows/deploy.yml` - GitHub Actions برای Liara
- [x] `.github/workflows/github-pages.yml` - GitHub Actions برای GitHub Pages
- [x] `public/_redirects` - تنظیمات SPA routing
- [x] `vite.config.ts` - بروزرسانی شده برای استقرار

### فایل‌های SEO و PWA
- [x] `index.html` - بروزرسانی شده با meta tags
- [x] `public/manifest.json` - تنظیمات PWA
- [x] `public/robots.txt` - تنظیمات SEO
- [x] `public/sitemap.xml` - نقشه سایت

### فایل‌های پیکربندی
- [x] `.gitignore` - بروزرسانی شده
- [x] `eslint.config.js` - موجود
- [x] `tailwind.config.ts` - موجود
- [x] `tsconfig.json` - موجود

## 🚀 مراحل استقرار در Liara

### مرحله 1: آماده‌سازی Git
```bash
# بررسی وضعیت فایل‌ها
git status

# اضافه کردن تمام فایل‌ها
git add .

# ایجاد commit
git commit -m "feat: prepare project for deployment to Liara and GitHub"

# Push به GitHub
git push origin main
```

### مرحله 2: ثبت پروژه در Liara
1. به [Liara Dashboard](https://console.liara.ir) بروید
2. روی "ایجاد پروژه جدید" کلیک کنید
3. نوع پروژه را "Static" انتخاب کنید
4. نام پروژه را `kalin-ai-assistant` قرار دهید
5. پروژه را ایجاد کنید

### مرحله 3: تنظیمات استقرار در Liara
در تنظیمات پروژه:
- **Build Command**: `npm run build`
- **Output Directory**: `dist`
- **Node Version**: `18`

### مرحله 4: اتصال به GitHub
1. در Liara، روی "Connect to Git" کلیک کنید
2. GitHub repository خود را انتخاب کنید
3. Branch اصلی را `main` انتخاب کنید
4. Auto-deploy را فعال کنید

### مرحله 5: تنظیم متغیرهای محیطی (اختیاری)
در Liara Dashboard، بخش "Environment Variables":
```
VITE_API_BASE_URL=https://api.avalai.ir/v1
VITE_API_MODEL=gpt-4o
VITE_APP_NAME=Kalin AI Assistant
VITE_APP_VERSION=1.0.0
```

## 🌐 مراحل استقرار در GitHub Pages

### مرحله 1: فعال‌سازی GitHub Pages
1. به تنظیمات repository در GitHub بروید
2. به بخش "Pages" بروید
3. Source را روی "GitHub Actions" تنظیم کنید

### مرحله 2: بررسی Workflow
فایل `.github/workflows/github-pages.yml` موجود است و به صورت خودکار کار خواهد کرد.

## 🔍 تست نهایی

### تست محلی
```bash
# نصب وابستگی‌ها
npm install

# اجرای linter
npm run lint

# ساخت پروژه
npm run build

# پیش‌نمایش
npm run preview
```

### تست عملکرد
- [ ] پروژه در مرورگرهای مختلف کار می‌کند
- [ ] عملکرد در دستگاه‌های مختلف مناسب است
- [ ] سرعت بارگذاری قابل قبول است
- [ ] تمام لینک‌ها کار می‌کنند

## 📊 مانیتورینگ

### Liara Analytics
- در Liara Dashboard، بخش "Analytics" را بررسی کنید
- آمار بازدید و عملکرد را مشاهده کنید

### GitHub Actions
- در GitHub، بخش "Actions" را بررسی کنید
- وضعیت استقرار را مشاهده کنید

## 🔄 بروزرسانی

برای بروزرسانی پروژه:
1. تغییرات را در GitHub push کنید
2. Liara و GitHub Pages به صورت خودکار استقرار جدید را شروع می‌کنند
3. در بخش‌های مربوطه پیشرفت را مشاهده کنید

## 📞 پشتیبانی

در صورت بروز مشکل:
1. Log های استقرار را در Liara بررسی کنید
2. GitHub Actions logs را بررسی کنید
3. با تیم پشتیبانی Liara تماس بگیرید
4. Issues را در GitHub repository ایجاد کنید

---

## 🎉 تبریک!

پروژه شما آماده استقرار است! پس از تکمیل مراحل بالا، پروژه شما در آدرس‌های زیر قابل دسترسی خواهد بود:

- **Liara**: `https://kalin-ai-assistant.liara.run`
- **GitHub Pages**: `https://[username].github.io/kalin-ai-assistant`

**نکته**: همیشه قبل از استقرار، پروژه را در محیط محلی تست کنید. 