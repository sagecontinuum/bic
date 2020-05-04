# Sage Web Portal (SWP)

#### Interim Lead: Wolfgang Gerlach

### Overview:

SAGE consists of multiple functional components that help users to develop and deploy 
software for SAGE edge nodes. In addition to an API for programmatic access of the 
SAGE functionality, a user-friendly web portal will make it easier and more convenient 
for SAGE users to browse and search data products. It provides an interface to uploads 
and downloads.

### Requirements:
* Tables to browse and search for SAGE data objects such as edge bundles, ML models and training datasets. 
* A login system to allow access to private data. Data sharing functionality. 
* Upload and download of files. 
* Creation of ECR bundles. 
* Any other functionality that may be required by other functional components.

### Milestones:
  * Draft version that allows user registration and login.
    - Admin interface
  * Add tables with sort and filter functionality to search objects.
    - Within data types
    - Across all data types
  * SSL-secured production deployment for access to public data only


### Implementation:
Django is being considered for fast prototyping.
