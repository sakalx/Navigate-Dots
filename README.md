________________________________________________________
________________________________________________________
# Add Vertical Navigation Dots

**[DEMO](https://sakalx.github.io/navigate-dots)**

> render vertical nav dods
 customized PgUp and PgDown scrolling between sections

## instaling:
+ between what sections need scrolling
add to this sections class (ANCHOR) **for example**:
```
<div class="js-navDots">section 1</div>
<div class="js-navDots">section 2</div>
...
...
<div class="js-navDots">section 5</div>
```
+ add to page CSS File: **styleVND.css**
  + `<link rel="stylesheet" type="text/css" href="styleNavDots.css">`
+ add to page (end of body HTML) Js File: **VND.min.js**
    + `<script src="verticalNavigationDots.js"></script>`
+ add to page (end of body HTML) Js Script:
```
<script>
  VND.init({
    cls: 'js-navDots', // anchor
    hideOnScreenLess: 640, // default = 0
  })
</script>
```

________________________________________________________
________________________________________________________

### Inside:
##### Render Methods:
```
  navDots - render vertical navigation dots in BODY
  ID fod each dot - nav-toSection#${indexOfSection}
  Class - nav__dot
```
##### Normalize Methods:
```
positionTop - normalized scrollTop value based on header height
```
##### Validate Methods
```
scrollThrowSection -  return boolean is scroll top going throw section
visibleElement - return boolean is visible element or not
```
##### Get Size Methods:
```
headerHeight - height of header
fullHeight - full height element with margin-bottom
```
##### Scrolling Methods:
```
top - scroll top to value
stop - run callBack when scrolling stop
```
##### Customized Keyboard Methods:
```
33 - PagUp Key
34 - PageDown Key
```
##### Dom Methods:
```
getAllElements - get array elements
containClass - check if element contain class (true/false)
addClass - add class to element
removeClass - find element with class between elements and remove that class
toggleCls - toggle class remove from Elements add to element
```
##### Position Methods:
```
rangeY - set & get range Y of element
scrollThrow - return true or false if scroll going throw range Y
getTop - position of top element
getPrevTop - distances from previous section to top
getNextTop - distances from next section to top
```
##### Handle Event Listener Methods:
```
navDots - handle scroll & toggle class when click on dots
pgUpDownKeys - handle scroll when press keys PgUpp PgDown
scrolling - handle scroll & toggle class when use scroll
resize - handle hide dots on small screen
```
