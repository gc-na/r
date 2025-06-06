<!--
Meta Description: # دالة ifelse في لغة R: دليل شامل ## ملخص تعتبر دالة `ifelse` في لغة R من الأدوات الأساسية للتحكم في التدفق، حيث تتيح للمستخدمين اتخاذ قرارات بناءً عل...
Meta Keywords: ifelse, البيانات, دالة, على, إذا
-->

# دالة ifelse في لغة R: دليل شامل

## ملخص
تعتبر دالة `ifelse` في لغة R من الأدوات الأساسية للتحكم في التدفق، حيث تتيح للمستخدمين اتخاذ قرارات بناءً على شرط معين، مما يسهل تنفيذ العمليات الشرطية في تحليل البيانات.

## الوثائق
### الغرض
تستخدم دالة `ifelse` لتطبيق شرط على مجموعة من القيم، حيث تعيد قيمة معينة إذا كان الشرط صحيحًا، وقيمة أخرى إذا كان الشرط خاطئًا. هذه الدالة مفيدة في معالجة البيانات وتحليلها، خاصة عند الحاجة إلى اتخاذ قرارات مبنية على قيم متغيرة.

### الاستخدام
تأتي دالة `ifelse` بالصيغة التالية:

```R
ifelse(test, yes, no)
```

- **test**: شرط منطقي يتم اختباره. يمكن أن يكون عبارة عن تعبير يعود بقيم TRUE أو FALSE.
- **yes**: القيمة التي يتم إرجاعها إذا كان الشرط صحيحًا (TRUE).
- **no**: القيمة التي يتم إرجاعها إذا كان الشرط خاطئًا (FALSE).

### التفاصيل
- يمكن أن تكون المدخلات `test` و`yes` و`no` مصفوفات أو قوائم. يجب أن تكون جميعها بنفس الطول أو قابلة للبث (broadcasting).
- تعمل `ifelse` بطريقة فعالة على مصفوفات البيانات، مما يجعلها مثالية لتحليل البيانات الكمية والنوعية.

## أمثلة
### مثال 1: استخدام ifelse مع أرقام
```R
x <- c(1, 2, 3, 4, 5)
y <- ifelse(x %% 2 == 0, "زوجي", "فردي")
print(y)
```
**الناتج**: "فردي" "زوجي" "فردي" "زوجي" "فردي"

### مثال 2: استخدام ifelse مع بيانات من إطار بيانات
```R
data <- data.frame(score = c(80, 55, 90, 70))
data$pass <- ifelse(data$score >= 60, "ناجح", "راسب")
print(data)
```
**الناتج**:
```
  score   pass
1    80 ناجح
2    55 راسب
3    90 ناجح
4    70 ناجح
```

## الشرح
### الأخطاء الشائعة
- التأكد من أن الأطوال متساوية: إذا كانت المدخلات `test` و`yes` و`no` بطول مختلف، ستظهر رسالة خطأ.
- استخدام التعبيرات المعقدة: يُفضل استخدام شروط بسيطة لزيادة وضوح الكود وسهولة القراءة.

### ملاحظات إضافية
- يمكن استخدام `ifelse` في تحليل البيانات الكبيرة دون الحاجة إلى حلقات، مما يحسن الأداء.
- يمكن أن تكون `ifelse` بديلاً جيدًا لدالة `if` التقليدية في حالات معينة، لكن يجب استخدامها بحذر لتجنب تعقيد الكود.

## ملخص من جملة واحدة
تتيح دالة `ifelse` في R اتخاذ قرارات شرطية فعالة على مجموعات البيانات، مما يسهل تحليل البيانات وإجراء العمليات الشرطية.