# Sage Continuous Integration (SCI):

#### Lead(s): [Wolfgang Gerlach](mailto:wolfgang@uchicago.edu) and [Joe Swantek](mailto:joseph.swantek@northwestern.edu)

### Overview:

We need a complete end-to-end testing framework for testing Sage code commits and 
generate software releases. Github pull requests can trigger automatic builds and 
tests to make sure that only changes are accepted that do not break existing edge code. 
This automatic testing can also be done for other SAGE software components such as 
edge infrastructure or beehive server. Virtual Waggle (VW) and Chameleon-attached 
Waggle nodes (BWD) can be used for testing. 

### Milestones:

  * Setup Jenkins server configured to check SAGE github repositories for Jenkins files.
  * Create Jenkinsfiles for edge bundles and other SAGE components
  * Deploy Jenkins slaves in compute resources such as Chameleon or SDSC. 
  * Dynamic allocation of compute resources for Jenkins slaves.
  
### Implementation Notes:
Jenkins is the most commonly used automation server for this purpose, which will 
be leveraged for SAGE-CI/CD.




