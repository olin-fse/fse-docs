## FSE Project Blueprint Guidelines

### Welcome

Welcome to the FSE Project Blueprint Guidelines. This document should walk you through everything you'll need to know to create a successful blueprint! 

**Remember! This document is as much for you as it is for us.**

After you've read through these guidelines, take a look at our [example blueprint](https://drive.google.com/open?id=1PjJR-U7jhpOoL7t2SwpDcnfYNZ6zstw0pcCaE7JGdOs) for Shawty, the next big name in URL shortening services.

##### Submission

Please create your blueprint as a pdf or markdown file in your project repository. To submit, use [this link](https://goo.gl/forms/pOrAnyf69azAs1NF2).

_One submission per team._

### Blueprint Guidelines

At the very minimum, your project blueprint should include the following:

##### Names
Who are you?

##### Project Abstract
Give us the 10,000 foot view of what you’re trying to accomplish.

##### Goals
Think about both your individual and team goals. This is by no means final, but this will help us orient our discussions when meeting with you and discussing 

##### Feature Set
Give us a comprehensive list of the feature set your application will include. Please group these into the following categories:

- **MVP** | The things that define your Minimum Viable Product
- **Next Steps** | The critical features that you think you'll have time for
- **Stretch Goals** | If you end up having extra time, what do you want to accomplish?

##### System Architecture
This is the most important section. Take some time with it. 

In this section, guide us through the technical details of what you're envisioning for your project. One of our major goals for you in this class is to learn how to effectively communicate technical designs and decisions, so treat this as an exercise in creating a formal technical design document. 

Before continuing, please read this quick (less than 5 min read) [blog post](http://blog.slickedit.com/2007/05/how-to-write-an-effective-design-document/) on How to Write an Effective Design Document written by Scott Hackett. 

Hackett writes a good deal about backing up decisions with convincing justifications. In The Real World<sup>TM</sup>, these should be grounded in sound technical arguments based on the requirements given.

For instance:

    We expect the operations on our database to be extremely read-heavy, so we will use _FastDB_ for its high read performance.

This is a class, however, and as such, personal growth and learning are acceptable justifications. 

As an example:

    We plan on using PatLang with HieuJS because we prioritize learning these technologies.

As a recommendation, consider thinking about the following questions when creating this section:

- What are the major components that will make up the system? Why are these the components? How do they interact? (Words/diagram, whatever you see fit) 
- What technologies might you use to build these components? Think about languages, frameworks, databases, testing suite, etc. 
    - What are the tradeoffs you're aware of between various options? 
    - What level of familiarity do you have/what would estimate the learning curve to be?

For a real-life example of evaluating technology options, take a look at this [blog post](http://eng.uber.com/go-geofence/) from Uber on February 24, 2016. Specifically, take a look at the section called _Ready, Set, Go!_ in which the author describes the key decision points in writing this new service in Go over Node.js. 

#### Project Timeline

In the format that will be most useful to you, give us a rough idea of what you view your trajectory will look like. As an example, you might set milestones (e.g. _By week 4, we plan on having x, y, and z major functionality all working_).

#### Risks
Walk us through what you view as being the biggest risks to your success. Then tell us what you're doing to make sure this doesn't happen.

Examples:
- We have no idea how we're going to implement _Functionality M_. To make sure that this doesn't get in the way of our success, we've found these resources that will help us figure it out.
- We've never used _Technology Z_ before, so learning how to effectively leverage it may be a learning process. We've started looking through the documentation here (link).

#### Documentation Plan
A major portion of this project will be keeping documentation. Think about answering the following questions:

- How will you show us what you’re working on?   
- How will you demonstrate that you’re making progress?  
- Where can we look to quickly see where you are in the project and where you’re going next?

