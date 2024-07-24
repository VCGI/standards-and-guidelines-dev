# Vermont GIS Parcel Data Standard

## Updates
- **October 20, 2016** - Version 2.3 adopted by Vermont Enterprise GIS Consortium
- **October 16, 2016** - Version 2.2 intermediate revised draft 
- **October 12, 2016** - Version 2.1 intermediate revided draft
- **August 19, 2016** - Version 2.0 draft posted for public comment
- **November 2013** - Version 1.1
- **March 2012** - Version 1.0

## Statutory Authority and Standard Review / Approval
The Vermont Center for Geographic Information (VCGI) has the [statutory authority](https://legislature.vermont.gov/statutes/fullchapter/10/008) to craft and adopt Vermont GIS standards and guidelines. Over the past 30 years, VCGI has worked with the Vermont GIS community to carefully craft these standards and guidelines, helping to ensure that Vermont GIS (VGIS) data is compatible with and useful to others in the Vermont GIS community. The [Transportation Bill of 2016 (Act 158)](https://legislature.vermont.gov/Documents/2016/Docs/ACTS/ACT158/ACT158%20As%20Enacted.pdf) created the Statewide Property Parcel Mapping Program by which a statewide digital parcel data layer (dataset) will be developed, maintained, and made available to state government, regional planning commissions, municipalities, and the public. The State’s Enterprise GIS Consortium (EGC) has been established as the organization responsible for reviewing and approving Vermont GIS standards crafted by VCGI in collaboration with the Vermont GIS Community.  

## Purpose
This document provides an overview of the municipal parcel mapping process and defines the technical requirements for participation in the statewide Parcel Program. A unification of the Vermont GIS Parcel Data Standard and the Vermont GIS Parcel Mapping Guidelines, this document reflects the best practices for maintaining municipal parcel data in the context of the statewide [Parcel Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) managed by VCGI. Listers, assessors, and other town officials may reference this document to support their duties as they relate to the development and maintenance of digital parcel maps and data. Adherence to the technical requirements outlined in this document is required for participation in the Parcel Program and ensures uniformity between municipal parcel data submitted by towns that VCGI in turn makes publicly available statewide. 

## Introduction
Digital parcel maps (also referred to as tax maps or property maps) and the geographic data used to make them (GIS data) are among the most important local government information assets a town owns. Parcel data is NOT the equivalent of legal property records (deeds) or land surveys, but it does assist municipal officials with functions such as accurate property tax assessment, conservation, planning, and zoning. Parcel maps are for tax assessment purposes and, unlike areas outside New England, are not the legal (cadastral) record of property ownership. While property boundaries on parcel maps often serve as a proxy for ownership, any authoritative representation of property ownership must be based on records from the municipality and/or work by a licensed professional land surveyor.  

As part of the 2017-2019 Parcel Project, the State worked with several mapping vendors to ensure digital parcel maps were standardized across Vermont for inclusion in the statewide parcel dataset. The scope of standardization included matching local parcel IDs to the statewide School Property Account Number (SPAN) in a uniform format. Modifying parcel boundaries, however, was out of scope. [Statewide parcel data products](https://geodata.vermont.gov/pages/parcels) are reflective of the quality of data available at the time the three-year project was executed, as well as [updates that have since occurred in a town](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6) as voluntarily submitted to VCGI. VCGI currently manages the Parcel Program to ensure that the data collected in this statewide effort stay current, available, and useful throughout Vermont. The program hosts the following applications to view and use these data anywhere in Vermont, free of charge to municipalities:

- [Parcel Viewer](https://maps.vcgi.vermont.gov/ParcelViewer)
- [Town Mapping Status dashboard](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6) 

Parcel data are uniformly joined with the annual, statewide Grand List. If desired, towns can link parcel data to their interal Grand Lists or CAMA products to display even more local information. Officials can show taxpayers how proposed development or changes in municipal services and regulations will affect them and their neighbors. In many towns, parcel data also help to provide public notices, allocate resources, and carry out other municipal services.

The Parcel Program also provides guidance on how to improve the accuracy and usefulness of parcel data over time. The need for accurate parcel data has increased as more mapping tools and business processes rely on up-to-date parcel geometry and attribution. To achieve the maintenance objectives of the Parcel Program, towns most commonly contract with a mapping services provider or employ a GIS professional. This document provides guidelines for municipalities working with a mapping vendor or GIS professional, either when renewing a contract or engaging them for the first time. The guidelines are also applicable to municipalities with internal GIS staff who may refer to them for various specifications and dataset submission requirements.  

Adequate preparation is essential prior to entering any contract for parcel mapping services. The municipality should evaluate its needs for listers, planning professionals and volunteers, zoning administrators, and public works staff, all of whom will benefit from using the resulting product. Major considerations include the type of products to maintain and efforts toward their continuous improvement; evaluating existing resources of official public records, personnel, facilities, data processing, and technical and administrative support; and determining funding and parcel data maintenance plans. Contact your Regional Planning Commission or VCGI for information on how to access and use the data.

## Parcel Mapping Process

### Preparing for Updates  
Maintenance of digital parcel data is detailed, technical, open-ended, and time-consuming. While some municipalities do have the resources necessary to maintain their own parcel data, all towns should carefully evaluate the feasibility of maintaining their own parcel data. In general, most towns will subcontract this work to the private sector. For municipalities interested in working with a mapping vendor, there are varying levels of support the town can provide in terms of time and materials which may include any records or information that can be used to improve not only parcel geometry and parcel attribution but also boundary lines between parcels. These materials may include parcel attribution information from the Grand List, municipal tax maps, recorded surveys, and deeds. 

Following the Parcel Project, all Vermont municipalities have standardized digital parcel data available to view and download free of charge. This data is available through the Vermont Open Geodata Portal and can be used as the basis to continue or start updating parcel geometry and attribution. Additionally, VCGI provides a [geodatabase template](https://vcgi.vermont.gov/document/geodatabase-template-parcel-data-standard) that can help in the conversion to or creation of parcel data meeting the technical requirements outlined in this document as some municipalities may choose to maintain their digital parcel data internally with different specifications.

### Contracting a Mapping Vendor
Municipalities who decide to work with a mapping provider should provide a Request for Proposal (RFP) which includes a set of mapping services to be performed (and the frequency in which they should be preformed) as well as available resources and oversight/communication expectations. While composing the RFP, towns should also consider the status of the following:

- A description of the town’s current tax maps, including the date they were last updated, how changes were tracked to date, and how the tax maps will be transmitted. Some of this information for data published by VCGI is available in the [Town Mapping Status dashboard](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6).
- A description of the data from the town’s Computer Assisted Mass Appraisal (CAMA) software. This should include schema-related information that the mapping service provider may find essential such as a list of tables, definitions of fields, and table relationships, if any. It should also include a description of how the data will be transmitted.
- A description of the town's current geographic information system (GIS). If a new mapping vendor is being chosen, this section should describe how the town's GIS data is currently hosted and maintained, and how this data may be transmitted to a new mapping vendor.

Cost is obviously important, yet a mapping vendor should not be selected on cost alone. A level of expertise is required to evaluate mapping professionals and contract proposals. If the expertise is not available at the municipal level, your town's [Regional Planning Commission](https://www.vapda.org/) may be able to provide such assistance. Assessment guidance as it relates to parcel mapping may also be provided by your town's [District Advisor](https://tax.vermont.gov/municipal-officials/listers-and-assessors/district-advisors).

### Performing and Reviewing Updates
Updates are performed after a signed contract is transmitted to the mapping vendor. A phased approach for improvements over multiple years may be needed if quotes come in over budget. This approach allows the municipality to gradually improve map accuracy.

Town staff can assist the mapping vendor with timely updates by answering questions and providing relevant source documentation for parcel changes. In most cases, records at the municipal clerk’s office should be made available for the vendor's use at no charge within reasonable working hours. Once the initial update has been completed, the mapping vendor should provide a “draft” version of the parcel map(s) for [review by the municipality](https://vcgi.vermont.gov/resources/frequently-asked-questions/parcel-program-faqs#17). This is an opportunity for the town to provide any additional feedback on the accuracy of the maps before they are finalized and submitted to VCGI.

### Finalizing Updates
Upon town approval, the vendor may [submit](https://vcgi.vermont.gov/data-and-programs/share-map-data) updated parcel data to the Parcel Program on behalf of the town. VCGI will publish updated town data after reviewing and joining it with the latest available statewide Grand List. Occasionally, an error in recently updated parcel data is flagged by a user of a statewide parcel tools, such as a property owner reviewing their parcel in the Parcel Viewer. For significant errors, the relevant parcel should be noted for incorporation in the town's next update by the town’s mapping provider (if applicable). VCGI will work with town staff to address minor inaccuracies. In such cases, corrections may be reflected in statewide parcel data products more quickly. 

## Parcel Data Standard

### Format and Naming Convention
All spatial and tabular data are to be delivered as a single version 10.x or higher file geodatabase (.gdb) that is named VTPARCELS_TOWNNAME_YYYY.gdb where YYYY represents the year of submission to the Parcel Program. All spatial data must be in the [Vermont State Plane Coordinate System](https://legislature.vermont.gov/Documents/2024/Docs/ACTS/ACT086/ACT086%20As%20Enacted.pdf). Each file geodatabase must be accompanied by a stand-alone FGDC CSDGM metadata file in XML format that is named VTPARCELS_ TOWNNAME_YYYY.xml where YYYY represented the year of submission to the Parcel Program.

### Metadata Specifications
A single metadata file in FGDC CSDGM XML format is required as part of a parcel data submission.  All feature classes and non-spatial tables are documented in that metadata file.  Content is required for the following core metadata elements:

- Identification_Information/Citation/Citation_Information/Title
- Identification_Information/Citation/Citation_Information/Originator
- Identification_Information/Citation/Citation_Information/Publication_Information/Publisher
- Identification_Information/Description
- Identification_Information/Time_Period_of_Content 

The Grand List year to which the data is current, using the format YYYY. The date of Grand List export for use in parcel data development shall be noted. 

- Identification_Information/Spatial_Domain  
- Identification_Information/Use_Constraints

Populate this attribute with the following disclaimer: *This data layer is not a legal survey.  It is not a legal conveyance or description of property and is intended for planning purposes only. VCGI and the State of VT make no representations of any kind, including but not limited to the warranties of merchantability or fitness for a particular use, nor are any such warranties to be implied with respect to the data.* 

- Data_Quality_Information

Include Lineage with Source_Information and Process_Step(s). 

- Entity_and_Attribute_Information

Include an individual Detailed_Description for every feature class (or shapefile) and non-spatial table. Provide Attribute information for all fields

### Feature Class Specifications

**Active Parcels** - This feature class consists of polygon features for all active parcels listed in a municipality’s Grand List as well as polygon features for public road rights-of-way, railroad rights-of-way, trail rights-of-ways, and surface water areas that serve as property boundaries. Active parcels represent the collective property boundaries of all abutting parcels under the same ownership. Each Grand List record should be assigned to only one active parcel record in the feature class where the SPAN serves as the unique identifier. Active parcels published as part of the Parcel Program are joined the annual Grand List published by the Vermont Department of Taxes. 

In cases where an active parcel represents of more than one Grand List record (e.g., condominiums, mobile home parks, seasonal camps, etc.) a new unique identifier should be populated in lieu of the SPAN per the syntax C-XXX-#### where XXX represents the first three digits in the municipality’s SPAN and #### represents the next available integer starting with 0001. This new unique identifier serves as a placeholder SPAN to be assigned the appropriate Grand List SPANs using the Intersection Table. 

|Field Name  |Field Type    |Length|Allow NULL|
|------------|--------------|------|----------|
|SPAN        |Text          |13    |Yes       |
|MAPID       |Text          |80    |Yes       |
|PROPTYPE    |Text          |9     |No        |
|YEAR        |Short Integer |4     |No        |
|TOWN        |Text          |30    |No        |
|SOURCENAME  |Text          |80    |Yes       |
|SOURCETYPE  |Text          |19    |No        |
|SOURCEDATE  |Text          |8     |No        |
|EDITMETHOD  |Text          |20    |No        |
|EDITOR      |Text          |50    |No        |
|EDITDATE    |Text          |8     |No        |
|MATCHSTAT   |Text          |9     |No        |
|EDITNOTE    |Text          |254   |Yes       |

- SPAN - A statewide 11-digit unique identification number assigned to each property in a municipality’s Grand List. Each SPAN in the Grand List is to be assigned to only one active parcel record in the feature class. Apart from some railroad rights-of-way which may have a SPAN in the Grand List, all non-parcel features represented in the feature class should be assigned a NULL value. Active parcels with no SPAN (no record in the Grand List) should also be assigned a NULL value.

- MAPID - A locally assigned unique identification number assigned to each property and used in conjunction with the SPAN.

- PROPTYPE - Type of property or area. Private road rights-of-way which overlay underlying parcels should be assigned as public road rights-of-way with a note added to the EDITNOTE field designating a private right-of-way. The inclusion of private road rights-of-way is not required.

|Value     |Description                                                  |
|----------|-------------------------------------------------------------|
|PARCEL    |Active parcel                                                |
|ROW_ROAD  |Public road right-of-way                                     |
|ROW_RAIL  |Railroad right-of-way                                        |
|ROW_TRAIL |Legal trail right-of-way (included in the Town Highway Maps) |
|WATER     |Surface water area                                           |

- YEAR - The year of the submission represented by 4 digits. 

- TOWN: The name of the municipality. Spaces are permitted. Spell out any abbreviations and remove any additional punctuation like periods or apostrophes (e.g., ‘SAINT JOHNSBURY’ and ‘AVERYS GORE’). 

- SOURCENAME - The name of the source information. 

- SOURCETYPE - The type of source information. 

|Value                |Description                                                                                                      |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
|SURVEY/PLAT          |Survey or plat                                                                                                   |
|DEED                 |Deed                                                                                                             |
|LINES OF OCCUPATION  |A physical boundary, such as a stone wall, which may be detected by technologies such as lidar or aerial imagery |
|NON-SCANNED TAX MAP  |Non-scanned tax map                                                                                              |
|UNKNOWN              |Unknown source such as pre-existing parcel data                                                                  |
|MULTIPLE             |Multiple sources                                                                                                 |

- SOURCEDATE - The date of the source information per the syntax YYYYMMDD. 

- EDITMETHOD - The method of capturing the feature’s geometry. 

|Value                |Description                                                                                           |
|---------------------|------------------------------------------------------------------------------------------------------|
|HEADS UP DIGITIZING  |Capturing geometry into a layer that is superimposed to underlying source data such as aerial imagery |
|COORDINATED COGO     |COGO lines placed in real-world coordinates                                                           |
|NON-COORDINATED COGO |COGO lines placed by best fit to other evidence                                                       |
|COORDINATED CAD      |CAD lines placed in real-world coordiantes                                                            |
|NON-COORDINATED CAD  |CAD lines place by best fit to other evidence                                                         |
|GIS GRADE GPS        |GIS-grade GPS collection                                                                              |
|RTK GPS              |High-precision GPS collection conducted with Real-Time Kinematic (RTK) positioning                    |
|OTHER                |Other                                                                                                 |
|UNKNOWN              |Unknown                                                                                               |

- EDITOR - The name or editor that added or modified the feature. 

- EDITDATE - The date on which the feature’s geometry or attribution was added or modified per the syntax YYYYMMDD.  

- MATCHSTAT - The status of the relationship between a record in the Grand List and the feature by SPAN.

|Value     |Description                                                    |
|----------|---------------------------------------------------------------|
|MATCH     |An active parcel with at least one valid Grand List record     |
|UNMATCHED |An active parcel which does NOT have a valid Grand List record |
|EXEMPT*   |For all features which are not active parcels                  |

*An EXEMPT entry in the MATCHSTAT field is not intended as an indication of tax exemption in this context. Property that may be tax exempt (e.g., Native American tribes, town-owned land, schools, etc.) should have a MATCH or UNMATCHED status as applicable.

- EDITNOTE - Additional information about the feature.

**Intersection Table** - The Intersection Table relates records from the Grand List to records in the Active Parcels (polygons) feature class to account for parcels associated with more than one Grand List record. The Intersection Table does not contain spatial data.

[IMAGE]

|Field Name  |Field Type    |Length|Allow NULL|
|------------|--------------|------|----------|
|GIS_SPAN    |Text          |13    |Yes       |
|GLIST_SPAN  |Text          |13    |Yes       |
|YEAR        |Short Integer |4     |No        |
|TOWN        |Text          |30    |No        |

- GIS_SPAN - The SPAN exactly as attributed in the SPAN field in the Active Parcels (polygon) feature class. Every SPAN listed in the Active Parcels (polygon) feature class, excluding NULLs, must be listed in the GIS_SPAN field of the Intersection Table. Duplicate SPANs are valid when one record in the Active Parcels (polygons) feature class is associated with more than one record in the Grand List; this is often the case for any placeholder SPANs (e.g., C-XXX-####). Each GIS_SPAN must have a corresponding GLIST_SPAN in the Intersection Table. 

- GLIST_SPAN - The SPAN exactly as attributed in the municipality’s Grand List. Each GLIST_SPAN listed in the Intersection Table must be a valid SPAN in the municipality’s Grand List. For records in the Grand List which are not yet included in the municipality’s parcel data, each record in the Grand List should be added as individual records in the Intersection Table where the associated SPANs are used in both the GIS_SPAN and GLIST_SPAN fields. 

- YEAR - The year of the submission represented by 4 digits. 

- TOWN - The name of the municipality. Spaces are permitted. Spell out any abbreviations and remove any additional punctuation like periods or apostrophes (e.g., ‘SAINT JOHNSBURY’ and ‘AVERYS GORE’).

**Inactive Parcels** - This feature class consists of all inactive parcels listed in the municipality’s Grand List and their related active parcels. All abutting parcels under the same ownership should be represented as separate polygons within this feature class. Parcels representing the collective boundary of all abutting parcels under the same ownership are modeled in the Active Parcels (polygons) feature class. 

[IMAGE]

|Field Name  |Field Type    |Length|Allow NULL|
|------------|--------------|------|----------|
|STATUS      |Text          |8     |No        |
|PARENTSPAN  |Text          |13    |Yes       |
|SPAN        |Text          |13    |No        |
|MAPID       |Text          |80    |Yes       |
|PROPTYPE    |Text          |9     |No        |
|YEAR        |Short Integer |4     |No        |
|TOWN        |Text          |30    |No        |
|SOURCENAME  |Text          |80    |No        |
|SOURCETYPE  |Text          |19    |No        |
|SOURCEDATE  |Text          |8     |No        |
|EDITMETHOD  |Text          |20    |No        |
|EDITOR      |Text          |50    |No        |
|EDITDATE    |Text          |8     |No        |
|MATCHSTAT   |Text          |9     |Yes       |
|EDITNOTE    |Text          |254   |Yes       |

- STATUS - Indicates if the record is for an active or inactive parcel. 

- PARENTSPAN - A statewide 11-digit unique identification number assigned to each property in a municipality’s Grand List. If the record is for an inactive parcel, populate field with the SPAN of the associated active parcel. If the record is for an active parcel both PARENTSPAN and SPAN fields should be populated with the appropriate SPAN. Duplicates are permitted. 

- SPAN - A statewide 11-digit unique identification number assigned to each property in a municipality’s Grand List. Only populate this field for records of active parcels. Duplicates are not permitted. 

- MAPID - A locally assigned unique identification number assigned to each property and used in conjunction with the SPAN. 

- PROPTYPE - Type of property or area. 

- YEAR - The year of the submission represented by 4 digits. 

- TOWN - The name of the municipality. Spaces are permitted. Spell out any abbreviations and remove any additional punctuation like periods or apostrophes (e.g., ‘SAINT JOHNSBURY’ and ‘AVERYS GORE’). 

- SOURCENAME - The name of the source information. 

- SOURCETYPE - The type of source information.

|Value                |Description                                                                                                      |
|---------------------|-----------------------------------------------------------------------------------------------------------------|
|SURVEY/PLAT          |Survey or plat                                                                                                   |
|DEED                 |Deed                                                                                                             |
|LINES OF OCCUPATION  |A physical boundary, such as a stone wall, which may be detected by technologies such as lidar or aerial imagery |
|NON-SCANNED TAX MAP  |Non-scanned tax map                                                                                              |
|UNKNOWN              |Unknown source such as pre-existing parcel data                                                                  |
|MULTIPLE             |Multiple sources                                                                                                 |

- SOURCEDATE - The date of the source information per the syntax YYYYMMDD. 

- EDITMETHOD - The method of capturing the feature’s geometry.

|Value                |Description                                                                                           |
|---------------------|------------------------------------------------------------------------------------------------------|
|HEADS UP DIGITIZING  |Capturing geometry into a layer that is superimposed to underlying source data such as aerial imagery |
|COORDINATED COGO     |COGO lines placed in real-world coordinates                                                           |
|NON-COORDINATED COGO |COGO lines placed by best fit to other evidence                                                       |
|COORDINATED CAD      |CAD lines placed in real-world coordiantes                                                            |
|NON-COORDINATED CAD  |CAD lines place by best fit to other evidence                                                         |
|GIS GRADE GPS        |GIS-grade GPS collection                                                                              |
|RTK GPS              |High-precision GPS collection conducted with Real-Time Kinematic (RTK) positioning                    |
|OTHER                |Other                                                                                                 |
|UNKNOWN              |Unknown                                                                                               |

- EDITOR - The name or editor that added or modified the feature. 

- EDITDTATE - The date on which the feature’s geometry or attribution was added or modified per the syntax YYYYMMDD.  

- MATCHSTAT - The status of the relationship between a record in the Grand List and the feature by SPAN. Only populate if the record is for an inactive parcel. 

|Value     |Description                                                   |
|----------|--------------------------------------------------------------|
|MATCH     |An active parcel with at least one valid Grand list record    |
|UNMATCHED |An active parcel which does NOT have a valid Grand List record|

- EDITNOTE - Additional information about the feature. 

**Parcel Lines (Deprecated)** - Municipalities may still submit the line counterpart to the Active Parcels (polygons) feature class as part of their parcel data submission, but it will not be published as part of the statewide parcel dataset.

## Complimentary Vermont GIS Data Products

### Property Transfers
The frequency in which property transfers occur far outpaces what can be reflected in the statewide Grand List which is published annual. The need for more real-time parcel attribution (specifically ownership) prompted the development of a workflow to publish the [Vermont Property Transfers layer](https://vcgi.vermont.gov/data-release/vermont-property-transfers-now-available-spatial-data). This layer provides approximate point locations and associated public information collected by the [Department of Taxes](https://tax.vermont.gov/property/property-transfer-tax) under [32 V.S.A. § 9606](https://legislature.vermont.gov/statutes/section/32/231/09606) for all property transferred by deed in Vermont beginning in January 2019 through present. The layer will be updated weekly. Most transfers (70%) will appear in the dataset within four to five weeks of the sale’s closing date. This layer is available as a standalone [data layer](https://geodata.vermont.gov/datasets/VCGI::vt-property-transfers/about) or can be viewed within the Parcel Viewer.

### Aerial Orthoimagery
The accuracy of existing parcel geometry for some towns may need to be improved. Aerial orthoimagery is maintained by VCGI as part of the [Imagery Program](https://vcgi.vermont.gov/data-and-programs/imagery-program). It is a freely available statewide resource that municipal officials and mapping service providers can use to improve the spatial accuracy of parcel maps. An orthophoto is an aerial photograph that has been rectified such that it is equivalent to a map at the same scale. The State funds the collection of orthophotos which can support the creation and maintenance of municipal tax maps and digital parcel data. Color imagery is used as reference layer in the Parcel Viewer and all [aerial orthoimagery datasets](https://geodata.vermont.gov/pages/imagery) are available for download through the Vermont Open Geodata Portal. Towns that wish to have additional coverage beyond what is provided by the State (for example, high resolution imagery in village areas) can contact their Regional Planning Commission for assistance in requesting "[buy-up areas](https://vcgi.vermont.gov/data-and-programs/imagery-program/imagery-buy-options)."

### Lidar-Derived Bare-Earth Hillshade
Light Detection and Ranging (lidar) data is collected using a small aircraft equipped with a laser scanner as well as a Global Positioning System (GPS) and an Inertial Navigation System (INS). Through the process of transmitting and detecting brief laser pulses, millions of individual points are collected. Collectively, this "point cloud" represents the 3D positions of objects like buildings, vegetation, and even the ground itself. Lidar data is maintained by VCGI as part of the [Lidar Program](https://vcgi.vermont.gov/data-and-programs/lidar-program).

A digital elevation model (DEM) is one of many products dervied from lidar data. DEMs repersent the earth's topographic surface and are considered "bare-earth" becuase they do not  inlude surface features such as buildings and vegetation. Hillshades enhance the appearance of the topographic surface using light and shadow. All [lidar-dervied products](https://geodata.vermont.gov/pages/elevation) are available for download through the Vermont Open Geodata Portal.

### Vermont Land Survey Library
The [Vermont Land Survey Library](https://maps.vcgi.vermont.gov/landsurveylibrary/) is a digital repository for land surveys maintained by VCGI as part of the Parcel Program but is maintained separately from parcel data. The library was developed in accordance with the amendment of [27 V.S.A. § 341](https://legislature.vermont.gov/statutes/section/27/005/00341) by the passing of Act 38 in 2019 requiring a land survey for a property line change, including a property line adjustment or a subdivision, effective January 1, 2020. In addition to this mandatory practice for all Vermont municipalities, sections [27 V.S.A. §1401](https://legislature.vermont.gov/statutes/section/27/017/01401) and  [27 V.S.A. §1403](https://legislature.vermont.gov/statutes/section/27/017/01403) require a digital copy of a land survey to be submitted to the library by a licensed land surveyor or a municipal official. Submissions are reviewed by VCGI before publishing to the library for public reference. While there is no legal requirement, land surveys predating the amendment can be submitted to the library by a licensed land surveyor or a municipal official. Others working in the public sector may also submit a land survey to the library (e.g., the Vermont Agency of Transportation).  

The library consists of a web map that displays the general location of a land survey with its related information (e.g., date of land survey, town name, and the name of the land surveyor) stored in a pop-up table. A copy of the land survey is also stored in the pop-up table as a PDF attachment. The public may search and view land surveys that have been published to the library. Other spatial data maintained by VCGI such as parcel data and orthoimagery are also available for additional reference. Parcel data are maintained independently from the library and thus parcel data may not reflect the property lines represented in a published land survey. VCGI encourages municipalities and GIS consultants to use the library to inform parcel data updates as applicable.

## Data Quality Challenges

### Inactive Parcels
There is no formally defined practice or requirement for the upkeep of inactive parcels in Vermont, and maintenance practices may vary by town. In some cases where two or more abutting parcels are owned by the same individual, one parcel is considered the main (or active) parcel while the remaining parcels are considered inactive. From a tax perspective, this is done in part so that a single owner of multiple abutting parcels receives one tax bill. Accordingly, and for mapping purposes, all abutting parcels under the same ownership are represented as a single parcel with the cumulative property boundary and acreage within the “active” or main parcel data layer. Associated attribution for the inactive parcels will reflect the aggregate active parcel. 

For those municipalities who choose to track inactive parcels, we recommended that a town work with their contracted GIS vendor to at least maintain these data in accordance with the VT Parcel Data Standard and submit them to the Parcel Program to be published along with the “active” parcel data layer. Published inactive parcels are viewable in both the Vermont Parcel Viewer and Town Mapping Status applications. In the future, it may be necessary for listers, assessors, the Vermont Department of Taxes, GIS professionals, and other related professionals to develop uniform policy, procedures, and requirements for the tracking and maintenance of inactive parcels. 

Alternatively, and contingent on an updated definition of a parcel in Vermont, all parcels representing a single unit of real property that may be separately sold and/or for which a single title exists—together a common definition of a parcel in other states—may be drawn and maintained as a single data layer, thus removing the distinction between “active” and “inactive” parcels. In their place a single, smallest-unit parcel layer could then be possible statewide. Existing inactive parcel data would be archived for reference as needed.

### Deeded Acreage versus GIS Acreage
The histories of parcels in Vermont may be long and complicated, with varied techniques used in the description of their bounds. It is not uncommon for deeds, for example, to refer to landmarks that no longer exist and/or are poorly documented in their position, at least in modern terms. Digital GIS parcel data also may have a development history in which reference data such as topographic maps and orthoimagery have greatly improved, yet original data built on less accurate sources persists. As a result, there may be differences between the listed grand list acreage and a calculated map or GIS acreage for the same parcel.

Differences between grand list (deeded) and GIS (calculated) acreage can be large and, in such cases, should be reviewed using best available, present-day information. Both acreage fields are within data published by the Parcel Program and are viewable within the Parcel Viewer and Town Mapping Status applications. Still, the calculated acreage should be considered an approximation of parcel size and should not be used for tax assessment purposes given the representative nature of parcel data. Acreages listed in a written deed should be given preference when significantly different from the calculated acreage, since a written deed represents the historic record of conveyance for property ownership and the primary legal record defining a property and its boundaries. We recommended that towns work with their contracted GIS vendor and review all relevant sources to address significant acreage discrepancies. Large discrepancies may warrant a modern land survey of the parcel(s) in question to update the legal documentation of their bounds, which in turn may be used to update the parcel(s) listed grand list acreage.

### Road Right-of-way and Road Centerlines
In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and with bearing on parcel mapping. Common, practical experience is that public rights-of-way such as roads and highways are just that—areas not to be obstructed by abutting private property owners. State highways, for example, involve the State purchasing lands between the road centerline and abutting parcel, whereas Towns may not. These differences contribute to a lack of clarity about the area that is within a right-of-way and between an abutting private parcel and road centerline and have occasionally led to differences in their depiction and resulting acreage calculations. How to map and calculate acreage given rights-of-way is an important consideration for town officials as parcel data continue to be an integral part of statewide mapping tools and property tax assessment.

Data adherent to VT Parcel Data Standard depicts rights-of-way as practically experienced, which shows parcels to the edge of the right-of-way and not the road centerline. This is the recommended mapping convention. Learning from some [other states](https://app.leg.wa.gov/rcw/default.aspx?cite=84.36.210), a change in Vermont statue could codify common experience and specify how public rights-of-way are to be handled for tax purposes, with mapping practices following suit. Doing so would encourage uniform practice across municipalities. Current Vermont law related to this subject is detailed in [19 V.S.A. § 1111](https://legislature.vermont.gov/statutes/section/19/011/01111).

### Parcels with Multiple SPANs
Most parcels have one SPAN to be joined to their respective Grand List record. It is not uncommon however to have a parcel with more than one SPAN, such as with condominiums and other unlanded structures. These cases reflect multiple units with different owners sitting atop a single common parcel, resulting in multiple SPANS for the underlying land. This situation alone is not the issue, but problems can arise with unattributed, non-uniform and/or print-focused means of accounting for them. For example, building footprints are often used by mapping professionals to visually distinguish between an unlanded structure and the common property, particularly as a paper tax map convention. While visually clear, this creates areas within a parcel that are not necessarily parcels. Without clear standards, this may result in confusing attribution and uneven calculations and distribution of acreage across individual units that, in some cases, should sum to the total common property acreage.

For digital parcel mapping, it is recommended to have related SPANs (such as all the SPANs associated with a new condominium development) assigned to one parcel. This allows common property to be included as part of the calculated acreage for analytical purposes. And just as with inactive parcels, it may be necessary for listers, assessors, the Vermont Department of Taxes, GIS professionals, and other related professionals to develop uniform policy, procedures, and requirements for tracking and depicting condominiums, mobile homes, energy infrastructure, and any other unlanded structures. Codifying standards and uniform practices across related professions and software tools will go a long way to ensuring accurate acreage, attribution, and proper depiction of these multi-part parcels. Current Vermont law related to this subject is detailed in [27 V.S.A. § 1322](https://legislature.vermont.gov/statutes/section/27/015/01322) and [27A V.S.A. § 1-105](https://legislature.vermont.gov/statutes/section/27a/001/00105).

### Parcels without a SPAN
The SPAN is a statewide unique identification number linking the parcel geometry to the Grand List. All property must have a unique record in the Grand List and have a corresponding SPAN. This includes non-taxable lots owned by the town, Native American tribes, the State of Vermont, federal entities, and non-profit organizations. While represented in the parcel data, some common property associated with mobile home parks and condominiums may not be the Grand List and therefore may not have a SPAN. These parcels are considered “unmatched.” Other examples of parcels that may be unmatched include cemeteries and fragments of parcels unclaimed or claimed by more than one abutting parcel. In such cases, local parcel IDs, which are often used in conjunction with the SPAN, become the primary unique identifier. Subdivisions that have occurred more recently than the date of the last grand list join may temporarily appear as without a SPAN, but these are a special case and should be attributed in the next Grand List join.

For parcels without SPANs, attribute information can be stored in the parcel data in lieu of the Grand List entry. It is recommended to provide a short description detailing the nature of its unmatched status to provide clarity for users viewing the parcel data through the Parcel Viewer or other online mapping tool. Similarly, parcels which do not have a SPAN in the Grand List because of a recent subdivision should be considered unmatched until a SPAN has been assigned. Finally, sometimes municipal grand lists or other sources contain new SPANs that are included in parcel data updates but do not yet have a match in the statewide Grand List. In this case, retain the SPAN in the parcel data (active/inactive data layers and the intersection table) and leave the status “Unmatched”. The missing SPAN should have a match once the subsequent version of the statewide Grand List is published. 

### Multi-part Polygons
State statute defines a parcel as "all contiguous land in the same ownership, together with all improvements thereon" (32 V.S.A. § 4152(a)(3)). Though not specifically stated above, the accepted interpretation is that division of a tract by a road does not create two parcels (but instead creates a multi-part parcel, a non-contiguous parcel, or a multipolygons). A parcel split by an ‘Exempt’ feature such as a road or water body, therefore, is still considered a single entity with a single data record and Grand List entry despite being represented as multiple polygons. Multi-part polygons that are distant from each other may suggest an error in the data; examine supporting documentation to determine if disassociating the polygons by splitting into multiple parcels is warranted. 

### Gaps and Overlaps
Topology refers to the spatial relationships between adjacent and neighboring features. The Active parcel data layer should contain no gaps or overlaps between parcels. If gaps or overlaps are discovered within the Active parcel layer, refer to source documentation for the best way to address them. In the case of gaps, sometimes a new feature is created to account for the error, with corresponding information added to the attribute table. Often these new features are left Unmatched unless a valid SPAN can be identified in the Grand List. 

Gaps and overlaps are most often found along town boundaries. Since all Vermont municipalities maintain parcel data separately and with varying methods, it is inevitable that parcels along town boundaries may be misaligned with respect to those in a neighboring town. Currently, VCGI recommends that municipalities work with neighboring towns to identify and correct these discrepancies to the best of their abilities. These efforts may require coordination with additional parties including surveyors and mapping vendors. 

### Border Boundary Discrepancies 
[INSERT TEXT]

### CAMA Integration and Multiple Systems
[INSERT TEXT]

### General Practices to Improve Data Quality
Accurate parcel representation and attribution are complicated by the speed at which different updates take place. Property transfers occur relatively quickly, while the statewide Grand List is published once per year and parcel geometry is updated on a rolling, sometimes irregular, basis. With so many moving pieces, it is important to acknowledge that parcel data are representative in nature and are continually evolving and improving. To facilitate long-term improvement of statewide parcel data, VCGI recommends the following:

- Municipalities should perform regular, consistent maintenance of parcel-related changes and updates to assist mapping vendors, GIS staff, and/or VCGI. This can include compiling and organizing relevant source documentation (surveys, deeds, etc.) for reference when parcel data updates are performed. 

- SPANs should be included for all parcels. If the parcel/SPAN is not in the Grand List, include a note in the layer’s EDITNOTE field to provide context (e.g., federal land, utility, etc.). 

- To the extent possible, municipalities should work with neighboring towns to address parcels along town boundaries with edge-matching discrepancies (gaps and overlaps).

- Review parcels in reference to best-available GIS information, particularly aerial imagery, as well as surveys. 

- Prioritize changes and professionalize maintenance to ensure timely updates. 

## Discrepancy Lists
A town’s discrepancy list forms the basis for identification of errors in digital parcel data and is often the first step to help address some of the challenges described in the previous section which negatively impact the usefulness of parcel data over time. Beyond any issues noted in previous updates, the discrepancy list may be amended to include anything identified by municipal officials as well as residents.  

The discrepancy list should be maintained in an agreed upon format indexed by SPAN and parcel identification number corresponding with the map. It should also include all relevant information from municipal land records and surveys. Items to note in a discrepancy list include but are not limited to the following:

- Parcels to be subdivided or merged 

- Boundary line changes 

- Active parcels to be updated to Inactive parcels (and vice versa) 

- Parcels without a SPAN 

- Parcels with an incorrect SPAN 

- Parcels to be linked to multiple SPANs 

- Corrections to be made to the town’s internal Grand List

A copy of the discrepancy list serves as a complementary tool for mapping providers to use during a parcel data update in addition to their standard practice reviewing existing municipal land records and surveys. The use of a discrepancy list should not necessarily relieve the mapping provider of their responsibility to continue efforts to map and identify the parcels properly. If, in the view of the municipality, the mapping provider has not used all the obvious and reasonably economical methods of approach, they should request the contractor to do so at the contractor’s expense.

## Accessing and Using Parcel Data Published by the Parcel Program
[INSERT TEXT]

## Access and Integration with Other VT GIS Data
[INSERT TEXT]

## Appendices

### Checklist for Municipalities Working with a Mapping Vendor or Municipal GIS Staff to Update Parcel Data

- [ ] Maintain a list of parcel changes each year to facilitate updates. Collect and organize corresponding source documents including surveys, plats, and deeds. Copies of recent surveys may also be available in the [Vermont Land Survey Library](https://maps.vcgi.vermont.gov/landsurveylibrary/) which is integrated into the Parcel Viewer.

- [ ] Maintain a Discrepancies List to track existing issues with parcel data that the vendor/GIS staff should address in the subsequent update.

- [ ] Review the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6), particularly the ‘Town Match Status’ tab, to locate parcels that may not have a match in the statewide Grand List (e.g., a missing or incorrect SPAN). Review all Unmatched parcels and add any changes/corrections to list of updates.

- [ ] Send the vendor/GIS staff the list of changes and discrepancies needed to perform updates. Support update process by answering questions and making source materials available.

- [ ] Review best practices around inactive parcels and determine how the municipality accounts for them spatially, if at all.

- [ ] If necessary, work with vendor/GIS staff to prioritize issues to be addressed in the current update and those that may be reserved for later updates. Not all edits may make it in one update cycle. 

- [ ] Review updated parcels prior to submittal to VCGI. Confirm that parcels without SPANs have been reviewed/resolved, inactive parcels are included if desired, multi-SPAN parcels are accurately represented, and large differences between deeded and GIS acreages are examined. Verify other documented changes and discrepancies have been addressed. Provide feedback to vendor/GIS staff as needed.

- [ ] Verify that vendor/GIS staff understands how to upload final products to VCGI via the [web submission form](https://vcgi.vermont.gov/data-and-programs/share-map-data), and that submittals have been received/published as expected using the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6). The status map is refreshed weekly; towns listed in the publishing queue are typically reviewed and published by VCGI within 1 to 3 weeks of receipt.

- [ ] Review the municipality’s update information in the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6) by selecting the town in the upper right search bar. Confirm that information in the right-side panel related to parcel maintenance (GIS publish date, current vendor, update frequency, etc.) is correct. Contact VCGI with any updates or changes.

- [ ] If working with a mapping vendor, revisit contract as needed. Consider any revisions based on desired deliverables (town-specific digital parcel viewer, paper maps, PDFs, etc.), budget, adherence to parcel data standards, timeline and schedule, etc.

### Checklist for Municipalities Finding a Mapping Vendor and/or Updating Parcel Data without a Mapping Vendor or GIS Staff

- [ ] Review the most recent parcel data for your municipality using the [Parcel Viewer](https://maps.vcgi.vermont.gov/parcelviewer/) and the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6).

- [ ] Review parcel data maintenance practices of other municipalities using the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6), particularly practices of neighboring towns and common [mapping vendors](https://airtable.com/appI2jeVIZTBdYISK/shrARBcXQsMkEvxz3/tbl1phknn1b8uhXt2) across the state. [Regional planning commissions](https://www.vapda.org/regions.html) (RPCs) may also be able to contract for parcel mapping services.

- [ ] Determine the frequency and immediate need for updates based on the number of discrepancies and changes each year. 

- [ ] Determine if there are official or employees of the municipality with the training, skills, and resources to support the town in making GIS/digital parcel data updates. If so, see checklist above.

- [ ] Review best practices around inactive parcels and determine how the municipality accounts for them spatially, if at all.

- [ ] If no municipal employees are available or able to perform parcel data updates, reach out to the appropriate RPC and/or mapping vendors to determine availability for services. Send a Request for Proposals (RFP) to interested parties outlining the needs and expectations of the municipality.

- [ ] Select a mapping vendor based on best fit including qualifications, price, and desired deliverables. At a minimum, mapping vendors should provide digital parcel data that is suitable for submittal to VCGI based on the standards in this document. Confirm that the municipality will own the final deliverables it paid for and will not have to pay again to access them in the future.

- [ ] Even without a mapping vendor or GIS staff, keep an ongoing list of parcel changes and a Discrepancies List. Collect and organize corresponding source documents including surveys, plats, and deeds, including any submissions to the [[Vermont Land Survey Library](https://maps.vcgi.vermont.gov/landsurveylibrary/). Maintaining good documentation of parcel changes and source documents will greatly facilitate updates when resources, staff, and/or funds allow. [Contact VCGI](https://vcgi.vermont.gov/resources/frequently-asked-questions/parcel-program-faqs#24) as needed for additional guidance and to communicate potential limitations surrounding updates.

### Checklist for Mapping Vendors or Municipal Staff when performing Parcel Data Updates

- [ ] Download published parcel data from the [Open Geodata Portal](https://geodata.vermont.gov/) for the municipality in geodatabase format. This ensures the most current version of the parcels will be updated, including any edits made by VCGI following the previous submission by the municipality/vendor.

- [ ] Data can also be loaded into the [empty Geodatabase Template](https://vcgi.vermont.gov/document/geodatabase-template-parcel-data-standard), which contains the appropriate layers, schema, and domains for parcel data. Update the file and folder names per the Format and Naming Convention section of this document.

- [ ] Using the municipality’s compiled list of updates and resources (surveys, deeds, municipal Grand List, etc.), perform GIS edits to the data in ArcGIS Pro 3.X or another compatible mapping software. Document edits in the appropriate fields of the Active parcels layer as needed.

- [ ] Review best practices around inactive parcels and determine how the municipality accounts for them spatially, if at all.

- [ ] Communicate with the municipality regarding their Discrepancy List; confirm existing/known issues with current parcels are addressed using appropriate source documents.

- [ ] Review the Data Quality Challenges section as needed to confirm that multi-part polygons, inactive parcels, multi-SPAN parcels and unlanded structures, road centerlines, and parcels without SPANs are being represented in the layer correctly.

- [ ] Review multi-SPAN parcels: confirm correct syntax is used for placeholder SPANs in the Active parcels layer (see the Parcels with Multiple SPANs section of this document).

- [ ] Review the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6), particularly the ‘Town Match Status’ tab, to locate parcels that may not have a match in the statewide Grand List (e.g., a missing or incorrect SPAN). Review all Unmatched parcels and address any changes/corrections to the extent possible. Additional communication with town officials may be required.

- [ ] Perform topology check on parcels to confirm layer does not include gaps or overlaps.

- [ ] Confirm that in the Active parcels layer all ‘PARCEL’ entries in the PROPTYPE field are either ‘MATCH’ or ‘UNMATCHED’ in the MATCHSTAT field. The MATCHSTAT ‘EXEMPT’ should only be used for roads, water bodies, and some railroad features.

- [ ] Check SPAN field in Active parcels layer for duplicates (not permitted). Duplicates often result when a parcel is subdivided but SPANs have not been updated. 

- [ ] Submit a draft version of a parcel data update to the municipality for review. Work with the municipality to address any unresolved or erroneous items using necessary source documents.

- [ ] Prior to finalizing updated parcels, confirm that data are formatted correctly and adhere to standard requirements, including coordinate system, naming conventions, schema, and metadata.

- [ ] Submit finalized, zipped geodatabase file to VCGI using the [web submission form](https://vcgi.vermont.gov/data-and-programs/share-map-data). VCGI will confirm receipt via email, and the municipality will appear in the ‘In Publishing Queue’ map of the [Town Mapping Status Application](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6) (application is updated weekly, therefore submitted town may not appear immediately). *Updated parcels will typically be reviewed by VCGI in 1 to 3 weeks and published for public access via the [Parcel Viewer](https://maps.vcgi.vermont.gov/parcelviewer/) and for download via the [Open Geodata Portal](https://geodata.vermont.gov/).*

## Sample Parcel Data Maintenance Schedule
The schedule below includes dates determined by the Vermont Department of Taxes for contextual reference. Italicized items are recommendations for how municipalities might work with a vendor/GIS staff to maintain their digital parcel data, with updates submitted annually to VCGI. This timeframe is intended to be an example; specific municipalities should make adjustments depending on their needs, resources, and the contract with their map vendor.

[INSERT SAMPLE]

## Glossary
**Abutting** - Sharing a contiguous border or boundary. 

**Active parcel** - In cases where two or more abutting parcels have the same owner, parcel to which a single tax bill is associated with all the abutting parcels under the same ownership.  

**Adjacent** - Two or more polygons sharing a side or boundary. 

**Appraisal** - A valuation or estimation of property value by person of suitable qualifications, usually including a description of the property at a specific date. 

**Assessor** - Elected or appointed official who determines the fair market value of property for a municipality. 

**Attribute** - Nonspatial information (e.g., property owner) used to describe spatial data and often stored in a table.

**Base map** - Map containing background upon which geographic information is overlayed and analyzed. Portrays basic spatial reference onto which other more specialized spatial information is placed. Often includes permanent physical features such as topography or hydrology, and/or manmade features such as political boundaries or roads; may also be aerial imagery. 

**Boundary** - Indicates border or limit. Typically designates the extents of contiguous areas such as parcels, easements, zoning designations, water bodies, etc. 

**Building footprint** - A polygon representing the general location and shape of a building, or other manmade structure, relative to its surroundings.

**CAD (computer-aided design)** - The use of computer-based software to aid in design and drafting processes. Unlike GIS, CAD does not inherently or easily include associated spatial information or relationships with drawings. 

**Cadastral survey** - Documents the boundaries of land ownership by the production of documents, diagrams, sketches, plans/plats, charts, and maps. Originally used to ensure reliable facts for land valuation and taxation.  

**Calculated acreage** - The estimated acreage of a parcel derived by using GIS. 

**CAMA (computer-assisted mass appraisal)** - Computer software that helps maintain property information. In Vermont, CAMA platforms are handled on a town-by-town basis. These systems may be a source of some of, but ultimately are not the same as data provided by the statewide parcel dataset. 

**Centerline** - Applied to a street, road, right-of-way, or other strip of land of uniform width, defines the line midway between the side lines of said strip. 

**Centroid** - The geometric center of a spatial feature. 

**COGO (coordinate geometry)** - Computer program within a CAD or GIS system that can process data such as bearings distances, and angles to generate precise spatial representation of land features and survey control networks. Similar to metes-and-bounds surveying, an input begins at a point, moves at a given angle or in a certain direction for a set distance, and continues in the same fashion until a geographic feature is completely outlined. 

**Condominium** - System of ownership of individual units in a multiple unit building. A single real property parcel with all the unit owners having a right in common to use the common elements with separate ownership confined to the individual units which are serially designated. 

**Contiguous** - Lying next to or close to one another; adjacent, having a common boundary, sharing an edge. 

**Conveyance** - In real property law, a transfer of legal title to land. It may be a deed, mortgage, or lease.  

**Coordinate system** - Reference framework for determining distance and direction in relative terms with respect to their location. A geographical coordinate system uses latitude and longitude to locate point on the Earth; most other (projected) coordinate systems use regularly spaced grids placed on artificially derived planes.  

**Classification** - Designation of lands as being valuable or suitable for specific purposes, uses, or resources.

**DA (District Advisor)** - Liaison from the Vermont Department of Taxes who oversees the listers/assessors of a municipality or region to assist with property valuation.  

**dBASE (.dbf)** - A tabular data format in which tabular information is stored, either as a component of a shapefile/geodatabase or as a stand-alone table.  

**Deed** - A legal document which transfers title to real property. 

**Deeded acreage** - The acreage of a parcel as recorded in the municipality’s land records and reflected in the Grand List. 

**DEM (digital elevation model)** - A digital representation of a continuous variable over a two-dimensional surface by a regular array of z-values referenced to a common data. Typically used to represent terrain relief. 

**Discrepancy list** - List of properties with ownership or area conflicts/uncertainty above a threshold agreed upon by municipality and map consultant. 

**Domain** - Rules that describe the available values of a field type. Used to constrain the values allowed in a particular attribute for a table or feature class to minimize erroneous entries.

**Easement** - An interest of right in land owned by another that entitles its holder to a specific limited use. Often granted across someone’s property for ingress and egress.  

**Egress** - The right to exit a property.

**Feature** - A GIS representation of a real-world object. 

**Feature class** - Homogeneous collections of features with a common spatial representation (most commonly points, lines, or polygons) and set of attributes stored in a database table. Feature classes are created and stored in a geodatabase as stand-alone objects, or they can be combined into a feature dataset.  

**Feature dataset** - A collection of related feature classes that share a common coordinate system. Used to facilitate controller datasets including parcel fabrics and topology, and to integrate related feature classes spatially or thematically. 

**FGDC-CSDGM** - Content Standard for Digital Geospatial Metadata authored and endorsed by the Federal Geographic Data Committee. The standard to intended to provide a common set of terminology and definitions for the documentation of digital geospatial data. 

**Geodatabase** - A data storage format that is based on relational database concepts. The geodatabase format can store spatial and non-spatial data types and supports complex data object relationships. The geodatabase format is scalable from the file-based “file geodatabase” (.gdb) implementation to an enterprise implementation within enterprise-oriented DBMS systems. Allows data layers to be created with geometry types that include points, lines, and polygons, as well as the creation and storage of annotation data layers.  

**Geometry** - A GIS representation of spatial data using points, lines, and polygons. 

**GIS (Geographic information systems)** - Computer-based tools used to store, visualize, and analyze spatial data. 

**Grand List** - Statewide list published each year on April 1st by the Vermont Department of Taxes, containing information on parcel ownership, location, size, and assessed value, and used in the collection of all property taxes in Vermont.  

**Grantee** - A person, firm, or corporation to whom land or easements are conveyed or granted; the purchaser or recipient on a deed. 

**Grantor** - A person, firm, or corporation granting or conveying land; the seller on a deed.

**Inactive parcel** - In cases where two or more abutting parcels have the same owner, parcel(s) that does not receive a tax bill. May be represented as multiple parcels within a larger boundary with a single SPAN and owner, for example. 

**Indexing** - Logically ordering information components by the values present in a key field. An identifier used to access stored information, typically within a database. 

**Ingress** - The right to enter a property.  

**Ingress-Egress Easement** - See Private Right-of-Way. 

**Intersection Table** - A table included with parcel data submissions that uses SPANs to link records of the municipality’s Grand List with the spatial parcel dataset.

**Land Surveying** - Practice of surveying areas for their correct determination and description and for conveyance or for the establishment of land boundaries and the plotting of lands and subdivisions. 

**Legal Description** - A written statement recognized by law as the definite location of a tract of land by reference to a survey recorded map or adjoining property. 

**Lister** - Elected official who determines the fair market value of property for the municipality in which they, the lister, reside. 

**Map ID** - Unique parcel identifier, determined by the municipality, which is distinct from the unique identifier in the Grand List.  

**Metadata** - Information about data such as its origin, content, quality, and limitations.  

**Metes and Bounds** - Description of perimeter of a tract of land containing recitations of measurements and boundaries in sequence around a parcel of land from the point of beginning. Bearings and distances usually given for each line. 

**Multi-part parcel** - A non-contiguous geometry object (multi-part polygon) modeling one Grand List record as one record in the GIS data. For example, a single parcel split into two pieces by a water body or road but with a single SPAN and Grand List record.

**Open data** - Data which are freely available for public use.  

**Parcel** - Vermont State statute defines a parcel as "all contiguous land in the same ownership, together with all improvements thereon" (32 V.S.A. § 4152(a)(3)). Though not specifically stated, the accepted interpretation is that division of a tract by a road does not create two parcels (see multi-part parcel). 

**Parcel data** - A map index of property ownership, consisting of a general representation of property boundaries (geometry) joined with Grand List information (attribution). 

**Parcel Program** - The 2020-present VCGI-led maintenance effort of collecting and publishing uniform, voluntarily submitted digital municipal parcel data in GIS format statewide. 

**Parcel Project** - The 3-year (2017-2019) federal and state-funded effort to make all Vermont municipal data uniformly digital and attributed, including with SPAN numbers. 

**Polygon** - A closed multi-sided geometric shape. 

**Plat** - A map showing the boundaries and other features of land parcels that are being newly established for transfer, sale, or building development. 

**Private Right-of-Way (or Ingress-Egress Easement)** - Arranged for access to locations by traversing one or more parcels. Ingress-egress easements that overlay underlying parcels are not considered to be public rights-of-way and are not considered to be parcels.

**PVR (Property Valuation and Review)** - Division of the Vermont Department of Taxes that works with municipalities to oversee and administer the property tax system. 

**Public Right-of-Way** - An area that is legally dedicated to public right-of-way purpose. Public rights-of-way areas do not have SPAN numbers.  

**Raster data** Data comprised of an evenly spaced grid where each cell has a value representing thematic or continuous data across a surface. 

**Real estate** - Land, improvements to the land, and certain buildings.  

**Real property** - Land and generally whatever is erected upon, growing on, or affixed to the land. 

**RPC (Regional Planning Commission)** - Political subdivisions of Vermont created by their member municipalities. RPCs act as a link between municipal affairs and state government in fields including land use, transportation, housing, economic development, and environmental quality.

**Schema** - The structure or design of a database or database object (e.g., table, view, index, etc.). Typically defines the tables, fields in each table, relationships between fields and tables, and the grouping of objects within the database. 

**Service or Web Service** - Spatial data made available via an internet connection. 

**Shapefile:=** - A GIS data format that is widely used in proprietary and open source realms of GIS software. The shapefile format allows data layers to be created with geometry types that include points, lines, and polygons.  

**SPAN (School Property Account Number)** - Unique, statewide eleven-digit identification number assigned by a municipality to a property. 

**State plane coordinate system** - Projected coordinate system comprised of geographic zones designed for specific regions of the United States to minimize distortion of a three-dimensional spherical surface onto a two-dimensional plane. 

**Subdivision** - Division of a lot, tract, or parcel of land into two or more lots, plats, sites, or other divisions of land for immediate or future sale or building development.  

**Survey** - The process of recording observations, making measurements, and marking the boundaries of tracts of land.

**Thematic map** - Representation of data to show trends or patterns. Data are highlighted or emphasized using properties and values such as color and line width.  

**Topology** - A set of defined relationships between links, nodes, and centroids. Topology describes how lines and polygons connect and relate to each other, and forms the basis for advanced GIS functions such as network tracing and spatial analysis. 

**Tract** - Generally, a metes and bounds survey of an area at large within a township. In modern surveying, specifically refers to a parcel of land that lies in more than one section or that cannot be identified completely as a particular section. 

**Traverse** - In surveying, a sequence of lengths and directions of lines between points on the Earth, obtained by field measurements and used to determine the positions of the point through use of trigonometric computations. 

**Unlanded building or structure** - A condominium unit, mobile home, camp, or other structure that is a unit of real estate which is separate from the underlying land surface. In some cases, the underlying land is rented.

**VALA (Vermont Assessors and Listers Association)** - Professional membership organization of municipal assessing officials and affiliates involved in the management of property assessment. 

**VAPDA (Vermont Association of Planning and Development Agencies)** - Association that governs municipal planning and land use regulations, as well as guiding Vermont’s eleven Regional Planning Commissions (RPCs).  

**Vector data** - The storage of x, y, and z coordinates connected to form points, lines, areas, and volumes. Vector data are best suited to store discrete, well-defined data that can be clearly delimited.  

**Vermont Open Geodata Portal** - A clearinghouse website that serves freely available Vermont GIS data that are published and maintained by different State of Vermont agencies and departments. 

**VLCT (Vermont League of Cities and Towns)** - Nonprofit, nonpartisan organization that serves Vermont local government through advocacy, municipal assistance, risk management, legislative support, and consultation. 

**VTPIE (Vermont Property Information Exchange)** - An integrated system overseen by the Tax Department to collect Vermont’s statewide education grand list and to manage the statewide education property tax system, to be used by every municipality in the state. Integrates with parcel data served by the Vermont Parcel Program. 

 **XML (Extensible Markup Language)** - Simple text-based format for representing structured information. In GIS data, .xml files are used to share changes or updates among geodatabases and between the geodatabase and external systems.         
  
