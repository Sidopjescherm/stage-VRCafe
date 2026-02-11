# Coding conventions for VRcafe

## Naming things
Naming things is een important part for coding. Keep your classes, id's, functions and `const`'s descriptive of what they are and keep to the style of writing. Use kebabcase for CSS and use camelCase for Javascript. Lastly don't shorten or nickname these names, write them out fully.
```css
    This is not the right way
    --color-one: #000000;
    --color-2: #ffffff;
    --acc-color: #FF00FF;
```
```css
    This is the right way
    --primary-color: #000000;
    --secondary-color: #ffffff;
    --accent-color: #FF00FF;
```

## Writing HTML`
Use semantic and logical HTML elements when creating a webpage. When a link is used make sure it is an `a` element and when a line of text is used to describe something it's a `p` element. When writing HTML and nesting make sure to use intendation.
```html
    This is not the right way
    <div onclick="goToRecommendations();">All recommendations</div>

```

```html
    This is the right way
    <a href="example.com">
```

## Writing CSS

## Using tailwindCSS

## Writing Javascript