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
    - all boxes get the same styling because they share the class "box"
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



- Inspect one of the boxes using Chrome Developer Tools
- Mouse over the box model and take note of the different parameters
  - margin
  - border
  - padding
- Note that the margin and padding are blank, and that the border is set to 1
- Note the value of 1 for border comes from the border-width parameter in the
  div.box styling (to the left of the box model)



- Update the CSS to set the border-width parameter to 10px
- Note how the values in the box model changes in Chrome Developer Tools
- Note how the border is thicker on all sides of all boxes in the page
- See http://www.w3schools.com/cssref/pr_border-width.asp on how to target
  each side of the elements individualy
- Commit your changes



- Update the CSS to set the padding parameter to 10px
- Note how the values in the box model changes in Chrome Developer Tools
- Note how the distance between the text and the border is greater than before
- Note how the entire box grows to accommodate the padding in addition to the
  content size
- See http://www.w3schools.com/css/css_padding.asp on how to target each side
  of the elements individually
- Commit your changes



- Update the CSS to set the margin parameter to 10px
- Note how the values in the box model changes in Chrome Developer Tools
- Note how the boxes are no longer touching and have space on all sides
- See http://www.w3schools.com/css/css_margin.asp on how to target each side
  of the elements individually
- Commit your changes



- block and inline are the standard display properties. Now there are new
  types like inline-block and flexbox that help alleviate some of the
  issues/restrictions of only have the two layouts, but those are more
  advanced
- To break out of the standard block (top to bottom) and inline
  (left to right) flow, positioning can be used
- "static" is the default positioning that is used if explicit positioning
  is not set



- Pick any box and give it an id of "the-fixed-box"
- Add styling to set the background-color of this element to red
  so it can be easily differentiated
- Add styling to set the display value for this element to absolute
- Note where you red box is
- Refresh the page and resize it to a size you get scroll bars
- Scroll around and see how the box moves relative to the page
  - When positioned in a _fixed_ manner, an element:
	- will NOT remain within the normal flow of the document.
	- will be offset with respect to the window.
	- will remain in place on scroll.