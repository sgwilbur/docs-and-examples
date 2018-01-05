# Continuous integration

Our goal here is to move away from the build and deploy per environment model and move to a build once deploy many model. The change in model may require some re-factoring to accomplish as environmental data needs to be externalized and/or refactored in a common code deployable and can be re-used in a data driven way across all possible target environments.

Supporting this model is version control for source of change and an asset management for storage of deployable versions. The streamlined version control here does not require multiple branches to represent desired environment targets and configuration points via tags/labels are created during build time to capture potential release candidates. The build automation provides a entry point for other types of tasks you may wish to automate as well and can perform some analysis to help identify which builds are considered 'healthy.' At the end of a successful build process the deployable artifact is archived and stored in asset management with a version matching the for use during deployment.



### Usage

The is that every application has at least one continuous integration job in Jenkins. For applications that have multiple components or make a distinction between different build types there will be more for supporting different needs. At a minimum we expect one `Release Candidate` build that will create downstream deployable artifacts, but it is also possible to have other component or test specific build jobs for `throwaway` CI only builds that will not feed the downstream delivery pipeline but are simply used for quicker validation.

---

## Jenkins

#### Overview

Jenkins is a industry leading open source platform for automation, the strong community and large user base makes it a popular choice for performing build, test, and deployment automation. Jenkins is the de facto standard for a continuous integration platform, and while it is a generic workflow system it has been extended and customized specifically for performing build automation as it's primary function.

#### Servers:

 * [Jenkins Prod - ](Jenkins URL)
 * [Jenkins Testing - ](Jenkins URL)
 * Other Servers...

#### Jenkins Pipeline

The [Jenkins pipeline](https://jenkins.io/doc/book/pipeline/jenkinsfile/) features provide a means for defining build process as part of your code so management and upkeep of the build process are part of the standard development effort once established.


You can see an examples here:

 * Build -  
 * Deploy -
