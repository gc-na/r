<!--
Meta Description: # تصفية البيانات في R: كيفية استخدام الدالة Filter ## ملخص تعتبر دالة `Filter` في R أداة قوية لتصفية البيانات بناءً على شروط محددة. يمكن استخدامها لتح...
Meta Keywords: filter, البيانات, على, دالة, بيانات
-->

# تصفية البيانات في R: كيفية استخدام الدالة Filter

## ملخص
تعتبر دالة `Filter` في R أداة قوية لتصفية البيانات بناءً على شروط محددة. يمكن استخدامها لتحديد عناصر معينة من قائمة أو بيانات إطار (data frame) بناءً على دالة شرطية.

## التوثيق
### الغرض
تستخدم دالة `Filter` لتصفية العناصر في قائمة أو بيانات إطار في R، حيث تقوم بإرجاع العناصر التي تحقق شرطًا معينًا.

### الاستخدام
تكون الصيغة العامة لدالة `Filter` كما يلي:
```R
Filter(f, x)
```
- **f**: دالة تأخذ عنصرًا واحدًا (مثل قيم قائمة) وتعيد TRUE أو FALSE بناءً على شرط معين.
- **x**: القائمة أو بيانات الإطار التي ترغب في تصفيتها.

### التفاصيل
تقوم دالة `Filter` بتطبيق الدالة المعطاة `f` على كل عنصر في `x`. إذا كانت النتيجة TRUE، يتم الاحتفاظ بالعنصر، وإذا كانت FALSE، يتم تجاهله. يمكن استخدام `Filter` مع أي نوع من البيانات، بما في ذلك القوائم، بيانات الإطار، والمصفوفات.

## أمثلة
### مثال 1: تصفية قائمة
```R
# قائمة من الأرقام
numbers <- c(1, 2, 3, 4, 5, 6)

# تصفية الأرقام الزوجية
even_numbers <- Filter(function(x) x %% 2 == 0, numbers)
print(even_numbers)  # الناتج: 2 4 6
```

### مثال 2: تصفية بيانات إطار
```R
# إنشاء بيانات إطار
df <- data.frame(name = c("علي", "فاطمة", "محمد"), age = c(25, 30, 22))

# تصفية الأشخاص فوق 24 سنة
adults <- Filter(function(x) x$age > 24, df)
print(adults)  # الناتج: الصفوف التي تحتوي على فاطمة
```

## الشرح
### الأخطاء الشائعة
- **عدم استخدام دالة شرطية صحيحة**: يجب التأكد من أن الدالة المستخدمة في `Filter` تعيد TRUE أو FALSE. إذا لم يتم ذلك، فإن النتيجة قد تكون غير متوقعة.
- **تصفية البيانات غير المتوافقة**: يجب أن يكون نوع البيانات في `x` ملائمًا لدالة `f`. على سبيل المثال، إذا كانت `f` تتوقع عددًا صحيحًا، فلا يمكن تمرير نصوص إليها.

### ملاحظات إضافية
- يمكن استخدام دوال مثل `sapply` أو `lapply` كبدائل لـ `Filter`، لكن `Filter` توفر طريقة أكثر مباشرة لتصفية البيانات.
- عند استخدام `Filter` مع بيانات إطار، يجب أن تكون الدالة المستخدمة قادرة على التعامل مع صفوف البيانات بشكل صحيح.

## ملخص جملة واحدة
تعتبر دالة `Filter` في R أداة فعالة لتصفية العناصر بناءً على شروط محددة، مما يسهل معالجة البيانات وتحليلها بشكل أكثر دقة.