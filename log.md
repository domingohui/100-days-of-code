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


##Day 19~29: February 9, 2017

I've been writing a [Redux app](https://github.com/domingohui/frontend-challenge-starter) as part of applying to be an organizer of Hack the North! It was my first time trying out Redux with React! It was a lot of fun. I definitely still have tons to learn. I'm also very happy to be able to setup webpack to use Materialize, React, custome CSS, and bunch of other things! webpack doesn't seem to work very well with Sass. I hope to get a chance to look into that!
I was also excited about using the isomorphic fetch to do some async with the thunk middleware!

**Thought**: I find debugging in Redux much easier than in just React. With Redux, everything flows in one direction while all of the data stays in one place. I feel that React definitely enforces the pardigm of unidirectional flow of data, but states (of each component) are still kinda scattered within and between each component. Not having a huge state tree could lead to better performance, but a tradeoff is that bugs are harder to find. 

In Redux, components (aka the view? the presentational components) dispatch actions which get passed to reducers, along with the current state (aka the model?). Reducers interpret the actions and the state and then create a new copy of the updated state. Components get rerendered if necessary, and actions are dispatched again. 

One of the things that I'm still thinking about Redux is its efficiency and performance. It looks like reducers make copies of the state everytime an action is dispatched even though, after all, unchanged segments of the state are just passed to the new state as a reference. But to perform a search, for example, it would still need to iterate every single entry even though some of them are not shown yet. I haven't been able to find a way to efficiently (re)render chunks of data. Maybe that's one tradeoff of using something functional like Redux. I haven't tried React's ListView, but it could be a way to more efficiently display data? I'm curious. A normalized state, as suggested in the Redux doc, also makes a lot of sense. 

I'm not too sure about this because I haven't really encountered this problem so far. If a slice of the state is dependent on one or more other slices, would it be a bit messy to [pass them around](https://github.com/reactjs/redux/issues/749)? I guess it's always better to set up the state so that each part can be "computed from lesser state" if necessary. The only downside is to write more reducers and/or actions to correspond each segment of the lesser state. 

**What's next**: Experiment with Listview/Scrollview to see if/how much they help in a sizable Redux front end. Also it's time to explore different kinds of starter kit out there. I also wonder how others set up their boilerplates. 

**EDIT**: Apparently, [Reselect](https://github.com/reactjs/reselect) is built just for optimizing displaying the views! Will definitely check that out.


##Day 30: February 11, 2017

**Progress**: Refactored and modulized some components in my cue card app.

**What's next**: Add navigation and data persistence.


##Day 31: February 12, 2017

**Progress**: Added navigation buttons on the cue card app! 

**What's next**: For data persistence on Django, I need a csrf token for security purposes. Will read more aobut it tomorrow! 
**Thoughts**: On a side note... I was using [react-table](https://github.com/tannerlinsley/react-table) in my first Redux app a few days ago. But I was bumping into some issues with the component (It's super neat, convenient and fast otherwise!). I would consider my problem as an unusual edge case. But I opend an issue anyway, and it was fixed in a day! I'm starting to fall in love with the open source community. I can't wait to see what we are going to build in the future! 


##Day 32: February 13, 2017

**Progress**: I read a bit on [CSRF(Cross-Site Request Forgery)](https://en.wikipedia.org/wiki/Cross-site_request_forgery). It's interesting to see how Django protects a site from CSRF attacks. I learned how to set up CSRF on client side and on Django side. For Django-rendered/managed templates, it's super easy - just add [{% csrf_token %}](https://docs.djangoproject.com/en/1.10/ref/csrf/#how-to-use-it) inside a form. 

But for dynamically generated forms on a template (e.g. using ReactJS to manage views and input components), it's a bit tricky. Since Django inspects [HttpRequest.POST](https://docs.djangoproject.com/en/1.10/ref/request-response/#django.http.HttpRequest.POST) for a csrf cookie (that is generated when the template is rendered and sent to client) to make sure data from client side hasn't been compromised and thus become potentially malicious, the csrf token must be present there within the POST QueryDict. The catch is that only *FormData* gets sent to the request.POST QueryDict. 

Using the {% csrf_token %} in the template is still a must. But, eventually, I use [js-cookie](https://github.com/js-cookie/js-cookie) to retrive the csrf cookie value on the client side (just ```Cookies.get('csrftoken')```). Then, I add it to a formdata along with other data that I want to send to the Django server. Also, when using the [fetch api](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch), it's important to set the ```credentials``` field to ```'same origin'```. It's a bit of digging to find out how Django the csrf middleware internally checks for the csrf token. But it makes sense to only look at FormData in a POST request since that's how Django templates are intended to set up anyway. 

An alternative would be setting the csrf cookie value within the [headers](https://docs.djangoproject.com/en/1.10/ref/csrf/#ajax).

**What's next**: Will implement data persistence fully soon.


##Day 33: February 14, 2017

**Progress**: Data persistence is working on my app! This is exciting. I will add more functionalities - adding and removing cards - soon. I'm also going to play around Google App Engine and hopefully get to test [trump2cash](https://github.com/maxbbraun/trump2cash) which is super cool :D


##Day 34~36: February 17~19, 2017

I was on a data science hackathon over the weekend. A lot of first time's for me! I learned R and used it to clean up data. I didn't know that there would be so many things to look out for. How to fill in/remove missing data, which features can we afford to drop, what specific columns mean, how to interpret missing data (also the invalid/unknown types). All without affecting accuracy at the end. 

The next thing is to evaluate which methods to use to train a model. Without in-depth knowledge of the maths behind the methods, it's almost impossible to get good insights, except trying different methods. We had medical data on diabetes. We thought of using a simple linear regression on it, but it didn't work quite well. A deep neural network would be nice, except that [TensorFlow](https://github.com/tensorflow/tensorflow) wasn't able to work with categorical columns very well yet. We either had to apply [One Hot columns](https://en.wikipedia.org/wiki/One-hot) on the data (which would take some time) or just stick with continuous columns (continuous data type obviously wouldn't be as accurate for categories) (Otherwise, TF is a great tool - also no one hot columns needed for a DNN). At the end, we decided to try a random forest which yielded 88% accuracy for predicting how a diabetic patient will be discharged (leave) from the hospital. 

Time to tackle some Kaggle challenges!


##Day 37: February 21, 2017

**Progress**: I improved the webapp from the hackathon in terms of views and navigation. I also touched up on the [R code](https://github.com/domingohui/deep_health/blob/master/training_model/clean_up_raw_data.R) that I used to clean up the data. It assigns separate categories for missing/invalid data now. I don't know how keeping missing data will impact the accuracy of the model. I'm going to try exploring gradient boost and random forest tomorrow. And see how good the models will be.


##Day 38: February 22, 2017

**Progress**: It took me a while to set up jupyter notebook within a virtualenv. I didn't realize jupyter should be installed within the virtualenv as well. The global jupyter doesn't care about virtualenv. It's time to dig into [scikit-learn's random forest](http://scikit-learn.org/stable/modules/ensemble.html#forest) now. 


##Day 39: February 23, 2017

**Progress**: Using scikit-learn, I built my first model on a huge dataset using random forest! It's impressive to see how the machine can just crunch those data so fast. I only had around 80% accuracy. I suspect the missing data category and the random diagnosis types contribute to the relatively high bias of the model. 

**What's next**: I need to rethink how to treat the missing data, and group the minor categories in a better way, perhaps ignoring them would be best if they are not that frequent. 


##Day 40~41: February 25~26, 2017

**Progress**: I started working on my [portfolio site](https://domingohui.github.io). I decided to use Jekyll because it's pretty easy to set up. Static sites generated by Jekyll are also very fast and sufficient as a portofolio site. It's also highly customizable. One advantage of Jekyll (or another static site generator) v.s. CMS is that I don't have to deal with databases. I also don't have to store my content on a third party site.

**What's next**: I will be working on the [deep_health](https://github.com/domingohui/deep_health) app while putting more content on my portfolio site in the next few weeks. 


##Day 42~45: February 27~March 2, 2017

Oops, I haven't been updating the log for a while! But I've been working on my [personal site](https://domingohui.github.io) lately. It's pretty fun building it with [jekyll](https://jekyllrb.com/) using the [minima theme](https://github.com/jekyll/minima) (for now). I also added some of my thoughts and progress from a data science hackathon on the site, in jupyter notebooks. 

I also improved the [deep health webapp](https://github.com/domingohui/deep_health/tree/master/app_doctor) a bit. It's time to work on the looks and its workflow :D Over the weekend, I really hope I can finanlly get a chance to dive into a D4D project - [internal displacement](https://github.com/Data4Democracy/internal-displacement) - it's a super cool project that combines data science with politics and the society. I really want to get involved in that. 


##Day 46~48: March 3~5, 2017

I stumbled upon the Google Foobar challenge while at work. I worked through the first two levels over the weekend. Feel free to follow my progress and submit better solutions and more questions [here](https://github.com/domingohui/google_foobar)!

I'm also working on a [D4D project](https://github.com/Data4Democracy/internal-displacement/).

##Day 49: March 6, 2017

More foobar!

##Day 50~51: March 7~8, 2017

Can't believe I'm already halfway through the challenge! It seems that I'm getting used to coding a bit everyday. It's always nice to learn something new everyday. 
I also started looking into the [D4D project](https://github.com/Data4Democracy/internal-displacement/). I'm also falling in love with the idea of open-source projects. Working with a team brings more diverse approaches and ideas to the project. It's also a great chance for me to get started with NLP. 


##Day 52: March 9, 2017

Cleaned up my D4D PR a bit. I also did another challenge in the Google foobar. TIL recursion is fun, intuitive and useful until there are thousands of stack frames. Optimization is possible, but much more easier to be done with an iterative approach. 


##Day 53: March 11, 2017

Tried running Docker today on an open source project. Docker is great since it provides a common environment for contributors to run the project. I find that issues are much more reproducible in a Docker environment. 

Quick thoughts on open source projects:

I haven't been working on open source projects for a long time. But so far, I really enjoy seeing commits, PRs coming from different members of the project everyday, while doing that myself at the same time. It's amazing that people dedicate their free time to work on a project over time. Knowing that I am part of a bigger team, even thought we don't see each other everyday, makes me more motivated to put in more efforts. While working alone, you know that people are less likely to see and use your code. But, in an open source project, documentation and code quality in general become very important. Others working on the project depend on the code I've written and need to understand what it does. The subtle but impactful extra responsibility that puts it on each contributor's shoulders is what makes open source code the best code. 


##Day 54: March 14, 2017

Nothing much today. Wrote a bash script that navigates to the root directory of a git project. It solves my super niched need to navigate through the folders in a project. Check it out [here](https://github.com/domingohui/up)!

##Day 55: March 15, 2017

I started learning Vue JS today. It's kinda related and comparable to ReactJS. I find Vue js more lightweight than React. And the fact that one doesn't have to use Babel or webpack to build a simple app is very attractive. I haven't had much experience with Vue js yet, but one downside is that variables (props) in HTML (and even in js when they are declared) are not strongly linked. They are written in plain old string which makes debugging a bit hard. But the dev tool comes in handy.

Check out the [little app Initial Commit](https://github.com/domingohui/initial-commit) that lets you find the earliest commit of a git repo! 
