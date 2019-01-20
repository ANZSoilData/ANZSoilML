# Australian and New Zealand Soil Mark-up Language (ANZSoilML)

## Contents
> 1. [Site Map](#Site-map)
> 1. [Summary](#Summary)
> 1. [The current state of ANZSoilML](#The-current-state-of-ANZSoilML)
> 1. [The future of ANZSoilML](#The-future-of-ANZSoilML)
> 1. [Contacts](#Contacts)

## Site map
| Page | Link | Description |
| ---- | ---- | ----------- |
| Canonical Schema | [ANZ Soil project website (external link)](http://anzsoil.org/def/schema/) | Canonical published location of ANZSoilML schema documents. |
| Documentation | [ANZSoilML GitHub Wiki](https://github.com/ANZSoilData/ANZSoilML/wiki) | Full documentation of the ANZSoilML information model and project work. |
| Public development resources | [anzsoildata.github.io](https://anzsoildata.github.io/ANZSoilML/) | Schema under development. Archived schema. |
| Project planning | [ANZSoilML GitHub Project](https://github.com/ANZSoilData/ANZSoilML/projects/1) | Known issues and planned future work. |

> As of January 2019, all ANZSoilML development is hosted in this GitHub repository.

## Summary
> ANZSoilML primer at the [repository wiki](https://github.com/ANZSoilData/ANZSoilML/wiki/ANZSoilML-Primer).

ANZSoilML is an information model that specifies the set of classes, properties, relationships and supporting
vocabularies needed to structure digital information used in the Australian and New Zealand soil sciences. It is
primarily concerned with observed properties of soils and their associated landscape features as specified in the:
- _Australian Soil and Land Survey Field Handbook, Third edition, 2009, The National Committee on Soil and Terrain._
([CSIRO Publishing](https://www.publish.csiro.au/book/5230/))
- _New Zealand Soil Description Handbook, Revised edition, 1995, Milne, J.D.G., Clayden, B., Singleton, P.L., Wilson,
A.D._ ([Manaaki Whenua Digital Library](http://digitallibrary.landcareresearch.co.nz/cdm/ref/collection/p20022coll14/id/79))

The main intention of ANZSoilML is to provide communities of data providers and users with a model that allows them to
publish and parse a consistent set of data across multiple data repositories. End users should be confident that, for a
given version of ANZSoilML, responses from providers will use the same data types, property names and vocabularies.

ANZSoilML also aims for consistency with other environmental datasets. Soil itself does not exist in isolation - its
formation is influenced by climate, hydrology, geology, topography and biology, and in return it influences those
aspects of the environment. This means that to effectively describe and model soil, data describing other parts of the
environment may be required, and aggregating these data is much easier if they are delivered in a consistent way. This
means ANZSoilML has been developed using a policy of re-use - importing and aligning itself with important standards
for observation and sampling data, geology, groundwater and hydrology.

ANZSoilML was derived from OzSoilML, which was developed in Australia by [CSIRO](https://www.csiro.au/) under the
auspices of the Australian Collaborative Land Evaluation Program (ACLEP) http://www.clw.csiro.au/aclep/. Later, CSIRO
worked with New Zealand's [Manaaki Whenua](https://www.landcareresearch.co.nz) to test and refine OZSoilML, this new
version was rebranded as ANZSoilML.

> Copyright (c) CSIRO, Landcare Research NZ Ltd and Federation University of Australia 2019. All rights reserved.  
> License: [CC-BY-SA-4.0](https://github.com/ANZSoilData/ANZSoilML/blob/master/LICENSE.md)

## The current state of ANZSoilML
> Full description at the [repository wiki](https://github.com/ANZSoilData/ANZSoilML/wiki/Current-Version).

The current version of ANZSoilML (2.0.1) has been designed and implemented as a
[Geography Mark-up Language (GML)](https://en.wikipedia.org/wiki/Geography_Markup_Language) [Application Schema](https://en.wikipedia.org/wiki/Geography_Markup_Language#Application_schema).
This approach involves the definition and provision of
'[Features](https://en.wikipedia.org/wiki/Geography_Markup_Language#Features)' (broadly speaking physical things) that
are of interest when dealing with soils. These include (in _italics_):
- _Soil Profiles_ as made up of _Soils_ and their _Horizons_
- Soil _Landscape Features_ (e.g. _Topography_, _Climatic Setting_ and _Vegetation_)
- Soil _Sites_
- Soil _Samples_ and _Specimens_
- _Laboratory Measurements_

ANZSoilML has focussed on defining the Features specific to soil and imported and extended other Application Schema:
- [Observations and Measurements 2.0 (O&M)](https://en.wikipedia.org/wiki/Observations_and_Measurements) - soil samples
and laboratory measurements
- [GeoScience Mark-up Language 3.0 (GeoSciML)](https://en.wikipedia.org/wiki/GeoSciML) - soil composition and parent
material

The use of GML Application Schema has these technical implications:
- GML is an XML grammar therefore XML documents are provided by default
- The physical model for the XML documents is provided as a collection of XML Schema Documents (XSDs)
([link](http://anzsoil.org/def/schema/))
- Documents are mainly provided via web services conforming to the OGC
[Web Feature Service (WFS)](https://en.wikipedia.org/wiki/Web_Feature_Service) specification
- Documents may be accessed via URLs acting as an identifier for a Feature (so called HTTP URIs) - these may proxy or
redirect to a WFS request or a static document

## The future of ANZSoilML
> Full description at the [repository wiki](https://github.com/ANZSoilData/ANZSoilML/wiki/Future-Work).

ANZSoilML 2.0.1 has defined a rich and robust conceptual model for the description, sampling and analysis of soils, and
the modelling of their distribution, productivity or health. The next steps for the ANZSoilML community are to:
- repackage the data model in a way that separates concepts (the 'data dictionary') from technology (encodings, and
web services and their APIs)
- define a modular framework that allows deployment of a range of tools that use technology and data that are
appropriate to different communities of users

These communities will be varied. They may be made up of any combination (often in the same individual) of:
-  _data providers_ who must publish and exchange rich, well documented data in a way that preserves the quality of the
data without the loss of _any_ content
- _data engineers_ who work with data providers to publish data in ways the meet the needs of users or with users to
extract and transform data according to their needs
- _data scientists_ who may need fast access to raw data for models and simulations with optional access to rich
metadata to help explain anomalies in results; or Semantic Web inferencing tools to discover new patterns in data
- _web developers_ who need simple, terse and fast interfaces that use widely used and supported technology (ReST, JSON
etc)

The tentative workplan for 'ANZSoilML 3' involves:
1. Converting the current GML Application Schema to a technology independent model that can be formally captured using
Semantic Web data modelling tools and also be published using lightweight web tools
2. Defining practices for publishing data in a manner best suited to web developers (particularly the use of JSON and
GeoJSON, and ReSTful interfaces)
3. The definition of a more advanced, but still relatively simple, delivery mechanism using the O&M data types
4. An investigation of the most effective way to deliver complex objects (for example a full soil profile description)

This work will begin in January 2019.

> The OGC is conducting the [ELFIE](https://github.com/opengeospatial/ELFIE/) initiative - a series of Interoperability
> Experiments (IEs) designed to promote web-friendly implementations of linked environmental data. Our vision for
> ANZSoilML as a usable standard closely aligned with other environmental data standards matches the long term vision
> for ELFIE. We are active participants and expect to use the findings of ELFIE to design implement and the new version.

## Contacts
ANZSoilML is developed by an informal group of research organizations that have a responsibility to deliver soil
information to their own scientists but also other agencies and the general public. They work in close consultation with
various environmental Domain Working Groups within the [Open Geospatial Consortium](https://www.opengeospatial.org/)
(OGC).

The group would be delighted to welcome new members and/or to receive feedback - contributors do not need to have a
research focus or be members of the OGC.

| Agency | Country | Contact |
| ------ | ------- | ------- |
| CSIRO | Australia | [Peter Wilson](https://people.csiro.au/w/p/peter-wilson) |
| Federation University of Australia | Australia | [Bruce Simons](http://www.cerdi.edu.au/cb_pages/bruce_simons.php) |
| Manaaki Whenua - Landcare Research | New Zealand | [Alistair Ritchie](https://www.landcareresearch.co.nz/about/people/staff-details?id=cml0Y2hpZWE=) |
