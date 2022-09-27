# 🧢 כובע

## כובע CustomModelData

אתה יכול ליצור כובעים מותאמים אישית פשוט באמצעות CustomModelData.

```yaml
  # Example manually created hat with CustomModelData
  cowboy_hat:
    display_name: "Cowboy Hat"
    type: HAT
    model:
      gui: potion:300003
      normal: potion:300003
    dye:
      enabled: false
```

בדוגמה זו יצרתי כובע מותאם אישית עם CustomModelData `300003`.\
החלטתי להשתמש באותו פריט הן עבור התצוגה המקדימה של GUI והן עבור הפריט בפועל אשר יונח על ראשו של השחקן.&#x20;

I set `dyeable: false` כדי למנוע צביעה של פריט זה.

## דגם ItemsAdder

אתה יכול לעשות את אותו הדבר אבל עם דגמי פריטי ItemsAdder ולהימנע מדאגה לגבי CustomModelData.

דוגמא:

```yaml
  # Example manually created hat with CustomModelData
  cowboy_hat:
    display_name: "Cowboy Hat"
    type: HAT
    model:
      gui: my_items:cowboy_hat_icon
      normal: my_items:cowboy_hat
    dye:
      enabled: false
```

בדוגמה זו אתה יכול לראות שהשתמשתי ב-'my_items:cowboy_hat_icon' כסמל 'my_items:cowboy_hat' כפריט.\
שניהם פריטים מ-ItemsAdder.

I set `dyeable: false` כדי למנוע צביעה של פריט זה.
