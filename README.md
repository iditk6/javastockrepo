# javastockrepo (iditex)

פרויקט Java לתרגול קורס — אפליקציית ווב על **Google App Engine** (Eclipse).  
שם הפרויקט ב-Eclipse: `iditex`. מזהה האפליקציה ב-App Engine: `javaiditwein`.

## מה האפליקציה עושה

- דף הבית (`index.html`) מציג ברכה וקישור לתרגיל.
- ה-Servlet בכתובת `/iditex` מחשב `(4 + 3) * 7` ומציג את התוצאה ב-HTML.

## דרישות

- Java (JRE / JDK תואם לפרויקט ב-Eclipse)
- Eclipse עם Google Plugin for Eclipse / Google App Engine Java SDK
- Git (אופציונלי)

## מבנה הפרויקט

```
src/com/myorg/javacourse/IditexServlet.java   # Servlet ראשי
src/META-INF/persistence.xml                  # JPA (DataNucleus / App Engine)
src/META-INF/jdoconfig.xml                    # JDO
src/log4j.properties
war/index.html                                # דף פתיחה
war/WEB-INF/web.xml                           # מיפוי Servlet
war/WEB-INF/appengine-web.xml                 # הגדרות App Engine
war/WEB-INF/logging.properties
```

## הרצה מקומית

1. פתחו את הפרויקט ב-Eclipse כ-Google App Engine Web Application.
2. הרצה: **Run As → Web Application**.
3. בדפדפן:
   - דף הבית: `http://localhost:8888/`
   - תרגיל המתמטיקה: `http://localhost:8888/iditex`

## מיפוי Servlet

| נתיב     | מחלקה                               |
|----------|-------------------------------------|
| `/iditex` | `com.myorg.javacourse.IditexServlet` |

המיפוי מוגדר ב-`war/WEB-INF/web.xml`.

## פריסה (Deploy)

האפליקציה מוגדרת ב-`war/WEB-INF/appengine-web.xml`:

- Application ID: `javaiditwein`
- Version: `2`
- Threadsafe: מופעל

פריסה מ-Eclipse: **Google → Deploy to App Engine** (נדרש חשבון Google עם הרשאות לפרויקט).

## רישוי

לא צוין רישיון בקובץ זה.
