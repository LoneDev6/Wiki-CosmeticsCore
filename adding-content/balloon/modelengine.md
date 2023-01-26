# ModelEngine

{% hint style="warning" %}
### This balloons type require ModelEngine to work.
{% endhint %}

## Creating a balloon

### Step 1

Create an ModelEngine entity, read the ModelEngine tutorials on their wiki (if available).\
Note that I'm not its developer.

### Step 2

Create the cosmetic configuration

```yaml
  # Example custom kite created with ItemsAdder entities 
  # (supports also animated ItemsAdder entities models)
  star_kite:
    display_name: "Star Kite"
    type: MEG_BALLOON_ENTITY
    # Showing a different item into the GUI 
    # (in this case it's a must because ModelEngine entities can't be put in GUIs)
    model:
      gui: minecraft:egg
      normal: star_kite
    dye:
      enabled: true # To allow this item from being colored.
```

As you can see I set the `normal` model to the name of the **custom entity** created with ModelEngine.

### Step 3

You're done

![](<../../.gitbook/assets/image (8) (1).png>)

## Final notes

{% hint style="info" %}
You can even create animated balloons, just animate the idle animation of the entity using Blockbench.\
For example you can create a complex dragon or a rotating UFO. &#x20;
{% endhint %}

## Leash location

{% content-ref url="leash-location.md" %}
[leash-location.md](leash-location.md)
{% endcontent-ref %}
