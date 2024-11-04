# Purpose

This document outlines all recommendations for parcel mapping and data maintenance as related to [Act 68 of 2023](https://legislature.vermont.gov/bill/status/2024/H.480). It is authored by the Vermont Center for Geographic Information (VCGI), state stewards of the [Statewide Property Parcel Mapping Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) since 2020, established via [19 V.S.A. § 44](https://legislature.vermont.gov/statutes/section/19/001/00044). The recommendations aim to improve parcel data quality to support timely, fair, accurate, and modern property valuation and reappraisals as sought by Act 68, which [asks the Tax Department to](https://legislature.vermont.gov/Documents/2024/Docs/ACTS/ACT068/ACT068%20Act%20Summary.pdf):

> [create] recommendations and considerations for distinguishing between different types and characteristics of property and their uses, and how different property data could be used to make policy decisions.

# Overview of All Recommendations

| **Recommendation**                                                                      | **Statute Change** | **Payment to Towns** | **Technical Guidance** | **New Technology** |
|:---------------------------------------------------------------------------------------:|:------------------:|:-----------:|:----------------------:|:------------------:|
| [1. Update Parcel Definition in VT Statute from "Contiguous" to Separate and Sellable Lots or Pieces of Real Property](#recommendation-1-update-parcel-definition-in-vt-statute)                                              | X                  |             |                        |                    |
| [2. Reward Standardized Digital Parcel Data Submittal to SoV via Per Parcel Payment](#recommendation-2-reward-digital-parcel-submittal-to-sov-via-per-parcel-payment)          | X                  | X           |                        |                    |
| [3. Implement VT CAMA Data Standard and Require Submittal to SoV](#recommendation-3-implement-vt-cama-data-standard-and-require-submittal-to-sov)                       | X                |             | X                      |                    |
| [4. Clarify Right-of-Way Mapping for Tax Purposes](#recommendation-4-clarify-right-of-way-mapping-for-tax-purposes)                         |                   |             | X                       |                    |
| 5. Clarify Grand List vs. GIS Acreage Guidance                                          |                    |             | X                      |                    |
| 6. Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract |                    |             | X                      | X                  |
| 7. Offer Updated Statewide Parcel Contract Guidance for Municipalities                  |                    |             | X                      | X                  |
| 8. Pilot Remotely-Sensed Tools to Support Appraisals                                    |                    |             |                        | X                  |
| 9. Modernize Current Use Map Standards and Submittals                                   |                    |             |                        | X                  |
| 10. Consider Updating and Moving Parcel Program in VT Statute                           | X                  |             |                        |                    |
| 11. Coordinate With Concurrent Efforts to Digitize Land Records                         |                   |             |                        | X                   |

# Recommendation 1: Update Parcel Definition in VT Statute
## 1.1 Summary
- Change the current parcel definition from a "contiguous" parcel defintition to one that requries tracking of separate and sellable pieces of real estate.
- This definition will replace the practice of mapping and tracking "inactive" parcels on a separate data layer and instead require towns to map and track all separate parcels individually, regardless of common ownership.
- "Contigous" parcels aggregated by common ownership may still be created for the purposes of tax billing, but they remain solely administrative.

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defines a parcel as:
> (3) A brief description of each parcel of taxable real estate in the town. “Parcel” means all contiguous land in the same ownership, together with all improvements thereon.

This is a "contiguous" parcel definition, depicted in figure 1 as option 1. Separate lots are grouped together by ownership for administrative purposes, primarily the sending of a single tax bill per owner per "parcel". Separate lots are sometimes managed as "inactive" parcels, although that term is not defined outside of the [parcel data standard](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) and their upkeep by towns is not uniform. The marketability of individual lots for sale is not clear, nor is how towns should map and track lots within a combined parcel. Aggregate parcel deliniation further complicates assignment of highest and best use valuation as assesors may have to generalize across several different lot types. Data management and downstream analysis are also negatively impacted by an aggregate, contiguous parcel definition.

![image](https://github.com/user-attachments/assets/6855b335-1e09-41fa-99d5-b4df4066b416)
*Figure 1: Existing contiguous parcel definition, depicted as option 1 on the left, and the proposed separate parcel defintion, depicted as option 2 on the right. The proposed separate parcel definition removes the need for tracking "inactive" parcels.*

Alternatively, defining parcel as a separate and sellable lot or piece of real property would bring parcel identification in line with their common understanding as "lots" while also reducing the need to generalize highest and best use across several different lots combined by owner (not use) during valuation. This change would enable improved parcel documentation, ease highest and best use valuation, faciliatate data maintenance and analysis, and continue to allow aggregation by owner for tax billing. 

As there are several variations in the timing of when a separate lot or piece of real property is created, an updated parcel defintion could be written so as to allow a legal document (deed or title), subdivision plats, or sale to help define the bounds of the separate mapped and tracked area. Existing "inactive" parcels, where they exist and are maintained, may be added to the "active" parcel layer with their unique SPAN and as much additional attribution as possible. Once added, maintenance of inactive parcels as separate entities on a separate data layer should cease.

These changes in parcel definition and mapping practices would increase the current count of parcels statewide from roughly 340,000 to at least 380,000. "At least" is stated as currently only 70% of towns (178 total) have submitted their inactive parcels as digital parcel data to VCGI. It remains unknown how many of the other 30% of towns actively track inactive parcels digitally.

## 1.2 Example Statute Update
> 32 V.S.A. § 4152 (a)(3) A brief description of each parcel of taxable real estate in the town. “Parcel” means a separate and sellable lot or piece of real estate. ~~all contiguous land in the same ownership, together with all improvements thereon~~

## 1.3 Related VT Statutes

[32 V.S.A. § 4152](https://legislature.vermont.gov/statutes/section/32/129/04152) - Taxation and Finance / Grand Tax Lists / Grand List of Town

[27 V.S.A. § 601](https://legislature.vermont.gov/statutes/section/27/005/00601) - Title 27: Property / Chapter 5: Conveyance of Real Estate / Subchapter 007 : Marketable Record Title 

# Recommendation 2: Reward Digital Parcel Submittal to SoV via Per Parcel Payment
## 2.1 Summary

- Institute a per parcel payment to municipalities to aid costs associated with parcel data maintenance.
- Make disbursement of this per parcel payment to municipalities contingent on submittal of [Vermont GIS Data Standard-compliant](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) digital parcel data to VCGI, maximum payment once per year per town.
- Per parcel payment is to be X, funded by Y, with estimated annual cost of Z.

Descriptive text.

## 2.2 Digital Parcel Submittals as of October 24, 2024
-	90% of towns are edited/updated by vendors or the town. 10% are edited/updated by VCGI (these are considered “not compliant”). 
-	10% of submissions require edits to parcel topology (i.e., geometry) to address gaps and/or overlaps among parcels.
-	50% of submissions required edits that were already made for the previous submission  (i.e., repeated revisions).
-	70% of submissions contain inactive parcels. Inactives exist for at least some towns that do not include them in their submissions.
-	96% of towns include and correctly represent rights-of-way. For those that do not, some map parcels to road centerlines, others only include main ROWs or those in the town/village center, and others have gaps in the parcel data where roads should be.
-	24% of submissions are fully compliant with the current parcel data standard. 26% are compliant with minor edits. 37% are compliant with major edits. 13% are not compliant (see criteria below).
-	11% of towns have a mapping vendor (to the best of VCGI's knowledge) but have not submitted an update since the original Parcel Project data (prior to 2020). These towns are currently classed as “fully compliant”, despite having stale data. 
-	12% of submissions are/have been reviewed by towns prior to submittal; 64% have not, and 24% are unknown. Some vendors are already working quite closely with towns as edits are being made (or edits are only being made at the direction of a town official), however, which may negate the need for a more formal review of the data prior to submission.

## 2.3 Considerations:
-	In addition to submittal compliance criteria, will need a timeframe component when assessing a town's eligibility for a per parcel payment (likely annual). Some towns are technically “compliant” and are working with a vendor but have not submitted an update to VCGI since before 2020. For small towns that may not have any changes from year to year (and therefore do not submit an update), VCGI should still receive an annual confirmation that no changes or updates are needed to the existing data.
-	Consider possible tiered system for payments to encourage compliance. E.g.: Fully compliant or minor edit towns receive full amount, major edit town receive 50%, and non-compliant towns receive none.
-	Based on vendor discussions, it is not necessarily practical or feasible for vendors to directly use parcel data published by VCGI (e.g., vendors are not downloading the latest data for a town from VCGI prior to making their next round of edits). Often vendors are maintaining additional fields and formats beyond what is submitted and used by VCGI. This is likely a factor leading to repeated edits with each submission. Consider a way to summarize/communicate submission issues or edits that VCGI makes so vendors are aware and can correct for their subsequent submission, ideally without creating significant extra work for either VCGI or vendor. 

## 2.4 Submittal Quality Criteria

 **Criteria**                | **Description/Examples**|
|:---------------------------|:------------------------|
|Fully Compliant             | •	Includes all towns that have not been updated since the Parcel Project (i.e., prior to 2020).<br>•	Valid topology; no gaps or overlaps among parcels<br>•	ROWs included and mapped correctly<br>•	Unmatched parcels only comprised of land expected to have no SPAN (common land, town/state/federally-owned land, etc.)<br>•	Multi-SPAN parcels (e.g., condos) are attributed correctly through the intersection table, if applicable<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly; does not require edits that were made in the previous submission; any unmatched parcels are expected to be unmatched given their status as common land, government-owned land, etc.; any multi-SPAN parcels are accounted for correctly in the intersection table. Includes towns that are working with a vendor to maintain parcels but have not submitted updates to VCGI since January 1, 2020.
|Compliant with Minor Edits  |•	Unmatched parcels (as received) are < 2%<br>•	ROWs included and mapped correctly<br>•	No/minimal repeated edits from prior submission during VCGI review<br>•	No/minimal (<10) edits to intersection table to account for multi-SPAN parcels<br>•	No topology errors<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly. Requires minor editing to address unmatched parcels (<2% of town’s total parcels) that should have SPANs and a match in the annual Grand List. May include <10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Compliant with Major Edits  |•	Unmatched parcels (as received) are > 2%<br>•	Topology errors resulting in gaps/overlaps among parcels<br>•	Incorrect or missing attribution of condos/multi-SPAN parcels in the intersection table<br>•	ROWs are missing or incomplete (e.g., parcels are mapped to road centerlines)<br>•	Repeated edits from prior submission during VCGI review<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard to the extent that it can be incorporated into the statewide parcel dataset following revisions. May require significant edits to address topology errors, missing or invalid SPANs, missing or incomplete ROWs, and/or missing or incomplete multi-SPAN parcel representation in the intersection table. Requires editing to address unmatched parcels (>2% of town’s total parcels) that should have SPANs and a match in the annual Grand List. May include >10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Not Compliant               |•	Includes all towns that are updated by VCGI/have no vendor or capacity to submit their own updates<br>•	Submission does not include SPANs or Parcel/Map IDs that can be linked to the Grand List<br>•	Submission is in an unusable format (e.g., CAD) that cannot be converted to a geodatabase<br>•	Usable format (i.e., GIS files) but missing or invalid fields that do not allow conversion to usable schema/dataset, or require significant effort to update using existing data and external sources/map viewers (e.g., loading existing attribution into new geometry; using E911, AxisGIS, or other to validate/verify SPANs; merging/splitting active and inactive parcels, etc.)<br><br>Summary: submission does not meet format and/or content allowing for inclusion in the statewide parcel dataset. Data format may be unusable/unable to convert to GIS, and/or attribution does not include valid SPANs or Parcel/Map IDs for linking to Grand List. May sometimes include a workable data format that requires significant geometry (e.g., active and inactive parcels) and/or attribute manipulation using internal and external data sources (e.g., AxisGIS sites, surveys, E911 data, etc.) to create dataset with valid schema and attribution. Also includes towns that do not have a vendor or the capacity to make their own edits and are updated by VCGI using data available in the VT Land Survey Library.

# Recommendation 3: Implement VT CAMA Data Standard and Require Submittal to SoV
## 3.1 Summary
- Create standardized Computer Assisted Mass Appraisal (CAMA) schema and domains based on fields from current CAMA software providers, with applicability to current and future CAMA providers operating in Vermont
- Require standardized land use codes and descriptions matching VT Department of Tax [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf)
- Normalize recording of other fields including actual year built, effective year built, and unit counts
- Use stacked polygons for representing and accounting for unlanded structures, including attribution and mapping
- Require submittal of CAMA data adherent to the CAMA data standard to the State of Vermont. Submittals are to come directly from each vendor via read-only API or file extract, with preference for API
- These recommondations are intended to provide as much useful property description information as possible to aid timely and accurate reappraisals, provide data to also aid key public policy concerns (e.g., housing) that are best served by CAMA data, and ease access to and use of this public information for data analysis and visualization by making it publicly avalable. Standardized CAMA data and integration with existing GIS data will have widespread utility, including aiding appraisals and housing policy while providing greater spatial context. 

## 3.2 CAMA Data Components

### 3.2.1 Design and Implement VT CAMA Data Standard
Four CAMA software providers [operate in Vermont](https://tax.vermont.gov/municipal-officials/listers-and-assessors/district-advisors) as of October 2024:
- MicroSolve (NEMRC)
- ProVal (Aumentum)
- Vision Government Solutions CAMA
- AssessPro (Catalis, Formerly Patriot)

Based on sample data and documentation, all providers differ in how they collect, format, and organize CAMA data. VCGI recommends devising a standardized template and schema, including domains for applicable fields, with input and agreement from each vendor. In most cases, vendors should be able to perform an extract of fields they are already collecting with little or no modification (or, ideally, provide VCGI with a read-only API). Some fields, particularly land use codes, will need to be standardized to a single set of codes and descriptions (see below).

### 3.2.2 Implement Changes to Parcel Definition in CAMA Data

Existing CAMA data software solutions offer advanced data maintenance capabilities and should accomodate a parcel definition change to separate and sellable pieces of real estate. Data entry and maintenance practices will need to adjust to reflect these changes.

### 3.2.3 Normalize Land Use Classification Codes

Standardized land use classification codes and descriptions are essential for integrating a statewide CAMA system. Currently, all four CAMA software providers use different coding systems for land use. Based on sample data, NEMRC appears to be the only vendor using codes conforming to the [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf) published by the VT Department of Tax. VCGI recommends that these codes be used by all vendors. These codes provide a relatively high level of specificity for different land use types, and are grouped by broader category codes at the '100 level' (e.g., all codes between 300 and 399 have a commercial use), which helps to quickly identify and group more general land use types. If a vendor chooses not to adopt the VT Department of Tax Property Class Codes, a crosswalk table should be created to allow standardization when VCGI reads and integrates CAMA data into the statewide dataset.

### 3.2.4 Normalize Actual Year Built, Effective Year Built, and Unit Count Information

Similar to Land Use Codes, consistent definitions and formatting for actual year built, effective year built, and unit count should be established for all CAMA vendors. While each of these fields appear to exist within the current schema for each vendor, it is essential that all are evaluated using the same methodology and definition.

### 3.2.5 Normalize Attribution and Mapping of Unlanded Structures

The [stacked polygons method](#stacked-method---recommended) is the current recommendation per the Vermont GIS Parcel Data Standard and continues to be recommended after considering the pros and cons of all methods detailed below. 

To improve the functionality of this method, the following recommendations should be considered: 

1. While condominiums represent a vast majority of unlanded structures reflected in statewide parcel data, it is necessary to create a comprehensive list of different types of unlanded structures to be uniformly attributed in CAMA and subsequent Grand List records. The Vermont GIS Parcel Data Standard defines an unlanded building as a “condominium unit, mobile home, camp, or other building that is a unit of real estate which is separate from the underlying land surface.”
   
2. The list below can be used to differentiate between unlanded structures in the parcel polygons layer, and if uniformly applied in CAMA and Grand List attribution, can be easily filtered for each record. Each unlanded structure can be represented as a prefix of two or three letters:

| Prefix Code | Applies To                |
|-------------|---------------------------|
| CO          | Condominiums              |
| CA          | Camps                     |
| MH          | Mobile Homes              |
| SA          | Ground-Mount Solar Arrays |
| WT          | Wind Turbines             |

3. While not the intended purpose, the SOURCENAME field in the parcel polygon layer can also be used to track this information.

4. This list can also be used to create GIS SPANs in the Intersection Table based on the type of unlanded structure. The same two-letter system described above can be implemented followed by the town code (first three digits of the town SPAN) and a four-digit numeric count.

5. Tax Department guidance on attribution of unlanded structures should be updated and made uniform to reflect the above prefixes and mapping practices (e.g., in the Listers and Assessors Handbook).

## 3.3 Require Standardized CAMA Data Submittal to SoV

<<<<<<< Updated upstream
CAMA data is the best source of information for detailed and current property descriptions statewide. Standardizing these data and requiring their submittal to the State of Vermont for regular and uniform public publication, particularly when combined with existing parcel data, will aid improved pace and accuracy of appraisals, provide spatial context, facilitate data visualization and trend analysis, and improve data accessibility. To remain complete and current, however, the submission of standardized CAMA data to SoV should be required. VCGI's Parcel Program, for example, is a voluntary program with data ranging from less than six months to over six years old, despite the widespread visibility, utility, and value of parcel data. Without a submittal requirement for CAMA data it is likely the dataset will become fragmented, incomplete, or stale over time.
=======
CAMA data are the best source of information for detailed and current property descriptions statewide. Standardizing these data and requiring their submittal to the State of Vermont for normalized public publication, particularly when combined with existing parcel data, will aid improved pace and accuracy of appraisals, provide spatial context, facilitate data visualization and trend analysis, and improve data accessibility. To remain complete and current, however, the submission of standardized CAMA data to SoV should be required. VCGI's Parcel Program, for example, is a voluntary program with data ranging from less than six months to over six years old depending on the town, despite the widespread visibility, utility, and value of parcel data. Without a submittal requirement for CAMA data it is likely the dataset will become fragmented, incomplete, or stale over time.
>>>>>>> Stashed changes

## 3.4 Example Statute Updates
>[Section] "Assessor database" means the database of property information maintained by a municipalities' lister(s) or assessor(s); it is also referred to as a Computer Aided Mass Appraisal (CAMA) system or Computer Aided Mass Appraisal database

>[Section] On or before [initial date], and not less than monthly thereafter, each municipality that possesses or contracts for services for the creation or maintenance of an assessor database shall transmit an extract of the database to [the State of Vermont]. The submitted database shall include, but need not be limited to information that uniquely identifies each property in the municipality, the description of each property, the size of each property, the year in which buildings were constructed on each property, and other fields described in the Vermont CAMA data standard.

# Recommendation 4: Clarify Right-of-Way Mapping for Tax Purposes

## 4.1 Summary
- Create guidance for treatment of the area between road centerline and edge of right-of-way for taxation purposes
- Promote mapping guidance specifying that parcels should be mapped to the edge of the right-of-way, not the road centerline

<<<<<<< Updated upstream
In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and its relation with parcel mapping. Common, practical experience is that public rights-of-way such as roads and highways are just that—areas not to be obstructed by abutting private property owners--be they owned in fee or easements. State highways, for example, often involve the State purchasing lands between the road centerline and abutting parcel, whereas towns may not. These differences contribute to a lack of clarity about how to account for the area that is within a right-of-way and between an abutting private parcel and road centerline and have occasionally led to differences in their depiction and resulting acreage calculations. The Tax Department, with aid of partners, should develop and offer guidance for considering these areas with regard to taxation and related acreage calcuations.

[DIAGRAMS of Right-of-Way Conditions]
=======
In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and with bearing on parcel mapping. Common, practical experience is that public rights-of-way such as roads and highways are just that—areas not to be obstructed by abutting private property owners, be they owned in fee or as easements. State highways, for example, often involve the State purchasing lands between the road centerline and abutting parcel, whereas towns may not. These differences contribute to a lack of clarity about how to account for the area that is within a right-of-way and between an abutting private parcel and road centerlin,e and have occasionally led to differences in their depiction and resulting acreage calculations. The Tax Department, with aid of partners, should develop and offer guidance for considering these areas with regard to taxation and related acreage calculations.
>>>>>>> Stashed changes

## 4.2 Related VT Statutes
[19 V.S.A. § 32 Assumed width of right-of-way](https://legislature.vermont.gov/statutes/section/19/001/00032)

[19 V.S.A. § 1111 Permitted use of the right-of-way relocation or adjustment orders](https://legislature.vermont.gov/statutes/section/19/011/01111)

# Recommendation 5: Clarify Grand List vs. GIS Acreage Guidance

## 5.1 Summary
- Develop criteria for when review of underlying legal property descriptions is needed given differences in listed and map acreage for the same parcel
- Specify actions to be taken in the Listers and Assessors handbook based on best available documentation for acreage discrepancies

In addition to acreage and resulting taxation associated with areas of property in road rights-of-way, acreage discrepancies between listed and mapped values are common. It is currently technically possible to easily display and compare differences between listed and mapped acreage. 

![image](https://github.com/user-attachments/assets/c19bbe86-0fa1-4fe1-ada6-df77229d5a97)
![image](https://github.com/user-attachments/assets/d723529b-89de-43e8-915a-312fdfe6d9b6)

*Figures X and Y: Visualized differences in listed acreage and GIS (drawn) acreage in Northfield. The amount of percent difference is shown in five ranges and colors, as well as described in text on each parcel. [See an interactive map of these differences here.](https://vcgi.maps.arcgis.com/apps/mapviewer/index.html?webmap=e452fa5505644e12b1bf8b6308f7b2e8)*

The Tax Deparment, in collaboration with partners, should develop guidance for handling of these acreage discrepancies. This may include specifying when the difference is large enough to trigger review of the parcel(s) underlying recorded legal descriptions, and when updating the listed and/or as-drawn acreage should result. These recommendations may be included in an updated Listers and Assessors handbook and ensuing training/guidance for municipalities.

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

## Appendix 1: Parcel Definition Alternatives
### A1.1 Current State of Mapped Inactive Parcels

![image](https://github.com/user-attachments/assets/c6b5cfef-b9e9-4056-8162-ad42b71a659a)

### A1.2 Aggregate Mapped Unit Defined by Ownership (Contiguous)

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defined parcel. This is a "contiguous" parcel definition. Separate parcels are grouped together by ownership for administrative purposes, primarily the sending of a single tax bill per owner per "parcel".

Depicted visually, a contiguous parcel definition means that the two parcels below, shown split with a dotted green line and both of which have the same owner, are drawn as the single outer rectangle. This results as one "parcel" in the spatial data layer.

![image](https://github.com/user-attachments/assets/239c3a7e-e6f5-44cd-bb89-e8768e81a1da)

Each of the two individual parts are considered "inactive" parcels, by practice only, and not uniformly across towns.

### A1.3 Separate Mapped Unit, Defined by Practice

Example:
> A separately assessed lot or piece of real property - *New York State Property tax and assessment administration definitions / [guidance](https://www.tax.ny.gov/research/property/equal/assessrpt/b_define.htm)*

### A1.4 Separate Mapped Unit, Defined by Unique Identifier

> "Parcel" means a separate plot of land as identified by the municipality tax map and lot number. - *[New Hampshire Admin. Code § Cub 301.15](https://casetext.com/regulation/new-hampshire-administrative-code/title-cub-chairman-current-use-board/chapter-cub-300-criteria-for-open-space-current-use-assessment/part-cub-301-definitions/section-cub-30115-parcel)*

### A1.5 Separate Mapped Unit, Defined by Legal Document

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

### A1.6 Separate Mapped Unit, Defined by Combination

Any combination of the examples above.

## Appendix 2: Per Parcel Payments

## Appendix 3: CAMA Data Standard

### A3.1 Land Use Codes
 Vermont Department of Tax [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf) (bold indicates category code):

 **PCCODE**          | **PCLASS**      |**PCCODE**    | **PCLASS**|
|:-------------------|:----------------|:-------------|:----------|
|0	| Unknown|413	|VT Elect Power Co
|**100**	|**Primary Year Round Residence**|414	|New Eng Power Co
|101	|Single Family|415	|VT Electric Co-Op
|102	|Two Unit|416	|Other
|103	|Three Unit|420	|Mining/Quarries
|104	|Four Unit|421	|Granite
|130	|Condo/Co-Op|422	|Marble
|131	|Condo < 6 ac|423	|Limestone
|132	|Condo > 6 ac|424	|Sand/Gravel
|135	|Co-op Apt|425	|Magnesium/Talc
|150	|Mobile Home|426	|Asbestos
|**200**	|**Secondary Residence**|427	|Other
|201	|Single Family|430	|Wood Manufacturer
|202	|Two Family|431	|Pulp/Paper Mills
|203	|Three Family|432	|Plywood/Veneer Mills
|204	|Four Family|433	|Sawmills/Finish Mill
|230	|Condo/Co-Op|434	|Wood Consm Prod
|231	|Common Land > 6 ac|440	|Creameries/Dairies
|232	|Secondary|450	|Other Industry
|235	|Co-op Apt|451	|Heavy Industry
|250	|Mobile Home|454	|Medium Industry
|**300**	|**Commercial**|455	|Light Industry
|310	|Auto Sales/Related|**500**	|**Operating Farm/Ag**
|311	|Auto/Truck/Bus Sales|511	|Dairy Farm/Prod
|312	|Gas Station/Garage|512	|Beef/Dairy Replace
|313	|Auto Repair|513	|Horses/Ponies
|314	|Car Wash|514	|Sheep/Wool
|315	|Auto/Truck Rental|515	|Hogs
|316	|Truck Terminals|519	|Animals Over 100#
|320	|Trans/Comm|520	|Birds/Assoc Prod
|321	|Apts/Bldg/Sales/Ser|521	|Chickens/Eggs
|322	|Railroad/Assoc.Fac|522	|Turkeys/Eggs
|323	|Ferry/Barges/Docks|523	|Aquatic Fowl
|324	|Marinas/Boat Sales|524	|Game/Show Birds
|325	|TV Studio/Broadcast|530	|Ag Ent/Living Cre
|326	|Radio Studio/Broadcast|531	|Rabbits meat/fur
|327	|Cable TV|532	|Fur Farm
|328	|Telephone/Telegraph|533	|Bees/Products
|330	|Rentals|534	|Aquatic Fowl
|331	|Business Blocks|540	|Field Crops
|332	|Office Buildings|550	|Truck Crops
|333	|Year Round Residence|560	|Orchards
|334	|Bank Building|561	|Apple
|335	|Shopping Centers|563	|Sugar Bush
|336	|Buildings|565	|Other Fruits/Nuts
|337	|Mobile Home Parks|570	|Fruits/Berries
|340	|Warehouses/ Distribution|580	|Nursery/Greenhouse
|341	|Beverage Warehouse|590	|Wildlife Preserves
|342	|Grocery Warehouse|**600**	|**Timberland**
|343	|Gas/Diesel/Heating|**700**	|**Government Use**
|344	|Auto Parts Distribution|710	|Federal
|347	|General Warehouse|720	|State
|348	|Boat Storage|730	|County
|350	|Travel Accommodation/Rest|740	|Local
|351	|Hotel|750	|School District
|352	|Motel|**800**	|**Open Land/Misc**
|353	|Inn/Overnight Cabins|810	|Year Round Residence
|354	|Lodges|811	|Rural
|355	|Snack Bars/Fast Food|812	|Urban
|356	|Restaurants|820	|Development
|360	|Service/Health|821	|Rural
|361	|Hospitals|822	|Urban
|362	|Nursing Home/Clinic|830	|Recreation
|363	|Funeral Home/Morgue|831	|Rural
|364	|Cemeteries|832	|Urban
|365	|Laundry/Dry Cleaning|840	|Industrial
|380	|Sales|841	|Rural
|381	|Small Retail Shop/Store|842	|Urban
|382	|Supermarkets|850	|Commercial
|383	|Building Supplies/Lumber Yard|851	|Rural
|384	|Propane/Heating Oil|852	|Urban
|385	|Feed/Grain/Seed|856	|Parking Lot
|386	|Farm Machinery/Equipment|860	|Farm Use
|387	|Small Grocery Stores|870	|Governmental
|390	|Miscellaneous/Multi use|880	|Vacation
|391	|Office Building/Apartments|890	|Other
|392	|Motel/Restaurant|891	|Right of Way
|393	|Store/Apartments|892	|Establish Bound Line
|395	|Lodge/Restaurant|894	|Water Rights
|**400**	|**Industrial**|**900**	|**Other**
|402	|Gas/Oil Pipe/Prod|910	|Religious
|405	|Other Energy Production|920	|Fraternal
|410	|Electric|930	|Non-Profit Org
|411	|CVPS|940	|Mineral Rights
|412	|Green Mtn Power

**Vermont Department of Tax Categories**
| Category Code | Category                     |
|---------------|------------------------------|
| 0             | Unknown                      |
| 100           | Primary Year Round Residence |
| 200           | Secondary Residence          |
| 300           | Commercial                   |
| 400           | Industrial                   |
| 500           | Operating Farm/Ag            |
| 600           | Timberland                   |
| 700           | Government Use               |
| 800           | Open Land/Misc               |
| 900           | Other                        |

### A3.2 Standardized CAMA schema
Proposed standardized CAMA schema, based on example data from CAMA vendors in Vermont as well as a similar schema being developed in Connecticut, can be viewed [here](https://vermontgov.sharepoint.com/:x:/t/ADS.VCGIGroup/EZEBDpDNLNNHk_dhFOhtNW8BiiuDlzcCbWzOrxTXDUgO_g?e=3QqTMj).

### A3.3 Mapping of Unlanded Structures
**Background** 

Statewide standardized parcel data in Vermont is currently comprised of parcel geometry, the approximate parcel boundary lines drawn as closed multi-sided shapes (parcel polygons) as sourced from municipalities, and parcel attribution from the annual Grand List collected and published by the Tax Department. These two components are joined together by a matching School Property Account Number (SPAN) in the attribute table of the parcel polygons layer and in the Grand List. In most cases, each polygon is joined to one Grand List record but it is not uncommon for more than one Grand List record to be joined to the same polygon. This happens most often with condominiums as they are typically described by their percentage of undivided interest in the common area and facilities rather than discrete boundaries that can be easily represented by polygons. While VCGI has provided some guidance on mapping condominiums per the Vermont GIS Parcel Data Standard, a more comprehensive recommendation for mapping all types of unlanded structures is necessary to improve data quality, clarity, and ease of use.

#### A.3.3.1 Current Unlanded Structure Mapping Practices in Vermont

**Discrete and Distributed Methods**

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
**Stacked Method - Recommended**

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
#### A.3.3.2 Other Unlanded Structures Mapping Practices from Other States

Parcel points are maintained by Dakota County in the State of Minnesota. This data layer is a compilation of tax parcel information, containing one record for each real estate/tax parcel identification number (PIN) within the county. Condominiums are included in this dataset (whereas they are not in the polygons).

Image 5: Parcel Points Method Mapping of Condos | *Source: [Dakota County, Minnesota](https://gis.co.dakota.mn.us/DCGIS/)*

![image](https://github.com/user-attachments/assets/3e0e0b19-c8eb-48ad-922e-44bcfc481928)

Pros
- Already practiced by some Vermont municipalities internally
- Creates some visual distinction without subtracting from total, calculated acreage
  
Cons
- Requires the creation and maintenance of separate geometry layer

### 3.4 Example CAMA Submittal Statutes in Other States

Connecticut
[Sec. 7-100l. Transmission of digital parcel file. Annual report.](https://www.cga.ct.gov/current/pub/chap_096a.htm#sec_7-100l)

## Appendix 4: ROW Statutes in Other States

### A4.1 Example Statutes in Other States

Washington
[RCW 84.36.210 Public right-of-way easements](https://app.leg.wa.gov/rcw/default.aspx?cite=84.36.210)

New Jersey
[N.J. Admin. Code § 18:23A-1.16 Rights-of-way and easements](https://www.law.cornell.edu/regulations/new-jersey/N-J-A-C-18-23A-1-16)


