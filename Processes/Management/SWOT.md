# SWOT

#### Strengths

##### From Customer PoV

* Everything in one application. Organizations and businesses no longer have to use multiple services from different providers and potentially integrate them into their existing applications
* Cheap for the customer compared to many other solutions
* Easy to use with modern visuals and layouts
* Good performance
* Modular. The customer can decide which modules he needs
* Solves real problems. Features are drafted and tested by business specialists in the respective fields
* Optimized for mobile and desktop
* Flexible setup (local or remote)
* Regular updates. Either manually or automatically
* Large amount of modules and functionality

##### Technical PoV

* Modular structure is designed in a very scalable way
* Multiple database support (mssql, mysql, postgresql)
* Multiple cache support (file, memcache, redis)
* Easily scalable
* Can be split across multiple servers

#### Weaknesses

##### From Customer PoV

* Installation for non-tech people is "difficult" (not the actual app installation but the WAMP or LAMP installation)

##### Technical PoV

* Request based code execution. Database and cache connection is request based and not persistent etc. therefor slower and more complicated to maintain state
* Concurrency is difficult to solve due to the request based code execution and state storage

#### Opportunities

* Continuous digitalization, automation and need to keep up with it
* Price attractiveness for all sizes of organizations and businesses
* Public free software tests (without registration)
* Growing demand for managing data (also for small businesses)

##### Technical PoV

* Programming language performance improvement through parallelization/asynchronism implementation
* Programming language performance improvement through usage of type hints during compilation
* Switch to a different language (e.g. c, c++, c#) for higher perform, parallelization and state

#### Threats

##### External

* Regulations. There are many different regulations for different regions and business fields that must be upheld
* Small customers still want to own software and not rent it and pay for it every year
* Since software is intangible it is generally attributed with a lower value than tangible assets
* Like for every programming language the general support for the language (updates, bug fixes, improvements)

##### Internal

* Own organization size/workload. A large amount of modules and tools are required to reach the critical size to make a product which is beneficial for a large amount of organizations and businesses