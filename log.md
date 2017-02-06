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


##Day 13: January 23, 2017

Set up webpack today! Took a bit long because I was reading the doc. But it was fun!


##Day 14: January 25, 2017

**Today's Progress**: Webpack with React and Babel is finally up and running. It took me a while to get the hang of it. I can see how useful this is in a large scale project. There should be a webpack setup somewhere out there!

**What's next**: As part of learning about backend, I thought about ways to fectch data from server to the client. It seems like two round-trips (fetch data after loading initial page) aren't that bad most of the time. I will implement that.


##Day 15: January 26, 2017

**Today's Progress**: Wasn't too productive today. Too tired from work :/ But I did some jquery to get card data from the server.

**What's next**: I'm planning to use Materialize to make things pretty!


##Day 16: January 27, 2017

**Today's Progress**: Implemented the get cards data function with jQuery.

**Thoughts**: Tons of frameworks out there. Web dev is quite convenient and light weight!


##Day 17: January 29, 2017

**Today's Progress**: Learned some jQuery and started looking into Materialize CSS. It looks fancy!


##Day 18: January 30, 2017

It was pretty fun to set up Materialize! Also played around with some css components.

**Thoughts**: webpack made it very easy to load up Materialize CSS. A steep learning curve still, but it just makes things so much easier after the inital setup!


##Day 19~25: February 5, 2017

I've been writing a [Redux app](https://github.com/domingohui/frontend-challenge-starter) as part of applying to be an organizer of Hack the North! It was my first time trying out Redux with React! It was a lot of fun. I definitely still have tons to learn. I'm also very happy to be able to setup webpack to use Materialize, React, custome CSS, and bunch of other things! webpack doesn't seem to work very well with Sass. I hope to get a chance to look into that!
I was also excited about using the isomorphic fetch to do some async with the thunk middleware!

**Thought**: I find debugging in Redux much easier than in just React. With Redux, everything flows in one direction while all of the data stays in one place. I feel that React definitely enforces the pardigm of unidirectional flow of data, but states (of each component) are still kinda scattered within and between each component. Not having a huge state tree could lead to better performance, but a tradeoff is that bugs are harder to find. 

In Redux, components (aka the view? the presentational components) dispatch actions which get passed to reducers, along with the current state (aka the model?). Reducers interpret the actions and the state and then create a new copy of the updated state. Components get rerendered if necessary, and actions are dispatched again. 

One of the things that I'm still thinking about Redux is its efficiency and performance. It looks like reducers make copies of the state everytime an action is dispatched even though, after all, unchanged segments of the state are just passed to the new state as a reference. But to perform a search, for example, it would still need to iterate every single entry even though some of them are not shown yet. I haven't been able to find a way to efficiently (re)render chunks of data. Maybe that's one tradeoff of using something functional like Redux. I haven't tried React's ListView, but it could be a way to more efficiently display data? I'm curious. A normalized state, as suggested in the Redux doc, also makes a lot of sense. 

I'm not too sure about this because I haven't really encountered this problem so far. If a slice of the state is dependent on one or more other slices, would it be a bit messy to [pass them around](https://github.com/reactjs/redux/issues/749)? I guess it's always better to set up the state so that each part can be "computed from lesser state" if necessary. The only downside is to write more reducers and/or actions to correspond each segment of the lesser state. 

**What's next**: Experiment with Listview/Scrollview to see if/how much they help in a sizable Redux front end. Also it's time to explore different kinds of starter kit out there. I also wonder how others set up their boilerplates. 

**EDIT**: Apparently, [Reselect](https://github.com/reactjs/reselect) is built just for optimizing displaying the views! Will definitely check that out.
