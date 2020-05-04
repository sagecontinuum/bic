# Storage & Storage API

#### Lead: [Wolfgang Gerlach](mailto:wolfgang@uchicago.edu)

### Overview:

Storage services are needed for various software components. Data objects like ML models, 
and training data need to be accessible and require permission control. A [simple API](https://github.com/sagecontinuum/sage-storage-api) will 
provide an unified view of the storage. Metadata stored in a database will make the objects 
searchable. A separate search engine service that holds a copy of all metadata and 
allows efficient search queries is being considered.

### Requirements:

#### Support for data types: 
This list includes data that may be stored on 3rd-party systems like github.

##### Basic Data:

  * Training data sets (public: LCRC, else object store) 
      -with or without labels
  * ML models (object store)
      - metadata: runtime requirements (PyTorch, OpenCV, etc.)
  * Optional: training data set annotations "labels" (object store)
  * Optional: ML model weigth files (object store)
      - specify model
  * Beehive data-decoding plugins (github)
  * Trigger apps (github)
  * Edge code (github)
  * ECR Bundles (just a collection of references, mysql?)
  * Docker Files (github)
  * Docker Images (dockerhub)
  * Sensor calibration parameters
  * Sensor data
  * Sensor blob data (large files)
  * May include: Binaries / GPU optimized code
  
##### Metadata:
Metadata that some of the objects will need:
  * Basic data type information
  * Provenance information
  * DOI

_A note about Provenance_ - 

The use of controlled vocabularies promises  better discoverability, understanding, 
and reuse of scientific data. Sage will look into controlled vocabularies with feedback 
from Sage users from different scientific domains to learn about their specific needs in terms 
of data discoverability.

#### Milestones:

  * SAGE Storage: storage system with support for metadata or storage + database for metadata
  * Use authentication service to enable upload and access to private data (see [Authorization Service](https://github.com/sagecontinuum/bic/blob/master/auth_service.md))
  * Metadata specification for common data types ( e.g. ML model )
  * Database (mySQL?) for ECR bundles
  * Search functionality for data in SAGE storage

#### Implementation Notes:

Depending on the storage being used SAGE may require an API server to support upload and download of public or private data.
Implementation options being considered - 
  * **golang**: gorilla/mux https://github.com/gorilla/mux
  * **python**: FastAPI https://github.com/tiangolo/fastapi
