# Grouped Products Block

Test Shopify Assignment
**Shopify Theme - DAWN v15.0.0**

## User Story

As a customer, I want to see every color a t-shirt is available in as a separate product on the
collection page. On the product page, I want to see colors and sizes styled similarly to
standard product options, even if colors link to different products.
As a store owner, I want to be able to set up these grouped products myself in the future using
Shopify metafields (and optionally collections) without needing a developer.
Examples: https://mightysparkfood.com/products/honey-jalapeno-snack-stick (Swap
between Flavors for products, Sizes for variant options) https://byltbasics.com/products/drop-
cut-shirt-lux?variant=27908801134694 (Swap between Lux Polo and Lux Short Sleeve for
products, colors for variant options)

### Goal

Using the latest version of the dawn theme this customisation adds a grouped product button block to the product details page, which allows the linking of products of the same type but with a different color. This is to also that the seperate products can have independent images and descriptions and be listed and filtered on collection pages. Rather than listing them as variants. This also helps to overcome the 100 variant limit which shopify had. (Althogh this limit is being removed in the future updates to 2000 in winter 24 edition reference [here](https://www.youtube.com/watch?v=IvNguac4WWA). )

## Setup

### Required Product Metafields

1. **Grouped Products** - key: "custom.grouped_products"
   Should be of type product as a list

2. **Color Swatch** - key: "custom.color_swatch"
   A custom product metafield is needed with the type **Metaobject** (see below)
   To create a Product Metafield go to:
   Settings -> Custom Data -> Metafield definitions -> Products

_Note that we are not using the build in Color Metaobject_

### Color Swatch Metaobject Creation

The Metaobject should have the id "color_swatch" and have the following fields:

- Name - key:color_swatch.name
- Hex - key:color_swatch.hex
- Swatch - key:color_swatch.image

  The logic behind this is for any product to be able to have either a hex color or an image file as a swatch. This type of metafield can then also be used for filtering in the same manner.
  To create a new Metaobject go to:
  Settings -> Custom Data -> Metaobject definitions -> Add Definition

### Linking Products

Now we can link all seperate product entities together. In the shopify admin product editor, we should now have access to the new product metafields:

**Grouped Products**
Here it is neccesary to add all the grouped products we want to display on the product detail page in our new block. (We must do this for every product that we want to link or group together) Keep there order the same so there is no layout shift.

**Color Swatch**
Add the product swatch images or colors for that specific product.

### Options in Customizer

In the product information section of the _Product Details Customizer_ we have a options block called **Grouped Product Links** where we can:

- Enable Grouped Product Buttons (enable or disable the block)
- Block Title (Change the Block Title on the PDP)
- Button Type (Choose either product name or Color Swatch)

### Feature Walkthrough

Link to feature walkthrough: [ video](https://www.loom.com/share/a0042a54fef24ded8ab97e494a6ab0db?sid=76b74cce-ce5a-4612-bba4-bf17482d3d76)

### Further Notes

For filtering in the wakthrough we have used the [Search & Discovery App](https://apps.shopify.com/search-and-discovery) from shopify.

For any questions contact me at: demetrius@dknzdesign.com
