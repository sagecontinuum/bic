# User Management and Authentication (UMA)

#### Lead: [Wolfgang Gerlach](mailto:wolfgang@uchicago.edu)

### Overview:
A database to manage SAGE users. 

### Requirements:
Each user needs login credentials, and the ability to get an OAuth2 token for programmatic access to SAGE resources. OAuth2 would enable users to use their home organization identities to log into SAGE.

### Milestones:
  * Decide on OAuth2 Authorization Server (Globus, CILogon… ?)
  * Create initial draft of (Django-based ?) web server for user management
  * Enable OAuth2 functionality

### Implementation Notes:

Globus OAuth server provides a login mechanism for SAGE users with institutional logins. 
[SAGE UI](https://github.com/sagecontinuum/sage-ui) is a django-based web server that allows 
SAGE users to login and generate SAGE tokens. A token introspection API allows other software 
components in SAGE (e.g. storage API) to match tokens to users. 
