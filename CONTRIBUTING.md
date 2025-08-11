# راهنمای مشارکت در Kalin AI Assistant

از مشارکت شما در توسعه Kalin AI Assistant سپاسگزاریم! این راهنما به شما کمک می‌کند تا به بهترین شکل در پروژه مشارکت کنید.

## 🚀 شروع کار

### پیش‌نیازها

- Node.js (نسخه 18 یا بالاتر)
- npm یا yarn
- Git

### راه‌اندازی محیط توسعه

```bash
# کلون کردن repository
git clone https://github.com/your-username/kalin-ai-assistant.git
cd kalin-ai-assistant

# نصب وابستگی‌ها
npm install

# اجرای پروژه در حالت توسعه
npm run dev
```

## 📝 راهنمای کدنویسی

### استانداردهای کدنویسی

- از **TypeScript** استفاده کنید
- از **ESLint** برای بررسی کد استفاده کنید
- از **Prettier** برای فرمت‌بندی کد استفاده کنید
- کامنت‌های فارسی برای توضیح منطق پیچیده بنویسید

### ساختار فایل‌ها

```
src/
├── components/          # کامپوننت‌های قابل استفاده مجدد
│   ├── ui/             # کامپوننت‌های UI پایه
│   └── [ComponentName].tsx
├── pages/              # صفحات اصلی
├── services/           # سرویس‌های API و منطق کسب‌وکار
├── hooks/              # Custom Hooks
├── contexts/           # Context های React
├── lib/                # توابع کمکی
└── types/              # تعاریف TypeScript
```

### نام‌گذاری

- **فایل‌ها**: PascalCase برای کامپوننت‌ها، camelCase برای سایر فایل‌ها
- **کامپوننت‌ها**: PascalCase
- **توابع**: camelCase
- **متغیرها**: camelCase
- **ثابت‌ها**: UPPER_SNAKE_CASE

## 🔄 فرآیند مشارکت

### 1. ایجاد Issue

قبل از شروع کار روی یک ویژگی جدید:

1. بررسی کنید که Issue مشابهی وجود ندارد
2. Issue جدید ایجاد کنید و توضیح دهید که چه کاری می‌خواهید انجام دهید
3. برچسب مناسب (bug, feature, enhancement) اضافه کنید

### 2. ایجاد Branch

```bash
# بروزرسانی branch اصلی
git checkout main
git pull origin main

# ایجاد branch جدید
git checkout -b feature/your-feature-name
# یا
git checkout -b fix/your-bug-fix
```

### 3. توسعه

- کد خود را بنویسید
- تست کنید که همه چیز کار می‌کند
- از ESLint استفاده کنید: `npm run lint`

### 4. Commit

```bash
# اضافه کردن تغییرات
git add .

# ایجاد commit با پیام مناسب
git commit -m "feat: add new feature description"
git commit -m "fix: resolve bug description"
git commit -m "docs: update documentation"
```

### 5. Push و Pull Request

```bash
# Push کردن branch
git push origin feature/your-feature-name
```

سپس در GitHub:
1. Pull Request ایجاد کنید
2. توضیح دهید که چه تغییراتی انجام داده‌اید
3. Screenshot اضافه کنید (در صورت نیاز)

## 🧪 تست

### تست محلی

```bash
# اجرای linter
npm run lint

# ساخت پروژه
npm run build

# پیش‌نمایش نسخه تولید
npm run preview
```

### تست عملکرد

- اطمینان حاصل کنید که پروژه در مرورگرهای مختلف کار می‌کند
- عملکرد را در دستگاه‌های مختلف تست کنید
- سرعت بارگذاری را بررسی کنید

## 📋 چک‌لیست Pull Request

قبل از ارسال Pull Request، موارد زیر را بررسی کنید:

- [ ] کد با ESLint سازگار است
- [ ] تمام تست‌ها موفق هستند
- [ ] مستندات بروزرسانی شده‌اند
- [ ] تغییرات در محیط محلی تست شده‌اند
- [ ] پیام commit مناسب است
- [ ] توضیحات Pull Request کامل است

## 🐛 گزارش باگ

برای گزارش باگ:

1. Issue جدید ایجاد کنید
2. برچسب "bug" اضافه کنید
3. توضیح دهید که چه اتفاقی افتاده
4. مراحل تکرار مشکل را بنویسید
5. اطلاعات سیستم عامل و مرورگر را اضافه کنید
6. Screenshot اضافه کنید (در صورت نیاز)

## 💡 پیشنهاد ویژگی جدید

برای پیشنهاد ویژگی جدید:

1. Issue جدید ایجاد کنید
2. برچسب "enhancement" اضافه کنید
3. توضیح دهید که چرا این ویژگی مفید است
4. نمونه‌های مشابه را ذکر کنید (در صورت وجود)

## 📞 ارتباط

- **Issues**: برای گزارش باگ و پیشنهاد ویژگی
- **Discussions**: برای سوالات و بحث‌های عمومی
- **Email**: برای مسائل خصوصی

## 🙏 قدردانی

از تمام مشارکت‌کنندگان که به بهبود Kalin AI Assistant کمک می‌کنند، سپاسگزاریم!

---

**نکته**: این پروژه تحت مجوز MIT منتشر شده است. با مشارکت در این پروژه، شما موافقت می‌کنید که کد شما تحت همین مجوز منتشر شود. 