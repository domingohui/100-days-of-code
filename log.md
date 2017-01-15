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


## Day 3: January 13, 2017

**Totay's Progress**: Read up more about React component rendering. Also figured out how to pass data from a Django server to.

**Thoughts**: By passing data to a global variable through a Django template is probably not the best idea, but will experiment it for now :P


##Day 4: January 14, 2017

**Today's Progress**: Halfway through implementing showing a card's data. ReactJS is interesting! Still playing around with state and props.

**Thoughts**: Seems like the only side effect of passing data through a global at server rendering is polluting the global scope. Will read up more about state and props.
