# מודלים רגילים ועצמיים

## מבוא

חשוב שיהיו שני דגמים נפרדים מכיוון שהמודל העצמי ימנע מהשגחת הראייה של השחקן על ידי הקוסמטיקה ועלול לגרום למטרדים במהלך המשחק (הצבת בלוקים, התקפה, הליכה).

{% tabs %}
{% tab title="בלי המודל העצמי" %}
![](../../../.gitbook/assets/2022-08-17\_17.47.53.png)

![](../../../.gitbook/assets/2022-08-17\_17.48.40.png)
{% endtab %}

{% tab title="עם המודל העצמי" %}
![](../../../.gitbook/assets/2022-08-17\_17.48.16.png)

![](../../../.gitbook/assets/2022-08-17\_17.48.40.png)
{% endtab %}
{% endtabs %}

{% hint style="warning" %}
אם אינך מעוניין להגדיר מודל 'עצמי' ו'רגיל', תוכל לדלג על הדרכה זו ולהשתמש רק בתכונה 'רגיל'\
אל תגדיר את התכונה 'עצמי' כלל אם אינך רוצה להשתמש בפריט אחר עבור התצוגה העצמית.
{% endhint %}

### דגם רגיל

מודל רגיל הוא המודל שמוצג לכל שחקן מלבד השחקן המקומי (בעצמך).

### מודל עצמי

מודל עצמי הוא המודל שמוצג רק לשחקן המקומי (בעצמך).

## יישום התיקון

### שלב 1

עליך ליצור עותק של קובץ המודל `.json` שלך, לשנות את שמו `_self.json`.\
לדוגמה: `squirrel_tail.json` -> `squirrel_tail_self.json`

### שלב 2

קבע **CustomModelData** חדש עבור פריט זה והוסף אותו לקובץ הפריט או השתמש ב-ItemAdder כדי להפוך את התהליך לאוטומטי (תלוי בצרכים שלך, עיין ב[ItemsAdder wiki ](https://itemsadder.devs.beer/) ל למד כיצד ליצור פריטים).

בדוגמה זו אני משתמש ב-`400008` עבור הדגם **רגיל** וב-`400009` עבור המודל **עצמי**.

`assets/minecraft/models/item/XXX.json`

```json
{
  "predicate": { "custom_model_data": 400008 },
  "model": "cosmetics:body/squirrel_tail"
},
{
  "predicate": { "custom_model_data": 400009 },
  "model": "cosmetics:body/squirrel_tail_self"
},
```

### שלב 3

ערוך את תצורת הקוסמטיקה שלך והוסף את דגם ה**עצמי**.

```yaml
  squirrel_tail:
    display_name: "Squirrel Tail"
    type: BODY_ITEM
    model:
      gui: potion:400008
      normal: potion:400008
      self: potion:400009   ### <------ HERE
    dye:
      enabled: false
```

### שלב 4

זה השלב החשוב ביותר, עליך לערוך את מודל ה**עצמי**.\
אתה צריך להזיז את הדגם למטה ככה, ואז לראות אותו במשחק עד שתהיה מרוצה מהתוצאה.

זה מחייב אותך לבדוק את המשחק מספר פעמים עד שהמודל ימוקם נכון, זה דורש כמה ניסיונות להשיג את המיקום המושלם, אבל אתה יכול בקלות להשתמש בכמה מהדגמים לדוגמה כדי למנוע אובדן זמן.vi

{% embed url="https://youtu.be/dmQI35Xd4Js" %}

## הבדלים

### דגם רגיל

![](<../../../.gitbook/assets/image (23).png>)

### מודל עצמי

![](<../../../.gitbook/assets/image (10).png>)

## בעיות עם דגמים גדולים

&#x20;קרא כאן אם אינך יכול להזיז את הדגם למטה מכיוון שהדגם שלך גדול מדי.

<figure><img src="../../../.gitbook/assets/move_down_problem.gif" alt=""><figcaption></figcaption></figure>

## גרסת וידאו

{% embed url="https://youtu.be/WBImTCMOZNA" %}

## גרסת טקסט

### שלב 1

בחר את כל הקוביות בדגם שלך (לחץ על כל קובייה ברשימה והקש CTRL+A).

### שלב 2

לחץ על **טרנספורמציה** (בחלק העליון) -> **קנה מידה**.

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

### שלב 3

הגדר את הסולם ל-'0.5' או כל ערך נמוך (בהתבסס על הדגם שלך, אתה צריך לעשות כמה בדיקות).

<figure><img src="../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

### שךב 4

הזז את הפריט למטה בתצוגת העריכה.

### שלב 5

כעת פתח את לשונית התצוגה, לחץ על הסמלים ArmorStand ו-HEAD ולאחר מכן הזז אותו למטה.\
לאחר מכן הכפיל את ערך הסולם.\
לדוגמה, אם ערך קנה המידה היה `1.3`, עליך להגדיר אותו ל-`2.6`.

### תוצאה

<div>

<figure><img src="../../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

 

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

</div>
