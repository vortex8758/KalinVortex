# راهنمای استقرار Kalin AI Assistant

## 🚀 استقرار در Liara

### مرحله 1: آماده‌سازی پروژه

1. اطمینان حاصل کنید که تمام تغییرات در Git commit شده‌اند:
```bash
git add .
git commit -m "Prepare for deployment"
git push origin main
```

2. فایل `liara.json` در ریشه پروژه وجود دارد و تنظیمات صحیح دارد.

### مرحله 2: ثبت پروژه در Liara

1. به [Liara Dashboard](https://console.liara.ir) بروید
2. روی "ایجاد پروژه جدید" کلیک کنید
3. نوع پروژه را "Static" انتخاب کنید
4. نام پروژه را `kalin-ai-assistant` قرار دهید
5. پروژه را ایجاد کنید

### مرحله 3: تنظیمات استقرار

در تنظیمات پروژه در Liara:

- **Build Command**: `npm run build`
- **Output Directory**: `dist`
- **Node Version**: `18`
- **Environment Variables**: (در صورت نیاز)

### مرحله 4: اتصال به GitHub

1. در Liara، روی "Connect to Git" کلیک کنید
2. GitHub repository خود را انتخاب کنید
3. Branch اصلی را `main` انتخاب کنید
4. Auto-deploy را فعال کنید

### مرحله 5: استقرار

پروژه به صورت خودکار استقرار خواهد شد. می‌توانید در بخش "Deployments" پیشرفت را مشاهده کنید.

## 🌐 استقرار در GitHub Pages

### مرحله 1: آماده‌سازی

1. فایل `vite.config.ts` را بررسی کنید که base URL صحیح تنظیم شده باشد:

```typescript
export default defineConfig({
  base: process.env.NODE_ENV === 'production' ? '/kalin-ai-assistant/' : '/',
  // ... سایر تنظیمات
});
```

### مرحله 2: فعال‌سازی GitHub Pages

1. به تنظیمات repository در GitHub بروید
2. به بخش "Pages" بروید
3. Source را روی "GitHub Actions" تنظیم کنید

### مرحله 3: ایجاد Workflow

فایل `.github/workflows/deploy.yml` در پروژه وجود دارد که استقرار خودکار را مدیریت می‌کند.

## 🔧 تنظیمات محیطی

### متغیرهای محیطی مورد نیاز

برای استقرار در Liara، متغیرهای زیر را تنظیم کنید:

```bash
# API Configuration
VITE_API_BASE_URL=https://api.avalai.ir/v1
VITE_API_MODEL=gpt-4o

# App Configuration
VITE_APP_NAME=Kalin AI Assistant
VITE_APP_VERSION=1.0.0
```

### تنظیم در Liara

1. در Liara Dashboard، به بخش "Environment Variables" بروید
2. متغیرهای بالا را اضافه کنید
3. تغییرات را ذخیره کنید

## 🔍 عیب‌یابی

### مشکلات رایج

1. **خطای Build**: 
   - بررسی کنید که تمام dependencies نصب شده‌اند
   - فایل `package-lock.json` را بررسی کنید

2. **خطای 404 در SPA**:
   - اطمینان حاصل کنید که Liara تنظیمات SPA routing دارد
   - فایل `_redirects` را در پوشه `public` اضافه کنید

3. **مشکلات API**:
   - CORS settings را بررسی کنید
   - API key ها را بررسی کنید

### فایل _redirects برای SPA

فایل `public/_redirects` را ایجاد کنید:

```
/*    /index.html   200
```

## 📊 مانیتورینگ

### Liara Analytics

- در Liara Dashboard، بخش "Analytics" را بررسی کنید
- آمار بازدید و عملکرد را مشاهده کنید

### Error Tracking

- در صورت نیاز، سرویس‌های error tracking مانند Sentry را اضافه کنید

## 🔄 بروزرسانی

برای بروزرسانی پروژه:

1. تغییرات را در GitHub push کنید
2. Liara به صورت خودکار استقرار جدید را شروع می‌کند
3. در بخش "Deployments" پیشرفت را مشاهده کنید

## 📞 پشتیبانی

در صورت بروز مشکل:

1. Log های استقرار را در Liara بررسی کنید
2. با تیم پشتیبانی Liara تماس بگیرید
3. Issues را در GitHub repository ایجاد کنید

---

**نکته**: همیشه قبل از استقرار، پروژه را در محیط محلی تست کنید. 