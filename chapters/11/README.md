# scaffold folders and package

[<<< 10. scaffolding the App](https://github.com/xgirma/mastering-react-testing-with-jest/tree/master/chapters/10)

So before we begin, let's ask the question why do we test our apps? - Well let's look at the following quote, 

> "Testing leads to failure, and failure leads to understanding." 

We basically write tests because we want tests to fail. If a test can't fail, then it's not a very useful - test as a test that passes 100% of the time doesn't tell us anything about the underlying code. 

So with this in mind, let's discuss our first demonstration. 

    1. First, we're going to make a **_tests_ folder**, 
    
    2. and then we're going to create a **_mocks_ folder**, 
    
    3. and then we're - going to add an entry to **package.json**.

The first thing to do is add a test directory. I'll call that _tests_ with a dunder on either side. **Dunder stands for double underscore**. So any files we put inside this test folder will be run when Jest is called. Next, let's create a _mocks_ folder. The _mocks_ folder doesn't go in your _tests_ folder or in your main directory. It goes in your app directory parallel to any JavaScript file you'll want to be loading. 

Alright, finally we need to update our **package.json** in Jest to work properly. 

**[1.]** we need to describe a preprocessor, "scriptPreprocessor": "<rootDir>/node_modules/babel-jest"
     
A **preprocessor** **is what will be run before Jest runs** to turn our ES6 and React into easily digestible JavaScript code.

**Babel-jest** basically allows us to seamlessly plug in Babel, with Jest.

**[2.]** Next, we need to define what extensions Jest is supposed to test. "testFileExtensions": ["es6", "js"]
    
Now any files that end with .es6 or .js will be tested. 

**[3.]** So this covers our test files, but not the actual files that will be tested,so we'll make a new entry called moduleFileExtensions. "moduleFileExtensions": ["es6", "js"]
    
**[4.]** Finally, we're going to want to collect coverage when we run our Jest test, so all we have to do to make this - happen is make **collectCoverage** `true`. 
    
```diff
{
  "name": "jest-examplar",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "jest",
    "start": "gulp serve"
  },
  "author": "",
  "license": "ISC",
+  "jest": {
+    "scriptPreprocessor": "<rootDir>/node_modules/babel-jest",
+    "testFileExtensions": ["es6", "js"],
+    "moduleFileExtensions": ["es6", "js"],
+    "collectCoverage": true
+  },
  "dependencies": {
    "babel-preset-es2015": "^6.1.18",
    "babel-preset-react": "^6.1.18",
    "babel-preset-stage-0": "^6.3.13",
    "bower": "^1.8.2",
    "browserify": "^12.0.1",
    "ejs": "^2.3.4",
    "express": "^4.13.3",
    "flux": "^2.1.1",
    "gulp": "^3.9.0",
    "jest": "^0.1.40",
    "jest-cli": "^0.7.1",
    "jquery": "^2.1.4",
    "react": "^0.14.7",
    "react-addons-test-utils": "^0.14.7",
    "react-dom": "^0.14.7",
    "vinyl-source-stream": "^1.1.0"
  },
  "devDependencies": {
    "babel": "^6.3.13",
    "babel-core": "^6.3.15",
    "babel-jest": "^6.0.1",
    "babel-loader": "^6.2.0",
    "babel-preset-react": "^6.3.13",
    "babelify": "^7.2.0",
    "browserify": "^12.0.1",
    "d3": "^3.5.10",
    "gulp-nodemon": "^2.0.4",
    "jest-cli": "^0.8.1",
    "nodemon": "^1.8.1",
    "react-tools": "^0.13.3",
    "webpack": "^1.12.9"
  }
}
```

Alright, so our Jest is fully set up. So go ahead and open up your terminal, and run Jest to make sure you haven't made any errors. After Jest has run, you should see your coverage statement, and more or less no message, since we haven't run any tests.

<img width="849" alt="screen shot 2018-01-15 at 4 46 37 pm" src="https://user-images.githubusercontent.com/5876481/34966864-f560c830-fa13-11e7-8169-21a2cd704c67.png">
