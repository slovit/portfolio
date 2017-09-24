# Secure communication between DCC Portal and Download server with JWT tokens

Users navigate [DCC Portal](https://dcc.icgc.org/releases)   and browse a virtual file system on the Download server. When they want to download different artifacts we want them to download directly from the Download server without proxying a download though the Portal. A process of transfer of a user from the Portal to the Download server and start of a download should be transparent to the user.

This functionality is achived with a HTTP redirects and JWT (encrypted and singed) tokens which contain all information required to authorize artifacts download.

DCC Download server codebase with a detailed description is available on [GitHub](https://github.com/icgc-dcc/dcc-download/tree/develop/dcc-download-server).

# Portal Query Language
Motivation for the project was to abstract away complex logic of creating Elasticsearch queries from [Advanced Search](https://dcc.icgc.org/search) filters on the DCC Portal.

To create an Elasticsearch(ES) query knowledge of ES index structure and complex business rules was required. Extraction of the functionality into a separate library and introduction of the Portal Query Language made the code simpler, testable, easy to extend and maintain.

A [detailed description](https://github.com/icgc-dcc/dcc-portal/blob/develop/dcc-portal-pql/PQL.md) of the module is available in the DCC Portal [repository](https://github.com/icgc-dcc/dcc-portal/tree/develop/dcc-portal-pql).

# DCC Release
A distributed data processing pipeline to process clinical data submitted by the ICGC participats.

The pipeline is run on a Apache Spark cluster.

A detailed description of the pipeline could be found [here](https://github.com/icgc-dcc/dcc-release/blob/develop/PROCESS.md).
[Code of the project](https://github.com/icgc-dcc/dcc-release) is publicly available.

