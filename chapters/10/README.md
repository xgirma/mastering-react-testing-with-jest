# 10. scaffolding the App

[09. capabilities of mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/09)

So for a quick overview of our app, it's basically a `simple shopping cart app`. It has a few features that you might not see in your average, everyday app like `localization` and `isomorphism`. So the `app can be rendered on the server`, and also it can change the language that the currency has displayed to suit the user's preferences, and behind it all, we're using `Express` to manage the routes.

<img width="1511" alt="screen shot 2018-01-15 at 1 49 18 am" src="https://user-images.githubusercontent.com/5876481/34936655-17a61bca-f997-11e7-802c-236725e0f983.png">

**Babel:** To process the JSX for React and also some ES6, which we've decided to use for this app, we're using **Babel**. `This is important because Babel is also going to be a key component for our Jest testing`, as Jest also must somehow translate JSX and ES6 into regular JavaScript. 

**Express:** We're using Express to respond to HTTP requests and send them out. Now we won't be testing Express too much as Express is best tested with an application called - SuperTest, but `we will be testing our application's interactions with our Express back end using Jest`. 

**React:** We'll be using React to visualize - everything the user's going to see. Not only that, but React is going to run on our front end for the live - single page app and on the back end to facilitate a fast page load 

[11. capabilities of mocks](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/11)