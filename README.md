# BestPractices-ModernWebDevelopment
Best Practices of Modern Web Development

HTML:
1) Do not use tabular layouts, it is not user friendly for screen readers
2) Try to use percentage for width/height, it is better for responsive website
3) Decrease unnecessary tages to reduce page weight

CSS:
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
Javascript:
1) Combine all the script files 
2) Do not use inline script if possible
3) Use minified javascript file
4) Only load the script is needed before page load
5) Use asynchronous method if possible, it will decrease page load time

   AJAX Example: Use ```XMLHttpRequest```,  it can get and send aHTTP requests
   
   a. Create http request - initialize ```XMLHttpRequest```
   
   ```
   var xhr = new XMLHttpRequest();
   ```
   
   b. Use ```open```, it has three arguments
   
   ```
   xhr.open('GET', "url", true);
   ```
   
   First argument: it has GET, POST, PUT, and DELETE. since we would like to get information, so we are using GET
   Second argument: URL. Put the URL you would like to get date with
   Third argument: requst asynchronous or synchronous. True means asynchronous request, it will make sure the web page is responsive and the remaining code is still running
   
   c. ```send``` method, it will send the request
   
   ```
   xhr.send();
   ```
   

Image:


Search Engine Optimization (SEO):
1) Create title and description
2) Add Image tag
