---
layout: post
title:      "Choosing Stocks with JavaScript"
date:       2020-09-06 19:58:09 -0400
permalink:  choosing_stocks_with_javascript
---

## JavaScript is becoming my favorite language

Everything seems like it is finally coming together. Going from Ruby to Javascript was a challenge because JavaScript is a lot more flexible, and allows you to do more with the language. One of the most challenging topics to master was the concept of asynchronous code. Asynchronous code means that multiple things can be executed at once instead of top to bottom execution. This was the first project where things came to me easier than the previous projects. Seeing a change appear on the DOM was a very satisfying feeling. All of the moving parts made me a little nervous, but "Thank God for console.log()". JavaScript's flexibility can also be a weakness and finding an error takes very careful reviewing.  Here are some of the key principles of JavaScript that I learned.

### Events

Events are what allow the user to interact with the DOM. With event listeners you can listen for certain events such as 'click' and 'keypress'.This is what adds the interactivity to most modern web pages. Now when I visit a webpage and click I understand what makes that click do something on the page. You can also change to functionality of the button by using event.preventDefault(). This allows you to click a button multiple times without refreshing the page. Being able to customize your elements with event listeners allowed a lot of possibilities.


 ```
 
 searchItem.addEventListener('keydown', function(event){
        if(event.key == 'Backspace') {
            searchItem.value =""
            searchContainer.innerHTML = ""
        }
    })
		
	```


### Manipulating the DOM

Being able to update the DOM and make changes appear, really helps me to grasp what separates JavaScript from other languages such as Ruby. JavaScript is a dynamic language that allows you to make changes on the fly. This allowed me to work my way through each step and build my project piece by piece. Being able to use the console in the Chrome browser really helped me to visual the html that was being created and changed. Whenever I got stuck, I would try to make a change in a particular area of code and see how it affected the DOM.


```

const p = document.createElement('p')
p.innerText = `Ticker: ${this.ticker}
                        Company: ${this.company}
                         Current Price: $${parseFloat(this.current_price).toFixed(2)}`
 p.style.color = "white"
 
 ```


### Communicating with the server

Fetch is an easy way to retrieve data from a server. I was able to read, update, and post data to the server with fetch, and turn it into json, which was easy to work with. This is probably the most important part of Javascript. Being able to get data from a server or send data to a server and then manipulate it. I was able to organize my data with my API Ruby backend and manipulate that data in multiple ways with the frontend power of JavaScript.


```

fetch('http://localhost:3000/stocks', {
     method: 'POST',
     headers: {
     'Content-Type': 'application/json'
     },
     body: JSON.stringify(newData)
 })
 .then(response => response.json())
 .then(stock => renderStock(stock))
 
 ```
 
 
 ### Conclusion
 
Overall this was a great learning experience. I look forward to mastering JavaScript. In the future JavaScript will evolve even further. I appreciate that the language is always evolving, as this makes me excited for my future as a Javascript developer.



