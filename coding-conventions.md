# Documentation VRcafe

## Dev lifecycle
<img src="/assets/coding-convention/dev-lifecycle.jpg" width="400">
In our way of coding we need to have a development lifecycle so that every component we have is up to our new standard. 

- Analyse: know who you're making this for and what they want from this page or component.
- Design: know what the user needs to feel welcome and motivated to interact with the website.
- Build: use accessable and progressivly enhanced practices to build better code.
- Test: test the page or component on lighthouse, validatortests, user tests, browsertest and device test.
- Integrate: by the use of pull request you integrate the code made from a branch and merge it into the dev branch.

### Pull request and branches
For the branches in this project we should have two main 'trees.' The main and the dev should always be there, but the other branches should be deleted via the Github desktop way of deleting a branch. With this way of thinking we will be using the [GitFlow's Workflow.](https://about.gitlab.com/blog/what-is-gitflow/#gitflows-workflow)
<br>
    <img src="/assets/coding-convention/branches.jpg" width="400">
</br>

#### Pull request
For pull requests it is important that a few rules are applied to help your colleagues test on a professional level. here's the way to write a pull request:
1. Title of the pull request
2. Description of what you've made
3. Visual documentation of what you've made
4. Which tests you've performed on the page or component
5. What you want your colleagues to test and review

### Commits
When writing commits for updating the code you need to write a descriptive title and in the commit message a condense summary of what you fixed. The way a commit message should be written is: 
```
(fix, feature or documentation) (title of what you've worked on)
```
```
(summary of what you've been working on)
```
<br>
    <img src="/assets/coding-convention/commit-message.png">
</br>

#### Commit often/Conventional commits
To make sure you have your code saved regularly and not be lost commit your changes regularly. This way part of your code is saved and you'll keep your colleagues more up to date on your work. Take a look at how [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) work.

### Standards
A great way to have a consistent status in SEO, Performance and Accessability is PE(progressivly enhanced.) This standard not only helps making your website usable for most people, it also helps search engines with indexing your content while still getting to have the 'fun' stuff. To learn more about how SEO practices are the same as Accessable practices read about SEO best [practices](https://dev.to/anisubhra_sarkar/frontend-seo-best-practices-a-developers-guide-to-optimizing-your-website-57j4).

### Naming things
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

## Coding conventions for VRcafe

### Syntax
- Use 1 tab indetation
- End your coding lines in CSS with a semicolon " ; "
- Do not end your coding lines in Javascript with a semicolon " ; "
- Use comments to explain code for youself and other developers. To successfully write comments about the code you'll need the following:
    1. Explain in two sentences max what it is you're making
    2. What certain functions need to do 
    3. How it will impact the user or developer

### Writing HTML
- Use semantic and logical HTML elements when creating a webpage, because a lot of HTML elements already have a good to use function and play naturally in their roles. Here's a good [article](https://css-tricks.com/explaining-the-accessible-benefits-of-using-semantic-html-elements/) about understanding semantic HTML.
- When a link is used make sure it is an `a` element and when a line of text is used to describe something it's a `p` element. 
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

### Writing CSS
- Follow how the HTML has been written and write the CSS in the same way. 
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

### Writing Javascript
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
#### Using const, let or var
- When writing Javascript it is key to always try to use `const`
- If a variable it's value will change after initalization it should be a let

### REACT
For components that are still made in React it would be smart to transfer them into Astro components due to the Javascript shipping in React.