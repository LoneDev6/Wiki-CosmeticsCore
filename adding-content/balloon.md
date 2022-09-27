# 🎈 בלון

{% hint style="warning" %}
### בלונים דורשים את ItemsAdder כדי לעבוד.
{% endhint %}

## יצירת בלון

### שלב 1

צור ישות ItemsAdder שקוראת את המדריך:

{% embed url="https://itemsadder.devs.beer/plugin-usage/adding-content/mobs/advanced-method/creation" %}

### שלב 2

צור את התצורה הקוסמטית

```yaml
  # Example custom kite created with ItemsAdder entities 
  # (supports also animated ItemsAdder entities models)
  star_kite:
    display_name: "Star Kite"
    type: BALLOON_ENTITY
    # Showing a different item into the GUI 
    # (in this case it's a must because ItemsAdder entities can't be put in GUIs)
    model:
      gui: minecraft:egg
      normal: cosmetics:star_kite
    dye:
      enabled: true
```
כפי שאתה יכול לראות, הגדרתי את המודל ה'רגיל' לשם של **הישות המותאמת אישית** שנוצרה עם ItemsAdder.

### שלב 3

אתה סיימת

![](<../.gitbook/assets/image (8) (1).png>)

## הערות אחרונות

{% hint style="info" %}
אתה יכול אפילו ליצור בלונים מונפשים, פשוט הנפשה את הנפשה סרק של הישות באמצעות Blockbench.\
לדוגמה אתה יכול ליצור דרקון מורכב או עב"ם מסתובב. &#x20;
{% endhint %}
