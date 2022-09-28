# התקן את חבילת המשאבים הבסיסית

**CosmeticsCore** משתמש בחבילת משאבים כדי לעבוד.\
החבילה כוללת גם את ה-GUI וממשקי UI שונים שהם חובה כדי שהפלאגין יפעל.

הוא מציע גם סט של מוצרי קוסמטיקה לדוגמה שתוכל להתקין אם תרצה בהם.

## התקנה

פתח את קובץ ה-zip שניתן למצוא כאן: `plugins/CosmeticsCore/default_assets.zip`

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

תיקיות:

* `Resourcepack` -> מכיל את חבילת המשאבים עם כל המודלים/טקסטורות
* `ItemsAdder_configurations` -> מכיל את תצורות (היצורים) הבלונים **ItemsAdder**
* `CosmeticsCore_configurations` -> מכיל את תצורת ברירת המחדל של מוצרי קוסמטיקה **CosmeticsCore**

## התקנת חבילת המשאבים <mark style="color:orange;">אם כבר יש לך חבילת משאבים מותאמת אישית</mark>

{% hint style="warning" %}
לקרוא [כאן](install-base-resourcepack.md#installing-the-resource-pack-if-you-dont-have-a-resourcepack) אם אין לך חבילת משאבים.
{% endhint %}

אם כבר יש לך ערכת משאבים מותאמת אישית בשרת שלך, עליך למזג את הדברים **CosmeticsCore** ואת מוצרי ברירת המחדל (אופציונליים).

### שלב 1

להעתיק `assets/z_cosmetics` ו `assets/cosmetics` תיקייה לתוך חבילת המשאבים שלך.

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

### שלב 2

פתח את הקובץ `assets/minecraft/models/item/fermented_spider_eye.json` עם העורך האהוב עליך (לדוגמא: **VSCode**) ואל תסגור אותו (הקובץ נמצא בתוך ה-zip).

<figure><img src="../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

### שלב 3

פתח את אותו נתיב קובץ קודם בחבילת המשאבים **שלך** (`fermented_spider_eye.json`).

הערה: אם אין לך את הקובץ הזה בחבילת המשאבים שלך דלג על שלב זה ופשוט העתק והדבק את הקובץ `fermented_spider_eye.json` בתוך ערכת המשאבים שלך לנתיב זה`assets/minecraft/models/item/fermented_spider_eye.json` .\\

השתמש בכלי זה כדי למזג את הקובץ **CosmeticsCore** והקובץ שלך:

{% embed url="https://itemsadder.github.io/jsonmerger/" %}

{% hint style="info" %}
`Json 1` הוא קובץ ה-json שלך, `Json 2` הוא קובץ ה-json `CosmeticsCore`.

התוצאה json היא זו שתצטרך להחליף בחבילה שלך.
{% endhint %}

כעת העתק את התוצאה json והדבק אותה בקובץ ה-json הישן שלך.

### שלב 4

בצע את אותם השלבים הקודמים עבור `potion.json`.

## התקנת חבילת המשאבים אם <mark style="color:orange;">אין</mark> לך חבילת משאבים

### שלב 1

חלץ את תיקיית 'Resourcepack' מקובץ ה-zip לכל תיקיה במחשב שלך.

### שלב 2

דחוס את התיקיה 'Resourcepack' תוכן (אל תדחס את התיקיה עצמה).\
בחר את כל הקבצים ודחס אותם.

<figure><img src="../.gitbook/assets/select.gif" alt=""><figcaption></figcaption></figure>

### שלב 3

כעת החליטו על דרך לארח את חבילת המשאבים שלכם, בדרך כלל תשתמשו ב-**Dropbox** וב-`server.properties`. בצע מחקר מקוון כיצד לארח חבילות משאבים.

## התקנת תצורת ברירת המחדל של מוצרי קוסמטיקה

פתח את קובץ ה-zip שניתן למצוא כאן: `plugins/CosmeticsCore/default_assets.zip` .

העתק את התוכן של `CosmeticsCore_configurations` לתיקיית הפלאגין `CosmeticsCore` שלך.

טען מחדש את התוסף באמצעות `/cosmeticsconfig cosmetics reload` .

## הסרת ברירת המחדל של מוצרי הקוסמטיקה

אם אתה לא צריך את ברירת המחדל של מוצרי הקוסמטיקה ואתה צריך רק את ממשק המשתמש, עליך למחוק את התיקיה הזו מהחבילה שלך: `asses/cosmetics/`

{% hint style="warning" %}
#### חשוב: לא למחוק `assets/z_cosmetics/`
{% endhint %}
