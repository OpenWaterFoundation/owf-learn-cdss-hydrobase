# CDSS HydroBase / Primary Datasets

HydroBase includes a number of important datasets, represented as [tables](https://en.wikipedia.org/wiki/Table_(database))
and [views](https://en.wikipedia.org/wiki/View_(SQL)) in the database.
The names of the tables and the relationships between tables may not be intuitive,
and it may not be obvious how the data can be used in analysis and modeling.

Therefore, this documentation tries to explain HydroBase contents by focusing on important datasets, with reference to tables to provide details.
This approach allows connections to other representations of datasets, including those on the [Colorado Information Marketplace](http://data.colorado.gov)
and [StateMod model datasets](http://cdss.state.co.us/Modeling/Pages/SurfaceWaterStateMod.aspx).

Important datasets in HydroBase can be categorized as follows, and will be highlighted throughout this documentation to emphasize their importance:

**Reference Data** - reference data, static data, definitions, etc., are generally simple tables that contain
static data, such as the list of water divisions, water districts, counties, crop types, etc.
These tables are useful because then constrain possible data values, and they help form the vocabulary when discussing datasets.

**Stations** - locations where measurements are made (e.g., stream gages), but which are not Structures (see below).
These locations are  sometimes seemingly redundant with structure data because of different measurement networks.
For example, diversion records are associated with Structures (see below) but many diversion headgates also
have real-time measurement devices, which report through the [Satellite Monitoring System](http://www.dwr.state.co.us/Surfacewater/default.aspx).
This can be confusing because the identifiers for stations is typically different from structures.
**TODO smalers 2016-11-18 need to explain this with examples and describe how to deal with this.**

**Structures** - locations with water rights or other administrative data.  Structures are often built by humans (e.g., diversions, dams, wells, reservoirs).
However, natural features such as instream flow locations, springs, etc., are also considered as Structures within HydroBase because they
have associated administrative data such as water rights.
Structures are associated with water rights as follows:  a structure can have one or more water right(s) (but might actually have zero if rights have been abandoned,
but more on that later).
Structures can be abandoned and therefore users of structure data needs to be aware of abandoned and active structures, and their associated data such as diversion records.

**Water rights** - water rights are decreed in water court and define the location, amount, and use type(s) for the diversion of water
to meet a beneficial use.  Water rights are associated with a Structure as follows:  A water right must be associated with a structure.
The simple definition becomes more complex when considering the water source, alternate point of diversion,
whether absolute or conditional right, units of the water right (flow or volume), etc.  These complexities are
discussed with descriptions of the datasets.  See the specific discussion of water rights datasets:

* [Water Rights Datasets](../datasets/water-rights/)

**Well permits** - Well permits are another way to grant permission to divert and use water.
In recent times, an effort has been made to ensure that large wells also have water rights, with smaller wells being associated with
domestic wells, such as for rural areas where no treated water supplier is available.  **TODO smalers 2016-11-18 need to explain.**

**Time series** - Most Stations and Structures in HydroBase may have associated time series, which are lists of time/value pairs.
For example, diversion structures have time series indicating how much water was diverted through the headgate over time (day, month, year).
Reservoir time series indicate reservoir level, release, evaporation, etc.
Stream gage time series indicate flow by the gage.  Irrigated lands time series indicated the acreage grown for different crops.
Time series are collected and defined in different ways and it can be difficult to directly query HydroBase for time series.
This is why tools have been developed to facilitate data access, such as the on-line tools and TSTool.
For example, the TSTool time series identifier (TSID) convention provides a generic way to identify time series and
underlying software does the mapping to associate with various HydroBase tables.
