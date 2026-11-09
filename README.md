# ساخت APK بازی جاسوس با GitHub Actions

این پروژه فایل HTML بازی جاسوس را با Capacitor داخل یک اپ اندرویدی قرار می‌دهد.
برای ساخت APK نیازی به نصب Android Studio روی کامپیوتر نیست؛ GitHub Actions آن را می‌سازد.

## مراحل

1. وارد GitHub شوید و یک Repository جدید بسازید.
2. فایل ZIP را Extract کنید.
3. تمام محتویات پوشه را در ریشه Repository آپلود کنید؛ پوشه `.github` هم باید آپلود شود.
4. تغییرات را با Commit به شاخه `main` یا `master` بفرستید.
5. در GitHub وارد تب Actions شوید.
6. اجرای workflow با نام **Build Jasoos APK** را باز کنید.
7. پس از سبز شدن اجرا، پایین صفحه در بخش Artifacts فایل `jasoos-debug-apk` را دانلود کنید.
8. ZIP دانلودشده را Extract کنید؛ فایل `app-debug.apk` داخل آن است.

## نکات

- این خروجی APK دیباگ برای نصب و تست است، نه نسخه امضاشده برای انتشار در Google Play.
- برای انتشار عمومی/Google Play باید نسخه Release و کلید امضای امن تنظیم شود.
- شناسه برنامه در `capacitor.config.json` برابر `com.sirmahdi.jasoos` است.
- برای تغییر نام یا شناسه برنامه، قبل از اولین build فایل `capacitor.config.json` را ویرایش کنید.
- فایل بازی در `www/index.html` قرار دارد.
