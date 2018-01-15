# 01 What is Jest

William Shakespeare was an English playwright who lived many hundreds of years ago. - In his play King Lear, he wrote this timeless quote, "In jest, there is truth." - What did he mean by this quote? Well, William Shakespeare was around hundreds of years before the library - Jest.js, so he probably did not mean that. _What he meant is that when you mock something or make fun of it, - you often reveal the true nature of that thing, and in Jest, the mocking test framework, we're also going to - find that mocking things really does reveal the truth about them_. - Thanks, Will. 

What is Jest?
 
So basically Jest is a testing framework. It's based on Jasmine. Jest is kind of a super version of Jasmine. 

But really if you ask me the difference, - what's the difference between Jest and Jasmine and Karma, that's kind of it. - It's kind of that **Just has automated dependency mocking**, and we'll be learning all about that.

So how come I am so happy to be testing our React - applications with Jest? 

Well first of all if you've worked with React, and I hope you have, you'll find that - **React's virtual DOM** makes testing with any framework incredibly easy. 

**Historically**, when you're testing your front-end code, most of the time **you need a headless browser**, some kind of - virtual browser like `PhantomJS` to run all your code, run HTML, figure out what's displayed, spit it back - out at you, and then you can analyze that. And this `usually takes a long time and a lot of processing power`. 

> But with the virtual DOM, you can kind of generate your HTML code to test against using just JavaScript.
 
As we know, this is how `React works, creating and diffing a virtual DOM`, **so that DOM already makes testing easy**.
 
Reality: Going a bit further into it, **React applications tend to use a lot of require calls**. - Typically **each one of your different components**, be they a list or a close button, **are all going to be in its own file**, and in your non-trivial app you'll - have hundreds if not thousands of require statements. 

`So when you take these two things and put them - together, you get a really simplified testing flow`. `You don't need a headless browser`, and `you don't have to - worry about the functionality of your other modules leaking into your current tests`. 

    That's what mocking does. 
    
In short, and we'll explain a lot more of this as we go on, when you're using - **Jest, you have to specifically say which modules you want to not mock**, **which modules you want to see the - actual thing of**, and in a React application where you have many modules, and it may be difficult for one - programmer, especially if they did not themselves program all the modules, to understand them, we're going to - find Jest is very, very useful. 

[>>> 02. Understanding Automatic Mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/02)