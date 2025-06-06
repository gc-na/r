<!--
Meta Description: # all.equal.default في R: مقارنة الكائنات بدقة ## ملخص دالة `all.equal.default` في R تُستخدم لمقارنة كائنين (مثل القوائم أو المصفوفات) وتحديد ما إذا ك...
Meta Keywords: all, equal, default, مقارنة, الكائنات
-->

# all.equal.default في R: مقارنة الكائنات بدقة

## ملخص
دالة `all.equal.default` في R تُستخدم لمقارنة كائنين (مثل القوائم أو المصفوفات) وتحديد ما إذا كانا متساويين، مع مراعاة الأخطاء العائمة والاختلافات الطفيفة.

## الوثائق
### الغرض
تُعتبر `all.equal.default` أداة قوية في R لمقارنة الكائنات بطريقة تتسم بالمرونة، حيث تأخذ في الاعتبار الفروقات الصغيرة التي قد تحدث بسبب العمليات الحسابية. تُستخدم هذه الدالة عادةً في الاختبارات والبرمجة التفاعلية لضمان أن النتائج تتوافق مع التوقعات.

### الاستخدام
يمكن استخدام الدالة كالتالي:

```R
all.equal(target, current, ...)
```

#### المعاملات
- `target`: الكائن المرجعي (الذي يتم المقارنة معه).
- `current`: الكائن الحالي (الذي يتم مقارنته).
- `...`: معاملات إضافية يمكن تمريرها لتخصيص المقارنة، مثل `tolerance` لتحديد مستوى السماحية للاختلافات.

### التفاصيل
تقوم `all.equal.default` بإرجاع:
- `TRUE` إذا كان الكائنان متساويين.
- رسالة نصية توضح الاختلافات إذا لم يكونا متساويين.

تستخدم الدالة تقنيات مقارنة متقدمة لتحديد الفروقات، مما يجعلها مثالية للاستخدام في السيناريوهات التي تتطلب دقة عالية.

## الأمثلة
### مثال 1: مقارنة الأعداد
```R
x <- 0.1 + 0.2
y <- 0.3
all.equal(x, y)
# النتيجة: [1] "Mean relative difference: 1.11022302462516e-16"
```

### مثال 2: مقارنة القوائم
```R
list1 <- list(a = 1, b = 2)
list2 <- list(a = 1, b = 2)
all.equal(list1, list2)
# النتيجة: TRUE
```

### مثال 3: مقارنة المصفوفات مع اختلافات طفيفة
```R
matrix1 <- matrix(c(1, 2, 3, 4), nrow = 2)
matrix2 <- matrix(c(1, 2, 3, 4 + 1e-10), nrow = 2)
all.equal(matrix1, matrix2, tolerance = 1e-9)
# النتيجة: TRUE
```

## الشرح
- **الفخاخ الشائعة**: قد تؤدي المقارنات مع الأعداد العائمة إلى نتائج غير متوقعة بسبب دقة الأعداد. يُوصى باستخدام معامل `tolerance` لتحديد مستوى السماحية للاختلافات.
- **ملاحظات إضافية**: يجب الانتباه إلى أن الدالة تُرجع معلومات تفصيلية عند عدم تطابق الكائنات، مما يمكن أن يكون مفيدًا لتصحيح الأخطاء.

## ملخص جملة واحدة
`all.equal.default` هي دالة في R تستخدم لمقارنة الكائنات بدقة، مع مراعاة الفروقات الطفيفة.