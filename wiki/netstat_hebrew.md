# [לינוקס] C Shell (csh) netstat שימוש: הצגת חיבורי רשת וסטטיסטיקות

## Overview
הפקודה `netstat` משמשת להצגת חיבורי רשת פעילים, סטטיסטיקות רשת ומידע נוסף על פרוטוקולי תקשורת במערכת. היא מאפשרת למשתמשים להבין את מצב הרשת שלהם ולזהות בעיות פוטנציאליות.

## Usage
התחביר הבסיסי של הפקודה הוא:
```
netstat [options] [arguments]
```

## Common Options
- `-a`: מציג חיבורים פעילים ופורט פתוח.
- `-n`: מציג כתובות IP במקום שמות מארחים.
- `-r`: מציג את טבלת הניתוב של המערכת.
- `-t`: מציג חיבורים TCP בלבד.
- `-u`: מציג חיבורים UDP בלבד.

## Common Examples
- הצגת כל החיבורים והפורט הפתוח:
  ```csh
  netstat -a
  ```

- הצגת חיבורים TCP עם כתובות IP:
  ```csh
  netstat -tn
  ```

- הצגת טבלת הניתוב:
  ```csh
  netstat -r
  ```

- הצגת חיבורים UDP:
  ```csh
  netstat -u
  ```

## Tips
- השתמש באופציה `-n` כדי להאיץ את התצוגה, במיוחד במערכות עם הרבה חיבורים.
- ניתן לשלב מספר אופציות יחד, לדוגמה `netstat -at` כדי לראות חיבורים פעילים של TCP בלבד.
- כדאי לבדוק את הפקודה באופן קבוע כדי לעקוב אחרי שינויים בחיבורי הרשת שלך.