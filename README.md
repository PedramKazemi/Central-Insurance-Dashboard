# داشبوردهای مدیریتی رئیس کل بیمه مرکزی

پروژه طراحی و مستندسازی داشبوردهای سطح‌بالا برای **رئیس کل بیمه مرکزی جمهوری اسلامی ایران**، قابل پیاده‌سازی در **Grafana 13**.

## هدف پروژه

ایجاد حداقل ۵ داشبورد مدیریتی که:

- از دید رئیس کل بیمه مرکزی طراحی شده باشند
- دید تحلیلی کامل داشته باشند و با یک نگاه اطلاعات کلیدی را منتقل کنند
- مبهم و نیازمند توضیح طولانی نباشند
- از نظر بصری حرفه‌ای و تمیز باشند
- از نظر فنی با Grafana نسخه ۱۳ سازگار باشند

## ساختار پروژه

```
bime-markazi-ceo-dashboards/
├── README.md                          # معرفی پروژه
├── docs/
│   ├── 01-project-control.md          # مفاهیم کنترل پروژه
│   ├── 02-scope-and-objectives.md     # دامنه و اهداف
│   └── 03-stakeholders.md             # ذی‌نفعان
├── harness/
│   ├── 00-harness-overview.md         # معرفی هارنس (قوانین حاکم)
│   ├── 01-design-principles.md        # اصول طراحی
│   ├── 02-clarity-rules.md            # قوانین شفافیت و عدم ابهام
│   ├── 03-visual-rules.md             # قوانین بصری
│   ├── 04-grafana-constraints.md      # محدودیت‌های فنی Grafana 13
│   └── 05-demo-mode-rules.md          # قوانین حالت نمایشی (دمو)
├── decisions/
│   ├── ADR-001-dashboard-structure.md
│   ├── ADR-002-kpi-definitions.md
│   ├── ADR-003-explanations-placement.md
│   └── ADR-004-map-and-geography.md
├── data-model/
│   ├── dimensions-and-facts.md
│   └── insurance-lines.md
└── dashboards/
    ├── 01-market-overview.md
    ├── 02-company-performance.md
    ├── 03-line-of-business.md
    ├── 04-claims-and-risk.md
    ├── 05-distribution-network.md
    └── 06-geographic-map.md
```

## وضعیت فعلی

- طراحی مفهومی و قوانین کامل شده است.
- نمونه‌های HTML تعاملی (حالت دمو) تولید شده‌اند.
- مدل داده بر اساس فایل Dimension & Fact و جداول تجمیعی موجود تعریف شده است.

## نحوه استفاده

1. ابتدا فایل‌های پوشه `harness/` را بخوانید (قوانین غیرقابل نقض).
2. سپس `docs/` را برای درک کنترل پروژه مطالعه کنید.
3. تصمیمات معماری در `decisions/` ثبت شده‌اند.
4. مشخصات هر داشبورد در `dashboards/` آمده است.
