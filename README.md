P5 - Website Optimization
============================

Changes Done for Optimization
------------------------------
###### PageSpeed Insights
1. Load google-analytics script as an async resource.
2. Add `media="print"` to print.css so it's not a critical resource.
3. Inline style.css and Google font stylesheet in `<head>`.
4. Minified font styling using a minifier online.
5. Replace perfmatters.js, profilepic.jpg, and pizzeria.jpg with compressed files generated by Google PageSpeed.


###### Pizzeria Optimization
**Improving FPS**

1. Replace `querySelector()` with `getElementsByClassName()` or `getElementById`.
2. Prevent multiple DOM traversals by moving code outside of loops, switch statements, or functions with multiple calls.
3. Reduce number of background pizzas from 200 to 40.
4. Improve `updatePositions()`.
    * Store all five possible phase values in an array to look up instead of performing the calculation for every pizza.
    * Use translate instead of left for positioning.
    * Moved calculation of scrollTop position to outside for loop.
    * Create throttle function to throttle calls to `updatePositions()` to once per 100ms.

**Improving pizza resizing**

1. Prevent mulitple DOM traversals by moving code to outside of `resizePizzas()`.
2. Calculate the new width of pizzas only once, outside of for loop, instead of for every pizza.

How to Run
--------------------------------
No setup needed. Navigate to:
* [Profile](http://lisatd.githib.io)
* [Pizzeria](http://lisatd.github.io/views/pizza.html)