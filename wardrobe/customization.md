# ⚙ 

## Configuration

<details>

<summary>Config.yml</summary>

{% code title="config.yml" %}
```yaml
wardrobe_room:
  camera:
    rotation:
      enabled: true
    zoom:
      enabled: true
      min: 2
    fade_effect: true
    location:
      world: flat
      x: 205
      y: -58.5
      z: 41
      yaw: 359.85
      pitch: 6.6
  mannequin:
    location:
      world: flat
      x: 204.5
      y: -60
      z: 45.5
      yaw: 180
      pitch: 0
  teleport_area:
    enter:
      world: flat
      pos1:
        x: 167
        y: -61
        z: 42
      pos2:
        x: 167
        y: -57
        z: 37
    exit_location:
      world: flat
      x: 164
      y: -60
      z: 40
      yaw: 98
      pitch: 10
```
{% endcode %}

</details>

## Locations

You have to set the world and its coordinates, you can also set the yaw and pitch rotations.\
To get these values just use `/coords` command of **Essentials** or use `F3`.

### Camera location

Command: `/cosmeticsconfig config set camera-location`

![](<../.gitbook/assets/image (2) (1).png>)

### Mannequin location

Command: `/cosmeticsconfig config set mannequin-location`

Location of the player to preview the cosmetics in the wardrobe.

![](<../.gitbook/assets/image (12).png>) ![](<../.gitbook/assets/image (7).png>)

### Teleport area

This is a bit different, you have to set two points which represent the area in which the player can enter to open the wardrobe.

Command: `/cosmeticsconfig config set door-area-locations`

![](<../.gitbook/assets/image (13).png>)

### Exit location

Command: `/cosmeticsconfig config set exit-location`

Location where the player will be teleported back when they leave the wardrobe.

![](<../.gitbook/assets/image (22).png>)

## Other camera settings

{% code title="" %}
```yaml
  camera:
    rotation:
      enabled: true
    zoom:
      enabled: true
      min: 2
    fade_effect: true
```
{% endcode %}

* **Rotation**: Set if you want players to be able to rotate the preview
* **Zoom**: Set if you want to enable zoom
* **Fade Effect**: Set if you want to enable the black screen fade animation on enter-exit the wardrobe.

## Graphics customization

```yaml
    slots:
      colors:
        not_owned: 195,147,57
        owned: 56,67,100
        wearing: 57,70,195
        wearing_preview: 195,120,57
        max_amount_reached: 111,111,111
```

{% hint style="warning" %}
### Warning

Colors must be int RGB colors separated with a comma, you can get them from any color picker.\
HEX and integer colors are not supported for now.
{% endhint %}

These properties are used to set colors of the slots in the wardrobe GUI.

![](<../.gitbook/assets/image (18) (1).png>)

* **Not owned**: color of the cosmetics not owned (no permission)
* **Owned**: color of the cosmetics owned (with permission)
* **Wearing**: color of the cosmetics currently equipped
* **Wearing** preview: color of the cosmetics currently equipped but not owned (no permission), equipped only as preview&#x20;
* **Max amount reached**: color of all the other cosmetics which cannot be equipped because the player is already wearing the max amount for that category&#x20;
