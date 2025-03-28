# ⚙️ Customization

## Locations

You have to set the world and its coordinates, you can also set the yaw and pitch rotations.\
To get these values just use `/coords` command of **Essentials** or use `F3`.

### Camera location

Command: `/cosmeticsconfig config set camera-location`

![](<../.gitbook/assets/image (2) (1) (1) (1).png>)

### Mannequin location

Command: `/cosmeticsconfig config set mannequin-location`

Location of the player to preview the cosmetics in the wardrobe.

![](<../.gitbook/assets/image (12).png>) ![](<../.gitbook/assets/image (7).png>)

### Teleport area

This is a bit different, you have to set two points which represent the area in which the player can enter to open the wardrobe.

Command: `/cosmeticsconfig config set door-area-locations`

<div align="center"><img src="../.gitbook/assets/image (13).png" alt=""></div>

#### For better precision

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Exit location

Command: `/cosmeticsconfig config set exit-location`

Location where the player will be teleported back when they leave the wardrobe.

![](<../.gitbook/assets/image (22).png>)

## Other camera settings

{% code title="" %}
```yaml
  camera:
    hide_actionbar_texts: true
    use_invisibility_potion: false
    rotation:
      manual:
        enabled: true
        step: 20
      auto:
        enabled: true
        direction: RIGHT
        step: 1.5
        pause_ticks_on_manual_rotation: 60
    zoom:
      enabled: true
      min: 2
    fade_effect: true
```
{% endcode %}

* `hide_actionbar_texts` : hide any actionbar message. Useful to hide HUDs created by ItemsAdder and similar plugins
* `use_invisibility_potion`: add invisibility potion to the player when they join the wardrobe (should not be needed)
* `rotation` : preview NPC rotation using the mouse wheel
  * `manual`: rotate the NPC using the mouse wheel while the cursor is not on the NPC
  * `auto`: automatically rotate the NPC
    * `pause_ticks_on_manual_rotation`: duration of the auto rotation pause after mouse scroll
* `zoom`: zoom using the mouse wheel, while the cursor is on the NPC&#x20;
  * `min`: is the min zoom amount
* `fade_effect`: black screen fade animation on enter-exit the wardrobe

## Graphics customization

```yaml
    slots:
      colors:
        owned: 56,67,100
        not_owned: 195,147,57
        wearing: 57,70,195
        wearing_preview: 195,120,57
        max_amount_reached_owned: 24, 29, 43
        max_amount_reached_not_owned: 64, 48, 17
```

{% hint style="warning" %}
### Warning

Colors must be int RGB colors separated with a comma, you can get them from any color picker.\
HEX and integer colors are not supported for now.
{% endhint %}

To generate these colors you can use any website which offers an **RGB color picker**.\
For example [this one](https://www.rapidtables.com/web/color/RGB_Color.html).

These properties are used to set colors of the slots in the wardrobe GUI.

![](<../.gitbook/assets/image (18) (1).png>)

* **Owned**: color of the cosmetics owned (with permission)
* **Not owned**: color of the cosmetics not owned (no permission)
* **Wearing**: color of the cosmetics currently equipped
* **Wearing** preview: color of the cosmetics currently equipped but not owned (no permission), equipped only as preview
* **Max amount reached**: color of all the other cosmetics which cannot be equipped because the player is already wearing the max amount for that category
