<!--
Meta Description: # تحويل كائنات POSIXlt إلى قائمة في R: as.list.POSIXlt ## ملخص `as.list.POSIXlt` هي دالة في لغة البرمجة R تستخدم لتحويل كائنات الزمن من نوع POSIXlt إل...
Meta Keywords: posixlt, إلى, قائمة, list, السنة
-->

# تحويل كائنات POSIXlt إلى قائمة في R: as.list.POSIXlt

## ملخص
`as.list.POSIXlt` هي دالة في لغة البرمجة R تستخدم لتحويل كائنات الزمن من نوع POSIXlt إلى قائمة، مما يسهل الوصول إلى مكونات الزمن الفردية.

## الوثائق
تُستخدم دالة `as.list.POSIXlt` لتحويل كائنات الزمن التي تمثل التواريخ والأوقات في R من نوع POSIXlt إلى قائمة. يتيح هذا التحويل للمستخدمين الوصول بسهولة إلى مكونات التاريخ والوقت مثل السنة، والشهر، واليوم، والساعة، والدقيقة، والثانية.

### الاستخدام
```R
as.list.POSIXlt(x)
```
- **x**: كائن من نوع POSIXlt.

### التفاصيل
عند استخدام `as.list.POSIXlt`، يتم تحويل كائن POSIXlt إلى قائمة حيث تتضمن العناصر:
- `$sec`: الثواني.
- `$min`: الدقائق.
- `$hour`: الساعات.
- `$mday`: اليوم من الشهر.
- `$mon`: الشهر (0-11).
- `$year`: السنة (من 1900).
- `$wday`: اليوم من الأسبوع (0-6، حيث الأحد هو 0).
- `$yday`: اليوم من السنة (0-365).
- `$isdst`: حالة التوقيت الصيفي (TRUE أو FALSE).

## الأمثلة
### مثال 1: تحويل كائن POSIXlt إلى قائمة
```R
# إنشاء كائن POSIXlt
time_object <- as.POSIXlt("2023-10-01 12:00:00")
# تحويله إلى قائمة
time_list <- as.list.POSIXlt(time_object)
print(time_list)
```

### مثال 2: الوصول إلى مكونات الزمن
```R
# الوصول إلى السنة والشهر
year <- time_list$year + 1900  # إضافة 1900 إلى السنة
month <- time_list$mon + 1      # إضافة 1 للشهر
cat("السنة:", year, "الشهر:", month)
```

## الشرح
عند استخدام `as.list.POSIXlt`، يجب الانتباه إلى أن مكونات السنة والشهر تبدأ من 0. لذا، يجب إضافة 1900 إلى قيمة السنة و1 إلى قيمة الشهر للحصول على القيم الصحيحة. كما أن البيانات الناتجة من الدالة هي قائمة، مما يعني أنه يمكن الوصول إلى كل عنصر من خلالها بسهولة، ولكن يجب أن تكون على دراية بالهيكل الداخلي للبيانات.

## ملخص جملة واحدة
دالة `as.list.POSIXlt` في R تُستخدم لتحويل كائنات الزمن من نوع POSIXlt إلى قائمة، مما يتيح الوصول السهل إلى مكوناته.