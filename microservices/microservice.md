Microservices is a specialisation of an implementation approach for service-oriented architectures (SOA) used to build flexible, independently deployable software systems. Services in a microservice architecture are processes that communicate with each other over a network in order to fulfill a goal. These services use technology-agnostic protocols. The microservices approach is a first realization of SOA that followed the introduction of DevOps and is becoming more popular for building continuously deployed systems.

In a microservices architecture, services should have a small granularity and the protocols should be lightweight. A central microservices property that appears in multiple definitions is that services should be independently deployable. The benefit of distributing different responsibilities of the system into different smaller services is that it enhances the cohesion and decreases the coupling. This makes it easier to change and add functions and qualities to the system at any time. It also allows the architecture of an individual service to emerge through continuous refactoring, and hence reduces the need for a big up-front design and allows for releasing software early and continuously.


"
You need to be this tall to use [micro] services:
* Basic Monitoring, instrumentation, health checks
* Distributed logging, tracing
* Ready to isolate not just code, but whole build+test+package+promote for every service
* Can define upstream/downstream/compile-time/runtime dependencies clearly for each service
* Know how to build, expose and maintain good APIs and contracts
* Ready to honor b/w and f/w compatibility, even if you're the same person consuming this service on the other side
* Good unit testing skills and readiness to do more (as you add more microservices it gets harder to bring everything up, hence more unit/contract/api test driven and lesser e2e driven)
* Aware of [micro] service vs modules vs libraries, distributed monolith, coordinated releases, database-driven integration, etc
* Know infrastructure automation (you'll need more of it)
* Have working CI/CD infrastructure
* Have or ready to invest in development tooling, shared libraries, internal artifact registries, etc
* Have engineering methodologies and process-tools to split down features and develop/track/release them across multiple services (xp, pivotal, scrum, etc)
* A lot more that doesn't come to mind immediately
Thing is - these are all generally good engineering practices.
But with monoliths, you can get away without having to do them. There is the "login to server, clone, run some commands, start a stupid nohup daemon and run ps/top/tail to monitor" way. But with microservices, your average engineering standards have to be really high. Its not enough if you have good developers. You need great engineers

" -rdsubhas

source: https://news.ycombinator.com/item?id=12508655
