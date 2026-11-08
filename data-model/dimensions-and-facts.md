# مدل ابعاد و حقایق (Dimension & Fact)

## منبع

فایل `Dimension & Fact.xlsx` و جداول نمونه تجمیعی (`Agg*PolicyTb` / `Agg*LossTb`).

## رشته‌ها و دیتابیس‌ها

| رشته | دیتابیس تقریبی |
|------|----------------|
| ثالث | CarThirdPartyDb |
| بدنه | CarBodyDb |
| آتش‌سوزی | FirePolicyDb |
| مشترکات | CommonPolicyDb |
| عمر | CIConvertData / Life |
| باربری | CrgDb |

## ابعاد مشترک مهم

- CompanyId
- IssueDate / YearNo / MonthNo
- AgencyId
- BranchId
- BrokerId
- CityId / Province
- VehicleGroupId (در رشته‌های خودرویی)

## حقایق (Facts) کلیدی

| شاخص | عملیات معمول | منبع نمونه |
|------|---------------|------------|
| تعداد بیمه‌نامه | COUNT(Id) | Policy tables / Agg*PolicyTb |
| حق‌بیمه | SUM(Premium / Prm) | Policy |
| سرمایه | SUM(Capital) | Policy |
| تعداد پرونده خسارت | COUNT | LossDocument / Agg*LossTb |
| مبلغ خسارت پرداختی | SUM(PayAmount / TotalLoss) | Loss |
| تعداد حواله خسارت | COUNT | Loss |

## جداول تجمیعی موجود در نمونه

- AggCarBodyPolicyTb / AggCarBodyLossTb
- AggCarThirdPartyPolicyTb / AggCarThirdPartyLossTb
- AggFirePolicyTb / AggFireLossTb
- AggLifePolicyTb / AggLifeLossTb
- AggCargoPolicyTb / AggCargoLossTb
- AggCommonPolicyTb / AggCommonLossTb

این جداول پایه اصلی برای KPIهای ماهانه و مقایسه‌ای هستند.
