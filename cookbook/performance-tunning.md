Performance Optimization  
==============================

First off, lets be clear that Meteor is simply Javascript and Node.js.  Yes, it's a very specific implementation of those two technologies, and has it's own unique ecosystem, and leverages isomorphic APIs and a JSON datastore to achieve some truly amazing results.  But, at the end of the day, Meteor is a web technology, and it's written in Javascript.  So all of your typical javascript performance techniques still apply.  Start there.

===========================
####Tutorials on Writing Performant Javascript

If you're not sure how to optimize your javascript, here are some tutorials that we've found useful.  

[25 Javascript Performance Techniques](http://desalasworks.com/article/javascript-performance-techniques/)  
[Performance Optimizations for High Speed Javascript](http://www.webreference.com/programming/javascript/jkm3/index.html)  
[Optimizing JavaScript Code](https://developers.google.com/speed/articles/optimizing-javascript)  
[Performance Tips for JavaScript in V8](http://www.html5rocks.com/en/tutorials/speed/v8/)  
[10 Javascript Performance Boosting Tip](http://jonraasch.com/blog/10-javascript-performance-boosting-tips-from-nicholas-zakas)  
[Write Efficient JavaScript](http://oreilly.com/server-administration/excerpts/even-faster-websites/writing-efficient-javascript.html)  
[Improving the Performance of your Meteor JS projects](http://projectricochet.com/blog/meteor-js-performance#.U-lvxo1dWnD)

===========================
####Designing and Deploying Production Ready Software  

Also, all the best practices of typical web architecture still apply.  As such, I recommend Michael Nygard's excellent, excellent book [Release It!  Design and Deploy Production-Ready Software](http://www.amazon.com/Release-It-Production-Ready-Pragmatic-Programmers/dp/0978739213).  Writing your app in Meteor doesn't absolve you of auditing third party libraries, writing circuit breakers, wrapping calls in timeouts, monitoring your resource pools, and all the rest.  If you want your application to perform well, you need to make sure you're using stability patterns, and avoiding anti-patterns.  

**Stability Patterns**
- Timeouts
- Circuit Breakers
- Bulkheads
- Handshaking

**Stability Anti-Patterns**  
- Integration Points
- Third Party Libraries
- Scaling Effects
- Unbalanced Capabilities

**Capacity Anti-Patterns**  
- Resource Pool Contention
- AJAX Overkill
- Overstaying Sessions
- Excessive White Space
- Data Eutropification

If these things are unfamiliar and don't seem like second-nature to you, it means that you haven't brought bigger production systems online.  Buy a copy of the book.  It will be time and money well spent.  

===========================
####Kadira

Okay... so, you've compressed all your images, linted and optimized your javascript, reduced resource bottlenecks by using servers with SSD drives, audited all of your 3rd party libraries, used content-delivery-networks to cache image assets as close to your users as possible, written your application with timeouts and circuit-breakers... you've done all that, and your app is *still* slow.  It's not the website.  It's something with Meteor.  And you need an industrial-strength solution.

You need [Kadira](https://kadira.io/)

![Kadira Screenshot](https://kadira.io/images/intro.png)  

Kadira is a performance profiling application that can do wonders for optimizing your application.  But it's also an advanced tool that's maybe best used when your application gets a little larger and you're trying to get it into production.  When you start using it, your knowledge of Meteor will drastically improve.  Yet, at the same time, you'll also need an application of sufficient complexity for it to be useful.  And you'll need to make sure that the issues are with Meteor, and not all the other parts of your application.  For those reasons, it's a tool that's perhaps more useful at the middle and end of your development process, rather than at the beginning.
