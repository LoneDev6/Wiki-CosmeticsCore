# 🧢 Hat

## CustomModelData hat

You can create custom hats simply by using CustomModelData.

```yaml
  # Example manually created hat with CustomModelData
  cowboy_hat:
    display_name: "Cowboy Hat"
    type: HAT
    model:
      gui: potion:300003
      normal: potion:300003
    dye:
      enabled: false # To avoid this item from being colored.
```

In this example I created a custom hat with CustomModelData `300003`.\
I decided to use the same item both for the GUI preview and for the actual item which will be put on player's head.&#x20;

## ItemsAdder model

You can do the same thing but with ItemsAdder items models and avoid worrying about CustomModelData.

Example:

```yaml
  # Example manually created hat with CustomModelData
  cowboy_hat:
    display_name: "Cowboy Hat"
    type: HAT
    model:
      gui: my_items:cowboy_hat_icon
      normal: my_items:cowboy_hat
    dye:
      enabled: false # To avoid this item from being colored.
```

In this example you can see I used `my_items:cowboy_hat_icon` as icon `my_items:cowboy_hat` as item.\
They both are items from ItemsAdder.
