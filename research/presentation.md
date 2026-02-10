# Presentation Ivan and Sidney
In this presentation Ivan and I will show what we found when doing our research for the website. We will explain our foundings in these four topics that we found to be essential for a better website.

## Table of Contents
- [Semantic HTML](#semantic-html)
    - [Headings](#headings)
    - [Correct usage of elements](correct-usage-of-elements)
    - [Tab test](#tab-test)
- [Mobile first](#mobile-first)
    - [Forced Synchronous Layout](#forced-synchronous-layout)
    - [Render Blocking](#render-blocking)
    - [Reducing JS and CSS](#reducing-js-and-css)
    = [Scaling Elements](#scaling-of-elements)

## Semantic HTML
Semantic HTML is crucial for both users and search engines! Aspects that people often overlook certainly have a significant impact.

### Headings
Headings and subheadings define the reading order of your content and should be structured from `h1` down to `h6`. Currently, this is not being handled correctly according to the HeadingsMap tool:
<br>
    <img src="../assets/seo-onderzoek/Semantische html/heading levels homepage.png">
    <img src="../assets/seo-onderzoek/Semantische html/drie h1&apos;s op een pagina.png">
    <img src="../assets/seo-onderzoek/Semantische html/incorrecte heading VR at home en leukste uitje in code.png">
</br>
By structuring your headings and subheadings correctly, you assist search engines in properly indexing your website. For users, headings also aid in the reading flow of your content, allowing them to 'skim' to find the right information. Another important rule to remember is to use only one `h1` element per page.

### Correct Usage of Elements
Regarding text on the homepage, I also noticed an `h2` containing a span referring to "Activiteiten," however this is semantically incorrect. Since "Activiteiten" is the focal point, it should be an `em` or a `strong` tag. This ensures it is not just a generic use of an element, but that it conveys clear meaning to both the user and the search engine.
<br>
    <img src="../assets/seo-onderzoek/span als tekst.png">
    <img src="../assets/seo-onderzoek/populaire-activiteiten-visueel.png">
</br>

### Tab Test
People who use a keyboard but do not use a mouse rely on the Tab key to navigate. While this is not important for search engines, it is vital for users on the website. If a user cannot clearly navigate through the page, it results in poor UX, and this is currently the case with the buttons and the menu. The logo is recognized (focusable), but the navigation menu is not, which is certainly incorrect for navigation
<br>
    <img src="../assets/tab wel logo.png">
    <img src="../assets/geen tab menu.png">
</br>
Furthermore, there is a `div` combined with an `a` tag on the page for booking an activity. This causes the focus to land first on the `div` and then on the `a`. In other words, it takes twice as many steps to focus on a button, and taking twice as long to perform an action is far too detrimental to UX.
<br>
    <img src="../assets/Screenshot 2026-02-03 153432.png">
    <img src="../assets/Screenshot 2026-02-03 153442.png">
</br>

## Mobile First
More than fifty percent of the people that use a search engine do it on their mobile device and it is therefore important to approach it with a mobile first approach. In the tests we have done there were some unfortunate results for performance and layout.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/lighthouse test performance, SEO, accessability en best practices.png">
</br>

### Forced Synchronous Layout
When JavaScript queries geometric properties after styles have changed for certain elements, this can significantly drag down your performance. In other words, this means that if someone intends to click on something like a button, there is a high chance it will shift a few seconds later, potentially causing them to click elsewhere, which creates user frustration.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/Gedwongen dynamische aanpassing mobile.png">
</br>

### Render-blocking
Because several requests are generated within the script first, it takes even longer to render the content. Therefore, what needs to be done is to ensure that the script only initiates its requests after the page has finished loading.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/renderblocking mobile.png">
</br>

### Reducing JS and CSS
Another factor that improves UX is reducing JavaScript and CSS and removing unused CSS and JS. This ensures that the page load time is reduced and that unnecessary code is not sent to the browser.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/beperk css mobile.png">
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/beperk JS mobile.png">
</br>

### Scaling of elements
For a mobile first approach it is also key to style the website so it is accessable for smaller screen sizes. Currently the mobile screen takes 9.9 seconds to load and that is way to long to load. To make these load times go down we need to scale the images correctly.
<br>
    <img src="../assets/seo-onderzoek/tests/pagespeed insight/mobile/statistieken mobile.png">
</br>