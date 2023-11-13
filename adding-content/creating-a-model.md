# Creating a model

To create a model you can use BlockBench.

{% hint style="warning" %}
This requires knowledge on how to create resourcepacks and how to manage CustomModelData.
{% endhint %}

### Step 1

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Step 2

Save the model file into your resourcepack

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

### Step 3

{% hint style="warning" %}
This requires knowledge on how to create resourcepacks and how to manage CustomModelData.
{% endhint %}

Create the entry inside the `potion.json` file and decide a CustomModelData to be used later in the CosmeticsCore configurations.

```json
{
  "parent": "item/generated",
  "textures": {
    "layer0": "item/potion_overlay",
    "layer1": "item/potion"
  },
  "overrides": [
    ......
    ......
    {
      "predicate": { "custom_model_data": 600001 },
      "model": "cosmetics:hat/chef_hat"
    },
    ......
    ......
```

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>



