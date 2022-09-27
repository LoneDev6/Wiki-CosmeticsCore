# פריט גוף סטטי

## שיטות יצירה

### פריט גוף CustomModelData

אתה יכול ליצור פריטי גוף מותאמים אישית פשוט באמצעות CustomModelData.

```yaml
  # Example manually created hat with CustomModelData
  squirrel_tail:
    display_name: "Squirrel Tail"
    type: BODY_ITEM
    model:
      gui: potion:400008
      normal: potion:400008
      self: potion:400009
    dye:
      enabled: false
```

בדוגמה זו יצרתי פריט גוף מותאם אישית עם CustomModelData `400008`.\
החלטתי להשתמש באותו פריט הן עבור התצוגה המקדימה של ממשק המשתמש והן עבור הפריט בפועל אשר יוצב על גוף השחקן.\
לאחר מכן הגדרתי מודל עצמי, שהוא המודל המוצג רק לנגן המקומי ולא לשחקנים האחרים, במקרה זה הגדרתי את CustomModelData ל-`400009`.&#x20;

הגדרתי 'dyeable: false' כדי למנוע את צביעה של פריט זה

### דגם ItemsAdder

אתה יכול לעשות את אותו הדבר אבל עם דגמי פריטי ItemsAdder ולהימנע מדאגה לגבי CustomModelData.

דוגמא:

```yaml
  # Example manually created hat with CustomModelData
  squirrel_tail:
    display_name: "Squirrel Tail"
    type: BODY_ITEM
    model:
      gui: squirrel_tail
      normal: squirrel_tail
      self: squirrel_tail_self
    dye:
      enabled: false
```

בדוגמה זו יצרתי פריט גוף מותאם אישית על ידי שימוש במודל ItemsAdder בשם `squirrel_tail`.\
החלטתי להשתמש באותו פריט הן עבור התצוגה המקדימה של ממשק המשתמש והן עבור הפריט בפועל אשר יוצב על גוף השחקן.\
לאחר מכן הגדרתי מודל עצמי, שהוא המודל שמוצג רק לשחקן המקומי ולא לשחקנים האחרים, במקרה הזה הגדרתי אותו ל-`squirrel_tail_self`.

הגדרתי 'dyeable: false' כדי למנוע את צביעה של פריט זה.

## הימנע ממוצרי קוסמטיקה כדי לחסום את הנוף

{% content-ref url="normal-and-self-models.md" %}
[normal-and-self-models.md](normal-and-self-models.md)
{% endcontent-ref %}
