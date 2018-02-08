## Week 2

### Integration Testing

_"This ain't yo mama's unit testing!" _ - Patrick Huston, 2018

Last week, we introduced the philosophies behind testing, and hit the ground running with the most ubiquitous type of tests, unit tests. This week, we continue our journey into the world of testing with the concept of integration tests.

#### Schedule

##### Monday, January 29

We'll start with a [presentation](https://drive.google.com/open?id=1NH2rWVJ6eifhT4tXVEVOq2zCzlOuqekIg9_KfLCG5lw) introducing the concept of integration testing.

After that, we'll do a live demo with a basic todo-api. You can find the source code [here](https://github.com/olin-fse/integration-demo).

##### Thursday, February 1

Today, we'll be doing a short lecture on relational database schema design. While it might not always feel like a straightforward process, there are a set of industry-standard practices used to approach this problem.

You can find the presentation [here](https://drive.google.com/open?id=1VcSSjzEcmM7EzV-mE9XuA2jGIB8DHOuTofSt_MWw4Bk)!

Some topics include:

* The concept of an [ERD](https://www.lucidchart.com/pages/er-diagrams) \(Entity Relationship Diagram\)
* How to convert an ERD into a relational schema
* [What](https://en.wikipedia.org/wiki/Database_normalization) normalization is, [why](https://en.wikipedia.org/wiki/ACID) it's important, and how you should [apply normalization](https://support.microsoft.com/en-us/help/283878/description-of-the-database-normalization-basics) to your schema

#### Deliverables \(Due Monday, February 12\)

**Coding Work**

We recognize that a lot of you have taken on learning new frameworks and technologies for your projects - and that's great! As a result, it's unlikely that you have a lot of real significant functionality complete in your applications just yet.

So - while we understand that many of the tests you're writing now might feel forced, we'd like you to start getting experience and get your hands dirty. When you start developing non-trivial functionality, these skills and resources should be second nature, and you won't have to figure out how to get tests to run while also thinking about how the tests should be designed themselves.

_For next week, we'd like you to have two integration tests written_. Some first candidates for points of integration that you could consider are \(1\) Between your backend and database and \(2\) Network calls to your API from the frontend.

#### Feedback

Fill out [this form](https://goo.gl/forms/eTzdgga9UpOhwWjm1) to give us feedback for this class.

#### Useful Links and Resources

**Class Resources**

[Presentation](https://drive.google.com/open?id=1NH2rWVJ6eifhT4tXVEVOq2zCzlOuqekIg9_KfLCG5lw) on integration testing

[Presentation](https://drive.google.com/open?id=1VcSSjzEcmM7EzV-mE9XuA2jGIB8DHOuTofSt_MWw4Bk) on relational database schema design

[Integration Testing Live Demo Repository](https://github.com/olin-fse/integration-demo)

**Good Articles/Posts**

_About Testing_

[https://www.thoughtworks.com/insights/blog/guidelines-structuring-automated-tests ](https://www.thoughtworks.com/insights/blog/guidelines-structuring-automated-tests)

[https://martinfowler.com/bliki/SelfTestingCode.html](https://martinfowler.com/bliki/SelfTestingCode.html)

[https://martinfowler.com/bliki/IntegrationTest.html](https://martinfowler.com/bliki/IntegrationTest.html)

[https://martinfowler.com/bliki/SelfInitializingFake.html](https://martinfowler.com/bliki/SelfInitializingFake.html)

[https://martinfowler.com/bliki/ContractTest.html](https://martinfowler.com/bliki/ContractTest.html)

[https://martinfowler.com/articles/mocksArentStubs.html](https://martinfowler.com/articles/mocksArentStubs.html)

[https://martinfowler.com/articles/nonDeterminism.html\#RemoteServices](https://martinfowler.com/articles/nonDeterminism.html#RemoteServices)

_On Databases/NoSQL vs SQL_

[https://martinfowler.com/bliki/OrmHate.html](https://martinfowler.com/bliki/OrmHate.html)

[https://martinfowler.com/books/nosql.html](https://martinfowler.com/books/nosql.html)

