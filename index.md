# Java EE 7 Training resources
At the training we followed book [Beginning Java EE 7](http://www.apress.com/9781430246268) from [Antonio Goncalves](https://antoniogoncalves.org/).

## The code

We followed [code samples from the book](https://github.com/agoncal/agoncal-book-javaee7) troughout the training.

## Other general resources

[Java EE 7 javadoc](http://docs.oracle.com/javaee/7/api/index.html) lists all of the relevant APIs defined by Java EE spec.

Adam Bien's book [Real World Java EE Patterns -- Rethinking Best Practices](http://realworldpatterns.com/) will help you put EJB and CDI in practice.

[Java EE 7 samples](https://github.com/javaee-samples/javaee7-samples) demonstrates Java EE 7 features in Arquillian-based tests.

[Arquillian](http://arquillian.org/) helps testing parts of your Java EE applications within container - be it just Weld, embedded Payara or remote standalone servers.

## CDI

Read [Weld Reference Documentation](http://docs.jboss.org/weld/reference/latest/en-US/html/) for in-depth details about all CDI features.

[Apache Deltaspike](https://deltaspike.apache.org/) is collection of CDI extensions covering various infrastructure aspects of your application.

## JPA

For in-depth look into JPA, design of the entities and trade-offs of the features, read [Pro JPA 2](http://www.apress.com/9781430219569) by  Mike Keith and Merrick Schincariol.

Another great source of JPA knowledge is [Vlad Mihalcea](https://vladmihalcea.com/).

Instead of Criteria API, consider using [QueryDSL](http://www.querydsl.com/).

For managing of database schema I recommend [FlyWay](https://flywaydb.org/).

## Security

Ultimate source on JAAS and JASPIC is [Arjan Tijms](http://arjan-tijms.omnifaces.org/) (and also for JSF and OmniFaces).

## Transactions

To understand cases, where distributed transactions are not a good choice, read [Your Coffee Shop Doesn’t
Use Two-Phase Commit](http://www.enterpriseintegrationpatterns.com/docs/IEEE_Software_Design_2PC.pdf) by Gregor Hohpe.

Also good source for understanding distributed systems, that usually reach outside scope of Java EE, look at [Distributed Systems for Fun and Profit](http://book.mixu.net/distsys/single-page.html) by Mikito Takada.

## Messaging

Even though Java Serialization is very comfortable, for high performance systems consider [other serialization libraries](https://github.com/eishay/jvm-serializers/wiki) that might give you smaller payloads, less CPU usage, and better interface evolution options.

For building business processes based on message passing you may want to read [Enterprise Integration Patterns](https://books.google.sk/books/about/Enterprise_Integration_Patterns.html?id=qqB7nrrna_sC&source=kp_cover&redir_esc=y) by Gregor Hohpe (yes, the one of the coffee shop article).

## REST

The origin of the term is in [Roy Fieldings' disertation](https://www.ics.uci.edu/~fielding/pubs/dissertation/fielding_dissertation.pdf), where it says it's not just about HTTP, but also [about hypermedia](http://olivergierke.de/2016/04/benefits-of-hypermedia/).

Serialization frameworks from above may also be a good option for message exchange over REST.

## JSF

I think no JSF app can survive without [PrimeFaces](http://www.primefaces.org/) and [OmniFaces](http://showcase.omnifaces.org/). And the [book explaining OmniFaces and therefore JSF](https://www.amazon.com/dp/1908689293).

## Application Servers

* [Payara](http://www.payara.fish/) - maintained fork of deceased platform reference implementation [Glassfish](https://glassfish.java.net/). See also (Glassfish Documentation)[http://docs.oracle.com/cd/E26576_01/index.htm] and [Payara Documentation](https://payara.gitbooks.io/payara-server/content)
* [Wildfly](http://wildfly.org/) - open source variant of [JBoss EAP 7](http://developers.redhat.com/products/eap/download/). See also [Development guide](https://docs.jboss.org/author/display/WFLY10/Developer+Guide) for server specifics.
* [TomEE](http://tomee.apache.org/apache-tomee.html) Java EE *6* application server built on top of Tomcat from Tomcat maintainers
* [WebShpere Liberty](https://developer.ibm.com/wasdev/websphere-liberty/) free version of WebShere with heap limit 2GB (total over all instances)

[Full listing of certified servers](http://www.oracle.com/technetwork/java/javaee/overview/compatibility-jsp-136984.html)

## Standards' specifications

All Java EE specifications are governed by [Java Comunity Process](http://jcp.org) as Java Speficication Requests (JSRs). The list of Java EE 7 JSR with links to spec downloads is available [at Oracle's site](http://www.oracle.com/technetwork/java/javaee/tech/index-jsp-142185.html)

## Misc

At heart of every server there is bytecode manipulation library like [ASM](http://asm.ow2.org/). Other good use cases are writing tests, that verify correctness of the code (e. g. security check is invoked in every method).