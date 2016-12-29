# Software-Architecture
My collection of notes on Software Architecture


Architects pay more attention to qualities that arise from architecture choices.

#### Lets design a system
Here's a situation
  you are a hosting provider
  you rent mail servers
  customers have problems
  you use the mail logs files to diagnose their problems

The big question:
  how would you build it?

Lets assume you can build it
  but different architectures yield different qualities

Why is it hard?
  you have hundreds of servers
  you generate GBs of logs daily
  collecting logs takes time
  searching logs takes time

Hints and options
  central collection of logs?
  distributed searching of logs?
  can you preprocess logs to speed up the queries?

Surprise!! this is a real system

#### Exercise based on real experience
  Rackspace is a hosting provider
  huge growth in customers, mail servers - and problems
  redesigns: 3 major versions(6 total versions)

  http://highscalability.com/how-rackspace-now-uses-mapreduce-and-hadoop-query-terabytes-data

#### Lets review the 3 systems they built.
  All 3 had the same functionality(!) but different architectures

#### Why this is so cool
  very expensive to build the same system 3 times
  the only big change was the architecture
  so we can see the effect of architecture
  especially on the quality attributes

##### Rackspace Architecture 1
Hosting provider of email service
email log files

Task:  debug user problems

Architecture:
  CSR desktop computer
  ssh connections to servers
  servers with local log files

Procedure
  write  query as a grep expression
  script runs via ssh on every server
  results aggregated

##### Rackspace Architecture 2
Architecture:
CSR desktop computer
web application
MySQL db
scp log transfer
Servers with local log files

Procedure:
  Every 10 minutes, send log files to MySQL server, delete original
  parse and load logs into MySQL
  combine new logs with old
  send query to MySQL server
  answered from DB Data

##### Rackspace Architecture 3
Architecture:
CSR desktop computer
web application
distributed filesystem
Map-Reduce job cluster
servers with local log files

Procedure:
  Log data continuously streamed from email servers to distributed filesystem (HDFS)
  Every 10 minutes, Map-Reduce jobs runs to process log files, create index
  Web app queries index

##### Rackspace: Quality attrubutes tradeoffs
Tradeoff: Data freshness
  V1: Queries run on current Data
  V2: Queries run on 10 minute old data
  V3: Queries run on 10-20 minute old data
Tradeoff: Scalability
  V1: Noticeable email server slowdown (when it went above dozens of servers)
  V2: MySQL speed/stability problems (when it went above hundreds of servers)
  V3: No problems yet
Tradeoff: Ad hoc query ease
  V1: Regular expression
  V2: SQL expression
  V3: Map-Reduce program

## 3-Tier system
Most important Architecture to know.

## Guiderails (constraints)
Developers voluntarily constrain a system
it counter intuitive
ensure what a system does not do.

##Architectural styles
Example
  * Big ball of mud
  * client server
  * pipe and filter
  * Map-Reduce
  * N- tier
  * Layered
  * ....

  
## References

A lot has been taken from George Fairbanks Lecture and notes
