# MongoDB Problems
## Troubleshoot Mongoose issues and warnings in NodeJS

When we work with MongoDB within a NodeJS project, we usually use Mongoose, which allows us to work better with this noSQL and non-relational database system in a simpler way.

But ... sometimes this module, Mongoose, can give you some problems or more than problems, it can show you some warnings in your Node.js console.

Notices related to FindAndModify, useNewUrlParser, useUnifiedTopology, and the like.

Today I'm going to show you how to fix these Mongoose issues and warnings in your Node projects.

Mainly we will be working in the index.js file of your project, or in the file where you make the connection to Mongo and create the Node server.

## First Step

Put these two statements before calling mongoose's connect method:

```
mongoose.set('useFindAndModify', false);
mongoose.Promise = global.Promise;

```
## Second Step

Then put this as the second parameter in your mongoose connect method:
`{ useNewUrlParser:true, useUnifiedTopology: true }`


**Remember that all this is done in the index.js of your backend with NodeJS.**

And this will fix these Mongoose problems and warnings
