# 08. mock functions

[<<< 07. defining a pre-processor](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/07)

By now we have a good idea of what a mock module is, but what's a mock function? 

Well, in your app it's highly likely that your modules are requiring other modules and that those modules - are taking advantage of functions that the modules have to offer. 

For example, a module may have an AJAX post method that makes it convenient to make a post request to a particular API. 

**When you require that module in a Jest test, the function will still be there, but it will be removed of all functionality**. 

`It will be what you might call a mock function`. So `when a mocked version of a module comes in, - it doesn't have its real methods`. All its **methods will be automatically replaced by mock methods**. 

**Mock methods are not stubs** because `they keep track of various things related to the function`. 

For example, a mocked method of get AJAX post would `remember how many times the argument is called, - with what parameters it's called, and then also you can specify specific things for it to return to make your - test happen in a predictable manner`. 

> So mock functions are very useful.

[>>> 09. capabilities of mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/09)
