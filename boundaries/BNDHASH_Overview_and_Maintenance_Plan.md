# Vermont Administrative Boundaries (BNDHASH) Dataset Overview and Maintenance Plan

## Purpose

The Vermont boundaries (BNDHASH) dataset depicts Vermont villages, towns, counties, and Regional Planning Commissions (RPC) boundaries and repersents the best available boundaries from various data sources. The name BNDHASH comes from the concept of “hashing together” best-available Vermont boundary information.  

With the creation of the City of Essex Junction in 2022, Vermont now has 256 municipalities: 237 towns, 10 cities, 5 unincorporated towns, and 4 gores. While BNDHASH does not attempt to provide a legally definitive boundary, it is important that BNDHASH reviewed on an annual basis to maintain a reasonably accurate representation of Vermont’s municipal boundaries. The purpose of the document is to provide an overview of BNDHASH and detail the procedure for its annual update.

## Description
BNDHASH was originally developed from TBHASH which was the master town boundary layer prior to the development of BNDHASH. The Vermont Center for Geographic Information (VCGI) manages BNDHASH as an Esri geodatabase feature dataset which includes the following layers:

1. **VILLAGES** = Vermont villages
2. **TOWNS** = Vermont towns
3. **COUNTIES** = Vermont counties
4. **RPCS** = Vermont Regional Planning Commissions
5. **VTBND** = Vermont state boundary

These feature classes are stored separately with a set of topology rules which binds them. This arrangement ensures vertical integration of these boundaries, simplifying maintenance. All boundaries have been derived from “best available” sources with the accuracy of each feature depending on its source. In most cases, boundary data derived from a land survey is considered the most accurate. BNDHASH does **not** repersent a legally definitive boundary layer. It is intended to provide a reasonably accurate representation of these boundaries for general mapping purposes. BNDHASH also includes annotation text for town, county and RPC names.

## Schema
The *VT Data - Boundaries, All Lines* [dataset](https://geodata.vermont.gov/datasets/VCGI::vt-data-boundaries-all-lines-1/about) provides line-level attribution for all other BNDHASH layers.

|Field     |Description                                                              |
|----------|-------------------------------------------------------------------------|
|BNDTYPE   |Boundary type (state, county, town or village)                           |
|ARC_SCR   |Source of line location                                                  |
|SRC_NOTES |Additional notes for ARC_SRC field                                       |
|CADFNAME  |File used to digitize line                                               |
|SRCORG    |Organization or project which digitized line                             |
|ORIG_ARC  |Whether line is the original line included in the 1993 release of TBHASH |
|UPACT     |Whether line was added, moved or new                                     |
|UPD_DATE  |Date of update                                                           |
|UPD_NOTES |Additional notes                                                         |

## Maintenance

### Schedule
TBD

### Types of Updates

**Attribute Update** - Attribute updates indicate a non-boundary change such as a municipality changing the spelling of its name or changing its name completely. Municipal, village and county names are based on official names as defined with the US Geographic Names Information System (GNIS) which is managed by the US Board on Geographic Names (BGN). In Vermont official geographic names are administered by the Vermont Board of Libraries.

**Geometry Update**

- **Legal Update** - A legal update is a geometry change due to Municipal Act. This is the primary way VCGI makes boundary updates to BNDHASH. In most cases, town boundary disputes are resolved through the drafting of a new boundary survey by a licensed land surveyor. The surveys are reviewed and adopted by the towns, then made official by the Legislature via a Municipal Act. In cases where a new boundary survey is not drafted (this is often the case when there is no town boundary line dispute), VCGI will use the best information available.

- **Boundary Correction** - A boundary correction is geometry change due to new or improved boundary-related information. Other state department and agencies such as the Vermont Agency of Transportation (VTrans) and the Enhanced 911 Board (E911) maintain their own boundary data which may differ from BNDHASH. As part of the annual update, VCGI will compare their data to compare against BNDHASH.

### List of Sources
Below is the list of sources used to make updates in BNDHASH generally from most to least authoritative (and accurate):

1. Municipal Acts 
2. Land surveys 
    - Vermont State Archives  
    - Municipal Records  
    - Vermont Land Survey Library 
3. VTrans surveys 
4. ANR surveys 
5. LiDAR and orthoimagery 
6. Parcel data 
7. E911 data 
8. Green Mountain Forest data 
9. Historical maps 
10. USGS topographic maps 

## Related Datasets

### Geographic Area Names and Codes
The [Vermont Geographic Area Names and Codes Standard](https://vcgi.vermont.gov/resources/vermont-gis-standards-and-guidelines/geographic-area-names-and-codes-standard) is maintained by VCGI and is often updated in conjunction with BNDHASH. The standard is a series of standalone tables containing universal codes for the following geographic areas in Vermont:

- State
- Counties
- Cities, Towns, Gores, and Grants
- Villages
- Regional Planning Commissions

### Boundary Annexation Survey
The U.S. Census Bureau conducts the [Boundary and Annexation Survey](https://www.census.gov/programs-surveys/bas.html) (BAS) annually to collect information from tribal, local, and state governments about their legally defined geographic areas. This information is then used to update data maintained by the U.S. Census Bureau. 

BNDHASH is used to complete the Boundary and Annexation Survey (BAS) conducted by the U.S. Census Bureau each year. VCGI reports all boundary-related updates on behalf of Vermont municipalities.

## Legislation

### Land Surveys and the Vermont Land Survey Library
27 V.S.A. § 341
Chapter 005: Conveyance of Real Estate
Requirements generally; recording

[https://legislature.vermont.gov/statutes/section/27/005/00341](https://legislature.vermont.gov/statutes/section/27/005/00341)

27 V.S.A. § 1401
Chapter 017: Filing of Land Plats
Acceptance of survey plats; definition

[https://legislature.vermont.gov/statutes/section/27/017/01401](https://legislature.vermont.gov/statutes/section/27/017/01401)

27 V.S.A. § 1403
Chapter 017: Filing of Land Plats
Composition of survey plats

[https://legislature.vermont.gov/statutes/section/27/017/01403](https://legislature.vermont.gov/statutes/section/27/017/01403)

### Geographic Names
10 V.S.A. §§ 151 - 154
Chapter 009: Geographic Names

[https://legislature.vermont.gov/statutes/fullchapter/10/009](https://legislature.vermont.gov/statutes/fullchapter/10/009)

### Municipal Boundaries
24 V.S.A. § 1461
Chapter 047: Municipal Lines
Location or alteration of municipal lines; monuments

[https://legislature.vermont.gov/statutes/section/24/047/01461](https://legislature.vermont.gov/statutes/section/24/047/01461)

24 V.S.A. §§ 1421-1430
Chapter 045: Voluntary Consolidation of Towns

[https://legislature.vermont.gov/statutes/fullchapter/24/045](https://legislature.vermont.gov/statutes/fullchapter/24/045)

24 V.S.A. §§ 1481-1487
Chapter 049: Merger of Municipalities

[https://legislature.vermont.gov/statutes/fullchapter/24/049](https://legislature.vermont.gov/statutes/fullchapter/24/049)

17 V.S.A. § 2645
Chapter 055: Local Elections
Subchapter 002: Town Meetings And Local Elections in General
Charters; adoption, repeal, or amendment; procedure

[https://legislature.vermont.gov/statutes/section/17/055/02645](https://legislature.vermont.gov/statutes/section/17/055/02645)

### State Boundary
1 V.S.A. § 611
Chapter 015: New Hampshire-Vermont Boundary

[https://legislature.vermont.gov/statutes/section/01/015/00611](https://legislature.vermont.gov/statutes/section/01/015/00611)

