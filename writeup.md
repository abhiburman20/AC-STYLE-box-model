##BOX-MODEL
###Display Properties
#### Inline, Inline-Block, Block, None

## Every element is a rectangular box on a page and it may have some width,
 height, padding, borders, and margins

Inline
### This will take space according to the content it wraps.
####
p {
    display: inline;
  }

Inline-Block
### Span is an inline-level element, but can be displayed as a
 block-level element.
####
span{
    display: inline-block;
  }

Block
### This will allows elements to behave as a block-level element 
accepting all the box-model properties.
####
{
    display: block;
  }

None
###This value will hide the element on the page.
####
{
    display: none;
  }

##Box Model Properties on Block-Level Element
###Div is a block-level element and all the box model property will work normally
 on block-level elements. Whatever the value you will apply for these properties on the block-level
  element, you will see the result as expected.
####
  div {
    width: 300px;
    height: 260px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }

##Inline-Level Element
###span is an inline-level element and it will not accept all the box model properties.
 But as we have overwritten it's display property to inline-block, therefore now the span
  will accept all the box model properties without any exception.
####
  span {
    width: 300px;
    height: 260px;
    padding: 20px;
    border: 10px solid blue;
    margin: 20px;
  }

##Removing Space between the inline-block elements.
### We may sometime encounter a problem, that is inline-block elements are not
 always touching when they line up one after another.There are different ways to 
 get rid of those small spaces. 
####
    //HTML SECTION//

  <div class="parent">
    <div class="inline-block>.....</div>
    <div class="inline-block>.....</div>
    <div class="inline-block>.....</div>
  </div>

  //or//

    <div class="inline-block>
    .......
  </div><div class="inline-block>
    .......
  </div><div class="inline-block>
    .......
  </div>

  //or//

    <div class="inline-block>
    .......
  </div><!--
  --><div class="inline-block>
    .......
  </div><!--
  --><div class="inline-block>
    .......
  </div>

    //CSS//

  .parent {
    font-size: 0;
  }
  .inline-block {
    display: inline-block;
    font-size: 16px;
  }

##Calculating the width and height of an element.
###According to the box model the total width of an element can be calculated using formula:
#### marging-left + border-left + padding-left + width + padding-right + border-right + margin-right
###And total height can calculated using formulat:
####marging-top + border-top + padding-top + width + padding-bottom + border-bottom + margin-bottom
