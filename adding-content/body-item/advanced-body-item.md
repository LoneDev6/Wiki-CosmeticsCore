# פריט גוף מתקדם

{% hint style="warning" %}
### פריט גוף מתקדם דורש את ItemsAdder כדי לעבוד.
{% endhint %}

## יצירת הישות

### שלב 1

צור ישות ItemsAdder שקוראת את המדריך:

{% embed url="https://itemsadder.devs.beer/plugin-usage/adding-content/mobs/advanced-method/creation" %}

### שלב 2

צור את התצורה הקוסמטית

```yaml
  wings_enderdragon:
    display_name: "Enderdragon Wings"
    type: BODY_ENTITY
    model:
      gui: dragon_head
      normal: cosmetics:wings_enderdragon
    dye:
      enabled: false
```

כפי שאתה יכול לראות, הגדרתי את המודל ה'רגיל' לשם של **הישות המותאמת אישית** שנוצרה עם ItemsAdder.

### שלב 3

אתה סיימת

<figure><img src="../../.gitbook/assets/ezgif-4-5e5291072e.gif" alt=""><figcaption></figcaption></figure>

## הערות אחרונות

{% hint style="info" %}
אתה יכול אפילו ליצור מוצרי קוסמטיקה מונפשים, פשוט הנפשה את האנימציה הסרק של הישות באמצעות Blockbench.
{% endhint %}

## בעיות ידועות

{% hint style="warning" %}
### קוסמטיקה מושהית בזמן תנועה
זוהי בעיה ידועה ולא ניתן לתקן אותה, אך שימו לב שהתנהגות זו גלויה רק לשחקן הנוכחי.\


כל שאר השחקנים יראו את הקוסמטיקה מחוברת לשחקן עם פחות עיכוב.\
זה תלוי גם בפינג השחקן ובביצועי השרת.
{% endhint %}

{% tabs %}
{% tab title="תצוגת שחקן נוכחי" %}
{% embed url="https://youtu.be/TiR3SKT_JRE" %}
{% endtab %}

{% tab title="שחקנים אחרים רואים" %}
{% embed url="https://youtu.be/YGCt6RXiMRw" %}
{% endtab %}
{% endtabs %}
