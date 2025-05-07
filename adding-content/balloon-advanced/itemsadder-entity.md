# ItemsAdder Entity

{% hint style="warning" %}
### This requires ItemsAdder to work!
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
  amogus_balloon:
    display_name: "Amogus Balloon"
    type: BALLOON_ENTITY
    balloon:
      leash: true
    # Showing a different item into the GUI 
    # (in this case it's a must because ItemsAdder entities can't be put in GUIs)
    model:
      gui: minecraft:egg
      normal: cosmetics:amogus
    dye:
      enabled: true # To allow this item from being colored.
```

As you can see I set the `normal` model to the name of the **custom entity** created with ItemsAdder.

### Step 3

You're done

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

## Final notes

{% hint style="info" %}
You can even create animated balloons, just animate the idle animation of the entity using Blockbench.\
For example you can create a complex dragon or a rotating UFO. &#x20;
{% endhint %}
