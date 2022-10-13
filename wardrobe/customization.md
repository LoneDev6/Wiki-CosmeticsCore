# ⚙ Anpassungen

## Konfiguration

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

## Standorte

Du musst die Welt und die Koordinaten festlegen und kannst ebenfalls die Gier- und Nickdrehungen einstellen.\
Um diese Werte zu erhalten, verwende einfach den `/coords` Command von dem Plugin **Essentials** oder Nutze die `F3` Taste.

### Kamera-Standort

Befehl: `/cosmeticsconfig config set camera-location`

![](<../.gitbook/assets/image (2) (1).png>)

### Preview-NPC Standort

Befehl: `/cosmeticsconfig config set mannequin-location`

Standort des Ebenbilds des Spielers, um die Cosmetics anzuprobieren.

![](<../.gitbook/assets/image (12).png>) ![](<../.gitbook/assets/image (7).png>)

### Teleport-Bereich

Das ist etwas anders als die vorherigen Punkte. Man muss zwei Punkte setzen, die den Bereich darstellen, in den der Spieler eintreten kann, um den Kleiderschrank zu öffnen.

Befehl: `/cosmeticsconfig config set door-area-locations`

![](<../.gitbook/assets/image (13).png>)

### Ausgangsort

Befehl: `/cosmeticsconfig config set exit-location`

Ort, an den die Spieler zurückteleportiert werden, wenn sie den Spind verlassen.

![](<../.gitbook/assets/image (22).png>)

## Andere Kameraeinstellungen

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

* **Rotation**: Lege fest, ob Spieler den NPC drehen können
* **Zoom**: Lege fest, ob Spieler zoomen können
* **Fade Effect**: Lege fest, ob die Blackscreen-Fade-Animation beim Betreten und Verlassen des Spinds abgespielt werden soll

## Grafikeinstellungen

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
### Warnung

Farben müssen in ganzzahligen RGB-Farben sein, die durch ein Komma getrennt sind, man kann sie in jedem Farbwähler anzeigen lassen.\
HEX- und Integer-Farben werden derzeit nicht unterstützt.
{% endhint %}

Diese Einstellungen werden verwendet, um die Farben der Slots in der Garderoben-GUI festzulegen.

![](<../.gitbook/assets/image (18) (1).png>)

* **Not owned**: Farbe der Cosmetics, welche man nicht besitzt (keine Berechtigung)
* **Owned**: Farbe der Cosmetics, welche man besitzt (mit Berechtigung)
* **Wearing**: Farbe der Cosmetics, welche man ausgerüstet hat
* **Wearing** Vorschau: Farbe der Cosmetics, welche gerade ausgerüstet sind, aber sich nicht im Besitz befinden (keine Berechtigung), nur als Vorschau ausgerüstet&#x20;
* **Max amount reached**: Farbe der Cosmetics, welche nicht angezogen werden können, da die maximale Anzahl der Cosmetics in dieser Kategorie schon erreicht ist&#x20;
