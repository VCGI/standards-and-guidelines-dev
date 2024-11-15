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

These changes in parcel definition and mapping practices would increase the current count of parcels statewide from roughly 340,000 to at least 380,000. "At least" is stated as currently only 70% of towns (178 total) have submitted their inactive parcels as digital parcel data to VCGI. It remains unknown how many of the other 30% of towns map inactive parcels digitally.

## 1.2 Example Statute Update
> 32 V.S.A. § 4152 (a)(3) A brief description of each parcel of taxable real estate in the town. “Parcel” means a separate and sellable lot or piece of real estate. ~~all contiguous land in the same ownership, together with all improvements thereon~~

## 1.3 Related VT Statutes

[32 V.S.A. § 4152](https://legislature.vermont.gov/statutes/section/32/129/04152) - Taxation and Finance / Grand Tax Lists / Grand List of Town

[27 V.S.A. § 601](https://legislature.vermont.gov/statutes/section/27/005/00601) - Title 27: Property / Chapter 5: Conveyance of Real Estate / Subchapter 007 : Marketable Record Title 

## 1.4 Practical Implications

# Recommendation 2: Reward Digital Parcel Submittal to SoV via Per Parcel Payment
## 2.1 Summary

- Institute a per parcel payment to municipalities to aid costs associated with parcel data maintenance.
- Make disbursement of this per parcel payment to municipalities contingent on submittal of [Vermont GIS Data Standard-compliant](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) digital parcel data to VCGI, maximum payment once per year per town.
- Per parcel payment is to be X, funded by Y, with estimated annual cost of Z.

## 2.2 Proposed Financial Incentive Model
- Consider each municipality on four key attributes:
   - **Desire to participate in Parcel Program** - At least one municipality has explicited refused to participate in the Parcel Program. Municipalities that elect to not particpate should be marked as "non-participatory" and will likely continue to recieve irregular updates by VCGI using the Vermont Land Survey Library. Non-participatory municipalities may opt-in to the Parcel Program at anytime.
   - **Estimated frequency of parcel geometry updates** - Most municipalities should update their parcel geometry annually (especially large towns and cities). Some smaller municipalies may be able to update every 2-3 years. 
   - **Ability to perform parcel geometry updates** - While a majority of municipalities are currently being updated by a mapping vendor or internally, a distinction should be made between GIS vendors and municipalities with "high confidence" in their ability to conduct parcel geometry updates internally; and non-GIS vendors (such as CAD vendors) and municipalities with "low confidence" in their ability to conduct parcel geometry updates internally
   - **Size of municipality (parcel count)**

- Indentify municipalities that may be good candidates for VCGI to assist in updating parcel geometry based on the four key attributes detailed above:
   - Municipalities that can be updated every 2-3 years
   - Municipalities not currently updating their parcel geometry, contracting with a non-GIS vendor, or having "low confidence" in their ability to conduct parcel geometry updated inernally
   - Municipalities under 500 parcels  

- Consider a per parcel fee between $5.00 and $7.00 based on the cost per parcel for a sample of municipalities completed during the first year of the Parcel Project. In *National Land Parcel Data: A Vision for the Future* (2007), the National Research Council found the average cost per parcel nationwide was $5.20 based on samples accross the country.

- Regardless of update frequency, for municipalities demostrating the ability to regularly update their parcel geometry (with a GIS vendor or internally with "high confidence") consider offering a "flat fee" bonus or rebate rather than a per parcel fee.

## 2.3 Digital Parcel Submittals as of October 24, 2024
-	90% of towns are edited/updated by vendors or the town. 10% are edited/updated by VCGI (these are considered “not compliant”). 
-	10% of submissions require edits to parcel topology (i.e., geometry) to address gaps and/or overlaps among parcels.
-	50% of submissions required edits that were already made for the previous submission  (i.e., repeated revisions).
-	70% of submissions contain inactive parcels. Inactives exist for at least some towns that do not include them in their submissions.
-	96% of towns include and correctly represent rights-of-way. For those that do not, some map parcels to road centerlines, others only include main ROWs or those in the town/village center, and others have gaps in the parcel data where roads should be.
-	24% of submissions are fully compliant with the current parcel data standard. 26% are compliant with minor edits. 37% are compliant with major edits. 13% are not compliant (see criteria below).
-	11% of towns have a mapping vendor (to the best of VCGI's knowledge) but have not submitted an update since the original Parcel Project data (prior to 2020). These towns are currently classed as “fully compliant”, despite having stale data. 
-	12% of submissions are/have been reviewed by towns prior to submittal; 64% have not, and 24% are unknown. Some vendors are already working quite closely with towns as edits are being made (or edits are only being made at the direction of a town official), however, which may negate the need for a more formal review of the data prior to submission.

## 2.4 Considerations:
-	In addition to submittal compliance criteria, will need a timeframe component when assessing a town's eligibility for a per parcel payment (likely annual). Some towns are technically “compliant” and are working with a vendor but have not submitted an update to VCGI since before 2020. For small towns that may not have any changes from year to year (and therefore do not submit an update), VCGI should still receive an annual confirmation that no changes or updates are needed to the existing data.
-	Consider possible tiered system for payments to encourage compliance. E.g.: Fully compliant or minor edit towns receive full amount, major edit town receive 50%, and non-compliant towns receive none.
-	Based on vendor discussions, it is not necessarily practical or feasible for vendors to directly use parcel data published by VCGI (e.g., vendors are not downloading the latest data for a town from VCGI prior to making their next round of edits). Often vendors are maintaining additional fields and formats beyond what is submitted and used by VCGI. This is likely a factor leading to repeated edits with each submission. Consider a way to summarize/communicate submission issues or edits that VCGI makes so vendors are aware and can correct for their subsequent submission, ideally without creating significant extra work for either VCGI or vendor. 

## 2.5 Submittal Quality Criteria

 **Criteria**                | **Description/Examples**|
|:---------------------------|:------------------------|
|Fully Compliant             | •	Includes all towns that have not been updated since the Parcel Project (i.e., prior to 2020).<br>•	Valid topology; no gaps or overlaps among parcels<br>•	ROWs included and mapped correctly<br>•	Unmatched parcels only comprised of land expected to have no SPAN (common land, town/state/federally-owned land, etc.)<br>•	Multi-SPAN parcels (e.g., condos) are attributed correctly through the intersection table, if applicable<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly; does not require edits that were made in the previous submission; any unmatched parcels are expected to be unmatched given their status as common land, government-owned land, etc.; any multi-SPAN parcels are accounted for correctly in the intersection table. Includes towns that are working with a vendor to maintain parcels but have not submitted updates to VCGI since January 1, 2020.
|Compliant with Minor Edits  |•	Unmatched parcels (as received) are < 2%<br>•	ROWs included and mapped correctly<br>•	No/minimal repeated edits from prior submission during VCGI review<br>•	No/minimal (<10) edits to intersection table to account for multi-SPAN parcels<br>•	No topology errors<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly. Requires minor editing to address unmatched parcels (<2% of town’s total parcels) that should have SPANs and a match in the annual Grand List. May include <10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Compliant with Major Edits  |•	Unmatched parcels (as received) are > 2%<br>•	Topology errors resulting in gaps/overlaps among parcels<br>•	Incorrect or missing attribution of condos/multi-SPAN parcels in the intersection table<br>•	ROWs are missing or incomplete (e.g., parcels are mapped to road centerlines)<br>•	Repeated edits from prior submission during VCGI review<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard to the extent that it can be incorporated into the statewide parcel dataset following revisions. May require significant edits to address topology errors, missing or invalid SPANs, missing or incomplete ROWs, and/or missing or incomplete multi-SPAN parcel representation in the intersection table. Requires editing to address unmatched parcels (>2% of town’s total parcels) that should have SPANs and a match in the annual Grand List. May include >10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Not Compliant               |•	Includes all towns that are updated by VCGI/have no vendor or capacity to submit their own updates<br>•	Submission does not include SPANs or Parcel/Map IDs that can be linked to the Grand List<br>•	Submission is in an unusable format (e.g., CAD) that cannot be converted to a geodatabase<br>•	Usable format (i.e., GIS files) but missing or invalid fields that do not allow conversion to usable schema/dataset, or require significant effort to update using existing data and external sources/map viewers (e.g., loading existing attribution into new geometry; using E911, AxisGIS, or other to validate/verify SPANs; merging/splitting active and inactive parcels, etc.)<br><br>Summary: submission does not meet format and/or content allowing for inclusion in the statewide parcel dataset. Data format may be unusable/unable to convert to GIS, and/or attribution does not include valid SPANs or Parcel/Map IDs for linking to Grand List. May sometimes include a workable data format that requires significant geometry (e.g., active and inactive parcels) and/or attribute manipulation using internal and external data sources (e.g., AxisGIS sites, surveys, E911 data, etc.) to create dataset with valid schema and attribution. Also includes towns that do not have a vendor or the capacity to make their own edits and are updated by VCGI using data available in the VT Land Survey Library.

## 2.6 Funding during the Parcel Project
The Parcel  Project (2017-2019) leveraged both state and federal funds with 80 percent coming from the Federal Highway Administration and the remaining 20 percent from several state agencies and departments. The Vermont Agency of Transporation contracted with several mapping vendor to update or create digital parcel data for each Vermont municipality over a three-year period. Each mapping vendor was assigned to a municipality through a competitive bid process. The cost per parcel for a sample of municipalities completed during the first year of the Parcel Project is depicted below.

[IMAGE]

# Recommendation 3: Implement VT CAMA Data Standard and Require Submittal to SoV
## 3.1 Summary
- Create standardized Computer Assisted Mass Appraisal (CAMA) schema and domains based on fields from current CAMA software providers and input from VT Department of Tax, with applicability to current and future CAMA providers operating in Vermont. Select 'priority fields' for initial standardization, with goal of expanding to additional fields over time (phased approach)
- Require standardized land use categories and descriptions matching VT Department of Tax [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf)
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

Following discussion with the VT Department of Tax, a phased approach for standardizing fields is likely the most feasible and realistic. The following fields comprise the first phase of standardization:
 - SPAN
 - Actual Year Built
 - Total Finished Square Feet
 - Heat IDs
 - Heat/Cool 
 - Heat/Cool %
 - Total Rooms 
 - Bedrooms
 - Full Baths
 - Half Baths
 - Kitchens
 - Effective Year Built
 - % Complete 
 - Unit Count
 - Story Count

All or most of these fields are present in the sample data/schema provided by three of the four CAMA vendors. 

### 3.2.2 Implement Changes to Parcel Definition in CAMA Data

Existing CAMA data software solutions offer advanced data maintenance capabilities and should accomodate a parcel definition change to separate and sellable pieces of real estate. Data entry and maintenance practices will need to adjust to reflect the se changes.

### 3.2.3 Normalize Land Use Classification Codes

Currently, all four CAMA software providers use different coding systems for land use. VCGI recommends that the category ('100 level') codes found in the VT Department of Tax's [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf) be used by all vendors. Using the broader category codes will help to quickly identify and group more general land use types without becoming overly granular and potentially less accurate. If a vendor chooses not to adopt the VT Department of Tax Property Category Codes, a crosswalk table should be created to allow standardization when VCGI reads and integrates CAMA data into the statewide dataset. 

If this particular set of category codes are not used, VCGI recommends using or creating another set of codes with a comparable level of detail (e.g., primary residence, commercial, agricultural, open land, etc.). 

### 3.2.4 Normalize Actual Year Built, Effective Year Built, and Unit Count Information

Similar to land use codes and categories, consistent definitions and formatting for actual year built, effective year built, and unit count should be established for all CAMA vendors. While each of these fields appear to exist within the current schema for each vendor, it is essential that all are evaluated using the same methodology and definition.

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

CAMA data is the best source of information for detailed and current property descriptions statewide. Standardizing these data and requiring their submittal to the State of Vermont for regular and uniform public publication, particularly when combined with existing parcel data, will aid improved pace and accuracy of appraisals, provide spatial context, facilitate data visualization and trend analysis, and improve data accessibility. To remain complete and current, however, the submission of standardized CAMA data to SoV should be required. VCGI's Parcel Program, for example, is a voluntary program with data ranging from less than six months to over six years old, despite the widespread visibility, utility, and value of parcel data. Without a submittal requirement for CAMA data it is likely the dataset will become fragmented, incomplete, or stale over time.

## 3.4 Example Statute Updates
>[Section] "Assessor database" means the database of property information maintained by a municipalities' lister(s) or assessor(s); it is also referred to as a Computer Aided Mass Appraisal (CAMA) system or Computer Aided Mass Appraisal database

>[Section] On or before [initial date], and not less than monthly thereafter, each municipality that possesses or contracts for services for the creation or maintenance of an assessor database shall transmit an extract of the database to [the State of Vermont]. The submitted database shall include, but need not be limited to information that uniquely identifies each property in the municipality, the description of each property, the size of each property, the year in which buildings were constructed on each property, and other fields described in the Vermont CAMA data standard.

# Recommendation 4: Clarify Right-of-Way Mapping for Tax Purposes

## 4.1 Summary
- Create guidance for treatment of the area between road centerline and edge of right-of-way for taxation purposes
- Promote mapping guidance specifying that parcels should be mapped to the edge of the right-of-way, not the road centerline

In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and its relation with parcel mapping. Common, practical experience is that public rights-of-way such as roads and highways are just that—areas not to be obstructed by abutting private property owners--be they owned in fee or easements. State highways, for example, often involve the State purchasing lands between the road centerline and abutting parcel, whereas towns may not. These differences contribute to a lack of clarity about how to account for the area that is within a right-of-way and between an abutting private parcel and road centerline and have occasionally led to differences in their depiction and resulting acreage calculations. The Tax Department, with aid of partners, should develop and offer guidance for considering these areas with regard to taxation and related acreage calcuations.

[DIAGRAMS of Right-of-Way Conditions]

## 4.2 Related VT Statutes
[19 V.S.A. § 32 Assumed width of right-of-way](https://legislature.vermont.gov/statutes/section/19/001/00032)

[19 V.S.A. § 1111 Permitted use of the right-of-way relocation or adjustment orders](https://legislature.vermont.gov/statutes/section/19/011/01111)

[19 V.S.A. § 717 Highways / Laying Out, Discontinuing, and Reclassifying Highways](https://legislature.vermont.gov/statutes/section/19/007/00717)

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

[19 V.S.A. § 10 Highways - State Highway Law; General Transportation Divisions](https://legislature.vermont.gov/statutes/section/19/001/00010)

> 19 V.S.A. § 10 (17) Administer the Statewide Property Parcel Mapping Program.

[19 V.S.A. § 44 Statewide Property Parcel Mapping Program](https://legislature.vermont.gov/statutes/section/19/001/00044)

[10 V.S.A. § 123 Geographic Information - Powers and Duties](https://legislature.vermont.gov/statutes/section/10/008/00123)

# Recommendation 11: Coordinate With Concurrent Efforts to Digitize Land Records

Text.

## Related VT Statutes and Bills

[H.512 (Act 171) of 2022 - An act relating to modernizing land records and notarial acts law](https://legislature.vermont.gov/bill/status/2022/H.512)

# Future Improvements 
## Surveying Municipal Boundaries
## Submittals of Land Surveys

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

### A1.7 Parcel Definitions and Interpretations in Existing Vermont Statute

This section lists existing Vermont statutes that define or interpret a definition of a parcel and/or have eligibilty requirements dependent on such definition. It does not list those statutes that use the term "parcel" as an identifier to clarify an idea or specify the location or applicability of what is being discussed without area requirements, unless otherwise noted.

#### 6 V.S.A. Agriculture

[6 V.S.A. § 564 - Agriculture / Hemp](https://legislature.vermont.gov/statutes/section/06/034/00564)
> **§ 564. State hemp program; registration; application; administration.** (i) the location and acreage of all parcels where hemp will be grown;

[6 V.S.A. § 4871 - Agriculture / Agriculture Water Quality / Small Farm Certification](https://legislature.vermont.gov/statutes/section/06/215/04871)
> **§ 4871. Small farm certification.** (a) Small farm definition. As used in this section, “small farm” means a parcel or parcels of land: (1) on which 10 or more acres are used for farming;

#### 9 V.S.A. Uniform Commercial Code

[9A V.S.A. § 2A-103 - Uniform Commercial Code / Leases](https://legislature.vermont.gov/statutes/section/09A/002A/00103)
> **§ 2A—103. Definitions and index of definitions.** (1) In this article unless the context otherwise requires:...(s) (s) “Lot” means a parcel or a single article that is the subject matter of a separate lease or delivery, whether or not it is sufficient to perform the lease contract.

#### 10 V.S.A. Conservation and Development

[10 V.S.A. § 1442 - Conservation and Development / Lake Shoreland Protection Standards](https://legislature.vermont.gov/statutes/section/10/049A/01442)
> **§ 1442. Definitions.** (13) “Parcel” means a portion of land or a tract of land with defined boundaries created by dividing the land by sale, gift, lease, mortgage foreclosure, court-ordered partition or decree, or filing of a plat, plan, or deed in the records of the municipality where the act of division occurred. 

[10 V.S.A. § 6201 - Conservation and Development / Mobile Home Parks](https://legislature.vermont.gov/statutes/section/10/153/06201)
> **§ 6201. Definitions.** (2)  “Mobile home park” means any parcel of land under single or common ownership or control that contains, or is designed, laid out, or adapted to accommodate, more than two mobile homes.

#### 11 V.S.A. Corporations, Partnerships and Associations

[11 V.S.A. § 1610 - Corporations, Partnerships and Associations / Cooperative Housing Ownership Act](https://legislature.vermont.gov/statutes/section/11/014/01610)
> **§ 1610. Separate taxation; mobile home cooperatives.** Each unit in a mobile home limited equity cooperative under proprietary lease, together with any improvements thereon and together with the proprietary lessee’s cooperative interest in the common areas and facilities owned by the cooperative, shall be considered to be a parcel, and shall be subject to separate assessment and taxation as real property by each assessing unit and special district for all types of taxes authorized by law, including special ad valorem levies and special assessments.

#### 24 V.S.A. Municipal and County Government

[24 V.S.A. § 4303 - Municipal and County Government / Municipal and Regional Planning and Development](https://legislature.vermont.gov/statutes/section/24/117/04303)
> **§ 4303. Definitions.** (10) “Land development” means the division of a parcel into two or more parcels, the construction, reconstruction, conversion, structural alteration, relocation, or enlargement of any building or other structure, or of any mining, excavation, or landfill, and any change in the use of any building or other structure, or land, or extension of use of land.

#### 27 V.S.A. Property

[27 V.S.A. § 341 - Property / Conveyance of Real Estate / Execution and Acknowledgment](https://legislature.vermont.gov/statutes/section/27/005/00341)
> **§ 341. Requirements generally; recording.** (b)(2) If the conveyance of land results in the subdivision of a parcel or a change in the boundaries of a parcel after January 1, 2020, the deed shall:
>(A) be accompanied by a survey plat that depicts the new parcel boundaries; or
>(B) cite the volume and page in the land records that indicates where the new parcel boundaries have previously been recorded. 

[27 V.S.A. § 1322 - Property / Condominium Ownership Act / Condominium Ownership](https://legislature.vermont.gov/statutes/section/27/015/01322)
> **§ 1322. Separate taxation.** Each apartment or site and its percentage of undivided interest in the common areas and facilities shall be considered to be a parcel and shall be subject to separate assessment and taxation by each assessing unit and special district for all types of taxes authorized by law, including special ad valorem levies and special assessments, except that parcels held in identical ownership may be combined and treated as one parcel for purposes of assessment and taxation at the discretion of the listers. Neither the building, the property, nor any of the common areas and facilities shall be deemed to be a parcel.

[27 V.S.A. § 1401 - Property / Filing of Land Plats](https://legislature.vermont.gov/statutes/section/27/017/01401)
> **§ 1401. Acceptance of survey plats; definition.** (b) As used in this chapter: (1) “Survey plat” means a map or plan drawn to scale of one or more parcels, tracts, or subdivisions of land, showing, but not limited to, boundaries, corners, markers, monuments, easements, and other rights. (2) “Center” means the Vermont Center for Geographic Information. (c)(1) Whenever a survey plat that maps the subdivision of a parcel or a change in a parcel boundary is filed for record with a town clerk, the surveyor who created the survey plat shall submit a digital copy of the plat to the Center. The Center shall maintain digital copies of survey plats in a statewide digital repository and make them available to the public. 

[27A V.S.A. § 1-105 - Uniform Common Interest Ownership Act (1994) / General Provisions](https://legislature.vermont.gov/statutes/section/27A/001/00105)
> **§ 1-105. Separate titles and taxation.** (a) In a condominium or planned community: (1) if there is any unit owner other than a declarant, each unit that has been created, together with its interest in the common elements, constitutes for all purposes a separate parcel of real estate; and (2) if there is any unit owner other than a declarant, each unit shall be separately taxed and assessed, and no separate tax or assessment may be rendered against any common elements for which a declarant has reserved no development rights; provided, however, that if a portion of the common elements is located in a town other than the town in which the unit is located, the town in which the common elements are located may designate that portion of the common elements within its boundaries as a parcel for property tax assessment purposes and may tax each unit owner at an appraisal value pursuant to 32 V.S.A. § 3481.

#### 32 V.S.A. Taxation and Finance

##### Use Value Appraisal Program

[32 V.S.A. § 3752 - Taxation and Finance / Agricultural Lands and Forestlands / Agricultural Land and Managed Forestland Use Value Appraisal Program](https://legislature.vermont.gov/statutes/section/32/124/03752)
> **§ 3752. Definitions.** (1)"Agricultural land" means any land, exclusive of any housesite, in active use to grow hay or cultivated crops, pasture livestock, cultivate trees bearing edible fruit, or produce an annual maple product, and that is 25 acres or more in size, except as provided in this subdivision (1).
> 
> (C) it has produced an annual gross income from the sale of farm crops in one of two, or three of the five, calendar years preceding of at least: (i) $2,000.00 for parcels of up to 25 acres; and (ii) $75.00 per acre for each acre over 25, with the total income required not to exceed $5,000.00. 
> 
> (5)(B) “Development” also means the subdivision of a parcel of land into two or more parcels, regardless of whether a change in use actually occurs, where one or more of the resulting parcels contains less than 25 acres each; but if subdivision is solely the result of a transfer to one or more of a spouse, ex-spouse in a divorce settlement, parent, grandparent, child, grandchild, niece, nephew, or sibling of the transferor, or to the surviving spouse of any of the foregoing, then “development” shall not apply to any portion of the newly created parcel or parcels that qualify for enrollment and for which, within 30 days following the transfer, each transferee or transferor applies for reenrollment in the Use Value Appraisal Program.
>
> (17) “Reserve forestland” means land that is managed for the purpose of attaining old forest values and functions in accordance with minimum acceptable standards for forest management and as approved by the Commissioner of Forests, Parks and Recreation. On parcels of up to 100 acres, 50 percent or more of the enrolled parcel acres shall be composed of significant and sensitive conditions in accordance with the minimum acceptable standards established by the Commissioner. On parcels of 100 acres or more, 30 percent of the enrolled parcel acres shall be composed of significant and sensitive conditions in accordance with the minimum acceptable standards established by the Commissioner.

[32 V.S.A. § 3755 - Taxation and Finance / Agricultural Land and Managed Forestland Use Value Appraisal Program](https://legislature.vermont.gov/statutes/section/32/124/03755)
> **§ 3755. Eligibility for use value appraisals.** 

See references to parcel defined by common ownership.

[32 V.S.A. § 3756 - Taxation and Finance / Agricultural Land and Managed Forestland Use Value Appraisal Program](https://legislature.vermont.gov/statutes/section/32/124/03756)
> § **3756. Qualification for use value appraisal.**

See references to parcel defined by common ownership.

[32 V.S.A. § 3757 - Taxation and Finance / Agricultural Land and Managed Forestland Use Value Appraisal Program](https://legislature.vermont.gov/statutes/section/32/124/03757)
> **§ 3757. Land use change tax.**

See references to parcel defined by common ownership.

[32 V.S.A. § 3760a - Taxation and Finance / Agricultural Land and Managed Forestland Use Value Appraisal Program](https://legislature.vermont.gov/statutes/section/32/124/03760a)
> **§ 3760a. Valuation audits.**

See references to parcel defined by common ownership.

##### Grand Tax Lists

[32 V.S.A. § 4041a - Taxation and Finance / Grand Tax Lists / Appraisals](https://legislature.vermont.gov/statutes/section/32/129/04041a)
> **§ 4041a. Reappraisal.** (a) A municipality shall be paid $8.50 per grand list parcel per year from the Education Fund to be used only for reappraisal and costs related to reappraisal of its grand list properties and for maintenance of the grand list.

[32 V.S.A. § 4152 - Taxation and Finance / Grand Tax Lists / Grand List of Town](https://legislature.vermont.gov/statutes/section/32/129/04152)
> **§ 4152. Contents.** (a) When completed, the grand list of a town shall be in such form as the Director prescribes and shall contain such information as the Director prescribes, including:... (3) A brief description of each parcel of taxable real estate in the town. “Parcel” means all contiguous land in the same ownership, together with all improvements thereon.

##### Chapter 135: Education Property Tax

[32 V.S.A. § 5401 - Taxation and Finance / Education Property Tax](https://legislature.vermont.gov/statutes/section/32/135/05401)
> **§ 5401. Definitions.** (7) “Homestead”: (A) “Homestead” means the principal dwelling and parcel of land surrounding the dwelling, owned and occupied by a resident individual as the individual’s domicile or owned and fully leased on April 1, provided the property is not leased for more than 182 days out of the calendar year or, for purposes of the renter credit under subsection 6066(b) of this title, is rented and occupied by a resident individual as the individual’s domicile.
>
> (B) The parcel of land surrounding the dwelling shall be determined without regard to any road that intersects the land. If the parcel of land surrounding the dwelling is owned by a cooperative housing corporation incorporated under 11 V.S.A. chapter 14 or owned by a nonprofit land conservation corporation or community land trust with exempt status under 26 U.S.C § 501(c)(3), the homestead includes a pro rata part of the land upon which the dwelling is built, as determined by the cooperative corporation, nonprofit corporation, or land trust.

[32 V.S.A. § 5404 - Taxation and Finance / Education Property Tax](https://legislature.vermont.gov/statutes/section/32/135/05404)
> **§ 5404. Determination of education property tax grand list.** (a)...f a homestead is located on a parcel of greater than two acres, the entire parcel shall be appraised at fair market value; the housesite shall then be appraised as if it were situated on a separate parcel, and the value of the housesite shall be subtracted from the value of the total parcel to determine the value of the remainder of the parcel.
>
> (b)...The data transmitted shall identify each parcel by a parcel identification number assigned under a numbering system prescribed by the Director. Municipalities may continue to use existing numbering systems in addition to, but not in substitution for, the parcel identification system prescribed by the Director.
>
> (d) Municipalities shall include, on all property tax bills, the parcel identification number prescribed in subsection (b) of this section.

[32 V.S.A. § 5404a - Taxation and Finance / Education Property Tax](https://legislature.vermont.gov/statutes/section/32/135/05404a)
> **§ 5404a. Tax stabilization agreements; tax increment financing districts.** (6) An exemption of a portion of the value of a qualified rental unit parcel. An owner of a qualified rental unit parcel shall be entitled to an exemption on the education property tax grand list of 10 percent of the grand list value of the parcel, multiplied by the ratio of square footage of improvements used for or related to residential rental purposes to total square footage of all improvements, multiplied by the ratio of qualified rental units to total residential rental units on the parcel. “Qualified rental units” means residential rental units that are subject to rent restriction under provisions of State or federal law but excluding units subject to rent restrictions under only one of the following programs: Section 8 moderate rehabilitation, Section 8 housing choice vouchers, or Section 236 or Section 515 rural development rental housing.

[32 V.S.A. § 5405 - Taxation and Finance / Education Property Tax](https://legislature.vermont.gov/statutes/section/32/135/05405)
> **§ 5405. Determination of equalized education property tax grand list and coefficient of dispersion.** (f) Within the limits of the resources available for that purpose, the Commissioner may employ such individuals, whether on a permanent, temporary, or contractual basis, as shall be necessary, in the judgment of the Commissioner, to aid in the performance of duties under this section. The Commissioner shall pay each municipality the sum of $1.00 per grand list parcel in the municipality for services provided to the Commissioner in connection with the performance of duties under this section. Each municipality shall deposit payments received under this subsection into a special fund that shall be used to support the preparation of the education property tax grand list.

[32 V.S.A. § 5412 - Taxation and Finance / Education Property Tax](https://legislature.vermont.gov/statutes/section/32/135/05412)
> **§ 5412. Reduction of listed value and recalculation of education tax liability.** (A) The reduction in valuation is the result of an appeal under chapter 131 of this title to the Director of Property Valuation and Review or to a court, with no further appeal available with regard to that valuation, or any judicial decision with no further right of appeal, or a settlement of either an appeal or court action if the Director determines that the settlement value is the fair market value of the parcel.

##### Chapter 154: Homestead Property Tax Credit and Renter Credit

[32 V.S.A. § 6061 - Taxation and Finance / Homestead Property Tax Credit and Renter Credit](https://legislature.vermont.gov/statutes/section/32/154/06061)
> **§ 6061. Definitions.** As used in this chapter unless the context requires otherwise:...(11) “Housesite” means that portion of a homestead, as defined under subdivision 5401(7) of this title but not under subdivision 5401(7)(G) of this title, that includes as much of the land owned by the claimant surrounding the dwelling as is reasonably necessary for use of the dwelling as a home, but in no event more than two acres per dwelling unit, and, in the case of multiple dwelling units, not more than two acres per dwelling unit up to a maximum of 10 acres per parcel. 
>
> (15) “Adjusted property tax” means the amount of education and municipal property taxes on the homestead parcel after reduction for any property tax credit under section 6066a of this chapter. 
>
> (16) “Unadjusted property tax” means the amount of education and municipal property taxes on the homestead parcel before any reduction for a property tax credit under section 6066a of this chapter.

[32 V.S.A. § 6066 - Taxation and Finance / Homestead Property Tax Credit and Renter Credit](https://legislature.vermont.gov/statutes/section/32/154/06066)
> **§ 6066. Computation of property tax credit and renter credit.** (g) Notwithstanding subsection (d) of this section, if the land surrounding a homestead is owned by a nonprofit corporation or community land trust with tax exempt status under 26 U.S.C. § 501(c)(3), the homeowner may include an allocated amount as property tax paid on the land with the amount of property taxes paid by the homeowner on the home for the purposes of computation of the credit under this section. The allocated amount shall be determined by the nonprofit corporation or community land trust on a proportional basis. The nonprofit corporation or community land trust shall provide to that homeowner, by January 31, a certificate specifying the allocated amount. The certificate shall indicate the proportion of total property tax on the parcel that was assessed for municipal property tax and for statewide property tax. 

[32 V.S.A. § 6066a - Taxation and Finance / Homestead Property Tax Credit and Renter Credit](https://legislature.vermont.gov/statutes/section/32/154/06066a)
> **§ 6066a. Determination of property tax credit.** (3) The property tax credit amount determined for the taxpayer shall be allocated first to current year property tax on the homestead parcel, next to current-year homestead parcel penalties and interest, next to any prior year homestead parcel penalties and interest, and last to any prior year property tax on the homestead parcel. No credit shall be allocated to a property tax liability for any year after the year for which the claim or refund allocation was filed. No municipal tax-reduction incentive for early payment of taxes shall apply to any amount allocated to the property tax bill under this chapter.

[32 V.S.A. § 6069 - Taxation and Finance / Homestead Property Tax Credit and Renter Credit](https://legislature.vermont.gov/statutes/section/32/154/06069)
> **§ 6069. Landlord certificate.** (a) On or before January 31 of each year, the owner of land rented as a portion of a homestead in the prior calendar year shall furnish a certificate of rent to the Department of Taxes and to each claimant who owned a portion of the homestead and rented that land as a portion of a homestead in the prior calendar year. The certificate shall indicate the proportion of total property tax on that parcel that was assessed for municipal property tax and for statewide property tax.

##### Chapter 236: Tax on Gains from the Sale or Exchange of Land 

[32 V.S.A. § 10002 - Taxation and Finance / Tax on Gains from the Sale or Exchange of Land](https://legislature.vermont.gov/statutes/section/32/236/10002)
> **§ 10002. Land and residences** (a) “Land” means all land, whether or not improved, that has been purchased and subdivided by the transferor within the six years prior to the sale or exchange of the land, but does not include land not exceeding 10 acres, necessary for the use of a dwelling used by the seller of such land as his or her principal residence. Buildings or other structures are not included in this definition of “land.” “Land” also means timber or rights to timber when that timber or those timber rights are sold within six years of their purchase, provided the underlying land is also sold within six years. “Underlying land” means the land from which timber or timber rights have been separated, whether subdivided or not. As used in this subsection, the term “subdivision” means a tract or tracts of land, owned or controlled by a person, that the person has partitioned or divided for the purpose of sale or transfer. Subdivision shall be deemed to have occurred on the conveyance of the first lot or the filing of a plat, plan, or deed in the town records, whichever first occurs. A subdivision shall not include a boundary adjustment between adjacent parcels.
>
> (f) Also excluded from the definition of “land” is any land up to 10 acres, with the modification permitted by subsection (c) of this section, acquired by a person who will build on that land a house that, by the next succeeding sale, will be the principal residence of the occupant when the person purchases from the person who built the house. The person acquiring such land must certify to the Commissioner of Taxes that the person will begin building within one year of date of purchase, complete the building within two years from the date of purchase, and sell it within three years from date of purchase to a person who qualifies under subsection (b) of this section. If the land is sold as more than one parcel by the builder who acquired it, only those parcels on which a dwelling has been completed in accordance with the requirements of this subsection shall be excluded from the definition of “land.” The deed for the property shall recite the fact that there is running with the land a lien equal to the amount of land gains tax exempted by this subsection until the time as all conditions of this subsection have been met.
>
> (m) Also excluded from the definition of “land” is a parcel of land 25 acres or less, purchased by a farmer, as defined in section 3752 of this title, for active and direct use by that farmer, and that, upon transfer, but for the acreage, meets the definition of “agricultural land” or “managed forestland” in section 3752 of this title, and continues to meet that definition for at least six years after the transfer.

#### Existing Legislation Overview

| Statute         | Title       | Chapter | Subchapter               | Section                                                       | Acreage Dependency | Acreage Amount | Eligibility   |
|-----------------|-------------|---------|--------------------------|---------------------------------------------------------------|--------------------|----------------|---------------|
| 6 V.S.A. § 564  | Agriculture | Hemp    |                          | State hemp program; registration; application; administration | No                 |                |               |
| 6 V.S.A. § 4871 | Agriculture | Hemp    | Small Farm Certification | Small farm certification                                      | Yes                | 10             | Certification |

## Appendix 2: Per Parcel Payments

## A2.1 Assessment of Current Practices
### A2.1.1 Voluntary Participation
The ongoing effort to publish parcel data (joined to the annual Grand List) in a uniform, digital format relies on municipalities voluntarily sharing updated parcel geometry with VCGI. While this approach has worked for the Parcel Program for nearly half a decade, the need to create a financial incentive to increase participation has always been considered as referenced in the 2015 Vermont Statewide Digital Parcel Lifecycle & Maintenance Plan:

> As implementation shifts into a maintenance stage, Vermont will want to pay close attention to challenges to compliance. While some impediments may be more attitudinal than logistical or economic, the state may want to consider creating incentives to comply.

As parcel data continues to be one of the most used statewide datasets in Vermont, creating a financial incentive is likely necessary not only to increase participation but also to improve data quality. To encourage participation from as many municipalities as possible, VCGI has largely been accepting parcel geometry "as-is" which often requirese significant edits before publishing to meet the existing data standard.

### A2.1.2 Shared Responsibility Model
The notable success of the Parcel Program as a voluntary-based initiative is due to the collaboration between municipalities, state government, and mapping vendors in the private sector. This "Shared Responsibility" model relies on all collaborators contributing resources to maintain statewide parcel data.

![image](https://github.com/user-attachments/assets/57368cfe-eb6c-47b7-99ad-66c17cb00e3d)

This graphic repersentation of the Shared Responsibility model indentifies one attribute: a municipality's ability to preform parcel geometry updates by contracting with a mapping vendor or doing updates internally. Municipalities unable to preform parcel geometry updates currently recieve irregular updates by VCGI as land surveys that can be used to update a municipality's parcel geometry are submitted to the [Vermont Land Survey Library](https://landsurvey.vermont.gov/). While this has been a sufficient approach to date, with the creation of the City of Essex Junction in 2022, Vermont now has 256 municipalities: 237 towns, 10 cities, 5 unincorporated towns, and 4 gores. With so many collaborators at the municipal level, the shared responsibility of each municipality should based upon more than one attribute.

## A2.2 Funding during the Parcel Project
The Parcel  Project (2017-2019) leveraged both state and federal funds with 80 percent coming from the Federal Highway Administration and the remaining 20 percent from several state agencies and departments. The Vermont Agency of Transporation contracted with several mapping vendor to update or create digital parcel data for each Vermont municipality over a three-year period. Each mapping vendor was assigned to a municipality through a competitive bid process. The cost per parcel for a sample of municipalities completed during the first year of the Parcel Project is depicted below.

![image](https://github.com/user-attachments/assets/0a2f0a02-5f07-41cb-b18a-78f785ca1d86)

## Appendix 3: CAMA Data Standard

### A3.1 Land Use Codes
 Vermont Department of Tax [Property Class Codes](https://tax.vermont.gov/sites/tax/files/documents/Property%20Class%20Codes.pdf) (category level only):

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
Proposed standardized CAMA schema, based on example data from CAMA vendors in Vermont as well as a similar schema being developed in Connecticut, can be viewed [here](https://vermontgov.sharepoint.com/:x:/t/ADS.VCGIGroup/EZEBDpDNLNNHk_dhFOhtNW8BiiuDlzcCbWzOrxTXDUgO_g?e=3QqTMj). See 'PriorityFields_v1' for fields to standardize first following agreement between VT Department of Tax and all CAMA vendors.

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


## Appendix X: Maps and Tables

### X.X Lands in Current Use

### X.X Lands in Current Use Needing Administrative Definition for Acreage

### X.X Acreage in Right-of-Way

### X.X Acreage Duplicately Counted

### X.X Acreage Not Counted (Gaps)

### X.X Acreage in Common Ownership

### X.X Discrepancies in Listed and Mapped Acreage

#### Sum of Listed Acreage

#### Sum of Mapped Acreage

#### State Boundary

| Geography | Total Area |         |            | Land Area |         |            | Water Area |         |         |
|-----------|------------|---------|------------|-----------|---------|------------|------------|---------|---------|
|           | Sq. Mi.    | Sq. Km. | Acres      | Sq. Mi.   | Sq. Km. | Acres      | Sq.Mi.     | Sq. Km. | Acres   |
| Vermont   | 9,615      | 24,903  | 6,153,746  | 9,217     | 23,873  | 5,899,041  | 398        | 1,031   | 254,705 |
|           |            |         | 100%       |           |         | 96%        |            |         | 4%      |

Table 1. Source: [2022 TIGER/Line Geodatabase File.](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-geodatabase-file.2022.html) U.S. Census Bureau.

Notes:
1. The [NIST standard](http://www.nist.gov/system/files/documents/2023/01/30/appc-23-HB44.pdf) for converting square meters into square miles was used (1 square mile = 2,589,988.110336 square meters).
2. Acres were calculated by multiplying square miles by 640, per conversion factors in the [NIST Handbook 44 (2023)](https://www.nist.gov/system/files/documents/2023/01/30/appc-23-HB44.pdf), Appendix C: General Tables of Units of Measurement.
3. Area measurements are from the Census Bureau's master TIGER database. Land and water classifications reflect updates made to the TIGER database through August 2022. Values reflect the ALAND and AWATER fields. Water measurements include only perennial water. All other water (intermittent, glacier, marsh/swamp) is included in the table as part of land area calculations.

![image](https://github.com/user-attachments/assets/c61cb466-6e03-46d7-83e9-ebda6adfc6c9)
Figure X. Vermont land and water areas as depicted using BNDHASH and NHDPlus HR input layers.

### X.X Estimated Percent Change in Parcel Counts

### X.X Age of Parcel Geometry by Town

### X.X Maintenance of Parcel Geometry by Town
