# CDSS HydroBase / Accessing HydroBase

HydroBase can be accessed multiple ways, as described in the following sections.

## Online HydroBase Resources

HydroBase provides data for the following online resources, including:

* [Interactive data displays on the CO DWR Data Search tools](http://water.state.co.us/DataMaps/DataSearch/Pages/DataSearch.aspx) - various
on-line query and display tools
* [HydroBase web services](http://water.state.co.us/DataMaps/WebServices/Pages/WebServices.aspx) - useful for automated data downloads
* Datasets exported to the [Colorado Information Marketplace](http://data.colorado.gov) (click on the Water icon) - State's open data portal
* Spatial data layers exported for the [CDSS Map Viewer](http://cdss.state.co.us/onlineTools/Pages/MapViewer.aspx) and data tools accessible from maps - map
displays using geographic information system tools

## Downloading and Using HydroBase

**Note:  Local installation of HydroBase puts the burden of troubleshooting on the user and State support
is limited.  The OpenCDSS project can help improve this process but users such as consulting companies may need to pay for support from
organizations like the Open Water Foundation.**

HydroBase is also available for download, with archives maintained by the Open Water Foundation, to facilitate software development and CDSS modeling.
A local copy of HydroBase allows for much faster data processing by tools such as StateDMI, TSTool, and StateView, which can be downloaded
from the [Open Water Foundation](http://openwaterfoundation.org/software-tools/colorados-decision-support-systems) and
[CDSS](http://cdss.state.co.us/software/Pages/SoftwareHome.aspx) websites.  These tools are also being moved to open source projects by OWF.

The following archives are not the authoritative source of all HydroBase versions but are provided to facilitate CDSS project work:

* [HydroBase Archive Download at Open Water Foundation](https://sites.google.com/site/cdssstaging/hydrobase/download).

Once downloaded and installed on a computer, HydroBase can be accessed by CDSS software tools.

**TODO smalers 2016-11-18 Need to fill this out with more background on the tools**

## Use TSTool to Query HydroBase

The CDSS TSTool software is useful for performing free-form queries on HydroBase because TSTool
provides a simple, standard interface to the HydroBase database (and other databases).
This requires knowledge of [SQL](https://en.wikipedia.org/wiki/SQL) and the HydroBase design for queries,
but provides opportunities for powerful automated queries.
Below is a summary of how to use TSTool to query HydroBase using a local copy of the database:

1. [Download and Install TSTool](http://openwaterfoundation.org/software-tools/tstool)
2. [Download and Install HydroBase](https://sites.google.com/site/cdssstaging/hydrobase/download)
3. Edit the `C:\CDSS\TSTool-Version\system\HydroBase.cfg` file so that:
	* `Enabled=True`.  This will enable a HydroBase datastore in TSTool.
	* `DataBaseName` is set to the version of HydroBase that was downloaded, for example `HydroBase_CO_20150304`.
	TSTool allows multiple datastores to be configured, each of which point to different databases, and
	therefore this property associates a specific HydroBase version with the general datastore name `HydroBase`.
4. Use the TSTool ReadTableFromDataStore command with the HydroBase datastore to run SQL statements and query data.
Note that this command can be used with any database that is enabled as a datastore.
Then use the table commands to process further or output to CSV and Excel.

**TODO smalers 2016-11-20 Need to rework how HydroBase connection defaults in TSTool so datastore is default for new downloads - work it
out as part of the OpenCDSS project**
