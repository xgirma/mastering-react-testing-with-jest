# 09. capabilities of mocks

[<<< 08. mock function](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/08)

What can a mock do? Is it really that much more than a stub? And the answer is yes. Mocks actually do a lot.

**[1]** So a **mock can return a predetermined value**. So if you're mocking an AJAX function, you can return a simple and predictable JSON object every time. You don't have to define something special for this. Mocks have this functionality built-in for you to leverage. 

**[2]** After your tests are run, you can verify things have been going correctly by `counting how many times your function has been called and has it been called with the correct arguments`. - Mocks make this very easy. 

**[3]** Next, if you mock a module, **you can keep track of how many times that module has been instantiated**. Has it only been created once, or somewhere in your code is it being created three times, and that's what's causing this unexpected behavior? Mocks make this trivial to do. 

So `all this information is going to be available in the mock property of those mocks`, so you can access them very easily and test their values against your tests. 

Finally, as if all that functionality weren't enough, **Jest has some custom matchers** as well that you can use with your mocks. 

So you could say expect and then pass your mock method, and then say **toBeCalledWith** and `pass the arguments - that it was expecting`. 

[>>> 10. mock function](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/10)