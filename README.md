# Grouped Products Block

Test Shopify Assignment
**Shopify Theme - DAWN v15.0.0**

Using the latest version of the dawn theme this customisation adds a grouped product button block to the product details page, which allows the linking of products of the same type but with a different color. This is to also that the seperate products can have independent images and descriptions and be listed and filtered on collection pages. Rather than listing them as variants. This also helps to overcome the 100 variant limit which shopify had. (Althogh this limit is being removed in the future updates to 2000 in winter 24 edition reference here: https://www.youtube.com/watch?v=IvNguac4WWA )

### Product Metafields Required

A custom product metafield is needed with the id "custom.color_swatch"
This should be of type **Metaobject** see below
To create a Product Metafield go to:
Settings -> Custom Data -> Metafield definitions -> Products

_Note that we are not using the new build in Color Metaobject_

### Metaobject Creation Required

The Metaobject should have the id "color_swatch" and have the following fields:

- Name - key:color_swatch.name
- Hex - key:color_swatch.hex
- Swatch - key:color_swatch.image

  The logic behind this is for any product to be able to have either a hex color or an image file as a swatch. This type of metafield can then also be used for filtering in the same manner.
  To create a Metaobject go to:
  Settings -> Custom Data -> Metaobject definitions -> Add Definition

### Settings Options

In the product informnation section of the _Product Details Customizer_ we have a options block called **Grouped Product Links** where we can change:

- Enable Grouped Product Buttons (enable or disable the block)
- Block Title (Change the Block Title on the PDP)
- Button Type (Choose either product name or Color Swatch)
