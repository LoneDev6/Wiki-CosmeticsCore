# Any plugin and resourcepack

## Installing the resourcepack <mark style="color:orange;">if you already have a custom resourcepack</mark>

If you already have a custom resourcepack on your server you must merge the **CosmeticsCore** assets and (optional) default cosmetics.

### Step 1

Open the zip file which can be found here: `plugins/CosmeticsCore/default_assets.zip` .

Extract it to a new folder, on your desktop for example.

Delete this folder: `plugins/ItemsAdder/`

Delete this folder if you don't have **ModelEngine** plugin: `plugins/ModelEngine/`

If you don't need the default cosmetics and you only need the UI you have to delete these folders and files:

* `resourcepack/assets/cosmetics/`
* `plugins/CosmeticsCore/`

Open the `resourcepack` folder.

Copy `assets/z_cosmetics` and `assets/cosmetics` folder into your resourcepack.&#x20;

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

### Step 2

Open the file `assets/minecraft/models/item/fermented_spider_eye.json` with your favorite editor (example: **VSCode**) and don't close it (the file is inside the zip).

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

### Step 3

Open the same previous file path in **YOUR** resourcepack (`fermented_spider_eye.json`).

Note: if you don't have this file in your resourcepack skip this step and simply copy and paste the `fermented_spider_eye.json` file inside your resoucepack into this path `assets/minecraft/models/item/fermented_spider_eye.json` .\


Use this tool to merge the **CosmeticsCore** file and your file:

{% embed url="https://itemsadder.github.io/jsonmerger/" %}

{% hint style="info" %}
`Json 1` is your json file, `Json 2` is the `CosmeticsCore` json file.

The result json is the one you will have to replace in your pack.
{% endhint %}

Now copy the result json and paste it into your old json file.

### Step 4

Follow the same previous steps for `potion.json`.
