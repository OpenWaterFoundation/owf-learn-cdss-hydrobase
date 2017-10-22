# Learn CDSS HydroBase #

This documentation provides training resources for Colorado's Decision Support Systems (CDSS) HydroBase database.

If you are reading this documentation, you have an interest in learning about how the State of Colorado
manages water resources data in the HydroBase database, and how you can use the database.
This documentation is intended to provide sufficient information to water resources engineers, water lawyers,
software developers, researchers, and others who are interested in Colorado's water resources data.

HydroBase is a [relational database](https://en.wikipedia.org/wiki/Relational_database), which more specifically uses
the [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) technology.

[Colorado Division of Water Resources](http://water.state.co.us) staff maintain several versions of HydroBase and related databases
necessary to do the work of State water agencies.  Examples of data maintained in these databases include:

* real-time streamflow data from the Satellite Monitoring System
* well permit applications
* water rights and diversion records

**This documentation is a work in progress and will contain notes for inserts until resources can
be devoted to filling in blanks.**

## Colorado's Decision Support Systems ##

Colorado's Decision Support Systems ([CDSS, cdss.state.co.us](http://cdss.state.co.us))
has been developed to answer important questions about Colorado's water resources.
CDSS efforts are led by the [Colorado Water Conservation Board (CWCB)](http://cwcb.state.co.us)
and [Colorado Division of Water Resources (DWR)](http://water.state.co.us).

![CDSS Website](images/CDSS-website.png)

One component of CDSS is the HydroBase databaes, in particular the "CDSS HydroBase", which
is used by modelers that have created model datasets as part of CDSS basin modeling projects.
The general term "HydroBase" refers to the DWR's database for Colorado's real-time and historical water resources data.

**This documentation focuses on the CDSS HydroBase and variations such as Colorado Informtion Marketplace dataset exports from HydroBase.**

## Open Water Foundation ##

The Open Water Foundation (OWF, [openwaterfoundation.org](http://openwaterfoundation.org)) is a 501(c)3 social enterprise
nonprofit that focuses on developing and supporting open source software to make better
decisions about water resources.  OWF helps to develop and maintain CDSS software and has a strong interest
in ensuring that CDSS software and HydroBase are effectively and efficiently used to address complex water resources issues.

OWF has created this website as a prototype to facilitate helping people understand and use HydroBase.

See also other [OWF learning resources](http://learn.openwaterfoundation.org).

## How to Use this Documentation ##

The documentation is organized in the order of basic concepts and then topics relevant to developing and supporting StateMod.

This website is intended as a companion to the StateMod source code repository and is the source of
information for software developers that support and enhance StateMod.

## Other HydroBase Learning Resources ##

The following are additional HydroBase learning resources:

* [HydroBase Data Dictionary](http://cdss.state.co.us/onlineTools/Documents/HBGuest.pdf).
* **TODO smalers 2016-11-20 need to hook in navigable HTML data dictionary, such as produced by TSTool**
* [A Hands-on Introduction to Conducting Water Rights Investigations](http://www.coloradowatertrust.org/resources-library//c/technical-resources) - Wilson Water Group training to Colorado Water Trust

## License ##

The license for this documentation is being determined in the CDSS open source project.
More information will be provided later.
However, at this time because this site is a prototype, there are no restrictions for use.

## Source Repository on GitHub ##

The source files for this documentation are maintained in a GitHub repository: [owf-learn-cdss-hydrobase](https://github.com/OpenWaterFoundation/owf-learn-cdss-hydrobase).

## Release Notes ##

This documentation was last updated 2017-10-21.
See the [Release Notes in the GitHub Project](https://github.com/OpenWaterFoundation/owf-learn-cdss-hydrobase#release-notes).
