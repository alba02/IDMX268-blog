---
template: blog-post
title: Shortcuts for CSS
slug: /shortcuts-in-css
date: 2022-02-26 19:50
description: Time reducing options when using CSS.
featuredImage: /assets/pankaj-patel-6jvlsdgmace-unsplash.jpg
---
When picking color values in CSS, we often think we have a color in mind. However, trying to find the exact shade can take time in our projects. Looking for the right shade for or web pages can be time consuming, especially if we need to use more than two colors for our page. Even though it is time consuming it is worth it because in the end our page will be well presented and visually appealing. However, to reduce the time it takes to look for each shade something very useful we can use is the hsl() function in CSS. Usually, we go online or find a swatches to find colors and build our palette one by one. With the hsl() function this can be easier to do. What does the hsl() function do exactly?

![HSL wheel degrees](/assets/quackit.png "Hue degree wheel by Quackit")

Like in the image above provided by [Quackit](https://www.quackit.com/css/color/values/css_hsl_function.cfm#:~:text=The%20CSS%20hsl()%20function,color%20space%20of%20computer%20graphics.) the first number is a degree. This degree is the hue. With practice you can have a general idea of where each hue color is and just go by that. Like for example, if you are looking for a green you can look in the 120-degree value and out that as the first. The second value is saturation. With this you can alter how saturated you want your color to be. It goes by percent so 0% would be no saturation and it would be very very light green. The next and final value is the lightness. If you want normal lightness, you would just go by 50 percent. The lightness value goes from really dark (100%) to really light (0%). The HSL function comes in handy if you’re trying to get the same hues within a page but have different lighter shades. For example, say your background of your page is a deeper blue like this image below by <https://www.w3schools.com/colors/colors_hsl.asp>. 

![Blue hue in hsl](/assets/screenshot-87-.png "HSL of the color blue.")

However, you want to add a box the same hue but lighter. All you have to do is change the lightness of it and it will be the same hue while being a shade lighter without having to change the saturating or pick another color online.

![Image of lighter blue hsl](/assets/screenshot-88-.png "Lighter blue")

Like shown in the image above by [w3schools](https://www.w3schools.com/colors/colors_hsl.asp) the only value that changed was the lightness. Once you play around with it you can get the hang of it and it will be easier to use. In the “CSS hsl() function” article by Quackit it shows a more in depth guide to how to use hsl. They stated that “Once you've picked your hue, it's just a matter of adjusting the saturation and lightness until you get it right.” This shows that once you hue your hue ready for your page you can just toggle and play around with the rest of the values for saturation and lightness. Using the hsl function like this can be easier than manually picking out shades from an online color swatcher to plan for your website.

Another time-consuming aspect of CSS that can be reused throughout your page are CSS custom properties. With CSS custom properties you are able to set a variable to something and reuse it throughout the style sheet without having to put the exact numbers to a color or number to a size. A way to do this would be shown in the “CSS Custom Properties” article by Stephanie Eckles. She explains “To define a custom property, use the name of your choice preceded by two dashes, for example: --my-property. Then you can use that value by calling it within the var() CSS function in place of providing a standard value.” This shows that for a custom property you name what you want to reuse. For example, you can put --my-font-color as a name for a default font color you want to reuse and set it to a specific color. All you have to do to call it and reuse it in your stylesheet would be how Stephanie mentions. By putting a var parenthesis then the name of your custom property inside the parenthesis. Doing this will save you a lot of time and reduce it because you can just copy and paste or just write the name you set it too instead of trying to remember what the exact value of your background color or font color was. Since you already have it set it is much easier to use. In the example below by [MDN mozilla](https://developer.mozilla.org/en-US/docs/Web/CSS/--*) you can see how these custom properties are used.

```
:root
  --first-color: #16f;
  --second-color: #ff7;
}

#firstParagraph {
  background-color: var(--first-color);
  color: var(--second-color);
}

#secondParagraph {
  background-color: var(--second-color);
  color: var(--first-color);
}

#container {
  --first-color: #290;
}

#thirdParagraph {
  background-color: var(--first-color);
  color: var(--second-color);
}
```

When writing in English things go from left to right. In different languages however writing can go from right to left and be written in a different direction either vertical or horizonal. How can we make sure that when our website is in another language these values are still read as they should? This is where logical properties come into play. Logical properties use block and inline values to take care of these directions. According to an article “Logical Properties” by web.dev they simplify the meaning of these both. “Block flow is the direction in which content blocks are placed.”  This means that the block direction is what the block flow property is used for. For example, in English the paragraphs go in a vertical way. Starting at the top to bottom. In other languages, they can go in other directions. Inline dimensions are another part of logical properties and are used to see the flow of text within a line. For example, in English it would be horizontal and would go from left to right. This because that is the direction of the way the text flows in English. For a language like Japanese, the flow of text goes vertically. This is because the text direction goes up and down. In logical properties in example of using block to make sure it’s the same in other languages you would use start and end keywords to place them where you want them. Start meaning left or the beginning and end meaning the right. So, for padding, if you want a value to start on the left for English you would put padding-block-start, and then the value. If you want the padding to be somewhere on the right you would use end keyword and then the value. For inline, they are the same keywords, start and end before inline. In example is seen below from the article by [web.dev.](https://web.dev/learn/css/logical-properties/)

```
.my-element {
  border-block-end: 1px solid red;
  border-inline-end: 1px solid red;
  border-end-end-radius: 1em;
}
```