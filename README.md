# Shopify---Change-Image-On-Hover

A few simple lines of code to swap product images on hover across collection pages and feature product sections on homepage and product pages in Shopify. Many projects in the Shopify App Store are a) expensive or b) do not work with the default Shopify Theme in 2020 (Debut) or c) do not work at all.

This is very simple to implement:

0) Login to Shopify, Go to Themes -> Actions -> Edit Code
1) Put the CSS into the theme.scss.liquid file in the Assets folder, make any changes you want.
2) Make a few lines of insertions into the product-card-grid.liquid file in the Snippets folder and adjust product.images[1] with whatever array index you want as the swap image on hover. Note this counts from 0 as it is an arrage of images linked to the product in Shopify. If you want the last image in the image array, you can use product.images.last

TODOs:

- Error handling if there are not more than 1 images per product
- Dynamic sizing of the swap image to match the image sizing setup in the theme, currently its hardcoded e.g. 450x450 but you can change to what you want in the meantime
- Use more obscure class names so as to not conflict with other Shopify plugins.

Observations:

- Why are people charging $4.99 per month for a plugin that does this? 6 lines of code.
- Many of the guides on Stack Overflow, etc do not work because they're trying to hook into very busy DOM elements that have a lot of javascript from Shopify and are getting confused finding two clean hover events to harness for the image swap.
