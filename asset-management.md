# Asset Management

Our path to production is dependent on the use of a Definitive Media Library to store the source of truth for our binary artifacts.

### Servers

Production:
 * [Nexus Repo](Repo URL)
 * [Nexus IQ](IQ URL)

Testing (only accessible in TestLab):
* [Nexus Repo](Repo URL)
* [Nexus IQ](IQ URL)


### Dependency Management

Part of this solution will also provide an internal proxy of external public repositories.

Remote Proxy Repositories:

 * [Maven](https://mavencentral.com)
 * [NPM](http://npm.org)
 * [Nuget](http://nuget.org)

### Policy Scanning

The policy management piece is responsible for scanning the third party open source dependencies. This will be referenced against a cultivated database of violations that is managed and updated by Sonatype. Policies and reporting information is provided by Nexus IQ.

IQ provides stages for a given application to run scans and provide a report against.  The stages are: build, stage, release, and operate.  The following IQ stage mapping was created:

For one branch SCM model( like iOS/Android ) <br/>
OLB UI - Build master CI  --- Build <br/>
OLB UI - Build master RC  --- Release <br/>

For two branch (4 build) model ( like OLB ) <br/>
OLB UI - Build develop CI --- Develop <br/>
OLB UI - Build develop RC --- Stage Release <br/>
OLB UI - Build master CI  --- Build <br/>
OLB UI - Build master RC  --- Release <br/>
