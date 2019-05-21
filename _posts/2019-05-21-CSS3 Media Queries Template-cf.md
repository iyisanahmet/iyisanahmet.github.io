---
layout: post
title:  "CSS3 Media Queries Template"
date:   2019-05-21 17:18:45 +0700
categories: [css]
---


**Smartphones (portrait and landscape)**
```css
@media only screen 
and (min-device-width : 320px) 
and (max-device-width : 480px) {
/* Styles */
}
```

** Smartphones (landscape)**
```css@media only screen 
and (min-width : 321px) {
/* Styles */
}
```

**Smartphones (portrait)**
```css@media only screen 
and (max-width : 320px) {
/* Styles */
}
```

**iPads (portrait and landscape)**
```css@media only screen 
and (min-device-width : 768px) 
and (max-device-width : 1024px) {
/* Styles */
}
```

**iPads (landscape)**
```css@media only screen 
and (min-device-width : 768px) 
and (max-device-width : 1024px) 
and (orientation : landscape) {
/* Styles */
}
```

**iPads (portrait)**
```css@media only screen 
and (min-device-width : 768px) 
and (max-device-width : 1024px) 
and (orientation : portrait) {
/* Styles */
}
```

**Desktops and laptops**
```css@media only screen 
and (min-width : 1224px) {
/* Styles */
}
```

**Large screens**
```css@media only screen 
and (min-width : 1824px) {
/* Styles */
}
```

**iPhone 4**
```css@media
only screen and (-webkit-min-device-pixel-ratio : 1.5),
only screen and (min-device-pixel-ratio : 1.5) {
/* Styles */
}
```