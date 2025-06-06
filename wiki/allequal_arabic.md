<!--
Meta Description: # الدالة all.equal في لغة R: مقارنة القيم بدقة ## الملخص الدالة `all.equal` في لغة R تُستخدم للمقارنة بين كائنين للتحقق مما إذا كانا متساويين بشكل تقر...
Meta Keywords: all, equal, الدالة, الأعداد, العائمة
-->

# الدالة all.equal في لغة R: مقارنة القيم بدقة

## الملخص
الدالة `all.equal` في لغة R تُستخدم للمقارنة بين كائنين للتحقق مما إذا كانا متساويين بشكل تقريبي، مما يجعلها مفيدة في التعامل مع الأعداد العائمة والبيانات ذات الدقة المتغيرة.

## الوثائق
### الغرض
تعتبر الدالة `all.equal` أداة قوية لتقييم ما إذا كانت كائنات R متساوية، مع الأخذ في الاعتبار بعض التسامحات التي قد تكون ضرورية عند التعامل مع الأعداد العائمة.

### الاستخدام
يمكن استخدام `all.equal` بشكل أساسي كالتالي:

```R
all.equal(target, current, ...)
```

- **target**: الكائن الأول الذي ترغب في مقارنته.
- **current**: الكائن الثاني الذي ترغب في مقارنته مع الأول.
- **...**: خيارات إضافية يمكن استخدامها لتخصيص المقارنة.

### التفاصيل
- تُرجع `all.equal` قيمة منطقية (TRUE) إذا كانت الكائنات متساوية، أو سلسلة نصية توضح الفرق بينهما إذا لم تكن كذلك.
- تعتمد الدالة على دقة الأعداد العائمة، حيث يمكن أن تختلف النتائج بسبب أخطاء التقريب. يتم استخدام معلمات مثل `tolerance` لتحديد مقدار الخطأ المقبول.

## الأمثلة
### مثال 1: مقارنة الأعداد العائمة
```R
x <- 0.1 + 0.2
y <- 0.3
all.equal(x, y)  # TRUE
```

### مثال 2: مقارنة القوائم
```R
list1 <- list(a = 1, b = 2)
list2 <- list(a = 1, b = 2)
all.equal(list1, list2)  # TRUE
```

### مثال 3: التعامل مع التسامح
```R
x <- 0.1 + 0.2
y <- 0.3
all.equal(x, y, tolerance = 1e-8)  # TRUE
```

## الشرح
### الأخطاء الشائعة
- **عدم الانتباه لدقة الأعداد العائمة**: قد تؤدي المقارنات المباشرة إلى نتائج غير صحيحة بسبب التقريب.
- **عدم استخدام المعاملات الإضافية**: في بعض الحالات، قد تحتاج إلى تخصيص الدالة لمراعاة خصائص البيانات.

### ملاحظات إضافية
- إذا كنت تعمل مع كائنات معقدة (مثل القوائم أو البيانات الإطارية)، تأكد من أن البنية متطابقة لضمان مقارنة صحيحة.

## ملخص في جملة واحدة
الدالة `all.equal` تُستخدم في R لمقارنة كائنين مع الأخذ في الاعتبار التسامحات المهمة خاصة عند العمل مع الأعداد العائمة.