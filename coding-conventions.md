# Coding conventions for VRcafe


## Commits
When writing commits for updating the code you need to write a descriptive title and in the commit message a condense summary of what you fixed. The way a commit message should be written is: 
```
(fix, feature or documentation) (number of the issue you're fixing) (title of the issue)
```
```
(summary of the isssue you've been working on)
```

### Commit often/Conventional commits
To make sure you have your code saved regularly and not be lost commit your changes regularly. This way part of your code is saved and you'll keep your colleagues more up to date on your work.

## Standards
A great way to have a consistent status in SEO, Performance and Accessability is PE(progressivly enhanced.) This standard not only helps making your website usable for most people, it also helps search engines with indexing your content while still getting to have the 'fun' stuff. 

## Naming things
- Keep your classes, id's, functions and `const`'s descriptive of what they are and keep to the style of writing. 
- Use kebabcase for CSS and use camelCase for Javascript. 
- Lastly don't shorten or nickname these names, write them out fully.
> [!CAUTION]
> This is not the right way
```css
    --color-one: #000000;
    --color-2: #ffffff;
    --acc-color: #FF00FF;
```
> [!TIP]
>This is the right way
```css
    --primary-color: #000000;
    --secondary-color: #ffffff;
    --accent-color: #FF00FF;
```

## Writing HTML
- Use semantic and logical HTML elements when creating a webpage. 
- When a link is used make sure it is an `a` element and when a line of text is used to describe something it's a `p` element. 
- When writing HTML and nesting make sure to use 1 tab indentation.
> [!CAUTION]
> This is not the right way
```html
    <div onclick="goToRecommendations();">All recommendations</div>
```
> [!TIP]
> This is the right way
```html
    <a href="example.com">
```

## Writing CSS
- When writing CSS make sure to use 1 tab indentation for clearer code. 
- Follow how the HTML has been written and write the CSS in the same way. Don't Repeat Yourself and use utility classes. 
- For future pages it would be the best to not use utility-first frameworks like TailwindCSS. Vanilla CSS could get you far enough.
- End your CSS lines with a semicolon " ; " 
- Use comments to explain code for youself and other developers
- Use @supports to progressivley enhance your elements
> [!CAUTION]
> This is not the right way
```css
    article {
        background-color: var(--primary-color)
        border-radius: 20%
        corner-shape: bevel
    }
```
> [!TIP]
> This is the right way
```css
    article {
        background-color: var(--primary-color);
        border-radius: 20%;
        /* For users that use browsers that support corner-shape  */
        @supports (corner-shape: bevel) {
            corner-shape: bevel;
        }
    }
```

## Writing Javascript
- Use 1 tab indentation for clearer code
- Unlike CSS do not end your lines with a semicolon " ; "
- Use comments to explain code for youself and other developers
> [!CAUTION]
> This is not the right way
```javascript
    let link = document.querySelector('a[href="#activiteiten"]');
    link.addEventlistener("mouseleave", linking);
    function linking() {
        link.classlist.add("activelink")
    };
```
> [!TIP]
>This is the right way
```javascript
    let activiteitenLink = document.querySelector('a[href="#activiteiten"')

    // listen to when the user their pointer leaves the area where they hover over
    activiteitenLink.addEventlistener("pointerleave", nonHover)

    // In this function i'll add the hover-leave classlist I made in css so it will create an effect when leaving
    funtion nonHover() {
        activiteitenLink.classlist.add("hover-leave")
    }
```
### Using const, let or var
- When writing Javascript it is key to always try to use `const`
- If a variable it's value will change after initalization it should be a let

## TailwindCSS
Utility-first frameworks like TailwindCSS actually don't help much more than regular CSS does. So the best thing would be to slowly roll back the TailwindCSS and replace it with vanilla CSS. 

## REACT
For components that are still made in React it would be smart to transfer them into Astro components due to the Javascript shipping in React.