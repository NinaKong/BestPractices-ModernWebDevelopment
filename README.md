# BestPractices-ModernWebDevelopment
Best Practices of Modern Web Development


## Search Engine Optimization (SEO):
1) Title tag: use the most important target keyword
   ```
   <title>SEO | SEO Best Practices | SEO for Front End Developers</title>
   ```
2) Meta description: it is not used for ranking directly, but still important for SEO
   ```
   <meta name="description” content=”Your page meta description, no more than 160 characters.”/>
   ```
3) Add Image tag
4) Clean URLs:  https://www.example.com/category/product-name
5) Semantic markup: not only helps SEO, but also goods for screen readers. It is also benefit the site's visitors and provides them an improved user experience.

**User Interface (UI) design:**
1) Keep a simple interface: avoid unnecessary elements, clear for labels and error messages, and reduce frustration for users
2) Keep web page consistency
3) Be purposeful in page layout: draw attention to the most important pieces of information, such as checkout button in an Ecommerce website
4) Use color and texture strategically : attention toward or redirect attention away from items using color, light, contrast, and texture to your advantage
5) Use typography to create hierarchy and clarity: different sizes, fonts, and arrangement of the text to help increase readability.

**User Experience (UX):**
1) Avoid giving visitors too many options
2) Avoid external links: keep users on your website as long as possible
3) Make responsive website
4) For long text/paragraph, make proper width
5) Use common/established/standard design patterns: avoid confusion visitors

    a. logo placed in the top left-hand corner
    b. navigation links running across the top
    c. footer and what type of info they usually contain: social media links and address

**HTML:**
1) Do not use tabular layouts, it is not user friendly for screen readers
2) Try to use percentage for width/height, it is better for responsive website
3) Decrease unnecessary tages to reduce page weight
4) Quality code: cleaner and concise code, and code weight

**CSS:**
1) Do not use inline CSS styles 
2) Ultilize minified CSS file
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
**Javascript:**
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
   

**Image:**


