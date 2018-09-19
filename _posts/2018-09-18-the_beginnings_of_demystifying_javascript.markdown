---
layout: post
title:      "The Beginnings of Demystifying Javascript "
date:       2018-09-19 03:45:05 +0000
permalink:  the_beginnings_of_demystifying_javascript
---


 These past couple of weeks, I've attended a few awesome meet-ups related to both vanilla javascript and AJAX. With Ruby as my first programming language, I often doubted my Javascript skills and avoided its convoluted kinks. That was until I learned what was *actually* going on "under the hood", so to speak, and can begin to demystify this incredibly powerful yet initially quirky language. 
 
 I'll be honest here- I'm guilty at using many methods at a very high level and barely knowing *how* they work, but that they do what I need them to do when I need them to do it. Yes, a very honest statement and very, very bad programming practice. Take for instance the fetch API used in Javascript. I knew that it was "fetching" data that I needed from my endpoint or external API but had no idea what was going on within those milliseconds it took to grab that handy data. 
 
 At the most basic level, fetch is essentially making an HTTP request that relies on a promise, which is much like a callback. A promise is a placeholder object for the eventual result value of our fetch method or reason for error will manifest. Now, what happens next is dependent on the execution context of your program. Normally, there are two different functions you can call, then() or catch() depending on the state of fetch. If it's fulfilled, then() is chained to handle any asynch actions that need to happen with the data object fetched from the API. That then returns another promise, which is handled by synch or asynch actions once again. 
 
 One thing to note about fetch() is that we use these promises because of Javascript's single threaded nature. We need a "placeholder" browser object to hold onto the data we need while our code executes so that way we can use this data to make another request if need be, instead of directly handling the result of the initial request. 
 
 Asynchrony in Javascript is tough because of the language's innnate single threaded execution, but once the mystery of fancy browser APIs like fetch() can be demystified, we're able to do cool things like make multiple data requests in a row and have our request send us the callback instead of including it in our original function parameters. Pretty cool if you ask me! 
