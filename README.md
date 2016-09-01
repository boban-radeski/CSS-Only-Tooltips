# CSS-Only-Tooltips
Custom implementation of tooltips using only SASS. 
For those who are tired of including one JavaScript and one CSS (2 requests) file to your project just to use tooltips, here's a way to accomplish the same
result with No JS, just (S)CSS.

# Usage

## Include style.scss into your SASS module architecture 
  For example: ``` @include style.scss ``` in your main SCSS file, for example main.scss
  
  In style.scss you can find variables the helps to configure the tooltip according to your design needs: 
  <dl>
     <dt> $tooltip-width: `200px; `</dt>
     <dt> $tooltip-animation: ` all .2s ease-in-out; ` </dt>
     <dt> $tooltip-bgcolor: ` rgba(65, 133, 217, 0.94); `</dt>
     <dt> $tooltip-text-color: ` #fff; ` </dt>
     <dt> $tooltip-padding: ` 8px; ` </dt>
     <dt> $tooltip-text-align: ` left; ` </dt>
     <dt> $tooltip-border-radius: ` 0px; `</dt>
     <dt> $tooltip-triangle-size: ` 15px; ` </dt>
     <dt>$tooltip-triangle-bgcolor: ` rgba(65, 133, 217, 0.76); ` </dt>
     <dt> $tooltip-font-size: ` 16px; ` </dt>
  </dl>    

## In your HTML view add the following code lines with **data-** attributes
#### Right positiоned tooltip, displayed right from the link:
```
<a href="#" data-tooltip-position="right" data-tooltip="this tooltip is made with nothing but the CSS">
    right tooltip
</a>
```
#### Left positiоned tooltip, displayed left from the link:
```
<a href="#" data-tooltip-position="left" data-tooltip="this tooltip is made with nothing but the CSS">
    left tooltip
</a>
```
#### Top positiоned tooltip, displayed on top of the link:
```
<a href="#" data-tooltip-position="top" data-tooltip="this tooltip is made with nothing but the CSS">
    top tooltip
</a>
```
#### Bottom positiоned tooltip, displayed on bottom of the link:
```
<a href="#" data-tooltip-position="bottom" data-tooltip="this tooltip is made with nothing but the CSS">
    bottom tooltip
</a>
```

## Example of usage:

```
<!DOCTYPE html>
<html>
<head>
    <title>CSS Tooltips</title>
    <link href="style.css" rel="stylesheet" />
</head>
<body>
    <div style="width: 960px; margin:0 auto;">
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquid natus molestias quam numquam dolorum
            ea labore eius iure saepe, accusamus, recusandae ipsum modi magnam ducimus dicta blanditiis
            id optio itaque?
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sit nam, saepe quis consequuntur.
            Magni asperiores
            <a href="#" data-tooltip-position="right" data-tooltip="this tooltip is made with nothing but the CSS">
                right tooltip
            </a>,
            illo suscipit excepturi natus libero consequatur odit quia, dolor animi sint amet!
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sit nam, saepe quis consequuntur.
            Magni asperiores
            <a href="#" data-tooltip="new one tooltip" data-tooltip-position="left">
                left tooltip
            </a>
            illo suscipit excepturi natus libero consequatur odit quia, dolor animi sint amet!
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sit nam, saepe quis consequuntur.
            Magni asperiores
            <a href="#" data-tooltip="new one tooltip" data-tooltip-position="top">
                top tooltip
            </a>
            illo suscipit excepturi natus libero consequatur odit quia, dolor animi sint amet!
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sit nam, saepe quis consequuntur.
            Magni asperiores
            <a href="#" data-tooltip="" data-tooltip-position="bottom">
                bottom tooltip
            </a>
            illo suscipit excepturi natus libero consequatur odit quia, dolor animi sint amet!
        </p>
    </div>
</body>
</html>
```

### If you are filing tooltips using AJAX and ``` data-tooltip="" ``` is empty, the tooltip will show message **Loading...** instead of displaying nothing

#### Note: Do not use this tooltip on full width layout. If the tooltip link is on the left:0 of the screen and ``` data-tooltip-position="left" ``` the tooltip will not be visible. Same for position right.

### Demo on [codepen.io!](http://codepen.io/anon/pen/akgAwy)
