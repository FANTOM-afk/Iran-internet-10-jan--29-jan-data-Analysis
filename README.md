# Iran-internet-10-jan--29-jan-data-Analysis
Technical Report: Forensic Analysis of the Iran Network Blackout (Jan 8 – Jan 29, 2026)
# 🛡️ Network Forensic Report: Jan 2026 Blackout Analysis
# گزارش تحلیل فارنزیک شبکه: تحلیل خاموشی ژانویه ۲۰۲۶

---

## 🇮🇷 بخش فارسی (Persian Section)

### گزارش تحلیلی: کالبدشکافی رفتار شبکه در بازه ۱۸ دی تا ۹ بهمن ۱۴۰۴
این گزارش به تحلیل عددی و نموداری وضعیت اینترنت در بحران اخیر می‌پردازد. در بخش نخست، بازیابی و بازسازی داده‌های از دست رفته انجام شد و در بخش دوم، این داده‌ها در قالب شاخص‌های آماری، مورد تحلیل فنی قرار گرفتند.

#### ۱. تحلیل شکاف لایه‌ای و اثبات لیست سفید (Whitelist)
نمودارهای بازه ۱۰ تا ۱۸ ژانویه، گویای یک «انقطاع گزینشی» هستند. در حالی که موتورهای جستجوی داخلی و سرویس‌های مبتنی بر هوش مصنوعی در پاسخگویی ناتوان بودند، شواهد موجود در **سلول شماره ۷** فرضیه قطع کامل فیزیکی را رد می‌کند:

* **پایداری هسته:** شاخص `Active Probing` با میانگین **۳.۵۲** نشان می‌دهد که بخش استراتژیکی از سرورها و زیرساخت‌ها هرگز ارتباط خود را با شبکه جهانی از دست نداده‌اند.
* **ترافیک انسانی گزینشی:** میانگین **۱.۷۳** در شاخص `Mozilla (City Count)` فرضیه وجود «سیم‌کارت‌های سفید» یا دسترسی‌های انسانی سطح‌بندی شده را تقویت می‌کند؛ موضوعی که نشان‌دهنده تبعیض در دسترسی به زیرساخت ملی است.

#### ۲. تحلیل رفتار تلسکوپ و رد فرضیه حملات سایبری
در این بازه، ادعاهایی مبنی بر حملات سایبری گسترده و اسکن‌های پیچیده شبکه مطرح شد. اما تحلیل **سلول شماره ۱۱** (نمودار میله‌ای ساعتی) این ادعا را به چالش می‌کشد:

* **ناهنجاری زمانی:** اوج فعالیت تلسکوپ در ساعاتی ثبت شده که بار ترافیکی روی هاست‌های داخلی در کمترین سطح بوده است.
* **نتیجه‌گیری فنی:** برخلاف حملات سایبری متداول که در ساعات اوج مصرف (برای بیشترین تخریب) رخ می‌دهند، این ترافیک در ساعات فعالیت حداکثری سیستم‌های DPI ثبت شده است. این ریتم، بیشتر نشان‌دهنده یک «پایش سیستماتیک داخلی» برای تست پایداری فیلترینگ یا پاکسازی شبکه است تا یک حمله خارجی.



#### ۳. مهندسی فریب در بازگشت ترافیک
تحلیل لحظه اتصال مجدد، نشان‌دهنده یک «مهندسی ترافیک» پیچیده برای مدیریت افکار عمومی و ابزارهای مانیتورینگ خارجی است:

* **سیاست ویترین‌سازی:** رشد ناگهانی شاخص `Google Search` در حالی که شاخص `Active Probing` ثابت مانده، نشان‌دهنده باز کردن یک «روزنه محتوایی» صرفاً برای جستجوی دامین‌هاست.
* **شکاف پایداری:** عدم تطابق نرخ رشد زیرساخت با دسترسی به موتور جستجو، ثابت می‌کند که کاربران به اینترنت آزاد دسترسی نداشتند، بلکه تنها در یک محیط قرنطینه شده (Sandbox) مجاز به جستجو در دامین‌های خاص بودند.

#### ۴. وضعیت کنونی: سقف شیشه‌ای و تعادل جدید
در نهایت، مشاهده می‌شود که محدودیت‌های «سقف شیشه‌ای» گوگل که در ابتدای اتصال برداشته شده بودند، جای خود را به یک پایداری شکننده داده‌اند. اگرچه در حال حاضر دسترسی به اینترنت آزاد (از طریق ابزارهای عبور از محدودیت) برای کاربران ممکن شده، اما وجود شکاف منفی میان ظرفیت زیرساخت و کیفیت دسترسی، نشان‌دهنده اعمال یک سیاست «خفگی تعمدی» (Throttling) است که از نظر فنی تأسف‌بار است.

---

## 🇺🇸 English Section (Technical Analysis)

### Forensic Report: Dissecting Network Behavior (Jan 8 – Jan 29, 2026)
This report provides a numerical and graphical analysis of the internet status during the recent crisis. The first section covers the reconstruction of lost data, while the second section provides a technical analysis through statistical indicators.

#### 1. Layered Gap Analysis & Whitelist Verification
Charts from January 10–18 indicate a "selective disruption." While domestic search engines and AI APIs were dysfunctional, evidence in **Cell #7** refutes the theory of a total physical shutdown:

* **Core Stability:** The `Active Probing` index, averaging **3.52**, shows that strategic segments of the infrastructure never lost connection to the global network.
* **Selective Human Traffic:** An average of **1.73** in the `Mozilla (City Count)` index supports the hypothesis of "White SIM cards" or tiered human access, highlighting discriminatory infrastructure access.

#### 2. Telescope Behavior & Debunking Cyber-Attack Claims
During this period, claims of widespread cyber-attacks were made. However, the analysis of **Cell #11** (Hourly Bar Chart) challenges this narrative:

* **Temporal Anomaly:** Peak Telescope activity occurred during hours when internal host traffic was at its lowest.
* **Technical Conclusion:** Unlike typical cyber-attacks that target peak hours for maximum impact, this traffic peaked during maximum DPI system activity. This suggests a "systematic internal monitoring" for testing filtering stability rather than an external attack.



#### 3. Deception Engineering in Reconnection
The reconnection phase reveals a complex "traffic engineering" strategy designed to mislead public opinion and external monitoring tools:

* **Window Dressing Policy:** The sudden surge in `Google Search` while `Active Probing` remained stagnant indicates the opening of a "content portal" solely for domain searching.
* **Stability Gap:** The mismatch between infrastructure growth and search engine access proves that users did not have free internet access; they were restricted to a "Sandboxed" environment.

#### 4. Current State: The Glass Ceiling & The New Normal
Finally, it is observed that the "Glass Ceiling" restrictions on Google, initially lifted, have been replaced by a fragile stability. Although access to the open internet via circumvention tools is now possible, the **negative gap** between infrastructure capacity and access quality indicates a deliberate "Throttling" policy, which is technically deplorable.

---
