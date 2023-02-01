---
title: 'How to change KaTeX Font and Color'
date: 2020-10-04 00:00:00 +0900
author: kintiru
categories: [English, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

While setting up the blog, I had some problem with KaTeX.

It was overflowing outside of the screen, and the color was same as the background so it was barely visible.

I did not like the font either, so I changed the settings.

You can change KaTeX styling like below.

```css
.katex { 
        font: 1em "your-font", font-family !important;
        color: white;
        overflow: auto;
    }
```