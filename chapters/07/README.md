# 07. defining a pre-processor

[06. specifying manual mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/06)

well it's everyone's favorite part of writing an application that uses **JSX, or ES6, or anything new**, - and that's `working with a preprocessor`. 

So, as you may know, JSX, which is the language of React, - and by extension much of Jest, is not supported natively by Node 4.0, nor is some ES6. 

So when you're writing your test, you're invariably going to have modules that contain JSX if you're writing React components. When those are brought in, Node will throw an error because it doesn't recognize the JSX. 

How can we deal with this? Well we can `define a preprocessor`. So **Jest gives us the opportunity to define a - preprocessor, which will be basically transform the files in any way we want before they arrive inside Node for processing**. - 

Generally, and by generally I mean almost 100% of the time, you're just going to be running your files through some kind of **Babel** variant or **reactify** variant that's going to turn it from JSX to JS.

**It should be noted that Babel, which is generally an ES6, ES2015 sort of processor, also processes JSX with** - a simple React plug-in. Since **it can do both**, you'll typically want your preprocessor to be Babel so that you can take advantage of both ES6 and JSX, which we'll be doing in this course.

<img width="300" alt="rectify" src="https://camo.githubusercontent.com/3dfbcb152a86884d2ef931e3e0ecc3e703ef52f9/68747470733a2f2f64337676366c703535716a6171632e636c6f756466726f6e742e6e65742f6974656d732f31353347326b31543155343433743144317a324c2f72656163746966792d6c6f676f2d322e706e673f582d436c6f75644170702d56697369746f722d49643d643430373439383635383733643762356162333263383038353231353066373426763d3862336563323261">

<img width="300" alt="babel" src="https://raw.githubusercontent.com/babel/logo/master/babel.png">

[08. specifying manual mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/08)