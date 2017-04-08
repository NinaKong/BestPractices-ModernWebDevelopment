# BestPractices-ModernWebDevelopment

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

Javascript:
1) Combine all the script files 
2) Do not use inline script if possible
3) Use minified javascript file
4) Only load the script is needed before page load

Image:

