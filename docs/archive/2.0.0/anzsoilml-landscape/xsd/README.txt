Files with "_1" first generation prior to adding GML:property stereotype to all attributes/associations
..._hand handcrafted from OzSoilML-Landscape - incomplete and used as a guide. To be discarded ASAP.
..._all includes Climate, StreamChannel, SoilLandscape and HumanActivity in one schema. As a test that the schema work together.
To be replaced by anzsoilml-landscape with imports when working.

All files require checking that the Term values have encoded corrrectly.

HumanActivity has a problem with the LandTermValueCategory Union encoding that needs sorting.

12/4/13 vegetation.xsd completed but not tested with instances
12/4/13	landscape_leaf completed but not tested - HumanActivity left out
12/4/13 streamchannel completed but not tested
12/4/13 climate completed but not tested
12/4/13 landscape completed - leaves human activity out until Union encoding determined

1/11/13 (ABHR - LCR NZ) removed anzsoilml-landscape_all_1.xsd
1/11/13 (ABHR - LCR NZ) removed anzsoilml-landscape_hand.xsd
1/11/13 (ABHR - LCR NZ) moved content of stream_channels.xsd into landscape_leaf.xsd
1/11/13 (ABHR - LCR NZ) removed stream_channels.xsd
4/11/13 (ABHR - LCR NZ) updated humanactivity.xsd to replace LandTermValueCategory with subtypes
                        of TermValue_Date (LandUseValue, LandManagementValue, LandCoverValue)
4/11/13 (ABHR - LCR NZ) corrected EA encoding of some nillable properties (added missing nilReason attributes)
4/11/13 (ABHR - LCR NZ) corrected EA encoding of swe:Quantity/QuantityRange references for some properties
20/11/13 (BAS - CSIRO) changed schema location from http://anzsoil.org/anzsoilml-landscape to http://anzsoil.org/def/anzsoilml-landscape