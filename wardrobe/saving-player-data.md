# שמירת נתוני שחקן

## תצורה

```yaml
save:
  # Use only one at a time
  file:
    enabled: true
  mysql:
    enabled: false
    url: "jdbc:mysql://my_url_database_69.com:3306/database_name"
    username: "username"
    password: "password"
    table: "cosmeticscore_saved"
```

## קובץ

זוהי שיטת ברירת המחדל, היא משתמשת בקובץ ארון בגדים עבור כל שחקן.

## MySQL

זו השיטה המשמשת רשתות, זה מאפשר לך להחזיק מספר שרתים המשתמשים באותם נתוני ארון בגדים עבור כל שחקן. אז לשחקנים שלך יהיו אותם פריטים מצוידים בעת נסיעה ברשת שלך.\
(זה כמובן מחייב אותך להגדיר את הפלאגין בכל שרת עם אותם קבצי קוסמטיקה).
