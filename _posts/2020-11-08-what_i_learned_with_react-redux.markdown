---
layout: post
title:      "What I learned with React-Redux"
date:       2020-11-09 04:32:25 +0000
permalink:  what_i_learned_with_react-redux
---

This was my final project for Flatiron and what can I say, this project really helped me hone my skills and combine all of the information I have  learned over the last several months. I really enjoyed React and its overall simplicity. Once you get the gist of how React works it can be a very enjoyable experience. I have a lot to learn because React keeps evolving, but one thing that sticks out to me is React keeps things very organized.here are some of the things that i used in my application.

## Components 
Components are what make React special is it allows us to separate our concerns and logic. There are container components which are in charge of data manipulation and communicating with Redux and presentational components which are responsible for the look of the application. Components are like the different parts of a body. They all do different things and come together in an application. 

## Reducers
In order to set Redux you can run the command:
```
npm install redux
```

After you install Redux these are the steps to create a redux store:


```
1. import { createStore } from 'redux
2. const store = createStore(reducer)
3. <Provider store={store}>
```

Provider allows any nested components to have access to the Redux store by using the connect() function.
After this is all set up you can now dispatch actions to the redux store.


Reducers allow us to change the state of our redux store by dispatching a particular action to the store. The action contains a type which tells the reducer what to do, and a payload which contains the new data. Reducers allow us to easily manipulate the Redux store. Redux was really useful by allowing me to save my state in the virtual DOM and then access that information whenever I needed it 

## Routes
Routing was also another important part of this project. it allowed me to not have to refresh my page and access different components just by routing to specific urls. I was able to make a navigation bar and link those routes to the bar. You can mount a component to a path in two ways:

```
<Route exact path="/" component={Welcome} />
<Route exact path="/profile" render={(props) => <Profile {...props} user={this.props.user}/>}/>
```

If you use render you can pass props to the component.
## Styling
The most challenging but fun part of this application for me was actually styling as I did not have much time to cover the css portion of the curriculum. I was able to learn how to use react bootstrap and combine it with regular css to give my page some basic styling. I look forward to mastering css and making my pages more beautiful. I prefer to use bootstrap for styling main parts of my application and regular css to make small changes.

