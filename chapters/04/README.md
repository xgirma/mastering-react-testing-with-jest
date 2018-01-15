# 04. disabling mocking

[<<< 03. understanding Jest API](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/03)

```javascript
jest.dontMock("myModule");
```

**Most of the time, the vast majority of the time, we're going to want to disable mocking for a single module.** - Let's look at how this works. 

In any test framework you're going to have your test, and if it's on Node, - the test is usually going to pull independencies. When your test pulls in a dependency, - **Jest is automatically going to convert that dependency to a mock**.  

`Now if you call dontMock on a file`, it will replace that file - with the actual module. 

So by disabling mocking for a single module and - sometimes two or three, you can make your tests a lot simpler. 

What happens when you have **libraries like jQuery in your tests**? 

So libraries like jQuery are usually **not mocked**. Usually, you want the actual jQuery. - 

Why is that? 

Well generally libraries like jQuery, Underscore already have a lot of tests. - They're tested by other people, so you can generally, with a great amount of caution, assume that they're - going to work properly. 

Libraries like jQuery and Underscore just kind of make up the backbone of our application. So if we mocked jQuery, **we'd find ourselves really often having to write in stubs for jQuery**, `say AJAX functions`, which might be better off left as they are. 

:tropical_fish: :tropical_fish: On that note, you usually do want to replace any sort of asynchronous functionality in your tests because - they tend to make your tests run very slow. :tropical_fish: :tropical_fish:

So with libraries like jQuery, you're going to have to **manually - specify you don't want these to be mocked, and you do that in a special field in the package.json file.** 

> Manual don't mock => package.json

[>>> 05. toggling automatic mocking](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/05)