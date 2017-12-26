# Documentation

“Documentation is like sex; when it’s good, it’s very, very good, and when it’s bad, it’s better than nothing.”


1. I personally believe documentation is very important if you code is expected to run/support for a long time.
2. The documentation should be either done in a platform that allows you to continuously edit, make comments etc.
3. If you can't have a live way to handle like in confluence etc, and it is going to be a word document then ensure versioning is done through a version control like git, mercurial etc. This helps in understanding why certain design decision were taken.
So a new person doesn't make the same mistake the team has already been through.

## Some Comments on Documentation

Nowadays, most web applications are developed by teams that have adopted an agile development method, like Scrum or Kanban. These methods do not prescribe the production of design documentation, which may give people the impression that such documentation is not needed. Furthermore, the Agile Manifesto says:
“We value working software over comprehensive documentation”.
The fact that the same manifesto also states that documentation is valuable, is sometimes ignored. Good developers can build high-quality applications without any technical design, but nevertheless, documenting any professional application up to a certain level of detail, not sacrificing an iterative process or prototyping. Why? Because it saves time and money and the users will get a better application!
There is one precondition: the developers must support it. The savings arise from the fact that the design provides insight into the software structure and thereby reduces the chance of a bad structure (spaghetti code, inconsistencies, code duplication). Both the insight into the structure of the software and the high quality of the structure subsequently diminish..
a. the chance of bugs and consequently the time it takes to solve bugs;
b. the time it takes to determine the best way of integrating a particular change or extension;
c. the time it takes to rectify flaws in the structure later on.
Like I said, applications need technical documentation up to a certain level of detail, i.e. not too detailed. The design should be sufficient to subsequently find more details in the source code. If the source code has not been written yet, the design should be sufficient for the developer to fill in the details on his own discretion. By the way, it is not always required to have the design finished before the coding starts. You may decide to make a prototype


For Web Apps
• Business process models and business object models.
• Functional requirements, in most cases written as user stories or use cases.
• Non-functional requirements, varying from business-level requirements to a reference architecture (see next section) and coding guidelines.
• User interface design, most often a prototype or a series of images.
• Back end API specifications and eventually the API(s) themselves.
• Documentation of JavaScript libraries that will be used or may be used.

Sources:
1. http://www.admiraalit.nl/admiraal/Technical-Design-For-AngularJS-Apps.pdf
2.
