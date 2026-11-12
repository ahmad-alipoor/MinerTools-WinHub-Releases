# MinerTools WinHub Releases

**Public distribution page for MinerTools WinHub.** The application source remains in a separate private repository. This repository is intended to contain approved release packages, checksums, and release notes only.

[فارسی](#فارسی) · [English](#english)

---

## فارسی

**MinerTools WinHub** برنامه‌ای ویندوزی برای پایش محلی ماینرهاست. عامل Go، داشبورد محلی و مدیر دسکتاپ WinUI 3 در یک برنامه کار می‌کنند. زبان‌های فارسی، انگلیسی، روسی و چینی ساده‌شده پشتیبانی می‌شوند.

### وضعیت انتشار عمومی

این مخزن فقط برای بسته‌های نهایی و تأییدشده است. نسخه‌های آزمایشی و Draft به اینجا منتقل نمی‌شوند. تا آماده‌شدن فرایند امضای فایل‌های ویندوز و انتشار پایدار، بسته‌ی عمومی برای دانلود ارائه نشده است. فهرست نسخه‌های تأییدشده را در [Releases](../../releases) ببینید.

### انتخاب بسته

| فایل | کاربرد |
| --- | --- |
| `*-setup.exe` | نصب کامل؛ فایل‌های لازم را همراه برنامه دارد. |
| `*-lite-setup.exe` | نصب کم‌حجم؛ پیش‌نیازهای Windows را بررسی می‌کند و در صورت نیاز راهنمای نصب نشان می‌دهد. |
| `*-portable.zip` | نسخه‌ی کامل قابل‌حمل؛ ZIP را کامل استخراج کنید و فایل `MinerTools-WinHub.exe` را اجرا کنید. پوشه‌ی `app` و فایل‌های همراه را جابه‌جا یا حذف نکنید. |
| `*-lite-portable.zip` | نسخه‌ی قابل‌حمل کم‌حجم؛ پیش‌نیازهای Windows را جداگانه لازم دارد. |
| `*-update.zip` | بسته‌ی به‌روزرسانی برای مسیر به‌روزرسانی Hub است؛ برای نصب اولیه یا استخراج و اجرای دستی نیست. |

نسخه‌های کم‌حجم به runtimeهای سازگار Microsoft نیاز دارند؛ راهنمای داخل بسته و صفحه‌های رسمی Microsoft را دنبال کنید. بسته‌های WinHub برای Windows x64 ساخته می‌شوند؛ نسخه‌ی بومی ARM64 ارائه نمی‌شود.

### نصب و اجرا

1. فقط از نسخه‌ی Stable منتشرشده در [Releases](../../releases) دریافت کنید.
2. فایل checksum همان نسخه را بازبینی کنید. در PowerShell، مقدار SHA-256 را با این دستور محاسبه کنید:

   ```powershell
   Get-FileHash .\MinerTools-WinHub-0.0.000-win-x64-setup.exe -Algorithm SHA256
   ```

   نام فایل نمونه است؛ آن را با نام فایل همان Release جایگزین کنید و مقدار را با `SHA256SUMS.txt` همان نسخه تطبیق دهید.
3. برای نصب، فایل setup را اجرا کنید. برای نسخه‌ی قابل‌حمل، ZIP را کامل استخراج و `MinerTools-WinHub.exe` را از پوشه‌ی استخراج‌شده اجرا کنید.
4. برنامه داشبورد محلی را به‌طور پیش‌فرض روی `http://127.0.0.1:8787/` ارائه می‌کند. دسترسی LAN اختیاری است و از داخل مدیر برنامه، با محدودیت شبکه‌ی خصوصی و TLS فعال می‌شود.

### داده و حریم خصوصی

پایش ماینر، تاریخچه و پایگاه‌داده SQLite روی همان رایانه‌ی Windows نگهداری می‌شوند. پس از نصب، جمع‌آوری محلی برای کارکردن به اینترنت نیاز ندارد. ارتباط با ماینر از Agent محلی انجام می‌شود؛ مرورگر مستقیماً به ماینر وصل نمی‌شود. برنامه برای پایش، تنظیمات ماینر یا Pool را تغییر نمی‌دهد.

### به‌روزرسانی

فایل `update.zip` به‌تنهایی نصب‌کننده نیست. به‌روزرسانی خودکار فقط وقتی انجام می‌شود که نسخه‌ی امضاشده و سازگار از طریق خوراک رسمی Hub در دسترس Agent باشد. انتشار یک ZIP در این مخزن به‌تنهایی به معنی فعال‌بودن آن در خوراک Hub نیست.

---

## English

**MinerTools WinHub** is a Windows application for local miner monitoring. Its Go Agent, local dashboard, and WinUI 3 desktop manager work together. The interface supports Persian, English, Russian, and Simplified Chinese.

### Public release status

This repository is for final, approved distribution packages only. Test builds and drafts are not mirrored here. Public downloads will be listed after Windows code signing and the stable-release process are ready. See [Releases](../../releases) for approved versions.

### Choose a package

| File | Purpose |
| --- | --- |
| `*-setup.exe` | Full installer; includes the required application runtimes. |
| `*-lite-setup.exe` | Smaller installer; checks Windows prerequisites and provides guidance when they are missing. |
| `*-portable.zip` | Full portable edition; extract the complete ZIP and run `MinerTools-WinHub.exe`. Keep the adjacent `app` folder and bundled files together. |
| `*-lite-portable.zip` | Smaller portable edition; requires compatible Microsoft runtimes to be installed separately. |
| `*-update.zip` | Package for the Hub update path; it is not a first-time installer or a ZIP to install manually. |

The lite editions require compatible Microsoft runtimes; follow the included guide and official Microsoft links. WinHub packages target Windows x64. There is no native ARM64 build.

### Install and run

1. Download only a published Stable version from [Releases](../../releases).
2. Verify its SHA-256 checksum. In PowerShell, calculate it with:

   ```powershell
   Get-FileHash .\MinerTools-WinHub-0.0.000-win-x64-setup.exe -Algorithm SHA256
   ```

   Replace the example filename with the asset name from the release, then compare the result with that release's `SHA256SUMS.txt`.
3. Run a setup executable to install. For a portable edition, extract the entire ZIP and run `MinerTools-WinHub.exe` from the extracted folder.
4. The local dashboard listens on `http://127.0.0.1:8787/` by default. Optional LAN access is enabled in the desktop manager and is protected with private-subnet scoping and TLS.

### Data and privacy

Miner polling, history, and the SQLite database stay on the Windows computer. After installation, local monitoring continues without an internet connection. The local Go Agent communicates with miners; the browser does not connect to miners directly. Monitoring does not change miner or pool settings.

### Updates

The `update.zip` is not an installer. Automatic updates require a compatible, signed release to be available from the official Hub feed. Publishing a ZIP in this repository alone does not make it available through the Hub update feed.
