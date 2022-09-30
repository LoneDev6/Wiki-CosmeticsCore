# Static Body Item

## Creation methods

### CustomModelData body item

You can create custom body items simply by using CustomModelData.

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

In this example I created a custom body item with CustomModelData `400008`.\
I decided to use the same item both for the GUI preview and for the actual item which will be put on player's body.\
I then set a self model, which is the model shown only to the local player and not to the other players, in this case I set the CustomModelData to `400009`.&#x20;

I set the `dye.enabled` option to `false` to avoid this item from being colored.

```yaml
    dye:
      enabled: false
```

### ItemsAdder model

You can do the same thing but with ItemsAdder items models and avoid worrying about CustomModelData.

Example:

```yaml
  # Example custom Item created by ItemsAdder
  squirrel_tail:
    display_name: "Squirrel Tail"
    type: BODY_ITEM
    model:
      gui: my_item:squirrel_tail
      normal: my_item:squirrel_tail
      self: my_item:squirrel_tail_self
    dye:
      enabled: false
```

In this example I created a custom body item by using the ItemsAdder model named `squirrel_tail`.\
I decided to use the same item both for the GUI preview and for the actual item which will be put on player's body.\
I then set a self model, which is the model shown only to the local player and not to the other players, in this case I set it to `squirrel_tail_self`.

I set the `dye.enabled` option to `false` to avoid this item from being colored.

```yaml
    dye:
      enabled: false
```

## Avoid cosmetics from obstructing view

{% content-ref url="normal-and-self-models.md" %}
[normal-and-self-models.md](normal-and-self-models.md)
{% endcontent-ref %}
