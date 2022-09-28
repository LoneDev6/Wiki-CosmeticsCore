# התאמה אישית

## תצורה

<details>

<summary>Config.yml</summary>

{% code title="config.yml" %}
```yaml
wardrobe_room:
  camera:
    rotation:
      enabled: true
    zoom:
      enabled: true
      min: 2
    fade_effect: true
    location:
      world: flat
      x: 205
      y: -58.5
      z: 41
      yaw: 359.85
      pitch: 6.6
  mannequin:
    location:
      world: flat
      x: 204.5
      y: -60
      z: 45.5
      yaw: 180
      pitch: 0
  teleport_area:
    enter:
      world: flat
      pos1:
        x: 167
        y: -61
        z: 42
      pos2:
        x: 167
        y: -57
        z: 37
    exit_location:
      world: flat
      x: 164
      y: -60
      z: 40
      yaw: 98
      pitch: 10
```
{% endcode %}

</details>

## מיקומים

אתה צריך לקבוע את העולם ואת הקואורדינטות שלו, אתה יכול גם להגדיר את סיבובים והגובה.\
כדי לקבל ערכים אלה פשוט השתמש בפקודה `/coords` של **Essentials** או השתמש ב-F3\`.

### מיקום המצלמה

פקודה: `/cosmeticsconfig config set camera-location`

![](<../.gitbook/assets/image (18).png>)

### מיקום בובות הראווה

פקודה: `/cosmeticsconfig config set mannequin-location`

מיקום השחקן לתצוגה מקדימה של מוצרי הקוסמטיקה בארון הבגדים.

![](<../.gitbook/assets/image (19).png>) ![](<../.gitbook/assets/image (8) (1).png>)

### אזור שיגור

זה קצת שונה, אתה צריך להגדיר שתי נקודות שמייצגות את האזור אליו השחקן יכול להיכנס כדי לפתוח את הארון.

פקודה: `/cosmeticsconfig config set door-area-locations`

![](<../.gitbook/assets/image (13).png>)

### יציאה ממיקום

פקודה: `/cosmeticsconfig config set exit-location`

מיקום שבו השחקן יועבר בשיגור חזרה כאשר הוא עוזב את הארון.

![](<../.gitbook/assets/image (22).png>)

## הגדרות מצלמה אחרות

{% code title="" %}
```yaml
  camera:
    rotation:
      enabled: true
    zoom:
      enabled: true
      min: 2
    fade_effect: true
```
{% endcode %}

* **סיבוב**: הגדר אם אתה רוצה ששחקנים יוכלו לסובב את התצוגה המקדימה
* **זום**: הגדר אם ברצונך להפעיל זום
* **אפקט דהייה**: הגדר אם ברצונך להפעיל את הנפשת דהיית מסך שחור בכניסה ליציאה מהארון.

## התאמה אישית של גרפיקה

```yaml
    slots:
      colors:
        not_owned: 195,147,57
        owned: 56,67,100
        wearing: 57,70,195
        wearing_preview: 195,120,57
        max_amount_reached: 111,111,111
```

{% hint style="warning" %}
#### Warning

הצבעים חייבים להיות צבעי RGB int מופרדים בפסיק, אתה יכול לקבל אותם מכל בוחר צבעים.\
צבעי HEX ומספר שלם אינם נתמכים לעת עתה.
{% endhint %}

מאפיינים אלה משמשים לקביעת הצבעים של החריצים ב-GUI של הארון.

![](<../.gitbook/assets/image (3) (1).png>)

* **לא בבעלות**: צבע מוצרי הקוסמטיקה לא בבעלות (ללא רשות)
* **בבעלות**: צבע מוצרי הקוסמטיקה שבבעלות (ברשות)
* **לבישה**: צבע הקוסמטיקה המצוידת כעת
* **לבישה** תצוגה מקדימה: צבע מוצרי הקוסמטיקה המצוידים כעת אך אינם בבעלותם (ללא רשות), מצויד רק כתצוגה מקדימה
* **הכמות המקסימלית שהושגה**: צבע של כל מוצרי הקוסמטיקה האחרים שלא ניתן לצייד מכיוון שהשחקן כבר לובש את הכמות המקסימלית עבור אותה קטגוריה
