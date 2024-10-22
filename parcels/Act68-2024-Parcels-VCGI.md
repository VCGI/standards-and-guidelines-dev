# Purpose

This document outlines all recommendations related to parcel mapping and data maintenance as related to [Act 68 of 2023](https://legislature.vermont.gov/bill/status/2024/H.480). It is authored by the Vermont Center for Geographic Information (VCGI), state stewards of the [Statewide Property Parcel Mapping Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) since 2020, established via [19 V.S.A. § 44](https://legislature.vermont.gov/statutes/section/19/001/00044). The recommendations aim to improve parcel data quality to support timely, fair, accurate, and modern property valuation and reappraisals as sought by Act 68, which [asks the Tax Department to](https://legislature.vermont.gov/Documents/2024/Docs/ACTS/ACT068/ACT068%20Act%20Summary.pdf):

> [create] recommendations and considerations for distinguishing between different types and characteristics of property and their uses, and how different property data could be used to make policy decisions.

# Overview of All Recommendations

| **Recommendation**                                                                      | **Statute Change** | **Payment to Towns** | **Technical Guidance** | **New Technology** |
|:---------------------------------------------------------------------------------------:|:------------------:|:-----------:|:----------------------:|:------------------:|
| [1. Update Parcel Definition in VT Statute from "Contiguous" to Separate and Marketable Lots or Pieces of Real Property](#recommendation-1-update-parcel-definition-in-vt-statute)                                              | X                  |             |                        |                    |
| [2. Reward Standardized Digital Parcel Data Submittal to SoV via Per Parcel Payment](#recommendation-2-reward-digital-parcel-submittal-to-sov-via-per-parcel-payment)          | X                  | X           |                        |                    |
| [3. Implement VT CAMA Data Standard and Require Submittal to SoV](#recommendation-3-implement-vt-cama-data-standard-and-require-submittal-to-sov)                       | X                |             | X                      |                    |
| 4. Clarify Right-of-Way Mapping for Tax Purposes in VT Statute                          | X                  |             |                        |                    |
| 5. Clarify Grand List vs. GIS Acreage Guidance                                          |                    |             | X                      |                    |
| 6. Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract |                    |             | X                      | X                  |
| 7. Offer Updated Statewide Parcel Contract Guidance for Municipalities                  |                    |             | X                      | X                  |
| 8. Pilot Remotely-Sensed Tools to Support Appraisals                                    |                    |             |                        | X                  |
| 9. Modernize Current Use Map Standards and Submittals                                   |                    |             |                        | X                  |
| 10. Consider Updating and Moving Parcel Program in VT Statute                           | X                  |             |                        |                    |
| 11. Coordinate With Concurrent Efforts to Digitize Land Records                         |                   |             |                        | X                   |

# Recommendation 1: Update Parcel Definition in VT Statute
## Summary
- Change the current parcel definition from a "contiguous" parcel defintition to one that requries tracking of separate and marketable pieces of real estate.
- This will replace the practice of mapping and tracking "inactive" parcels on a separate data layer and instead require towns to map and track all separate parcels individually, regardless of common ownership.
- "Contigous" parcels aggregated by common ownership may still be created for the purposes of tax billing, but they remain solely administrative.

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defines a parcel as:
> (3) A brief description of each parcel of taxable real estate in the town. “Parcel” means all contiguous land in the same ownership, together with all improvements thereon.

This is a "contiguous" parcel definition, depicted in figure 1 as type 1. Separate lots are grouped together by ownership for administrative purposes, primarily the sending of a single tax bill per owner per "parcel". Separate lots are sometimes managed as "inactive" parcels, although that term is not defined outside of the [parcel data standard](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) and their upkeep by towns is not uniform. The marketability of individual lots is not clear, and neither is it for how towns should map and track lots within a combined parcel. Aggregate parcel deliniation further complicates assignment of highest and best use valuation as assesors may have to generalize across several different lot types. Data management and downstream analysis are also negatively impacted by an aggregate, contiguous parcel definition.

![image](https://github.com/user-attachments/assets/6855b335-1e09-41fa-99d5-b4df4066b416)
*Figure 1: Existing contiguous parcel definition, depicted as option 1 on the left, and the proposed separate parcel defintion, depicted as option 2 on the right. The proposed separate parcel definition removes the need for tracking "inactive" parcels.*

Alternatively, defining parcel as a separate and marketable lot or piece of real property would bring parcel identification in line with their common understanding as "lots" while also reducing the need to generalize highest and best use across several different lots combined by owner (not use) during valution. This change would enable improved parcel documentation, ease highest and best use valuation, faciliatate data maintenance and analysis, and continue to allow aggregation by owner for tax billing. 

As there are several variations in the timing of when a separate lot or piece of real property is created, an updated parcel defintion could be written so as to allow a legal document (deed or title), subdivision plats, or sale to help define the bounds of the separate mapped and tracked area. Existing "inactive" parcels, where they exist and are maintained, may be added to the "active" parcel layer and be attributed, maintain their unique SPAN and be attributed as completely as possible. Once added, maintenance of inactive parcels as separate entities on a separate data layer should cease.

These changes in parcel definition and mapping practices would increase the current count of parcels statewide from roughly 340,000 to at least 380,000. "At least" is stated as currently only 70% of towns (178 total) have submitted their inactive parcels as digital parcel data to VCGI. It remains unknown how many of the other 30% of towns actively track inactive parcels digitally.

## Example Statute Update
> 32 V.S.A. § 4152 (a)(3) A brief description of each parcel of taxable real estate in the town. “Parcel” means a separate and marketable lot or piece of real estate. ~~all contiguous land in the same ownership, together with all improvements thereon~~

## Parcel Definition Alternatives

### Aggregate Mapped Unit Defined by Ownership (Contiguous)

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defined parcel. This is a "contiguous" parcel definition. Separate parcels are grouped together by ownership for administrative purposes, primarily the sending of a single tax bill per owner per "parcel".

Depicted visually, a contiguous parcel definition means that the two parcels below, shown split with a dotted green line and both of which have the same owner, are drawn as the single outer rectangle. This results as one "parcel" in the spatial data layer.

![image](https://github.com/user-attachments/assets/239c3a7e-e6f5-44cd-bb89-e8768e81a1da)

Each of the two individual parts are considered "inactive" parcels, by practice only, and not uniformly across towns.

### Separate Mapped Unit, Defined by Practice

Example:
> A separately assessed lot or piece of real property - *New York State Property tax and assessment administration definitions / [guidance](https://www.tax.ny.gov/research/property/equal/assessrpt/b_define.htm)*

### Separate Mapped Unit, Defined by Unique Identifier

> "Parcel" means a separate plot of land as identified by the municipality tax map and lot number. - *[New Hampshire Admin. Code § Cub 301.15](https://casetext.com/regulation/new-hampshire-administrative-code/title-cub-chairman-current-use-board/chapter-cub-300-criteria-for-open-space-current-use-assessment/part-cub-301-definitions/section-cub-30115-parcel)*

### Separate Mapped Unit, Defined by Legal Document

> "Legal parcel" means any parcel of real property that may be separately sold in compliance with the Subdivision Map Act (Division 2 (commencing with Section 66410) of Title 7 of the Government Code). - *[California, Sierra County](http://sierracounty.ca.gov/AgendaCenter/ViewFile/Agenda/05052014-115). In Compliance with State Subdivision Law.*

This example is notable in that any **one** of the following must be met to define a legal parcel, per commentary by [CA Real Estate Law Firm](https://www.lee-associates.com/elee/sandiego/Newsletter/2017April/Miller.pdf):
> - A lot shown on a Final Map. (Major Subdivision Map)
> - A lot or parcel shown on a Record of Survey approved by the Board of Supervisors or Planning Commission.
> - A parcel shown on a Parcel Map or Certificate of Compliance recorded in lieu of a Parcel Map.
> - A recorded Certificate of Compliance.
> - A parcel shown on an approved Division of Land Plat.
> - A parcel shown on a Lot legalization Plat used as evidence of legal parcel prior to a Certificate of Compliance.
> - A parcel shown on an approved Boundary Adjustment Plat.
> - A parcel described in a Grant Deed or other bona fide conveyance document recorded prior to February 1, 1972. The deed/document does not have to be in the name of the present owner. However, it must describe the perimeter boundaries only of the subject property and no other contiguous property. The legal description and County Recorder’s information must be legible to County staff. The Deed need not be an original or certified copy.

There is no statewide subdivision requirement in Vermont, and not all municipalities require subdivisions. Thus, several instruments may be relied upon to help define a parcel (deed, sudvision plat where required by municipality, or property transfer / sale).

### Separate Mapped Unit, Defined by Combination

Any combination of the examples above.

## Related VT Statutes

[32 V.S.A. § 4152](https://legislature.vermont.gov/statutes/section/32/129/04152) - Taxation and Finance / Grand Tax Lists / Grand List of Town

[27 V.S.A. § 601](https://legislature.vermont.gov/statutes/section/27/005/00601) - Title 27: Property / Chapter 5: Conveyance of Real Estate / Subchapter 007 : Marketable Record Title 

# Recommendation 2: Reward Digital Parcel Submittal to SoV via Per Parcel Payment
## Summary

- Institute a per parcel payment to municipaltiies to aid costs associated with parcel data maintenance.
- Make disbursement of this per parcel payment to municipalities contingent on submittal of [Vermont GIS Data Standard-compliant](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) digital parcel data to VCGI, maximum once per yer per town.
- Per parcel payment is to be X, funded by Y, with estimated annual cost of Z.

Descriptive text.

# Recommendation 3: Implement VT CAMA Data Standard and Require Submittal to SoV
## Summary
- Point
- Point
- Point

## CAMA Data Components

### Design and Implement VT CAMA Data Standard
Four CAMA software providers operate in Vermont as of October 2024:
- MicroSolve (NEMRC)
- ProVal (Aumentum)
- Vision Government Solutions CAMA
- AssessPro (Catalis, Formerly Patriot)

### Implement Changes to Parcel Definition in CAMA Data

Existing CAMA data software solutions offer advanced data maintenance capabilities and should accomodate a parcel definition change to separate and marketable pieces of real estate. Data entry and maintenance practices will need to adjust to reflect these changes.

### Normalize Attribution and Mapping of Unlanded Structures

The [stacked polygons method](#stacked-method---recommended) is the current recommendation per the Vermont GIS Parcel Data Standard and continues to be recommended after considering the pros and cons of all methods detailed below. 

To improve the functionality of this method, the following recommendations should be considered: 

1. While condominiums represent a vast majority of unlanded structures reflected in statewide parcel data, it is necessary to create a comprehensive list of different types of unlanded structures to be uniformly attributed in CAMA and subsequent Grand List records. The Vermont GIS Parcel Data Standard defines an unlanded building as a “condominium unit, mobile home, camp, or other building that is a unit of real estate which is separate from the underlying land surface.”
   
2. This list can be used to differentiate between unlanded structures in the parcel polygons layer, and if uniformly applied in CAMA and Grand List attribution, can be easily filtered for each record. Each unlanded structure can be represented as a prefix of two or three letters:
  * CO for condominiums
  * CA for camps
  * MH for mobile homes
  * SA for solar arrays
  * WT for wind turbines

3. While not the intended purpose, the SOURCENAME field in the parcel polygon layer can also be used to track this information.

4. This list can also be used to create GIS SPANs in the Intersection Table based on the type of unlanded structure. The same two-letter system described above can be implemented followed by the town code (first three digits of the town SPAN) and a four-digit numeric count.

5. Tax Department guidance on attribution of unlanded structures should be updated and made uniform to reflect the above prefixes and mapping practices (e.g., in the Listers and Assessors Handbook).

**Background**

Statewide standardized parcel data in Vermont is currently comprised of parcel geometry, the approximate parcel boundary lines drawn as closed multi-sided shapes (parcel polygons) as sourced from municipalities, and parcel attribution from the annual Grand List collected and published by the Tax Department. These two components are joined together by a matching School Property Account Number (SPAN) in the attribute table of the parcel polygons layer and in the Grand List. In most cases, each polygon is joined to one Grand List record but it’s not uncommon for more than one Grand List record to be joined to the same polygon. This happens most often with condominiums as they are typically described by their percentage of undivided interest in the common area and facilities rather than discrete boundaries that can be easily represented by polygons. While VCGI has provided some guidance on mapping condominiums per the Vermont GIS Parcel Data Standard, a more comprehensive recommendation for mapping all types of unlanded structures is necessary to improve data quality, clarity, and ease of use.

**Current Unlanded Structure Mapping Practices in Vermont**

***
#### Discrete and Distributed Methods

Building footprints  are often used to visually distinguish between unlanded structures and the common land, particularly as a paper tax map convention. The difference between the “Distributed” and “Discrete” building footprint methods is whether or not the common land has a SPAN. Per the Vermont GIS Parcel Data Standard, “in some instances, a deed specifies a percentage of common land ownership to each condominium unit and the common land does not have a SPAN number. In other instances, a deed does not allocate the common land, and the common land does have a SPAN number.”

Image 1: Discrete Method Mapping of Condos | *Source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)*

![image](https://github.com/user-attachments/assets/2ff17158-461a-490d-8062-6c014960c6f0)

Image 2: Distributed Method of Mapping Condos | *Source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)*

![image](https://github.com/user-attachments/assets/b39db8ec-ef97-477d-b394-b303d2ff0c4d)

Pros
- Creates visual distinction between unlanded structures and common land
- Avoids potential confusion caused by the use of different GIS and Grand List SPANs in the Intersection Table
  
Cons
- Time intensive to create/maintain individual building footprints geometry

***
#### Stacked Method - Recommended

Stacked polygons use a standalone Intersection Table to relate multiple SPANs from the Grand List to the same “placeholder” SPAN assigned to a polygon in the parcel data. 

Image 3: Relationship of Grand List SPANs and GIS (drawing) SPANs in Vermont Parcel Data | *Source: VT Standardized Parcel Data*

![image](https://github.com/user-attachments/assets/959a5b13-4dd0-484c-b064-758ae657ee00)

This creates identical polygons "stacked" on top of each other, which can be “flattened” to remove all but one polygon for each parcel for analytical purposes. Unlike the building footprints methods, there is no visual distinction between unlanded structures and the common land. Because to this, parcel geometry is simpler to maintain.

Image 4: Stacked Method Mapping of Condos | *Source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)*

![image](https://github.com/user-attachments/assets/8da7e8ab-d3e0-4423-881a-1ce1e2a9d399)

Pros
- Geometry is easier to maintain when compared to the building footprints methods
- Geometry includes common land to reflect total, calculated acreage and is relatively easy to “flatten” stacked polygons for analysis purposes

Cons
- Requires the creation and maintenance of GIS SPANs in the Intersection Table

***
**Other Unlanded Structures Mapping Practices from Other States**

Parcel points are maintained by Dakota County in the State of Minnesota. This data layer is a compilation of tax parcel information, containing one record for each real estate/tax parcel identification number (PIN) within the county. Condominiums are included in this dataset (whereas they are not in the polygons).

Image 5: Parcel Points Method Mapping of Condos | *Source: [Dakota County, Minnesota](https://gis.co.dakota.mn.us/DCGIS/)*

![image](https://github.com/user-attachments/assets/3e0e0b19-c8eb-48ad-922e-44bcfc481928)

Pros
- Already practiced by some Vermont municipalities internally
- Creates some visual distinction without subtracting from total, calculated acreage
  
Cons
- Requires the creation and maintenance of separate geometry layer

### Normalize Land Use Classification Codes

Text.

### Normalize Actual Year Built, Effective Year Built, and Unit Count Information

Text.

## Require Standardized CAMA Data Submittal to SoV

Text.

## Example Statutes in Other States

Connecticut
[Sec. 7-100l. Transmission of digital parcel file. Annual report.](https://www.cga.ct.gov/current/pub/chap_096a.htm#sec_7-100l)

# Recommendation 4: Clarify Right-of-Way Mapping for Tax Purposes in VT Statute

Text.

## Related VT Statutes
[19 V.S.A. § 32 Assumed width of right-of-way](https://legislature.vermont.gov/statutes/section/19/001/00032)

[19 V.S.A. § 1111 Permitted use of the right-of-way relocation or adjustment orders](https://legislature.vermont.gov/statutes/section/19/011/01111)

## Example Statutes in Other States

Washington
[RCW 84.36.210 Public right-of-way easements](https://app.leg.wa.gov/rcw/default.aspx?cite=84.36.210)

New Jersey
[N.J. Admin. Code § 18:23A-1.16 Rights-of-way and easements](https://www.law.cornell.edu/regulations/new-jersey/N-J-A-C-18-23A-1-16)

# Recommendation 5: Clarify Grand List vs. GIS Acreage Guidance

Text.

# Recommendation 6: Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract

Text.

# Recommendation 7: Offer Updated Statewide Parcel Contract Guidance for Municipalities

Text.

# Recommendation 8: Pilot Remotely-Sensed Tools to Support Appraisals

Text.

# Recommendation 9: Modernize Current Use Map Standards and Submittals

Text.

# Recommendation 10: Consider Updating and Moving Parcel Program in VT Statute

Text.

## Related VT Statutes

[19 V.S.A. § 44 Statewide Property Parcel Mapping Program](https://legislature.vermont.gov/statutes/section/19/001/00044)

[10 V.S.A. § 123 Geographic Information - Powers and Duties](https://legislature.vermont.gov/statutes/section/10/008/00123)

# Recommendation 11: Coordinate With Concurrent Efforts to Digitize Land Records

Text.

## Related VT Statutes and Bills

[H.512 (Act 171) of 2022 - An act relating to modernizing land records and notarial acts law](https://legislature.vermont.gov/bill/status/2022/H.512)

# Responsibilities and Implementation

# Cost Estimates and Potential Funding Sources

# Appendices

## Current State of Mapped Inactive Parcels

![image](https://github.com/user-attachments/assets/c6b5cfef-b9e9-4056-8162-ad42b71a659a)
