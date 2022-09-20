# 🎈 Balloon

{% hint style="warning" %}
### Balloons require ItemsAdder to work.
{% endhint %}

## Creating a balloon

### Step 1

Create an ItemsAdder entity reading the tutorial:

{% embed url="https://itemsadder.devs.beer/plugin-usage/adding-content/mobs/advanced-method/creation" %}

### Step 2

Create the cosmetic configuration

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

As you can see I set the `normal` model to the name of the **custom entity** created with ItemsAdder.

### Step 3

You're done

![](<../.gitbook/assets/image (8) (1).png>)

## Final notes

{% hint style="info" %}
You can even create animated balloons, just animate the idle animation of the entity using Blockbench.\
For example you can create a complex dragon or a rotating UFO. &#x20;
{% endhint %}
