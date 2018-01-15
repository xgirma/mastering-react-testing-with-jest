# 03. understanding Jest API

[<<< 02 understanding automatic mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/02)

An in-depth look at the Jest API.

So as we've touched on previously, **most Jest methods relate to mocking**. - 

Other test frameworks exist, which already provide tests, but Jest kind of takes the framework already - provided by Jasmine and adds a lot of mocking capability to it. 

**dontMock**

> Of all the Jest API methods, dontMock is the - most common one

Jest is the `automatic mocking framework`, - so it's going to mock everything unless you call dontMock on that module. 

Now, as mentioned, Jest is based on Jasmine, so you'll see a lot of familiar syntaxes. - Jasmine supports both the TDD and BDD method of testing. 

You're probably more familiar with the BDD style, - which includes common keywords like **describe** and **it**. So if you have any knowledge of Jasmine, you'll be able - to apply it to everything you do in Jest. 

Generally going to be working with mocks when you're doing Jest. - A lot of this course will be about learning what do the mocks that Jest provides have, what functionality do - they have because, as we know, **mocks contain a lot more functionality than mere stubs**.

[>>> 04. disabling mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/04)
