# ANZSoilML Soil Schema
## Development notes
anzsoilml-soil.xsd points to externally hosted schema:
```xml
<xs:import namespace="http://xmlns.anzsoil.org/ANZSoilML-Core/1.0" schemaLocation="http://www.clw.csiro.au/aclep/ANZSoilML/trunk/ANZSoilML_Core/xsd/anzsoilml-core.xsd"/>
<xs:import namespace="http://xmlns.anzsoil.org/ANZSoilML-SoilSample/1.0" schemaLocation="http://www.clw.csiro.au/aclep/ANZSoilML/trunk/ANZSoilML_SoilSample/xsd/anzsoilml-soilsample.xsd"/>
```
These depend on regular updating from the subversion directory and as such may be out of date. The most recent schema are at:
- https://svnserv.csiro.au/svn/TernSoils/ANZSoilML/trunk/ANZSoilML_SoilSample/xsd/anzsoilml-soilsample.xsd
- https://svnserv.csiro.au/svn/TernSoils/ANZSoilML/trunk/ANZSoilML_Core/xsd/anzsoilml-core.xsd