# ANZSoilML Notes

## Change Log

### ANZSoilML v2.0.0 Changes
- physicalProperty:
  - QuantitativeMeasure now PhysicalPropertyValue
  - QuantitativeMeasureObservationMethodTerm now PhysicalPropertyObservationMethodTerm
  - propertyResult (mandatory) now propertyQuantityValue (optional)
  - contraint added: count(propertyQuantityValue) + count(propertyTermValue) >= 1
  - Purpose: allows catageorical physical property values to be recorded (previously they had to be quantitative).

### ANZSoilML v2.0.1 Changes
- Created package ANZSoilML_GSM - merges GSMML (Oceania) into ANZSoilML.
- Created primary/secondary spatial entity classes as sub-types of SoilProfile
- All mandatory properties are now optional (but still nillable).
- Removed redundant classes (Field_PH)
- Reconciled inconsistencies between UML and XSD (SoilFeature.samplingFeature).

## Configuring Enterprise Architect for trunk ANZSoilML

__Step 1__. Make a SVN 'working copy' of public XMI documents:

SVN checkout the following directories:
- https://www.seegrid.csiro.au/subversion/HollowWorld/branches/release_4 (this is the most recent stable release of
HollowWorld, and it contains the SWE Common Data Model that is required for GeoSciML v3 and later versions - December 2012)
- https://www.seegrid.csiro.au/mirrors/iso-harmonized-model
- https://www.seegrid.csiro.au/subversion/GeoSciML/tags/3.1/model
- https://svnserv.csiro.au/svn/ext/TernSoils/ANZSoilML/trunk/model
- NOTE: The SVN Externals configuration uses the SVN 1.5 syntax, so your SVN client must be 1.5 or later.

__Step 2__. Set up Enterprise Architect Version Control Configurations:

In Enterprise Architect, set up or confirm the following Version Control Settings:

| Unique ID | Type | Repository |
| --------- | ---- | ---------- |
| HollowWorld | Subversion working copy of https://www.seegrid.csiro.au/subversion/HollowWorld/branches/release_4 |
| isotc211 | Subversion  working copy of https://www.seegrid.csiro.au/mirrors/iso-harmonized-model |
| GeoSciML | Subversion  working copy of https://www.seegrid.csiro.au/subversion/GeoSciML/tags/3.1/model |
| ANZSoilML-trunk | Subversion  working copy of https://svnserv.csiro.au/svn/ext/TernSoils/ANZSoilML/trunk/model |

__Step 3__. Load HollowWorld (branch release 4)

Follow the instructions at [SEEGrid - Configuring UML Tool For HollowWorld](https://www.seegrid.csiro.au/wiki/bin/view/AppSchemas/ConfiguringUMLToolForHollowWorld).

- Note: the HollowWorld configuration changes occasionally. If users wish to change the release version of HollowWorld
that they are using (eg, from a release version to trunk, or vice-versa), users should reload HollowWorld into a brand
new, blank Enterprise Architect project with new Version Control Settings (see step 2 above), before then loading the
GeoSciML and EarthResourceML models.
- EA v7.5 or later is recommended for full compatibility with the SVN systems.

__Step 4__. Load the GeoSciML UML model

In Enterprise Architect:
1. Right click on the root model icon... Package Control -> Get Package
1. Select the Version Control Configuration for GeoSciML
1. Select the shared file for 'geosciml.xml' (!! don't load any of the other packages manually - you'll get them in the next step.)
1. Right click on the root model icon and select Package Control -> Get All latest

__Step 5__. Load the ANZSoilML UML model

In Enterprise Architect:
1. Right click on the root model icon... Package Control -> Get Package
1. Select the Version Control Configuration for ANZSoilML-1.0
1. Select the shared file for 'ANZSoilML.xml' (!! don't load any of the other packages manually - you'll get them in the next step.)
1. Right click on the root model icon and select Package Control -> Get All latest