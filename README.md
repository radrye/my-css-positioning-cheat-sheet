# my-css-positioning-cheat-sheet

Boilerplate for creating a CSS positioning cheat sheet

## Purpose

- What you should end up with is a styled document that you can reference
  quickly for lookup some CSS positioning

## Instructions

- Since you are already an HTML master, I've already helped you out by
  creating some content.

- You should take a note of what you are getting for free.
  - 4 rows created by 4 sequential div elements
  - 4 boxes within each row
    - all boxes get the same styling because they share the class of "box"
    - all boxes get their shape by the height and width settings
    - the boxes are laid out next to each other because of the
      display property, which is set to inline-block
      - inline-block basically tells the browser to render the blocks inline
        while retaining their block characteristics, such as height and
        width
    - the boxes have some borders to separate them from each other
  - all styling is in the head to keep things simple for this example

- Set up your development environment
  - Open up this project in your editor (e.g., Sublime Text)
  - Start up a web browser in the project root
  - Open the index.html page in a browser



### Box Model

- Inspect one of the boxes using Chrome Developer Tools
- Mouse over the box model and take note of the different parameters
  - margin
  - border
  - padding
- Note that the margin and padding are blank, and that the border is set to 1
- Note the value of 1 for border comes from the border-width parameter in the
  div.box styling (to the left of the box model)



- Update the CSS to set the border-width parameter to 10px

      div.box {
        ...
        border-width: 10px;
        ...
      }

- Note how the values in the box model changes in Chrome Developer Tools
- Note how the border is thicker on all sides of all boxes in the page
- See http://www.w3schools.com/cssref/pr_border-width.asp on how to target
  each side of the elements individualy
- Commit your changes



- Update the CSS to set the padding parameter to 10px

      div.box {
        ...
        padding: 10px;
        ...
      }

- Note how the values in the box model changes in Chrome Developer Tools
- Note how the distance between the text and the border is greater than before
- Note how the entire box grows to accommodate the padding in addition to the
  content size
- See http://www.w3schools.com/css/css_padding.asp on how to target each side
  of the elements individually
- Commit your changes



- Update the CSS to set the margin parameter to 10px

      div.box {
        ...
        margin: 10px;
        ...
      }

- Note how the values in the box model changes in Chrome Developer Tools
- Note how the boxes are no longer touching and have space on all sides
- See http://www.w3schools.com/css/css_margin.asp on how to target each side
  of the elements individually
- Commit your changes



### Positioning

- block and inline are the standard display properties. Now there are new
  types like inline-block and flexbox that help alleviate some of the
  issues/restrictions of only have the two layouts, but those are more
  advanced
- To break out of the standard block (top to bottom) and inline
  (left to right) flow, positioning can be used



#### static

- "static" is the default positioning that is used if explicit positioning
  is not set



#### fixed

- Pick any box and give it an id of "the-fixed-box"

      <div id="the-fixed-box" class="box">06</div>

- Add styling to set the background-color of this element to red
  so it can be easily differentiated
- Add styling to set the display value for this element to fixed

      #the-fixed-box {
        background-color: red;
        position: fixed;
      }

- Refresh the page and note where the box is
- Resize the window to a size you get scroll bars and scroll around
- Note where the box is when you scroll
- Add top and left positioning of 50px

      #the-fixed-box {
        ...
        top: 50px;
        left: 50px;
        ...
      }

- Refresh the page and note where the box is
- Resize the window to a size you get scroll bars and scroll around
- Note where the box is when you scroll
- bottom and right can also be used to offset fixed elements
- properties:
  - does NOT remain in the normal document flow
  - offset relative to the window
  - remains in place on scroll
- Commit your changes



#### relative

- Pick any box and give it an id of "the-relative-box"

      <div id="the-relative-box" class="box">10</div>

- Add styling to set the background-color of this element to yellow
  so it can be easily differentiated
- Add styling to set the display value for this element to relative

      #the-relative-box {
        position: relative;
        background-color: yellow;
      }

- Refresh the page and note where the box is
- Resize the window to a size you get scroll bars and scroll around
- Note where the box is when you scroll
- The box should be in the same place
- add top and left offsets of 50px

      #the-relative-box {
        ...
        top: 50px;
        left: 50px;
        ...
      }

- Refresh the page and note where the box is
- Resize the window to a size you get scroll bars and scroll around
- Note where the box is when you scroll
- bottom and right can also be used to offset relative elements
- properties:
  - remains in the normal document flow
  - offset relative to its normal position (i.e., display: relative alone)
    does not change anything
- Commit your changes



#### absolute

- Pick any box and give it an id of "the-absolute-box"

    <div id="the-relative-box" class="box">13</div>

- Add styling to set the background-color of this element to green
  so it can be easily differentiated
- Add styling to set display value for this element to absolute
  and the top and left offsets to 50px

      #the-absolute-box {
        position: absolute;
        background-color: green;
        top: 50px;
        left: 50px;
      }

- Refresh the page and note where the box is
- Resize the window to a size you get scroll bars and scroll around
- Note where the box is when you scroll
- The box should have jumped 50px from the top and to the right of
  the window

- Pick the parent div of the #the-relative-box element and
  give it an inline styling of relative

    <div style="position: relative;">

- Refresh the page and note where the box is
- properties:
  - does NOT remain in the normal document flow
  - offset relative to the position of its closest non-statically
    positioned parent
- Adding the inline style made the row container the "closest non-statically
  positioned parent," which is why the box moved
- Commit your changes



- read for more details: http://www.w3schools.com/cssref/pr_class_position.asp
