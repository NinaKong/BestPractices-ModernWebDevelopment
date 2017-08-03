# BestPractices-ModernWebDevelopment
Best Practices of Modern Web Development

## Best Practices Table of Contents
  - [Search Engine Optimization (SEO)](#search-engine-optimization-seo)
  - [Accelerated Mobile Pages (AMP)](#accelerated-obile-pages-amp)
  - [User Interface (UI) design](#user-interface-ui-design)
  - [User Experience (UX)](#user-experience-ux)
  - [Usability](#usability)
  - [Accessibility](#accessibility)
  - [Hypertext Markup Language (HTML)](#html)
  - [CSS](#css)
  - [Javascript](#javascript)
  - [Responsive Designs](#responsive-designs)
  - [Image](#image)
  
## Search Engine Optimization (SEO)
1) Title tag: use the most important target keyword
   ```
   <title>SEO | SEO Best Practices | SEO for Front End Developers</title>
   ```
2) Meta description: it is not used for ranking directly, but still important for SEO
   ```
   <meta name="description” content=”Your page meta description, no more than 160 characters.”/>
   ```
3) Add Image tag
    ```
    <img src="smile-face.gif" alt="Smile face">
    ```
4) Clean URLs:  https://www.example.com/category/product-name
5) Semantic markup: not only helps SEO, but also goods for screen readers. It is also benefit the site's visitors and provides them an improved user experience.
## Accelerated Mobile Pages (AMP)
## User Interface (UI) design
1) Keep a simple interface: avoid unnecessary elements, clear for labels and error messages, and reduce frustration for users
2) Keep web page consistency
3) Be purposeful in page layout: draw attention to the most important pieces of information, such as checkout button in an Ecommerce website
4) Use color and texture strategically : attention toward or redirect attention away from items using color, light, contrast, and texture to your advantage
5) Use typography to create hierarchy and clarity: different sizes, fonts, and arrangement of the text to help increase readability.

## User Experience (UX)
1) Avoid giving visitors too many options
2) Avoid external links: keep users on your website as long as possible
3) Make responsive website
4) For long text/paragraph, make proper width
5) Use common/established/standard design patterns: avoid confusion visitors
   - Logo placed in the top left-hand corner
   - Navigation links running across the top
   - Footer and what type of info they usually contain: social media links and address

## Usability
1) Identify the users and improve design: SEO and usability work together to create persuasive design
2) Know your devices screen sizes: in order to maximize the customer's purchase and responsive for viewing on mobile devices
3) Support most of browser: Internet Explorer, Mozilla Firefox, Google Chrome, Opera, and Safari
4) Find usability errors to improve SEO
5) Cut down your load time
   - Compress your images to smaller file sizes
   - Use CSS for the layout of your website
   - Reduce the number of HTTP requests
   - Set up browser caching
6) 404 Error Page helpful
   - Design the page in a brand-cohesive way
   - Give visitors an easily way to contact you to inform the error

## Accessibility
1) Validate your code: follow Web Content Accessibility Guidelines (WCAG 2.0)

   [Four WCAG Principles](https://www.w3.org/TR/UNDERSTANDING-WCAG20/intro.html#introduction-fourprincs-head)
   - Perceivable: Information and user interface components must be presentable to users in ways they can perceive
   - Operable: User interface components and navigation must be operable
   - Understandable: Information and the operation of user interface must be understandable
   - Robust - Content must be robust enough that it can be interpreted reliably by a wide variety of user agents, including assistive technologies.
   
2) Navigate website with a keyboard only
   - Tab in a logical order
   - Enter, edit, or submit a form
   - Left, right, up and down arrow keys to navigate
   - Enter key to take an action
3) Text Clarity and concise: double-check your spelling and grammar
4) Don’t rely exclusively on color
5) Provide appropriate alternative text: helpful for people who are blind and rely on a screen reader to have the content of the website 
    ```
    <img src="smile-face.gif" alt="Smile face">
    ```
6) Provide headers for data tables
7) Ensure users can complete and submit all forms: Ensure that every form element (text field, checkbox, dropdown list, etc.) has a label and make sure that label is associated to the correct form element using the <label> element
8) Try to avoid slideshow

## HTML
1) Do not use tabular layouts, it is not user friendly for screen readers; only use them when you need to display tabular data
2) Try to use percentage for width/height, it is better for responsive website
3) Decrease unnecessary tages to reduce page weight
4) Quality code: cleaner and concise code, and code weight
5) HTML5 Elements: to provide semantic value and make use of HTML5 elements such as <header>, <nav>, and <footer>, however, do not apply IDs or classes to them, since older browsers do not understand some of HTML5 elements by default and do not apply styling to them.
    ```
    <footer>
      <div class="site-footer">
          ...
      </div>
    </footer>
    ```
6) Validation: if it is not correct, it may affect page performance, accessibility, and SEO. The W3C validator can be found [here](http://validator.w3.org/)

## CSS
1) Do not use inline CSS styles 
2) Ultilize minified and compressed CSS file
3) Avoide to use duplicated styles
4) Even though CSS files are downloaded in parallel, combine all the CSS files if possible, it can reduce the http calls to server
5) Consider for browser compatibilities, do not style in a HTML5 element, use .header instead
    ```
    <header>
        <div class="header">
            ...
        </div>
    </header>
    ```
6) Order CSS properties - grouped by type (from  Nicolas Gallagher's Idiomatic CSS: http://nicolasgallagher.com/)
    ```
    .selector {
      /* Positioning */
      position: absolute;
      z-index: 10;
      top: 0;
      right: 0;

      /* Display & Box Model */
      display: inline-block;
      overflow: hidden;
      box-sizing: border-box;
      width: 100px;
      height: 100px; 
      padding: 10px;
      border: 10px solid #333;
      margin: 10px;

      /* Color */
      background: #000;
      color: #fff

      /* Text */
      font-family: sans-serif;
      font-size: 16px;
      line-height: 1.4;
      text-align: right;

      /* Other */
      cursor: pointer;
    }
    ```
7) Use modular CSS Name convention: BEM - The Block, Element, Modifier methodology
   
   The following example is from ROBIN RENDLE https://css-tricks.com/bem-101/
    ```
    /* Block component */
    .btn {}

    /* Element that depends upon the block */ 
    .btn__price {}

    /* Modifier that changes the style of the block */
    .btn--orange {} 
    .btn--big {}
    ```
8) Avoid using !important



## Javascript
1) Combine all the script files 
2) Do not use inline script if possible
3) Use minified javascript file
4) Only load the script is needed before page load
5) Use asynchronous method if possible, it will decrease page load time

   AJAX Example: Use ```XMLHttpRequest```,  it can get and send HTTP requests
   
   a. Create http request - initialize ```XMLHttpRequest```
   
   ```
   var xhr = new XMLHttpRequest();
   ```
   
   b. Use ```open```, it has three arguments
   
   ```
   xhr.open('GET', "url", true);
   ```
   
   - First argument: it has GET, POST, PUT, and DELETE. since we would like to get information, so we are using GET
   - Second argument: URL. Put the URL you would like to get date with
   - Third argument: requst asynchronous or synchronous. True means asynchronous request, it will make sure the web page is responsive and the remaining code is still running
   
   c. ```send``` method, it will send the request
   
   ```
   xhr.send();
   ```
6) Avoid using document.write   
7) Avoid using global variables, wrap them in closures

## Responsive Designs
1) Percentage-based grids
2) Flexible scaled images
3) CSS media queries
   ```
    .example {...}
    @media(min-width: 480) {
      .example {

      }  
    }

    @media(min-width: 768px) {
      .example {

      }  
    }

    @media(min-width: 1024px) {
      .example {
      
      }  
    }
   ```

## Image
1) Use .jpg for background image
2) Use .svg or .png as logo

