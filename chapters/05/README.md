# 05. toggling automatic mocking

[<<< 04. disabling mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/04)

By default Jest automatically mocks everything. 

However, `occasionally` instead of mocking all your modules automatically, - `you're going to want to specifically select the ones you want to mock`.

A good example is if you have a very **small application with only a few modules** and `it actually takes less - time to say what to mock than what not to mock`. So if you call **jest.autoMockOff()**, it will disable this, - and whenever you make a require call, you'll get the correct module. - Calling **jest.autoMockOn()** `restores the default setting` so that all the modules are mocked. 

calling **jest.autoMockOff()** is completely equivalent to calling **dontMock()** on every single dependency, - so there's really not a lot of magic going on there with those two functions. 

[>>> 06. specifying manual mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/06)
