# 02. understanding automatic mocking

[<<< 01. what is Jest](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/01)

So what is automatic mocking? Why does Jest mock modules automatically, and why is it important to us as developers? 

So in your typical Node.js app you have many require statements. In a large-scale application, you may find that there are thousands of require statements. Now when you're running tests, it can be very - difficult to account for all these different require statements, so how does Jest help this?

In order to test your Node.js application, you're going to have to write many tests, and those tests are all - going to make require statements that are going to go inside your Node.js app and get different pieces of - files, different modules that are going to test.

Now if all these tests are just going into your app, - they're going to pull all kinds of files that are already being tested by other tests. - **For example, you're testing your contact list app, it may use functionality from say a mathematics component, - which you have been tested somewhere else**. 

**Automated mocking allows mocks to exist in your test, - which automatically replace the requested files with a mock with no functionality.** 

> That means when your contact list app calls require in the context of the mock test, instead of getting your - mathematical module, you're just going to get an empty mock. This means that an error inside your math - module can't possibly cause an actual error in the test for your contact list module. 

_So what is mocking in a programming context_? 

So to be a bit technical, mocking is the process of replacing a module with a **generic and mostly empty** - object, and we call this object a mock.

So you can imagine in a piece of code when you're calling a require - statement what you're getting back is a module. However, `if you use automatic mocking`, it's going to - automatically send you a mock of that module or `a mostly empty object`. 


So why would you want this? 

**Well once you have a mock, you can give it a specific functionality**. - So going back to our previous example, if you have a math module that has lots of useful math functions, - and there's one that say returns a number from 0-1 based on some complex calculation, and it could really - return anything from 0-1, you could mock that with a function that just returns a random number. Since the application could return anywhere from 0-1, you're still getting the full width of the test. 

:poodle: **Also, this is very important, a mock is not a stub.** :poodle:

:hatched_chick: `A stub is just an empty object with literally more or - less no functionality`. However, `mocks have many useful features`. :hatched_chick: 


The mocks inside Jest can 

    1. keep track of how many times a function has been called,
     
    2. it can keep track of what a arguments with which a function has been called, 
    
    3. it can even implement functions - that automatically return specific values. - 
    
So many frameworks support mocks, or even if they don't, you know, you could always create your own mock - because `it's just an object with no special powers`. Some do not support mocking at all. 

> So with Jest, all the modules are mocked by default. 

Rather than specifying what you do want to mock, - you have to specify what you don't want to mock. This kind of seems confusing, but believe me it is - absolutely amazing in a practical sense. You can actually focus on the module you're trying to test when - you're writing tests for it. This leads to much better testing. 

So comparing a typical framework like Jasmine with an automatic framework like Jest, we can see that in Jest - the user defines what not to mock, whereas in another framework like Jasmine the user defines what to mock. - **That's why Jest is an automatically mocking test framework**. 

<img width="1079" alt="auto-mocking" src="https://user-images.githubusercontent.com/5876481/34926881-42ef3058-f967-11e7-9a2d-1f3ca5e1151c.png">

So basically what I'm trying to tell you here is that 

> in short all modules are mocked by default with automatic mocking. 

So when you first open up your Jest application and you see all your modules are replaced by mocks, - don't be surprised because we've talked all about it, and this is the big thing about Jest that we're going - to want to deal with. 

**Advantages of mocking** 

Why do we - want to use mocks, why should I switch from Jasmine or Karma, why should we do any of this automated mocking testing?  

**[1]** **mocking isolates your code - from the other code it's dependent on**. So with automated mocking you're just taking that, you're taking all those dependencies, you're just taking - them and you're `throwing them in the dustbin`, forgetting about them, and you're isolating your code from your dependency. - So when you require a file in an automatic mocking situation, `you just get that file`. 

**[2]** No need to change tests after change to dependencies. 

**[3]** Reduce false positives. In addition, you reduce false positives by removing unknown elements of code from your test.

**[4]** Tests are less fragile. 

**[5]** Easier for other developers to understand. when you write a test with mocks, - you're forced to specify everything that's supposed to go inside that test right in that file.

[>>> 03 understanding Jest API](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/03)
