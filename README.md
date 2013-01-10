animate-text-content.js
=======================

This JS micro-library allows you to animate the text content of elements in the DOM. It employs the method chaining pattern to construct a timeline of sequential animations.

Example
=======

To start, you select a DOM element by its ID:

HTML

        <div id="exampleDiv"></div>
        
JS

        var example = animateTextContent("exampleDiv");
        
Then, you construct a series of animations, which are placed in a queue in the order they are given.

        example
          .typeIn("I like to eat ")
          .html("I like to eat <span id='fruit'></span>")
          .switchElement("fruit")
          .pause()
          .typeIn("apples")
          .pause()
          .erase()
          .typeIn("bananas")
          .pause()
          .erase()
          .typeIn("oranges");
          
When you want the animations to play, you use `.go()`. 

      example.go();

Caution
=======
Current build state is incomplete. Bugs are likely.