Ewe platform Showcase
2013q1

---

EWE Platform Q1 Accomplishments

---

# Team
## Problem:
* Insufficient capacity to meet the demands on the platform team

## Deliverables:
* Hire additional staff in Bellevue and Gurgaon

## Benefits:
* Increased delivery and support capacity

## Metrics:
* 7 Devs in Gurgaon
* 3 devs + 1 QA in Bellevue

---

# Data access 
## Problem:
* Service Invoker is legacy custom E3 platform code that is difficult to use, and hard to manage.

## Deliverables:
* Removed old map service related code
* Removed user service messages that goes through 
* Database calls through Camel routes, in domain (formerly in data access) service invoker

## Benefits:
* Removed dependencies on service 

## Metrics:
* TODO: get count of files f& classes removed

owner: Gaurav & Nancy
get metrics on number of classes and files removed.

---

# Spring Context
## Problem:
* Current spring contexts are not a good fit for the current expweb architecture.
* Database calls mislocated domain and not data access.

## Deliverables:
* Spring aware of all of the application contexts in expweb
* Collapsed the application contexts from 8 to 4
	* Activity
	* Platform
	* System
	* ui 
* Created new naming conventions for Spring beans and files.
* All database calls are moved to camel and dataaccess layer.
* Refreshable beans are moved to expweb servlet context

## Benefits:
* Better alignment of spring context with expweb arch layers.
	* Makes it harder to do bad things
* Clean data access layer.
* Better alignment with spring community norms
* Less coupling to e3.foundation

## Metrics:
* 86% of data  calls going through camel

Owner: Ken \ Jason
TODO: Get the metrics
283 out 328 service alls

---

# User End 2 End
## Problem:
* User related pages are hosted in emain
* Lacking global persistent view of users

## Deliverables:
* 30 day spike shows that we can associate registered user with an unregistered user via email address.	
* POC for the "fly out" login
* New e3 login page (Not yet trafficked)

## Benefits:
* Shows that approach is viable

## Metrics:

Owner: Ranjan, Amit - showcase video
TODO: Think about the metrics - not live yet - so is hard.

---

# User Interaction 
## Problem:
* No ability to understand user interaction & behavior with site in real time

## Deliverables:
* Capture user interaction within expweb
* user interaction IDL & Management process
* user interaction service & management infrastructure
	* (github, maven, AWS)

## Benefits:
* system that allows us to capture AND understand user behavior in real time
* Ability to create compulsion loops based on real time interaction of all users
* Enables Data Capture toolkit

## Metrics:
* 50% of .com 251 rps @ 25ms response time (99.9)  2 AWS instances behind 1 load balancer

Owner: Anuraag

---

# Platform Enhancements
## Problem:
* Cost of ownership of the machine we have created.

## Deliverables:
* Created initial version of dashboard for ewe platform events
* Validation of log4j.xml parse errors at startup
* Report for invalid site requests into one common place with clear message
* Deleted compact cookie code
* Enabled and supported application engineerings rollout of Staying Alive
* Platform test case migration from junit to test (60%-80%)
* Remaining 20% to deprecate with refactorings.

## Benefits:

## Metrics:

---

# Localization
## Problem:
* Localization take place via vendors

## Deliverables:
* Support for inhouse localization via worldserver

## Benefits:
* No longer pay vendors, All localizers are employees
* stages us for higher frequency localization

## Metrics:
* No longer paying vendors
* Improved ad hoc turn around time.

Steve C - Video

---

# E3`
## Problem: 
* Current applocaiton infrastrcutre challenges rapid serving of pages to locations around the world, since all requests come to Chandler.

## Deliverables: 
* Camel Abacus Route & Unit & Integration test with Camel test suite
* Adding new library for Camel EIPs &  tests
* Caching Abacus result using Camel Cache & test cases
* Site Service POC using DropWizard
* Created Interfaces of Various E3 components. e.g. experiment, site, usercontext, etc.

## Benefits:
* Gelocation of page rendering will allow increased performance to the user
* High availbiilty in multiple datacenters
* decoupling of teams development, testing and deployment
* These modules are independent of the E3 platform
* Expweb will be consuming these modules as well to replace the E3 platform libraries

## Metrics:
* 11 modules planned. 
* 3 standalone already (Camel, monitoring, STCS). Others in DX Web 
* High level design of e3` platform modules.
* Bug reporting / tracking using unit tests

Owner: Aaron
https://github.com/ExpediaInc/exp-dx-web/blob/master/dxweb/platform/docs/component-dependencies.png
OWNER: lakshmi

place holder QA and bug tracking approach for e3' libraries of failiung unit test

---

# EWE Platform Q2 plan

https://confluence/display/POS/EWE+Platform+2013+Road+Map

* Finish Spring context refactor
* Refactor Domain and presentation.
* All of the bean loading is specified in spring xml files instead of foundation open.

---

# Data Access
* Remove dependency on service invoker modules

---

# E3`
* First release of Platform e3` modules for DX Web
* User End2End 
* New E3 login page going live

Owner Hao
TODO: feedback from 120 day planning

---

# User Interaction 
* Writing raw logs to s3
* Realtime filtering capabilities
* Trend analyser in place to produce compulsion loops
* Filtered trace logging from live site (client perf, errors, Interaction and server side interaction) all available in one place for analysis

---

# Platform Enhancements

* UPgrades
	* Quova
	* JDK
