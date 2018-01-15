# 06. specifying manual mocks

[<<< 05. toggling automatic mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/05)

Now often you'll want to have **functionality on your mock**. Your mock may need to have sort of **a shell function** so that you won't get an error when the module they're actually testing calls it expecting it to exist. 

Jest offers us **two ways of creating a manual mock**

**[1]** Jest allows us to use a **mocks folder with a dunder**, - or a double underscore on each side of the word mocks. 

Now any files we put inside that **_mocks_** folder will - be automatically called if they match the name and path of a file that is being mocked.
 
`Example`: So if in my app directory I have **app/component.js**, that's going to be automatically mocked by Jest naturally, but if I have in my _mocks_ folder **__mocks__/app/component.js**, that JS file will actually be substituted in the place of an empty mock. 

**[2]** On the other hand, I can simply **require my mocked module** and add functionality to it on the fly. 

Typically you're going to want to use the _mocks_ - folder if you're reusing a mock multiple times. So perhaps you have an AJAX module, which makes an AJAX request. However, for your mock, it's much more appropriate just to have a really short, simple timeout and then - return a prepared value, so you might have the function that does that in your _mocks_ folder. 

[>>> 07. defining a pre-processor](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/07)