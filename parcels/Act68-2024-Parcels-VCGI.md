# Purpose

This document outlines all recommendations for parcel mapping and data maintenance as related to [Act 68 of 2023](https://legislature.vermont.gov/bill/status/2024/H.480). It is authored by the Vermont Center for Geographic Information (VCGI), state stewards of the [Statewide Property Parcel Mapping Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) since 2020, established via [19 V.S.A. § 44](https://legislature.vermont.gov/statutes/section/19/001/00044). The recommendations aim to improve parcel data quality to support timely, fair, accurate, and modern property valuation and reappraisals as sought by Act 68, which [asks the Tax Department to](https://legislature.vermont.gov/Documents/2024/Docs/ACTS/ACT068/ACT068%20Act%20Summary.pdf):

> [create] recommendations and considerations for distinguishing between different types and characteristics of property and their uses, and how different property data could be used to make policy decisions.

# Overview of All Recommendations

| **Recommendation**                                                                      | **Statute Change** | **Incentive / Payment** | **Technical Guidance** | **New Technology** |
|:---------------------------------------------------------------------------------------:|:------------------:|:-----------:|:----------------------:|:------------------:|
| [1. Update Parcel Definition in Vermont Statute](#recommendation-1-update-parcel-definition-in-vermont-statute)                                              | X                  |             |                        |                    |
| [2. Support Digital Parcel Maintenance and Submittal to the State](#recommendation-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont)          | X                  | X           |                        |                    |
| [3. Implement Vermont CAMA Data Standard and Require Submittal to State](#recommendation-3-implement-vermont-cama-data-standard-and-require-submittal-to-state)                       | X                |             | X                      |                    |
| [4. Clarify Right-of-Way Mapping for Tax Purposes](#recommendation-4-clarify-right-of-way-mapping-for-tax-purposes)                         |                   |             | X                       |                    |
| [5. Clarify Grand List vs. GIS Acreage Guidance](#recommendation-5-clarify-grand-list-vs-gis-acreage-guidance)                                          |                    |             | X                      |                    |
| 6. Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract |                    |             | X                      | X                  |
| 7. Pilot Remotely-Sensed Tools to Support Appraisals                                    |                    |             |                        | X                  |
| [8. Develop and Offer Updated Parcel Contract Guidance](#recommendation-8-develop-and-offer-updated-parcel-contract-guidance)                  |                    |             | X                      | X                  |
| [9. Modernize Current Use Map Standards and Submittals](#recommendation-9-modernize-current-use-map-standards-and-submittals)                                   |                    |             |                        | X                  |
| [10. Consider Updating and Moving Parcel Program in VT Statute](#recommendation-10-consider-updating-and-moving-parcel-program-in-vt-statute)                           | X                  |             |                        |                    |
| [11. Coordinate With Concurrent Efforts to Digitize Land Records](#recommendation-11-coordinate-with-concurrent-efforts-to-digitize-land-records)                         |                   |             |                        | X                   |
| [12. Make Proposed Assessment Districts Consistent and Compatible with Existing Administrative Boundaries](#recommendation-12-make-proposed-assessment-districts-consistent-and-compatible-with-existing-administrative-boundaries)                         |                   |             | X                        |                    |

# Recommendation 1: Update Parcel Definition in Vermont Statute
## 1.1 Summary
- Change the current parcel definition from solely a "contiguous" parcel definition to one that also requires tracking of separate and sellable pieces of real estate
- This definition will replace the undefined practice of mapping and tracking "inactive" parcels and instead require towns to map and track all separate parcels individually, regardless of common ownership
- "Contiguous" parcels aggregated by common ownership are still to be created for the purposes of tax administration
- Two parcel map layers will continue to be published via the Statewide Parcel Program: one for tax administration (formerly known as "active parcels"), and one for tracking all parcels separately (formerly known as "inactive parcels")

## 1.2 Justification
Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defines a parcel as:
> (3) A brief description of each parcel of taxable real estate in the town. “Parcel” means all contiguous land in the same ownership, together with all improvements thereon.

This is a "contiguous" parcel definition, depicted in figure 1. Separate lots are grouped together by ownership for administrative purposes, including the sending of a single tax bill per owner per "parcel". Separate lots are sometimes managed as "inactive" parcels, although that term is not defined outside of the [parcel data standard](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) and their upkeep by towns is not uniform. The marketability of individual lots for sale is not clear, nor is it clear is how towns should map and track lots within a combined parcel. Aggregate parcel delineation further complicates assignment of highest and best use valuation as assessors may have to generalize across several different lot types. Data management, change tracking, and downstream analysis are also negatively impacted by an aggregate, contiguous parcel definition.

![Parcel Types Diagram For Statute Change_v4d-01](https://github.com/user-attachments/assets/6f5e420e-9a2f-45b7-8fe7-40772bb5a618)
**Figure 1: Current and Proposed Parcel Definition.** *The proposed separate parcel definition removes the need for tracking "inactive" parcels, while ensuring all component parts of parcels are assigned a unique identifier.*

Alternatively, defining parcel as a separate and sellable lot or piece of real property would bring parcel identification in line with their common understanding as "lots" (as opposed to grouped areas) while also reducing the need to generalize highest and best use across several different parcels combined by owner during valuation. This change would enable improved parcel documentation by ensuring that no parcel in full or in part goes unidentified, ease highest and best use valuation, improve data maintenance, long-term record keeping, and analysis, and continue to allow aggregation by owner for tax administration. It could also have bearing on any parcel count-dependent fee or payment as what constitutes a "parcel" would need to be defined and confirmed should funds be contingent on their amount (see [recommendation 2](#recommendation-2-reward-digital-parcel-submittal-to-state-of-vermont-via-per-parcel-payment)).

With variations in the timing of when a separate lot or piece of real property is created, an updated parcel definition could be written to allow a legal document (deed or title), subdivision plats, or sale to help define the bounds of the separate mapped and tracked area. Existing "inactive" parcels, where they exist and are maintained, should be tracked and mapped with their unique SPAN and attribution and ultimately incorporated with the current "active" parcel layer to create a map layer of the smallest, documented, bounded sellable areas. A separate parcel layer with parcels combined on ownership should persist for tax administration use. Two statewide parcel map layers would result, one that reflects documented, bounded, sellable pieces of real estate, and the other that represents contiguous parcels combined on ownership. Both layers would continue to be published and made publicly available by the Statewide Parcel Property Program.

These changes in parcel definition and mapping practices would increase the current count of parcels statewide from roughly 340,000 to an estimated 380,000. This figure is estimated as currently only 70% of towns (178 total) have submitted their inactive parcels as digital parcel data to VCGI. It remains unknown how many of the other 30% of towns map inactive parcels digitally.

## 1.3 Example Statute Update

> 32 V.S.A. § 4152 (a)(3) A brief description of each parcel of taxable real estate in the town. “Parcel” means <ins>a separate and sellable lot or piece of real estate. Parcels are to be combined to represent</ins> *all contiguous land in the same ownership, together with all improvements thereon* <ins>for tax administration.</ins>

## 1.4 Related Statutes

See [Appendix A1.8 Parcel Definitions and Interpretations in Existing State Statute](#a18-parcel-definitions-and-interpretations-in-existing-vermont-statute). 

## 1.5 Implementation

Vermont municipalities would be expected to continue to aggregate parcels by common ownership and map them as they do currently. This aggregate, "contiguous" map layer would continue to be submitted by towns to the Statewide Property Parcel Program overseen by VCGI, and remain adherent to an updated VT GIS Parcel Data Standard. The layer will be renamed from "active" parcels to "administrative" parcels by VCGI. SPAN numbers for administrative parcels would be maintained in a field called ADMINSPAN, and mirror the source ADMINSPAN of its constituent parts that have the same ownership (see Figure 1 and [Appendix 1.7](#a17-proposed-parcel-layers-and-vt-gis-data-standard-schema-per-updated-parcel-definition)). When a parcel has only one bounded area in common ownership, its ADMINSPAN would be the same value as its SPAN.

Municipalities would also be expected to track and map what are currently called "inactive" parcels, however, these parcels would reflect the updated parcel definition and depict separately sellable pieces of real estate given their best available documentation, and regardless of common ownership. Data are to remain adherent to an updated VT GIS Parcel Data Standard, albeit "inactive" parcels are to be renamed to simply "parcels". They are also to continue to be submitted to the State Property Parcel Program overseen by VCGI, who will rename the current "inactive" parcels layer as "parcels". It is expected that mapping and tracking of these parcels reflective of an updated parcel definition by municipalities will take time and improve with continued maintenance.

Advance notice of these changes will be sent by VCGI to the VT GIS community, municipalities, and their mapping vendors.

A full description of proposed changes is within [Appendix 1.7: Proposed Parcel Layers and VT GIS Data Standard Schema, per Updated Parcel Definition](#a17-proposed-parcel-layers-and-vt-gis-data-standard-schema-per-updated-parcel-definition).

# Recommendation 2: Support Digital Parcel Maintenance and Submittal to the State of Vermont
## 2.1 Summary

- The current model of town-based parcel maintenance with voluntary submittal to the state has reached its limits in data quality and currentness, further improvements will need support
- The design of support for parcel data maintenance and submittal will depend on the jurisdiction ultimately responsible for mapping: town (current), region, or state
- If municipalities are to remain responsible for mapping: institute a per parcel payment to municipalities to aid costs associated with parcel data maintenance
- Make disbursement of this per parcel payment to municipalities contingent on submittal of [Vermont GIS Data Standard-compliant](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) digital parcel data to VCGI, maximum payment once per year per town
- A payment should help compensate only for those parcels that are changed in geometry since the last update
- Per parcel payments may be administered and normalized by proposed Regional Appraisal Districts
- If Regional Appraisal District or state is to assume responsibility for parcel mapping, those practices should be required to adhere to the state data standard, maintain and share with the state on a normalized schedule, and be funded accordingly


## 2.2 Justification

Vermont has 256 municipalities: 237 towns, 10 cities, 5 unincorporated towns, and 4 gores. Unlike other states with county government that oversee the task, in Vermont individual municipalities are responsible for parcel mapping of taxable lands in their jurisdiction. Most towns budget to hire a GIS vendor to maintain their digital parcel data and depend on them to reflect any changes to parcel geometry since the town's last update. Frequency of geometry updates varies by town and may be completed annually to every 2-3 years or more. Some towns remain without any digital parcel geometry maintenance. Town oversight of parcel mapping is typically the responsibility of its listers or assessors.

The [Statewide Property Parcel Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) publishes municipal parcel map data joined to the annual statewide grand list in a uniform, digital format. The Program relies on towns voluntarily sharing updated parcel geometry with VCGI, typically via their vendor. These data are then made publicly available by VCGI in a uniform, accessible way. They drive applications such as the [Vermont Parcel Viewer](https://maps.vcgi.vermont.gov/ParcelViewer/) that draws more than 500,000 unique views a year, and are offered as raw spatial data that sees more than 1 million unique views a year.

Parcel data sourced in this voluntary way are now one of the State of Vermont's most-used spatial datasets, supporting state, regional, and local efforts in emergency management, natural resources policy and planning, permitting and compliance, and transportation. They also support efforts to address pressing issues such as flood response, resilience planning, and housing. All municipalities may use these data and applications to display their digital parcel maps free of charge. Some towns pay vendors for additional map services such as custom web applications and print map production. The current overarching incentive for municipal parcel data maintenance is for towns to ensure the most accurate, consistent, and timely data exist across all representations of who owns which lands where and with what details, be that in grand list tables or on maps that see high use.

While relatively successful, there are improvements that are needed in the current town-sourced model of parcel data maintenance and publishing. About 60% of municipalities have submitted updated parcel geometry to VCGI within the last year. In contrast, about 16% of municipalities have not submitted updated parcel geometry to VCGI in over three years, indicating a divide in participation in the Parcel Program and limitations to its voluntary model. Inaccurate, untimely data impacts downstream uses that are now dependent on this information.

### 2.2.1 Submittal Status
VCGI tracks municipal parcel data maintenance and voluntary submittals and presents this information via the [Parcel Program's Town Mapping Status application](https://maps.vcgi.vermont.gov/parcelstatus/), updated weekly. These statistics represent five years (2020 - 2024) of oversight of the Statewide Property Parcel Program. They highlight the need for improvements to the current data maintenance model.

As of October 24, 2024:
-	90% of towns are edited/updated by vendors or the town. 10% are edited/updated by VCGI (these are considered “not VT GIS Parcel Data Standard compliant”) 
-	10% of submissions require edits to parcel topology (i.e., geometry) to address gaps and/or overlaps among parcels
-	50% of submissions required edits that were already made for the previous submission  (i.e., repeated revisions)
-	70% of submissions contain inactive parcels. Inactives exist for at least some towns that do not include them in their submissions
-	96% of towns include and represent rights-of-way. For those that do not, some map parcels to road centerlines, others only include main ROWs or those in the town/village center, and others have gaps in the parcel data where roads should be
-	24% of submissions are fully compliant with the current parcel data standard. 26% are compliant with minor edits. 37% are compliant with major edits. 13% are not compliant (see [submittal criteria](#232-submittal-quality-criteria) )
-	11% of towns have a mapping vendor (to the best of VCGI's knowledge) but have not submitted an update since the original Parcel Project data (prior to 2020). These towns are currently classed as “fully compliant” despite having stale data.
-	12% of submissions are/have been reviewed by towns prior to submittal; 64% have not, and 24% are unknown. Some vendors are working closely with towns as edits are being made (or edits are only being made at the direction of a town official), which may negate the need for a more formal review of the data prior to submission

## 2.3 Design

The design of a financial incentive to reward parcel data upkeep and quality improvements that is contingent on data submittal to the State should consider Municipal maintenance costs, be reflective of only those parcels that are changed (and thus need maintenance) since the last update, and potentially, account for cost differences by regional location and/or situation.

### 2.3.1 Support By Maintenance Type

A financial incentive to assist [JURISDICTION] with the cost of parcel mapping that is contingent on data standard-compliant parcel geometry submissions to VCGI could be designed to close this “participation gap” while improving data quality. An incentive is preferable to a submittal requirement as the latter may not be possible to meet by some towns and challenging to enforce. An incentive, when combined with the fact that standardized GIS parcel data exist statewide (albeit they may not be up to date), may be enough to enable the remaining 10-15% of towns without GIS parcel data maintenance to begin upkeep and improvement. Creating incentives to increase data maintenance and sharing was also a recommended consideration in the [2015 Vermont Statewide Digital Parcel Lifecycle & Maintenance Plan](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/VT_Parcel%20Data%20Lifecycle%20and%20Maintenance%20Plan_2015_FINAL.pdf):

> As implementation shifts into a maintenance stage, Vermont will want to pay close attention to challenges to compliance. While some impediments may be more attitudinal than logistical or economic, the state may want to consider creating incentives to comply.

Other states have implemented similar contingent financial incentives to maintain foundational, local spatial data (Massachusetts, for example, [with their 911 addressing data](https://www.mass.gov/doc/standard-for-digital-parcels-and-related-data-sets-version-3/download)). Assuming that municipalities remain responsible for and the authoritative source of land records, 
[It is time to consider supporting Vermont municipalities in the upkeep of parcel data on which many State programs now depend.]

### 2.3.1 Eligibility

- VCGI will continue to accept and review parcel geometry updates on a rolling basis. A municipal official (or a contact from a municipality’s mapping vendor) must send a standard-compliant parcel geometry update to VCGI by October 1st of a calendar year to be eligible to receive a financial incentive the following year.
- No more than one standard-compliant parcel geometry update per municipality will be accepted each calendar year.
- Parcel geometry updates will continued to be submitted to VCGI using the [Share Map Data](https://vcgi.vermont.gov/data-and-programs/share-map-data) form.
- VCGI should be notified if a municipality has no changes to report. A municipality that reports no changes will not be eligible to receive a financial incentive.
- Some municipalities may choose to “opt-out,” forgoing their eligibility in exchange for VCGI assisting in their parcel geometry update. Municipalities that may be good candidates to opt-out include:
    - Municipalities not currently updating their parcel geometry, contracting with a non-GIS vendor, or having "low confidence" in their ability to conduct parcel geometry updated internally.
    - Municipalities with a relatively small parcel count or relatively few parcel geometry updates.

### 2.3.2 Submittal Quality Criteria

|**Criteria**                | **Description/Examples**|
|:---------------------------|:------------------------|
|Fully Compliant             | •	Includes all towns that have not been updated since the Parcel Project (i.e., prior to 2020).<br>•	Valid topology; no gaps or overlaps among parcels<br>•	ROWs included and mapped correctly<br>•	Unmatched parcels only comprised of land expected to have no SPAN (common land, town/state/federally-owned land, etc.)<br>•	Multi-SPAN parcels (e.g., condos) are attributed correctly through the intersection table, if applicable<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly; does not require edits that were made in the previous submission; any unmatched parcels are expected to be unmatched given their status as common land, government-owned land, etc.; any multi-SPAN parcels are accounted for correctly in the intersection table. Includes towns that are working with a vendor to maintain parcels but have not submitted updates to VCGI since January 1, 2020.
|Compliant with Minor Edits  |•	Unmatched parcels (as received) are < 2%<br>•	ROWs included and mapped correctly<br>•	No/minimal repeated edits from prior submission during VCGI review<br>•	No/minimal (<10) edits to intersection table to account for multi-SPAN parcels<br>•	No topology errors<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly. Requires minor editing to address unmatched parcels (<2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include <10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Compliant with Major Edits  |•	Unmatched parcels (as received) are > 2%<br>•	Topology errors resulting in gaps/overlaps among parcels<br>•	Incorrect or missing attribution of condos/multi-SPAN parcels in the intersection table<br>•	ROWs are missing or incomplete (e.g., parcels are mapped to road centerlines)<br>•	Repeated edits from prior submission during VCGI review<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard to the extent that it can be incorporated into the statewide parcel dataset following revisions. May require significant edits to address topology errors, missing or invalid SPANs, missing or incomplete ROWs, and/or missing or incomplete multi-SPAN parcel representation in the intersection table. Requires editing to address unmatched parcels (>2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include >10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Not Compliant               |•	Includes all towns that are updated by VCGI/have no vendor or capacity to submit their own updates<br>•	Submission does not include SPANs or Parcel/Map IDs that can be linked to the Grand List<br>•	Submission is in an unusable format (e.g., CAD) that cannot be converted to a geodatabase<br>•	Usable format (i.e., GIS files) but missing or invalid fields that do not allow conversion to usable schema/dataset, or require significant effort to update using existing data and external sources/map viewers (e.g., loading existing attribution into new geometry; using E911, AxisGIS, or other to validate/verify SPANs; merging/splitting active and inactive parcels, etc.)<br><br>Summary: submission does not meet format and/or content allowing for inclusion in the statewide parcel dataset. Data format may be unusable/unable to convert to GIS, and/or attribution does not include valid SPANs or Parcel/Map IDs for linking to Grand List. May sometimes include a workable data format that requires significant geometry (e.g., active and inactive parcels) and/or attribute manipulation using internal and external data sources (e.g., AxisGIS sites, surveys, E911 data, etc.) to create dataset with valid schema and attribution. Also includes towns that do not have a vendor or the capacity to make their own edits and are updated by VCGI using data available in the VT Land Survey Library.

### 2.3.3 Communication and Timing

Text.

### 2.3.4 Funding

In November 2024 VCGI organized a focus group of 12 municipalities selected based on parcel count, location, and mapping vendor. A municipal official (Lister, Assessor, or Town Clerk) from each municipality was contacted by email and asked how much the municipality currently spends on parcel mapping. While sample size is a limiting factor, based on the information provided by the 7 municipalities that responded, the cost of ongoing parcel data maintenance is less than the initial cost during the Parcel Project. This is true even for municipalities that are no longer contracting with their Parcel Project mapping vendor. The current cost per parcel averaged $2.66 compared to $5.87 during the Parcel Project (55% cost reduction).

|Municipality    |2023 Grand List Parcel Count|Active Polygons|Inactive Polygons|Current Vendor        | Parcel Project Vendor|
|----------------|----------------------------|---------------|-----------------|----------------------|----------------------|
|Bakersfield     |739                         |778            |0                |CTI                   |CTI                   |
|**Belvidere**   |**290**                     |**317**        |**0**            |**Chris Chamberlain** |**CAI**               |
|Ferrisburgh     |1625                        |1719           |0                |Chris Chamberlain     |VHB                   |
|Grand Isle      |1345                        |1374           |154              |CAI                   |Russell Graphics      |
|**Huntington**  |**944**                     |**983**        |**0**            |**Chris Chamberlain** |**Atlas Geographic**  |
|**Landgrove**   |**226**                     |**249**        |**5**            |**CAI**               |**CAI**               |
|**Londonderry** |1575                        |1528           |277              |CAI                   |CAI                   |
|Maidstone       |376                         |384            |53               |CAI                   |CAI                   |
|**Montpelier**  |**3280**                    |**3065**       |**46**           |**CAI**               |**Russell Graphics**  |
|**Pownal**      |**1764**                    |**1772**       |**162**          |**CTI**               |**CTI**               |
|**Randolph**    |**2154**                    |**2219**       |**65**           |**CAI**               |**CAI**               |
|Stratton        |1621                        |1630           |325              |CTI                   |CTI                   |

**Table X: Municipalities contacted for current parcel data maintenance cost information.** *Bold text denotes towns that responded with current maintenance costs.*

While VCGI would continue to receive parcel data updates from municipalities, funding could be allocated by the proposed "Assessment Districts" which could help account for any geographic variance between municipalities with respect to parcel mapping. Using counties as an example, there is a significant range between cost per parcel during the Parcel Project:

|County     |2024 Grand List parcel count (perliminary)|Parcel Project cost|Parcel Project cost per parcel|
|-----------|------------------------------------------|-------------------|------------------------------|
|Addison    |18,733                                    |$116,084           |$6.20                         |         
|Bennington |22,178                                    |$117,199           |$5.28                         |
|Caledonia  |17,901                                    |$89,378            |$4.99                         |
|Chittenden |61,096                                    |$117,333           |$1.92                         |
|Essex      |6,431                                     |$67,634            |$10.52                        |
|Frankin    |24,657                                    |$109,960           |$4.46                         |
|Grand Isle |6,446                                     |$38,191            |$5.92                         |
|Lamoille   |15,107                                    |$65,354            |$4.33                         |
|Orange     |17,297                                    |$92,272            |$5.33                         |
|Orleans    |18,832                                    |$109,721           |$5.83                         |
|Rutland    |35,781                                    |$212,839           |$5.95                         |
|Washington |31,613                                    |$137,526           |$4.35                         |
|Windham    |31,727                                    |$119,424           |$3.76                         |
|Windsor    |36,289                                    |$148,672           |$4.10                         |

At the county-level, the average cost per parcel during the Parcel Project was $5.21 which is slightly below the average cost per parcel of the focus group during the Parcel Project. If the estimated 55% cost reduction was applied to the cost per parcel for each county during the Parcel Project, **funding for a proposed financial incentive would need to be about $700,000 annually for the state**:

|County     |Estimated cost reduction per parcel|Estimated funding|
|-----------|-----------------------------------|-----------------|
|Addison    |$2.79                              |$52,238          |  
|Bennington |$2.38                              |$52,740          |
|Caledonia  |$2.25                              |$40,220          |
|Chittenden |$0.86                              |$52,800          |
|Essex      |$4.73                              |$30,435          |
|Frankin    |$2.01                              |$49,482          |
|Grand Isle |$2.67                              |$17,186          |
|Lamoille   |$1.95                              |$29,409          |
|Orange     |$2.40                              |$41,552          |
|Orleans    |$2.62                              |$49,374          |
|Rutland    |$2.68                              |$95,778          |
|Washington |$1.96                              |$61,887          |
|Windham    |$1.69                              |$53,741          |
|Windsor    |$1.84                              |$66,902          |
|**Total**  |                                   |**$693,714**     |

Each county could be assigned its own per parcel fee or a single per parcel fee could be established for the state with some counties receiving an additional percentage above the per parcel fee based on financial capacity. While there are multiple ways to determine financial capacity, two methods using the Real Listed Value field from the 2023 Grand List are shown below. For both methods, any county that is **below** the average value would receive an adjusted per parcel fee. The remaining counties would receive the standard per parcel fee.

**Real Listed Value per Capita**

|County       |2020 Census Population|Total Real Listed Value|Real Listed Value per capita|Percent difference|Per parcel multiplier|
|-------------|----------------------|-----------------------|----------------------------|------------------|---------------------|
|Addison      |37,363                |$5,988,167,654         |*$160,270*                  |7%                |1.07                 |
|Bennington   |37,347                |$6,826,419,057         |$182,784                    |                  |                     |
|Caledonia    |30,233                |$3,890,741,398         |*$128,692*                  |29%               |1.29                 |
|Chittenden   |168,323               |$29,382,064,381        |$174,558                    |                  |                     |          
|Essex        |5,920                 |$1,053,422,600         |$177,943                    |                  |                     |
|Frankin      |49,946                |$6,618,293,728         |*$132,509*                  |26%               |1.26                 |
|Grand Isle   |7,293                 |$1,836,562,678         |$251,825                    |                  |                     |
|Lamoille     |25,945                |$5,794,509,702         |$223,338                    |                  |                     |
|Orange       |29,277                |$4,074,229,888         |*$139,161*                  |21%               |1.21                 |
|Orleans      |27,393                |$3,906,839,150         |*$142,622*                  |19%               |1.19                 |
|Rutland      |60,572                |$8,280,781,106         |*$136,710*                  |23%               |1.23                 |
|Washington   |59,807                |$9,733,853,072         |*$162,754*                  |6%                |1.06                 |
|Windham      |45,905                |$9,476,204,580         |$206,431                    |                  |                     |
|Windsor      |57,753                |$10,979,699,045        |$190,115                    |                  |                     |
|**Average**  |                      |                       |**$172,122**                |                  |                     |

**Real Listed Value per Acre**

|County       |Total Acres (parcels only)|Total Real Listed Value|Real Listed Value per acre|Percent difference|Per parcel multiplier|
|-------------|--------------------------|-----------------------|--------------------------|------------------|---------------------|
|Addison      |485,308                   |$5,988,167,654         |*$12,339*                 |52%               |1.52                 |
|Bennington   |423,954                   |$6,826,419,057         |*$16,102*                 |26%               |1.26                 |
|Caledonia    |405,042                   |$3,890,741,398         |*$9,606*                  |74%               |1.74                 |
|Chittenden   |333,079                   |$29,382,064,381        |$88,214                   |                  |                     |
|Essex        |421,257                   |$1,053,422,600         |*$2,501*                  |157%              |2.57                 |
|Frankin      |396,210                   |$6,618,293,728         |*$16,704*                 |23%               |1.23                 |
|Grand Isle   |51,370                    |$1,836,562,678         |$35,752                   |                  |                     |
|Lamoille     |291,881                   |$5,794,509,702         |*$19,852*                 |6%                |1.06                 |
|Orange       |428,914                   |$4,074,229,888         |*$9,499*                  |75%               |1.75                 |
|Orleans      |435,479                   |$3,906,839,150         |*$8,971*                  |80%               |1.80                 |
|Rutland      |585,673                   |$8,280,781,106         |*$14,139*                 |39%               |1.39                 |
|Washington   |430,387                   |$9,733,853,072         |$22,617                   |                  |                     |
|Windham      |493,362                   |$9,476,204,580         |*$19,207*                 |9%                |1.09                 |
|Windsor      |604,359                   |$10,979,699,045        |*$18,168*                 |14%               |1.14                 |
|**Average**  |                          |                       |**$20,976**               |                  |                     |

### 2.3.5 Considerations
-	In addition to submittal compliance criteria, will need a timeframe component when assessing a town's eligibility for a per parcel payment (likely annual). Some towns are technically “compliant” and are working with a vendor but have not submitted an update to VCGI since before 2020. For small towns that may not have any changes from year to year (and therefore do not submit an update), VCGI should still receive an annual confirmation that no changes or updates are needed to the existing data.
-	Consider possible tiered system for payments to encourage compliance. E.g.: Fully compliant or minor edit towns receive full amount, major edit town receive 50%, and non-compliant towns receive none.
-	Based on vendor discussions, it is not necessarily practical or feasible for vendors to directly use parcel data published by VCGI (e.g., vendors are not downloading the latest data for a town from VCGI prior to making their next round of edits). Often vendors are maintaining additional fields and formats beyond what is submitted and used by VCGI. This is likely a factor leading to repeated edits with each submission. Consider a way to summarize/communicate submission issues or edits that VCGI makes so vendors are aware and can correct for their subsequent submission, ideally without creating significant extra work for either VCGI or vendor. 

## 2.4 Example Statute Update

Text.

## 2.5 Implementation

Text.

# Recommendation 3: Implement Vermont CAMA Data Standard and Require Submittal to State
## 3.1 Summary
- Create Computer Assisted Mass Appraisal (CAMA) data standard based on fields from current CAMA software providers and input from the Tax Department, with applicability to current and future CAMA providers operating in Vermont
- Normalize 'priority fields' in initial standardization, expanding to additional fields in future phases
- Use stacked polygons for representing and accounting for unlanded structures and common interest parcels
- Improve attribution of unlanded structures and common interest parcels via prefix codes
- Require monthly submittal of CAMA data, or provide read-only source, adherent to the VT CAMA data standard to the State of Vermont
- Make submitted CAMA data publicly available and relatable with parcel map data

## 3.2 Justification
These recommendations are intended to provide useful property description information to aid timely and accurate reappraisals, while also supporting key public policy concerns (e.g., housing) that are best served by CAMA data. The recommendations are also intended to improve access to and use of public information for data analysis and visualization. Linking standardized CAMA information with existing GIS data, namely parcels, will further enhance visual and spatial data analysis and accessibility.

## 3.3 Data Management

### 3.3.1 Design and Implement VT CAMA Data Standard
Four CAMA software providers [operate in Vermont](https://tax.vermont.gov/municipal-officials/listers-and-assessors/district-advisors) as of October 2024:
- MicroSolve (NEMRC)
- ProVal (Aumentum)
- Vision Government Solutions CAMA
- AssessPro (Catalis, Formerly Patriot)

Based on sample data and documentation, all providers differ in how they collect, format, and organize CAMA data. VCGI recommends developing a standardized template and schema, including domains for applicable fields, with input and agreement from each vendor. In most cases, vendors should be able extract fields they are already collecting with little or no modification (or, ideally, provide VCGI with a read-only API). 

Following discussion with the VT Department of Tax, a phased approach for standardizing fields is the most feasible and realistic. The following fields comprise the first phase of standardization. All fields except 'SPAN' allow Null values.

|Type           |Field   |Alias   |Description                             |Field Type |Length |Example  |
|---------------|--------|--------|----------------------------------------|-----------|-------|---------|
|Identification|SPAN    |SPAN    |Unique identifier for record, with dashes |String     |13     |001-002-12345|
|History        |YearBuilt|Actual Year Built|Actual year built    |Integer |4 |1950|
|History        |YearReno|Year Renovated|Year of most recent renovation|Integer|4|2003|
|Building|TotFinSqFt|Total Finished Square Feet|Total finished square footage of structure|Decimal|10|4500|
Building|Heat1ID|Primary Heat/Cool Source|Primary heat/cool source, corresponding with following field|String (domain) |30|Heat Pump|
|Building|Heat1Pct|Primary Heat/Cool Source Percent|Percentage of usage of primary source for heating/cooling the structure|Percent (integer)|3|75|
Building|Heat2ID|Secondary Heat/Cool Source|Secondary heat/cool source, corresponding with following field|String (domain) |30|Forced Air|
|Building|Heat2Pct|Secondary Heat/Cool Source Percent|Percentage of usage of secondary source for heating/cooling the structure|Percent (integer)|3|25|
|Building|TotRooms|Total Rooms|Total count of rooms|Integer|5|10|
|Building|Bdrms|Bedrooms|Total count of bedrooms|Integer|5|3|
|Building|FullBths|Full Baths|Total count of full bathrooms|Integer|5|1|
|Building|ThrQtBths|Three Quarter Baths|Total count of three quarter bathrooms|Integer|5|0|
|Building|HalfBths|Half Baths|Total count of half bathrooms|Integer|5|1
|Building|Ktchns|Kitchens|Total count of kitchens|Integer|5|1|
|Building|PctCmplt|Percent Complete|Percent of structure that is complete|Integer|3|100|
|Building|UnitCnt|Unit Count|Count of inhabitable units within structure|Integer|5|1|
|Building|StoryCnt|Story Count|Total count of stories within structure|Integer|3|2|
|Building|UnlndCode|Unlanded Code|Prefix for unlanded structure type if applicable|String (domain)|2|Null|

*Revisions to proposed schema: used 'Heat1ID' as combination of HeatID and Heat/Cool fields as originally proposed; added 'Heat2ID' and 'Heat2Pct' in case of multiple heat sources. Added 'Three Quarter Baths' field. Used 'Year Renovated' in place of 'Effective Year Built' or similar.

**Heat source domains, per NEMRC (verify, potentially revise)**: Forced Air, Air Oil, Space Heater, Electric Radiator, Electric Baseboard, Hot Water Baseboard, WrmCool(?), Heat Pump, Exp Cool(?), Air Exchange, Gravity Furnace, Individual Unit, Hot Water Radiator.

**Unlanded code domains**: CO (condominium), CA (camp), MH (landed or unlanded mobile home), SA (ground mount solar array), WT (wind turbine)

All or most of these fields are present in the sample data/schema provided by three of the four CAMA vendors. 

### 3.3.2 Implement Changes to Parcel Definition in CAMA Data

Existing CAMA data software solutions offer advanced data maintenance capabilities and should accommodate a parcel definition change to separate and sellable pieces of real estate. Data entry and maintenance practices will need to adjust to reflect these changes.

### 3.3.3 Normalize Actual Year Built, Effective Year Built, and Unit Count Information

Consistent definitions and formatting for actual year built, year renovated, unit count, and story count should be established for all CAMA vendors. While each of these fields appear to exist within the current schema for each vendor, it is essential that all are evaluated using the same methodology and definition.

### 3.3.4 Normalize Attribution and Mapping of Unlanded Structures and Common Interest Parcels

The [stacked polygons method](#stacked-method---recommended) is the current and continuing recommendation for representing unlanded structures and common interest parcels, per the Vermont GIS Parcel Data Standard. Alternative methods are described in Appendix 3.3. 

To improve the functionality of using stacked polygons to represent unlanded structures and common interest parcels, the following recommendations should be considered: 

1. The Vermont GIS Parcel Data Standard defines an unlanded structure as a “condominium unit, mobile home, camp, or other building that is a unit of real estate which is separate from the underlying land surface.” Condominiums represent the vast majority of unlanded structures reflected in statewide parcel data, but a comprehensive list of different types of unlanded structures and common interest parcels should be developed for uniform attribution in CAMA and Grand List records. 
   
2. The list below can be used to differentiate between unlanded structures and common interest parcels in the parcel polygons layer, and if uniformly applied in CAMA and Grand List attribution, can be filtered for each record. Each unlanded structure or common interest parcel can be represented as a prefix of two letters:

| Prefix Code | Applies To                |
|-------------|---------------------------|
| CO          | Condominiums              |
| CA          | Camps                     |
| MH          | Mobile Homes              |
| SA          | Ground-Mount Solar Arrays |
| WT          | Wind Turbines             |

3. While not the intended purpose, the SOURCENAME field in the parcel polygon layer can also be used to track prefix codes without the need to revise the schema. This is most applicable for mapping vendors who have already established workflows including conforming to the Vermont GIS Parcel Data Standard.

4. Prefix codes can also be used to create GIS SPANs in the Intersection Table based on the type of unlanded structure or common interest parcel. The same two-letter system described above can be implemented followed by the town code (first three digits of the town SPAN) and a four-digit sequential numeric count (e.g., CO-003-0001, MH-003-0002, CO-003-0003, CO-003-0004, etc.).

5. Tax Department guidance on attribution of unlanded structures should be updated and made uniform to reflect the prefix codes and mapping practices (e.g., in the [Lister and Assessor Handbook](https://tax.vermont.gov/sites/tax/files/documents/GB-1143.pdf)).

## 3.4 Submittal Requirement

CAMA data are the best source of information for detailed and current property descriptions statewide. Standardizing these data and requiring their submittal to the State of Vermont for regular and uniform publication, particularly when combined with existing parcel data, will aid improved pace and accuracy of appraisals, facilitate data visualization and trend analysis, and increase data accessibility. Without a submittal requirement for CAMA data it is likely the dataset will become fragmented, incomplete, or stale over time. VCGI's Parcel Program, for example, is a voluntary program with data ranging from less than six months to over six years old, despite the widespread visibility, utility, and value of parcel data. 

Ideally, CAMA vendors will provide VCGI with access to a read-only, credentialed API service endpoint for the transfer and extraction of CAMA data. VCGI will work with CAMA vendors to ensure compatibility with the data standard and schema. In the absence of a service endpoint, vendors should submit standardized CAMA directly to VCGI. In either case, updated data should be made available and/or submitted on a monthly basis for the dataset to remain complete and current. 

Following receipt of the updated CAMA data each month, VCGI will work to incorporate the fields listed in Section 3.2.1 in the [Parcel Viewer](https://experience.arcgis.com/experience/b5a5cc7663c84761a305f70b913e1a60) and [Geodata Portal](https://geodata.vermont.gov/). In the Parcel Viewer, users will be able to access CAMA data easily and in relation to existing parcel, Grand List, and Property Transfer data. The comprehensive, tabular CAMA dataset will be available publicly for download through the Geodata Portal. 

## 3.5 Example Statute Update
>[Section] "Assessor database" means the database of property information maintained by a municipalities' lister(s) or assessor(s); it is also referred to as a Computer Aided Mass Appraisal (CAMA) system or Computer Aided Mass Appraisal database

>[Section] On or before [initial date], and not less than monthly thereafter, each municipality that possesses or contracts for services for the creation or maintenance of an assessor database shall transmit an extract of the database to [the State of Vermont]. The submitted database shall include, but need not be limited to information that uniquely identifies each property in the municipality, the description of each property, the size of each property, the year in which buildings were constructed on each property, and other fields described in the Vermont CAMA data standard.

# Recommendation 4: Clarify Right-of-Way Mapping for Tax Purposes

## 4.1 Summary
- Create guidance for treatment of the area between road centerline and edge of right-of-way for taxation purposes
- Promote mapping guidance specifying that parcels should be mapped to the edge of the right-of-way, not the road centerline

In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and its relation with parcel mapping. Common, practical experience is that public rights-of-way such as roads and highways are just that—areas not to be obstructed by abutting private property owners--be they owned in fee or easements. State highways, for example, often involve the State purchasing lands between the road centerline and abutting parcel, whereas towns may not. These differences contribute to a lack of clarity about how to account for the area that is within a right-of-way and between an abutting private parcel and road centerline and have occasionally led to differences in their depiction and resulting acreage calculations. The Tax Department, with aid of partners, should develop and offer guidance for considering these areas with regard to taxation and related acreage calculations.

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

# Recommendation 7: Pilot Remotely-Sensed Tools to Support Appraisals

Text.

# Recommendation 8: Develop and Offer Updated Parcel Contract Guidance

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

# Recommendation 12: Make Proposed Assessment Districts Consistent and Compatible with Existing Administrative Boundaries

Text.

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

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defined parcel. This is a "contiguous" parcel definition. Separate parcels are grouped together by ownership for administrative purposes.

Depicted visually, a contiguous parcel definition means that the two abutting parcels below, shown split with a dotted green line and both of which have the same owner, are drawn as the single outer rectangle. This results as one "parcel" in the spatial data layer.

![image](https://github.com/user-attachments/assets/239c3a7e-e6f5-44cd-bb89-e8768e81a1da)

One of the individual parts is to be considered an "inactive" parcel, but this is not uniformly tracked across towns. The other part is to be considered "active", but its status is also not tracked uniformly across towns. These result in data incompleteness that impact analysis as well as long-term change tracking.

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

There is no statewide subdivision requirement in Vermont, and not all municipalities require subdivisions. Thus, several instruments may be relied upon to help define a parcel (deed, subdivision plat where required by municipality, or property transfer / sale).

### A1.6 Separate Mapped Unit, Defined by Combination 

Any combination of the examples above.

### A1.7 Proposed Parcel Layers and VT GIS Data Standard Schema, per Updated Parcel Definition

VCGI currently publishes and maintains two statewide parcel layers: Active Parcels and Inactive Parcels (as available). Following a change to the parcel definition, VCGI will continue to publish and maintain two layers, but with slightly modified purpose, content, and schema. The following describes the existing and proposed statewide parcel data layers:

#### 1. Active Parcels --> Administrative Parcels

|Criteria  |Existing                    |Proposed                       |
|:---------|:---------------------------|:------------------------------|
|Name      |Active Parcels              |Administrative Parcels         |
|Purpose   |Primary statewide parcel layer. Groups contiguous separate lots by common ownership to single parcel polygon, conforming to current parcel definition. Included for all municipalities. |Secondary statewide parcel layer. Continues to group separate lots by common ownership to facilitate tax administration, but does not represent new parcel definition of separate and sellable lots. Included for all municipalities. |
|Schema|- SPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area<br>|- ADMINSPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area|

Schema change for the Administrative Parcels layer is renaming "SPAN" to "ADMINSPAN". The ADMINSPAN is the common identifier for all contiguous lots with the same ownership. SPANs for other individual lots within an Administrative Parcel are not included in this layer.

#### 2. Inactive Parcels --> Parcels

|Criteria  |Existing                    |Proposed                       |
|:---------|:---------------------------|:------------------------------|
|Name      |Inactive Parcels            |Parcels         |
|Purpose   |Secondary statewide parcel layer. Splits contiguous active parcels with common ownership into individual lots where applicable. Included for approximately two-thirds of municipalities. |Primary statewide parcel layer. Depicts parcels as separate and sellable lots or pieces of real property, regardless of contiguous ownership. Conforms to proposed new parcel definition. Included for all municipalities. |
|Schema|- STATUS<br> - PARENTSPAN<br>- SPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area<br>|- ADMINSPAN<br>- SPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area|

Schema changes for the Parcels layer are removing the "STATUS" field and renaming "PARENTSPAN" to "ADMINSPAN". The ADMINSPAN is the common identifier for all contiguous parcels under the same ownership; this field can contain duplicates and can be used to aggregate parcels to the Administrative Parcel layer. The SPAN is the unique identifier for each separate and sellable lot (i.e., a parcel under the proposed new definition); this field should not contain duplicates. In many cases, and all instances where a parcel has no neighbors with the same owner/tax bill, the ADMINSPAN and SPAN fields will be the same. 

![AdminSPANs_SPANs](https://github.com/user-attachments/assets/cbb220fb-17ba-4a2a-bafb-6918cb4d5024)

### A1.8 Parcel Definitions and Interpretations in Existing Vermont Statute

This section lists existing Vermont statutes that define or interpret a definition of a parcel and/or have eligibility requirements dependent on such definition. It does not list those statutes that use the term "parcel" as an identifier to clarify an idea or specify the location or applicability of what is being discussed without area requirements, unless otherwise noted.

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

### A2.1 Shared Responsibility Model
The notable success of the Parcel Program as a voluntary-based initiative is due to the collaboration between municipalities, state government, and mapping vendors in the private sector. This "Shared Responsibility" model relies on all collaborators contributing resources to maintain statewide parcel data.

![image](https://github.com/user-attachments/assets/57368cfe-eb6c-47b7-99ad-66c17cb00e3d)

This graphic representation of the Shared Responsibility model identifies one attribute: a municipality's ability to preform parcel geometry updates by contracting with a mapping vendor or doing updates internally. Municipalities unable to preform parcel geometry updates currently receive irregular updates by VCGI as land surveys that can be used to update a municipality's parcel geometry are submitted to the [Vermont Land Survey Library](https://landsurvey.vermont.gov/).

### A2.2 Funding during the Parcel Project
The Parcel  Project (2017-2019) leveraged both state and federal funds with 80 percent coming from the Federal Highway Administration and the remaining 20 percent from several state agencies and departments. The Vermont Agency of Transportation contracted with several mapping vendor to update or create digital parcel data for each Vermont municipality over a three-year period. Each mapping vendor was assigned to a municipality through a competitive bid process. 

The average cost per parcel for the 67 municipalities completed during the first year of the Parcel Project in 2017 (excluding unincorporated towns and gores) was $6.85 which is slightly more than the national average of $5.20 reported 10 years prior by the National Research Council in *National Land Parcel Data: A Vision for the Future* (2007). The cost per parcel for municipalities completed during the first year of the Parcel Project (excluding unincorporated towns and gores) is depicted below.

![Parcel Project Year 1 Table](https://github.com/user-attachments/assets/cb114846-6a1b-45c1-89b4-f7a8833b9981)

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

### A3.3 Mapping of Unlanded Structures and Common Interest Parcels
**Background** 

Statewide standardized parcel data in Vermont is currently comprised of parcel geometry, the approximate parcel boundary lines drawn as closed multi-sided shapes (parcel polygons) as sourced from municipalities, and parcel attribution from the annual Grand List collected and published by the Tax Department. These two components are joined together by a matching School Property Account Number (SPAN) in the attribute table of the parcel polygons layer and in the Grand List. In most cases, each polygon is joined to one Grand List record but it is not uncommon for more than one Grand List record to be joined to the same polygon. This happens most often with condominiums as they are typically described by their percentage of undivided interest in the common area and facilities rather than discrete boundaries that can be easily represented by polygons. While VCGI has provided some guidance on mapping condominiums per the Vermont GIS Parcel Data Standard, a more comprehensive recommendation for mapping all types of unlanded structures is necessary to improve data quality, clarity, and ease of use.

#### A.3.3.1 Current Unlanded Structure and Common Interest Parcel Mapping Practices in Vermont

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

This creates identical polygons "stacked" on top of each other, which can be “flattened” to remove all but one polygon for each parcel for analytical purposes. Unlike the building footprints methods, there is no visual distinction between unlanded structures and the common land. Because of this, parcel geometry is simpler to maintain.

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

In 2023 over 19,000 parcels were enrolled in Current Use, totaling over 2.5 million acres statewide. [Explore parcels enrolled in Current Use](https://arcg.is/1vXL4u1).

![CU](https://github.com/user-attachments/assets/c43d6573-861f-4f47-9e32-6099e8c4bf77)

*Figure X: Parcels enrolled in Current Use statewide.*

![CUenrolled](https://github.com/user-attachments/assets/761ac768-286c-44b2-9587-e25a507ea362)


### X.X Lands in Current Use Needing Administrative Definition for Acreage

A change to the parcel defintion would have impacts on parcels enrolled in [Current Use](https://tax.vermont.gov/property/current-use/property-types). A primary requirement for eligibility is at least 25 acres of contiguous land in active agricultural use or forested land managed to state standard and an approved forest management plan. Parcels containing inactives and enrolled in Current Use may become eligible based on acreage if a parcel is defined by separate and sellable pieces of real estate rather than by common ownership. In the example below, the green parcel contains four inactive parcels; the "ACTIVE" status parcel is 70.64 acres, however, so this parcel would still be eligible for Current Use. The red parcel, however, is comprised of two inactives where the "ACTIVE" status parcel is 10.28 acres. As such, it would no longer be eligibile for Current Use based on acreage. This example also highlights the implications associated with which parcel receives the "ACTIVE" status. Brown parcels are enrolled in Current Use but do not contain inactive(s). The eligibility of these parcels for Current Use would not be impacted by a change to the parcel defintion. [Explore parcels enrolled in Current Use](https://arcg.is/1vXL4u1) and potential eligibility impacts associated with a change to the parcel definition.

![CU_ActiveInactive](https://github.com/user-attachments/assets/5b8af80f-80aa-4dd3-811c-c13f350bfc14)

*Figure X: Example of parcels enrolled in Current Use and containing inactive parcels (red and green). Based on the status of a parcel ("ACTIVE" or "INACTIVE") and the acreage, eligibility for Current Use could be impacted with a change to the parcel definition. The acreage eligibility for parcels enrolled in Current Use and without any inactives (brown parcels) would not be impacted by a change to the parcel defintion.*


Examining Current Use parcels with inactives statewide, the following impacts are seen by town:

![Inactives_CU](https://github.com/user-attachments/assets/16d095e6-ec20-405c-b295-f8a07145bd24)

*Figure X: Count of parcels with at least one inactive parcel and enrolled in current use (2023), by town.*

Total bar count represents parcels per town enrolled in Current Use and with at least one inactive. Green count represents parcels whose parent parcel is >25 acres, deeming the parcel still eligible for Current Use under the new parcel definition. Red count represents parcels whose parent parcel is <25 acres and therefore no longer eligible for Current Use based on acreage. 


![image](https://github.com/user-attachments/assets/0364e196-1b06-429d-8f6b-58178a1cd86c)

*Table: Count and percentage of parcels with at least one inactive parcel and enrolled in current use, by town. Approximately 32% of parcels statewide would lose their eligibility for current use based on acreage following a change to the parcel definition.*


Note: inactive parcels are not managed consistently across towns; currently 178 towns (70%) submit inactive parcels. In addition, attribution of the parcel status field (active/inactive) is not complete or consistent for all submitting towns. This analysis is based on a subset of 138 towns with inactives and a presumably accurate "STATUS" field. This means the parent parcel has an "ACTIVE" status and all associated "INACTIVE" status parcels have a PARENTSPAN matching the "ACTIVE" status SPAN. 

![ActiveInactive](https://github.com/user-attachments/assets/9ebd72bc-9f34-4c54-aa2a-e930529b9803)

*Table X: Example of correct attribution in the inactive parcel layer. The parcel with an "ACTIVE" status has a SPAN entry, followed by the associated "INACTIVE" status parcels with PARENTSPAN entries linking them to the "ACTIVE" parcel. In the Active Parcels layer, these five parcels would be merged to a single parcel. In some cases, "INACTIVE" status parcels may also include a unique SPAN entry. Typically these are placeholders used by town officials.*




### X.X Acreage in Right-of-Way

Correct mapping of Rights-of-Way has important implications for taxation purposes. Based on the parcel data, over 133,000 acres in Vermont are classified as a Right-of-Way. [Explore ROW Acreage by Town here](https://arcg.is/1qLPXv1) and in the images below. Acreage is based on the sum of parcels by town where the Property Type is classified as "ROW_ROAD", "ROW_RAIL", or "ROW_TRAIL". The second image provides an example of each ROW.  

Note: while the majority (96%) of municipalities include ROWs, a small number do not. Parcels in these towns are generally mapped to centerlines where ROWs are missing. These municipalities include:

- Averill (only main roads)
- Bloomfield (only main roads)
- Eden (few road fragments)
- Johnson (only in town center)
- Norton (only main roads)

In addition, ROWs for the following municipalities are typically missing or incorrectly attributed when updated data are sent to VCGI: Canaan, Royalton, Saint Albans Town, West Windsor, and Wolcott. ROWs for these municipalities can often be restored, however, using the existing data. 


![ROW_acreage](https://github.com/user-attachments/assets/cd87c576-58a5-443e-8a3b-a31288008565)

*Figure X: ROW acreage displayed by town, as summed for all parcels with a Property Type of ROW_Road, ROW_Rail, or ROW_Trail. Total statewide ROW acreage is 133,150 acres, average per town is 522 acres, maximum is 1,883 acres (Randolph), and minimum is 16 acres (Avery's Gore).*

![ROW_zoom](https://github.com/user-attachments/assets/6c4da9a4-2798-4ad9-89b9-ee3a0a5ff5e4)

*Figure X: Example of parcels with Property Type of ROW_Road (grey), ROW_Rail (red), and ROW_Trail (green) in Ferrisburgh.*


### X.X Acreage Not Counted (Gaps) and Duplicately Counted (Overlaps)
![WinooskiTopology_example](https://github.com/user-attachments/assets/c94e43ea-2df6-4d89-9d60-a22c4a7c611b)

*Figure X: Example of gaps (red) and overlaps (blue) between parcel geometry at municipal boundaries between Winooski and bordering South Burlington, Burlington, and Colchester. Black lines repersent town boundaries as reflected in the [town boundary dataset](https://geodata.vermont.gov/datasets/VCGI::vt-data-town-boundaries-1/about) maintained by VCGI.*

### X.X Acreage in Common Ownership
![CommonOwnership_statewide](https://github.com/user-attachments/assets/2eecb05d-b610-4d0c-97e0-ab4c7a197e55)

*Figure X: Statewide distribution of common ownership or "stacked" parcels where more than one grand list record is assigned to the same parcel feature.*

![CommonOwnership_Brattleboro](https://github.com/user-attachments/assets/9580c23e-579e-41fe-aa55-b9fc13aa058b)

*Figure X: Stacked parcels in Brattleboro repersenting a mobile home park.*

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
