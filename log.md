# 100 Days Of Code - Log

### Day 0: January 10, 2017

**Today's Progress**: First day of 100 days of code! Finally got back to working on my cue_card app, which was suposed to be finished long ago... Fixed up some old ReactJS code.

**Thoughts**: I'm new to webdev. I was going to build the cue_card in Django only. But I want to learn about front end using ReactJS too. So I'll be using that to build the front end and Django just for a REST api for now. I will (hopefully) also be doing the ReactJS tutorial at the same time!

**Link to work:** [Cue_card App](https://github.com/domingohui/cue_card)


### Day 1: January 11, 2017

**Today's Progress**: I decided not to use React to render the index page, but will use it to present actual cards. Will keep reading the ReactJS tutorial. I also fixed up the serializer to make it easier to communicate with DB.

**Thoughts**: Eventually, I wnat to be able to send data (how long the user has spent reading the card, how many times it's been read, etc) from the present_card page to the server. Don't know if this is doable using only JS without reloaidng or even sending a POST response. So the app doesn't have to reload the page hopefully. 

**What's next**: Will start working on building present_card page wiht React.


### Day 2: January 12, 2017

**Today's Progress**: Wrote a minimal present_card page with ReactJS. Finishing the ReactJS tutorial.

**Thoughts**: It seems that it's fairly trivial to render data to a ReactJS from the server. But it'd be interesting to see how to push/post data back to the server.


### Day 3: January 13, 2017

**Totay's Progress**: Read up more about React component rendering. Also figured out how to pass data from a Django server to.

**Thoughts**: By passing data to a global variable through a Django template is probably not the best idea, but will experiment it for now :P


### Day 4: January 14, 2017

**Today's Progress**: Halfway through implementing showing a card's data. ReactJS is interesting! Still playing around with state and props.

**Thoughts**: Seems like the only side effect of passing data through a global at server rendering is polluting the global scope. Will read up more about state and props.


### Day 5: January 15, 2017

**Today's Progress**: State, props and lifecycle are much clear now! I removed a few unnecessary state properties. I also started working on gathering analytics.

**Thoughts**: React's state and props make a lot of sense now. Also, apparently, the JSON data rendered and passed to HTML from Django is just injected into the script. It's kinda ugly tbh. 

**What's next**: Will find a better way to pass data from Django. Also need to start working on the CSS soon!!


### Day 6: January 16, 2017

**Today's Progress**: Picked up some CSS for the first time!

**Thoughts**: TIL it's surprisingly easy to implement animations with CSS! It's a bit inconvenient to toggle CSS classes in React, unlike other libraries like jQuery. But it's still pretty interesting and efficient to render components with different properties that depend on each other!

**What's next**: Need to keep working on displaying a card properly with nice CSS.


## Day 7: January 17, 2017

**Today's Progress**: Instead of working on the app, I was setting up yarn and the dependencies of the app. Didn't get to finish tho. Will keep working on getting Babel compiler running properly tomorrow!


## Day 8: January 18, 2017

**Today's Progress**: Had to do something in the work repo... Sorry!


## Day 9: January 19, 2017

Need to rest up for a hackathon tomorrow. Will try harder. 


## Day 10~12: January 20 ~ 22, 2017

We were building a note editor that handles all of the fancy foramtting (bullet lists, highlighting, headers, generating headers based on contents, etc). But we didn't have enough time to finish it :/ Hopefully, over the next week, I can finish it and make it better over time.

ReactJS, node JS.

Also learned how to use Webpack to set up all modules locally including Babel. It's such a steep learning curve!! But worth.
