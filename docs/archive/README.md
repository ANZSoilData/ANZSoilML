# ANZSoilML Archive

## Overview
Archive of previous versions of ANZSoilML. Imported from the CSIRO subversion repository at
[https://svnserv.csiro.au/svn/TernSoils/ANZSoilML](https://svnserv.csiro.au/svn/TernSoils/ANZSoilML).
- ANZSoilML was developed using the [Enterprise Architect](https://sparxsystems.com/) UML modelling tool. A
[trial version](https://sparxsystems.com/products/ea/trial/request.html) is available to allow the UML to be reviewed.
- ANZSoilML is sub-dived into UML packages that allow them to be maintained independently. An 'all components' package
brings together all schema documents, model artefacts and documentation. This includes an un-versioned copy of the EA
Project file the model was developed in.

## Folder Structure
| Folder | Purpose | Description |
| ------ | ------- | ----------- |
| anzsoilml | package | The 'all components' package. Linking to the all components anzsoilml.xsd should import all other XSDs. |
| anzsoilml-core | package | Core classes used by all packages. |
| anzsoilml-landscape | package | Classes describing landscape, land use, climate and vegetation features. |
| anzsoilml-soil | package | Classes describing the classification and composition of soils and their horizons. |
| anzsoilml-soilsample | package | Classes describing soil sampling and analysis. |

## Sub-folder Structure
| Folder | Purpose | Description |
| ------ | ------- | ----------- |
| classmap | design | Enterprise Architect XML configuration for mapping ISO/OGC UML types to their XML Schema - uses the [EA UML Profile for GML](https://sparxsystems.com/enterprise_architect_user_guide/14.0/domain_based_models/uml_profile_for_gml.html). |
| html | documentation | An HTML representation of the UML model. All components package only. |
| instances | example | Example GML instance documents for commonly used Feature Types. |
| uml | design | [Enterprise Architect XML Metadata Interchange (XMI)](https://sparxsystems.com/enterprise_architect_user_guide/14.0/model_publishing/importexport.html) documents containing the UML classes for the package. |
| xsd | xsd | XML Schema Documents (XSDs). |