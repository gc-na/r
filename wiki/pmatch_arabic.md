<!--
Meta Description: # الدالة pmatch في لغة R: المطابقة الجزئية للعناصر ## ملخص تعتبر الدالة `pmatch` في لغة R أداة فعالة للمطابقة الجزئية بين العناصر، حيث تُستخدم لمطابقة...
Meta Keywords: pmatch, الدالة, result, table, المطابقة
-->

# الدالة pmatch في لغة R: المطابقة الجزئية للعناصر

## ملخص
تعتبر الدالة `pmatch` في لغة R أداة فعالة للمطابقة الجزئية بين العناصر، حيث تُستخدم لمطابقة سلاسل نصية مع مجموعة من الخيارات وتُعيد موضع العنصر المطابق.

## الوثائق
تُستخدم الدالة `pmatch` لأغراض المطابقة الجزئية، مما يسمح للمستخدمين بالبحث عن تطابقات نصية غير كاملة. تعد هذه الدالة مفيدة بشكل خاص عند التعامل مع البيانات النصية، مثل أسماء المتغيرات أو القيم في إطار البيانات.

### الاستخدام
```R
pmatch(x, table, nomatch = NA_integer_, duplicates.ok = FALSE)
```

### المعاملات
- `x`: سلسلة نصية أو مجموعة من السلاسل النصية التي ترغب في مطابقتها.
- `table`: مجموعة من السلاسل النصية التي سيتم المطابقة معها.
- `nomatch`: قيمة تُعاد إذا لم يتم العثور على تطابق. القيمة الافتراضية هي `NA_integer_`.
- `duplicates.ok`: إذا كانت `TRUE`، فإن الدالة ستسمح بتطابقات مزدوجة في `table`.

## أمثلة
### مثال 1: مطابقة بسيطة
```R
# مجموعة من الأسماء
names <- c("حسن", "علي", "فاطمة", "سلمى")

# استخدام pmatch للبحث عن "علي"
result <- pmatch("علي", names)
print(result)  # النتيجة ستكون 2، حيث أن "علي" هو العنصر الثاني
```

### مثال 2: عدم وجود تطابق
```R
# محاولة مطابقة اسم غير موجود
result <- pmatch("محمد", names)
print(result)  # النتيجة ستكون NA، لأنه لا يوجد تطابق
```

### مثال 3: تحديد قيمة عدم المطابقة
```R
result <- pmatch("محمد", names, nomatch = -1)
print(result)  # النتيجة ستكون -1، كما تم تحديدها
```

## الشرح
عند استخدام `pmatch`، يجب الانتباه إلى بعض النقاط:
- الدالة تقوم بمطابقة النصوص بناءً على أول تطابق جزئي. لذا، إذا كان لديك عناصر في `table` تبدأ بنفس الحروف، فقد يحدث أن تعود الدالة بأحدها فقط.
- إذا كانت `duplicates.ok` مُعينة على `FALSE`، ووجدت الدالة تطابقات متعددة، ستعيد `NA` بدلاً من ذلك.
- تأكد من أن البيانات في `x` و `table` متجانسة من حيث نوع البيانات، حيث يمكن أن تؤدي الأنواع المختلفة إلى نتائج غير دقيقة.

## ملخص جملة واحدة
تعتبر الدالة `pmatch` في R أداة قوية للمطابقة الجزئية للنصوص، مما يسهل البحث عن العناصر في القوائم.