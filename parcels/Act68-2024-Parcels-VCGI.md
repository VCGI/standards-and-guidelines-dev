![Act68_Part_II_Report_Cover_Slide_HigherRes](https://github.com/user-attachments/assets/ded4f679-6fe5-4367-8823-95fd213417d8)

# Purpose

This document outlines all recommendations for parcel mapping and data maintenance as related to [Act 68 of 2023](https://legislature.vermont.gov/bill/status/2024/H.480). It is authored by the Vermont Center for Geographic Information (VCGI), state stewards of the [Statewide Property Parcel Mapping Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) since 2020, established via [19 V.S.A. § 44](https://legislature.vermont.gov/statutes/section/19/001/00044). The recommendations aim to improve parcel data quality to support timely, fair, accurate, and modern property valuation and reappraisals as sought by Act 68, which [asks the Tax Department to](https://legislature.vermont.gov/Documents/2024/Docs/ACTS/ACT068/ACT068%20Act%20Summary.pdf):

> [create] recommendations and considerations for distinguishing between different types and characteristics of property and their uses, and how different property data could be used to make policy decisions.

# Overview of All Recommendations

| **Recommendation**                                                                      | **Statute Change** | **Incentive / Funding** | **Technical Guidance** | **New Technology** |
|:---------------------------------------------------------------------------------------:|:------------------:|:-----------:|:----------------------:|:------------------:|
| [1. Update Parcel Definition in Vermont Statute](#recommendation-1-update-parcel-definition-in-vermont-statute)                                              | X                  |             |                        |                    |
| [2. Support Digital Parcel Maintenance and Submittal to the State](#recommendation-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont)          | X                  | X           |                        |                    |
| [3. Implement Vermont CAMA Data Standard and Require Submittal to State](#recommendation-3-implement-vermont-cama-data-standard-and-require-submittal-to-state)                       | X                |             | X                      |                    |
| [4. Clarify Right-of-Way Mapping for Tax Purposes](#recommendation-4-clarify-right-of-way-mapping-for-tax-purposes)                         |                   |             | X                       |                    |
| [5. Clarify Grand List vs. GIS Acreage Guidance](#recommendation-5-clarify-grand-list-vs-gis-acreage-guidance)                                          |                    |             | X                      |                    |
| [6. Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract](#recommendation-6-acquire-and-publish-annual-high-resolution-imagery-and-offer-buy-up-imagery-contract) |                    |             | X                      | X                  |
| [7. Pilot Remotely-Sensed Tools to Support Appraisals](#recommendation-7-pilot-remotely-sensed-tools-to-support-appraisals)                                    |                    |             |                        | X                  |
| [8. Develop and Offer Updated Parcel Contract Guidance](#recommendation-8-develop-and-offer-updated-parcel-contract-guidance)                  |                    |             | X                      | X                  |
| [9. Modernize Current Use Map Standards, Submittals, and Access](#recommendation-9-modernize-current-use-map-standards-submittals-and-access)                                   |                    |             |                        | X                  |
| [10. Consider Updating and Moving Parcel Program in VT Statute](#recommendation-10-consider-updating-and-moving-parcel-program-in-vt-statute)                           | X                  |             |                        |                    |
| [11. Coordinate With Concurrent Efforts to Digitize Land Records](#recommendation-11-coordinate-with-concurrent-efforts-to-digitize-land-records)                         |                   |             |                        | X                   |
| [12. Make Proposed Appraisal Districts Consistent and Compatible with Existing Administrative Boundaries](#recommendation-12-make-proposed-appraisal-districts-consistent-and-compatible-with-existing-administrative-boundaries)                         |                   |             | X                        |                    |

| **Additional Recommended Improvements**                              |
|----------------------------------------------------------------------|
| [Improve Submittal of Land Surveys to the Vermont Land Survey Library](#improve-submittal-of-land-surveys-to-vermont-land-survey-library) |
| [Support Survey of Municipal Boundaries and/or Corner Points](#support-survey-of-municipal-boundaries-andor-corner-points)          |

# Recommendation 1: Update Parcel Definition in Vermont Statute
## 1.1 Summary
- While functional for tax administration, the current parcel definition has limitations for valuation, data management, complete documentation, and parcel-dependent analysis that informs policy
- Changing the current parcel definition from solely "contiguous" to one that also requires tracking of separate and sellable pieces of real estate should help overcome these issues
- This definition would replace the undefined practice of mapping and tracking "inactive" parcels and instead require mapping and tracking all separate parcels individually, regardless of common ownership
- "Contiguous" parcels aggregated by common ownership are still to be created for the purposes of tax administration
- Two parcel map layers will continue to be published via the Statewide Parcel Program: one for tax administration (formerly known as "active parcels"), and one for tracking all parcels separately (formerly known as "inactive parcels")

## 1.2 Justification
Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defines a parcel as:
> (3) A brief description of each parcel of taxable real estate in the town. “Parcel” means all contiguous land in the same ownership, together with all improvements thereon.

This is a "contiguous" parcel definition, depicted in Figure 1. Separate lots are grouped by ownership for administrative purposes, including the sending of a single tax bill per owner per "parcel". Separate lots are sometimes managed as "inactive" parcels, but that term is not defined outside of the [parcel data standard](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) and maintenance varies by town. The marketability of individual lots for sale is not clear, nor is it clear is how towns should map and track lots within a combined parcel. Aggregate parcel delineation further complicates assignment of highest and best use valuation as assessors may have to generalize across several different lot types. Data management, change tracking, and downstream analysis are also negatively impacted by a contiguous parcel definition.

![Parcel Types Diagram For Statute Change_v4d-01](https://github.com/user-attachments/assets/6f5e420e-9a2f-45b7-8fe7-40772bb5a618)
**Figure 1: Current and Proposed Parcel Definition.** *The proposed separate parcel definition removes the need for tracking "inactive" parcels, while ensuring all component parts of parcels are assigned a unique identifier.*

Defining parcel instead as a separate and sellable lot or piece of real property would bring parcel identification in line with their common understanding as "lots" as opposed to grouped areas. This definition would would improve parcel documentation by ensuring that no parcel in full or in part goes unidentified; ease highest and best use valuation by reducing the need to generalize across different parcels; improve data maintenance, long-term record keeping, and analysis; and continue to allow aggregation by owner for tax administration. In addition, the definition of a parcel has implications for any potential fee or payment related to a municipality's parcel count (see [Recommendation 2](#recommendation-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont)).

An updated parcel definition could allow a legal document (deed or title), subdivision plats, or sale to help define the bounds of the separate mapped and tracked area. Existing "inactive" parcels, where they exist and are maintained, should be tracked and mapped with their unique SPAN and attribution. These parcel would ultimately be incorporated with the current "active" parcel layer to create a map layer of the smallest, documented, bounded sellable areas. A separate parcel layer combining parcels on ownership should persist for tax administration (such as current use enrollment). Two statewide parcel map layers would result, one that reflects documented, bounded, sellable pieces of real estate, and the other that represents contiguous parcels combined on ownership. Both layers would continue to be published and made publicly available by the Statewide Property Parcel Program.

These changes in parcel definition and mapping practices would increase the current count of parcels statewide from roughly 340,000 to an estimated 380,000. This figure is estimated since only 70% of towns (178 total) currently submit their inactive parcels digitally to VCGI. It remains unknown how many of the remaining 30% of towns map inactive parcels digitally. This definition change could be designed to require no changes to current use and other programs dependent on acreage thresholds that may only be met by aggregating lands in common ownership (see [Recommendation 9](#recommendation-9-modernize-current-use-map-standards-submittals-and-access)).

## 1.3 Example Statute Update

> 32 V.S.A. § 4152 (a)(3) A brief description of each parcel of taxable real estate in the town. “Parcel” means <ins>a separate and sellable lot or piece of real estate. Parcels are to be combined to represent</ins> *all contiguous land in the same ownership, together with all improvements thereon* <ins>for tax administration.</ins>

## 1.4 Related Statutes

See [Appendix A1.5 Parcel Definitions and Interpretations in Existing State Statute](#a15-parcel-definitions-and-interpretations-in-existing-vermont-statute). 

## 1.5 Implementation

Vermont municipalities would be expected to continue to aggregate parcels by common ownership and account for them as they do currently. An aggregate, "contiguous" map layer reflecting this accounting would still be submitted to the Statewide Property Parcel Program overseen by VCGI, and remain adherent to an updated VT GIS Parcel Data Standard. The layer will be renamed from "active" parcels to "administrative" parcels by VCGI. SPANs for administrative parcels would be maintained in a field called ADMINSPAN, and match the source ADMINSPAN of abutting lots under the same ownership (see Figure 1 and [Appendix 1.4](#a14-proposed-parcel-layers-and-vt-gis-data-standard-schema-per-updated-parcel-definition)). When a parcel has only one bounded area in common ownership, its ADMINSPAN would be the same value as its SPAN. CAMA providers would be engaged to reflect these changes in their accounting systems.

Municipalities would also be expected to account for what are currently called "inactive" parcels. These parcels would reflect the updated parcel definition and depict separately sellable pieces of real estate given their best available documentation, and regardless of common ownership. This practice is compatible with at least one parcel map vendor's current practices in Vermont (see [Appendix 1.2: Comments on Maintaining Inactive Parcels at the Municipal Level](#a12-comments-on-maintaining-inactive-parcels-at-the-municipal-level)). Representative spatial data are to remain adherent to an updated VT GIS Parcel Data Standard, albeit "inactive" parcels are to be renamed to simply "parcels". This layer will be submitted to the State Property Parcel Program overseen by VCGI, who will rename the current "inactive" parcels layer as "parcels".

VCGI will send advance notice of these changes to the VT GIS community, municipalities, and their mapping vendors. It is expected that mapping and tracking of parcels that reflect an updated parcel definition will take time and improve with continued maintenance.

A full description of proposed changes is in [Appendix 1.4: Proposed Parcel Layers and VT GIS Data Standard Schema, per Updated Parcel Definition](#a14-proposed-parcel-layers-and-vt-gis-data-standard-schema-per-updated-parcel-definition).

![Woodstock_Inactives_Labels](https://github.com/user-attachments/assets/fd77e797-1a94-4419-9131-cc8536f4a266)
**Figure 2: Example of Current Practices for Mapping Inactive Parcels.** *Inactive parcels are tracked differently depending on municipality. Woodstock and Hartford, for example, currently manage inactive parcels and provide them to VCGI while Hartland, Pomfret, and Bridgewater do not. For the latter towns it is unknown whether inactive parcels are only managed internally or not at all.*

# Recommendation 2: Support Digital Parcel Maintenance and Submittal to the State of Vermont
## 2.1 Summary

- The current model of town-based parcel maintenance with voluntary submittal to the state has reached its limits in data quality and currentness
- If municipalities are to remain responsible for reappraisals, grand list maintenance, and tax mapping, any additional per-parcel funding should be contingent on the submittal of standardized GIS parcel data to the state
- Any change in the jurisdiction responsible for tax assessments/reappraisals should be accompanied by corresponding adjustments to the processes, responsibilities, and resources for tax mapping to ensure statewide consistency and accuracy 

## 2.2 Justification

Vermont has 256 municipalities: 237 towns, 10 cities, 5 unincorporated towns, and 4 gores. In Vermont individual municipalities are responsible for parcel mapping of taxable lands in their jurisdiction, unlike other states with county governments that often oversee the task. Most towns budget to hire a GIS vendor to maintain their digital parcel data and reflect any changes to parcel geometry since the town's last update. Frequency of geometry updates varies depending on the needs and resources of the town, with some updates performed annually and others completed every two to three years or more. Some towns do not update their digital parcel geometry. Town oversight of parcel mapping is typically the responsibility of listers or assessors. Accuracy of taxation and identification of land-based and parcel-related trends suffer without a tight relationship between grand list and map maintenance.

The [Statewide Property Parcel Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) publishes municipal parcel map data joined to the annual statewide grand list in a uniform, digital format (see [Glossary: VT GIS Parcel Data Standard](#vermont-gis-parcel-data-standard)). The Program relies on towns voluntarily sharing updated parcel geometry with VCGI, typically via their vendor (see [Appendix 2](#a21-current-shared-responsibility-model-town-maintenance)). VCGI reviews submissions, performs any edits required for standard compliance, and makes the data publicly available with [enhanced functionality](https://github.com/VCGI/documentation/blob/main/parcelviewer4/User_Guide.md). The data drive applications such as the [Vermont Parcel Viewer](https://maps.vcgi.vermont.gov/ParcelViewer/), which draws more than 500,000 unique views a year, and are also provided as raw spatial data which sees over 1 million unique views a year. Parcel data are one of the state's most-used spatial datasets.

This voluntary method of sourcing parcel data has supported state, regional, and local efforts in emergency management, natural resources policy and planning, permitting and compliance, and transportation. Parcel data also support efforts to address pressing issues such as flood response, resilience planning, and housing. All municipalities may use these data and applications to display their parcels digitally and free of charge. Some towns pay vendors for additional map services such as custom web applications and print map production. The overarching incentive for municipal parcel data maintenance is for towns to ensure the most accurate, consistent, and timely data exist across all representations of land ownership and location, be that in grand list tables or on maps that see high use.

While relatively successful, improvements are needed in the current town-sourced model of parcel data maintenance and publishing. About 60% of municipalities have submitted updated parcel geometry to VCGI within the last year. In contrast, about 16% of municipalities have not submitted updated parcel geometry to VCGI in over three years, indicating a divide in participation in the Parcel Program and limitations to its voluntary model. Inaccurate, stale data impacts downstream uses that are now dependent on this information.

### 2.2.1 Submittal Status

VCGI tracks municipal parcel data maintenance and voluntary submittals in the [Parcel Program's Town Mapping Status application](https://maps.vcgi.vermont.gov/parcelstatus/), which is updated weekly. These statistics represent five years (2020 - 2024) of oversight of the Statewide Property Parcel Program. They highlight the need for improvements to the current data maintenance model.

As of October 24, 2024:
- **90%** of towns are edited/updated by vendors or the town. 10% do not maintain their data and receive limited edits/updates by VCGI
- **24%** of submissions are fully compliant with the current parcel data standard
- **76%** of submissions are not compliant with the data standard. Of these, 26% become compliant with minor edits, 37% become compliant with major edits, and 13% are unusable (see [Appendix 2.3: Submittal Quality Criteria](#a23-submittal-quality-criteria))
- **11%** of towns maintain digital parcel data but have not submitted an update since the original Parcel Project data (prior to 2020)
- **12%** of submissions are/have been reviewed by towns prior to submittal; 64% have not, and 24% are unknown

## 2.3 Implementation

The implementation of recommendations to support parcel data submissions is significantly influenced by the jurisdiction responsible for tax assessments. Any modifications to the current responsibilities should be accompanied by corresponding adjustments to the existing tax mapping practices within the state. It is crucial to continue the aggregation of parcels into a single standardized statewide layer as it has become critical information relied on by many policies, programs, and practices. These data are expected by most to remain available and useful as a fundamental public resource.

### 2.3.1 Scenario A: Continued Municipal Assessment Jurisdiction

The size and capacity of some small Vermont municipalities make it difficult to mandate that they maintain and submit standardized parcel data to the state without providing resources to help cover costs. Still, it is important to note that 90% of towns in Vermont currently maintain parcel data, either independently or through vendors.

Municipalities that do maintain parcel data should be required to adhere to the State's basic standard and submit their data to the state. This approach would mirror the adoption of Municipal Plans in Vermont, where towns are not mandated to adopt plans, but if they do, they must include provisions specified in [24 V.S.A. § 4382](https://legislature.vermont.gov/statutes/section/24/117/04382).

At the same time, adding new requirements for municipalities without new incentives may not significantly increase the number of towns maintaining and submitting standardized data. Therefore, it is recommended that this be done in tandem with the approach outlined in Act 68 Section 4. (3) (G):

> Incentivizing municipalities to submit grand list parcel map data to the Vermont Center for Geographic Information, including conditioning payment of higher per grand list parcel fees on the submission of data.

Increasing the per-parcel payment to municipalities, even marginally, could meaningfully increase the number of municipalities sharing quality data with the state.  Creating incentives to improve data maintenance and sharing was also a recommendation in the [2015 Vermont Statewide Digital Parcel Lifecycle & Maintenance Plan](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/VT_Parcel%20Data%20Lifecycle%20and%20Maintenance%20Plan_2015_FINAL.pdf):

> As implementation shifts into a maintenance stage, Vermont will want to pay close attention to challenges to compliance. While some impediments may be more attitudinal than logistical or economic, the state may want to consider creating incentives to comply.

New contract guidance could also be developed to ensure municipalities maintain quality data that are eligible for a per parcel payment (see [Recommendation 8: Develop and Offer Updated Parcel Contract Guidance](#recommendation-8-develop-and-offer-updated-parcel-contract-guidance)).

While such requirements and incentives are likely effective for most municipalities, they may not be significant enough for small municipalities that do not maintain parcel data. In such cases, those updates should be managed by VCGI's Parcel Program staff given available time and resources, including the [Vermont Land Survey Library](#improve-submittal-of-land-surveys-to-vermont-land-survey-library). 

Further considerations regarding per parcel payments are in [Appendix 2](#appendix-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont-considerations).

### 2.3.2 Scenario B: New Regional/State Assessment Jurisdiction

This scenario assumes the creation of regional assessment districts as discussed in part 1 of this report, representing a change from the current assessment jurisdiction of the municipality. An assessment jurisdiction is typically responsible for all of the components of assessing property for tax purposes, therefore the responsibility for tax mapping should also shift to that jurisdiction.

In Vermont, this could mean that all towns within the regional assessment jurisdiction are mapped under one contract, and likely by the same vendor. There may be advantages to this approach as the details and costs of the mapping contract could be met with contributions from all towns, while potentially enabling modern mapping to cover all towns statewide. Should this change occur, and assuming that the assessment jurisdiction is in some way related to the State's Tax Department, standardized parcel submittal to the state should become mandatory. The cumulative advantage from a mapping perspective is that all towns would be covered with uniform, up-to-date parcel data, which is supports many other uses beyond tax assessment.

Additional per parcel payments in this scenario would likely not exist as an additional payment to towns. Instead, parcel counts for the entire assessment jurisdiction could be used to tailor adequate funding to support the parcel mapping function of the district. Funding for these services may be comprised of a combination of state funds and those from towns in the district, with the relative amounts of each to be considered both within and across districts. Further considerations regarding funding are in [Appendix 2](#appendix-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont-considerations).

There are likely advantages to the use of a single CAMA system for each district which would also ease mapping and data maintenance. The management of land records in this scenario would need serious consideration. It is not clear how major inefficiencies could be avoided without progress in digital land records statewide (see [Recommendation 11](#recommendation-11-coordinate-with-concurrent-efforts-to-digitize-land-records)).

# Recommendation 3: Implement Vermont CAMA Data Standard and Require Submittal to State
## 3.1 Summary
- Create Computer Assisted Mass Appraisal (CAMA) data standard based on fields from current CAMA software providers and input from the Tax Department, with applicability to current and future CAMA providers operating in Vermont
- Normalize 'priority fields' in initial standardization, expanding to additional fields in future phases
- Use stacked polygons to represent and account for unlanded structures and common interest parcels
- Improve attribution of unlanded structures and common interest parcels via prefix codes
- Provide read-only source of CAMA data, or require monthly submittal, adherent to the VT CAMA data standard to the State of Vermont
- Make submitted CAMA data publicly available and relatable with parcel map data

## 3.2 Justification
These recommendations are intended to provide useful property description information to aid timely and accurate reappraisals, while also supporting key public policy concerns (e.g., housing) best served by CAMA data. The recommendations are also intended to improve access to and use of public information for data analysis and visualization. Linking select standardized CAMA information with existing GIS data such as parcels and spatialized property transfers will further enhance data analysis and parcel-dependent policy decisions.

## 3.3 Components

### 3.3.1 Design and Implement VT CAMA Data Standard
Four CAMA software providers [operate in Vermont](https://tax.vermont.gov/municipal-officials/listers-and-assessors/district-advisors) as of October 2024:
- MicroSolve (NEMRC)
- ProVal (Aumentum)
- Vision Government Solutions CAMA
- AssessPro (Catalis, Formerly Patriot)

Based on sample data and documentation, all providers differ in how they collect, format, and organize CAMA data. VCGI recommends developing a standardized template and schema, including domains for applicable fields, with input and agreement from all vendors. In most cases, vendors should be able extract fields they are already collecting with little or no modification (or, ideally, provide VCGI with a read-only API). 

Following discussion with the VT Department of Tax, a phased approach for standardizing fields is the most feasible and realistic. The following fields comprise the first phase of standardization. All fields except 'SPAN' would allow Null values.

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

**Table X: Proposed CAMA Data Schema.** *CAMA data schema for initial phase of data standardization. Following agreement with CAMA vendors, these fields should be made available to VCGI for inclusion in a statewide CAMA dataset.*

**Proposed heat source domains**: Forced Air, Air Oil, Space Heater, Electric Radiator, Electric Baseboard, Hot Water Baseboard, WrmCool, Heat Pump, Exp Cool, Air Exchange, Gravity Furnace, Individual Unit, Hot Water Radiator.

**Unlanded code domains**: CO (condominium), CA (camp), MH (landed or unlanded mobile home), SA (ground mount solar array), WT (wind turbine)

All or most of these fields are present in the sample data/schema provided by three of the four CAMA vendors. 

![CAMA_Example_Patriot_01](https://github.com/user-attachments/assets/29202d0a-44a5-4630-a220-b13f4a6bb563)

![CAMA_Example_Patriot_02](https://github.com/user-attachments/assets/dfc4c324-d4d9-47f9-9d5d-73ad8f9e13ba)
**Figure 3: Example of CAMA Data Sheet.** *CAMA data and documentation, as provided by AssessPro. Numerous fields exist beyond those in the initially proposed schema; fields available in the statewide dataset will expand over time using a phased approach.*

### 3.3.2 Implement Changes to Parcel Definition in CAMA Data

Existing CAMA data software offers advanced data maintenance capabilities and should accommodate a parcel definition change to separate and sellable pieces of real estate, per [Recommendation 1](#recommendation-1-update-parcel-definition-in-vermont-statute). Data entry and maintenance practices will need to adjust to reflect these changes.

### 3.3.3 Normalize Actual Year Built, Effective Year Built, and Unit Count Information

Consistent definitions and formatting for actual year built, year renovated, unit count, and story count should be established for all CAMA vendors. While each of these fields appear to exist within the current schema for each vendor, it is essential that all are evaluated using the same methodology and definition.

### 3.3.4 Normalize Attribution and Mapping of Unlanded Structures and Common Interest Parcels

The [stacked polygons method](#a331-current-unlanded-structure-and-common-interest-parcel-mapping-practices-in-vermont) is the current and continuing recommendation for representing unlanded structures and common interest parcels, per the Vermont GIS Parcel Data Standard. Alternative methods are described in [Appendix 3.3](#a33-mapping-of-unlanded-structures-and-common-interest-parcels). 

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

**Table X: Unlanded Structure and Common Interest Parcels Prefix Codes.** *Prefix codes should be used to signify parcel type where stacked parcel geometry exists in the parcel polygons dataset.*

3. Prefix codes can be used to create GIS SPANs in the Intersection Table based on the type of unlanded structure or common interest parcel. The same two-letter system described above can be implemented followed by the town code (first three digits of the town SPAN) and a four-digit sequential numeric count (e.g., CO-003-0001, MH-003-0002, CO-003-0003, CO-003-0004, etc.).

4. While not the intended purpose, the SOURCENAME field in the parcel polygon layer can also be used to track prefix codes without the need to revise the schema. This is most applicable for mapping vendors who have already established workflows including conforming to the Vermont GIS Parcel Data Standard.

5. Tax Department guidance on attribution of unlanded structures should be updated and made uniform to reflect the prefix codes and mapping practices (e.g., in the [Lister and Assessor Handbook](https://tax.vermont.gov/sites/tax/files/documents/GB-1143.pdf)).

## 3.4 Submittal Requirement

CAMA data are the best source of information for detailed and current property descriptions statewide. Standardizing these data and requiring their submittal to the State of Vermont for regular and uniform publication, particularly when combined with existing parcel data, will improve the pace and accuracy of appraisals, facilitate data visualization and trend analysis, and increase data accessibility. Without a submittal requirement for CAMA data it is likely the dataset will become fragmented, incomplete, or stale over time. The voluntary nature of the Parcel Program, for example, has resulted in data ranging from less than six months to over six years old, despite the widespread visibility, utility, and value of the program. 

Ideally, CAMA vendors will provide VCGI with access to a read-only, credentialed API service endpoint for the transfer and extraction of CAMA data. VCGI will work with CAMA vendors to ensure compatibility with the data standard and schema. In the absence of a service endpoint, vendors should submit standardized CAMA directly to VCGI. In either case, updated data should be made available and/or submitted on a monthly basis for the dataset to remain complete and current. 

Following receipt of the updated CAMA data each month, VCGI will work to incorporate the fields listed in Section 3.2.1 in the [Parcel Viewer](https://experience.arcgis.com/experience/b5a5cc7663c84761a305f70b913e1a60) and [Geodata Portal](https://geodata.vermont.gov/). In the Parcel Viewer, users will be able to access CAMA data easily and in relation to existing parcel, Grand List, and Property Transfer data. The comprehensive, tabular CAMA dataset will also be available publicly for download through the Geodata Portal. 

![Spatialized_Property_Transfers_Dash](https://github.com/user-attachments/assets/b72f62e8-953a-4c61-b342-721c17ee9414)
**Figure 4: Dashboard Displaying Property Transfer Data.** *Parcels are the primary unit allowing for the spatial display of property transfer data, either via SPAN or property address. Viewing transfer data on a map reveals spatial patterns and allows convenient filtering and querying. The inclusion of CAMA data using a simliar method will expand the completeness and capabilities of statewide property data and subsequent analyses.*

![PTTRs_Primary_and_Secondary_Sales_2020-2024_v2](https://github.com/user-attachments/assets/4f9fe44a-5b02-4c1f-85f3-0bbd8a49a493)
**Figure 5: Property Transfers of Primary and Secondary Homes.** *Patterns of ownership and building use are revealed when filtering property transfer data on price and primary or secondary homes. The availability of CAMA fields such as year built, unit count, or other building qualities would provide further insight into these data.*

![ParcelViewer_Survey_Library_Animation](https://github.com/user-attachments/assets/968d8e9f-b5c0-4702-82e0-8a22db989969)
**Figure 6: Survey Data Available within the Parcel Viewer.** *Surveys listed in the [Vermont Land Survey Library](https://landsurvey.vermont.gov/) are included in the Parcel Viewer and linked to their relevant parcel for quick access. Parcels again are the primary unit linking multiple data sources and displaying information collectively.*

## 3.5 Example Statute Update

>32 V.S.A. § 5404(b) (b) Annually, on or before August 15, the clerk of a municipality, or the supervisor of an unorganized town or gore, shall transmit to the Director in an electronic or other format as prescribed by the Director: education and municipal grand list data, including exemption information and grand list abstracts; tax rates; and the total amount of taxes assessed in the town or unorganized town or gore...

>[Section] "Assessor database" means the database of property information maintained by a municipalities' lister(s) or assessor(s); it is also referred to as a Computer Aided Mass Appraisal (CAMA) system or Computer Aided Mass Appraisal database

>[Section] On or before [initial date], and not less than monthly thereafter, each municipality that possesses or contracts for services for the creation or maintenance of an assessor database shall transmit an extract of the database to [the State of Vermont]. The submitted database shall include, but need not be limited to information that uniquely identifies each property in the municipality, the description of each property, the size of each property, the year in which buildings were constructed on each property, and other fields described in the Vermont CAMA data standard.

## 3.6 Implementation

In coordination with the Department of Tax, VCGI will work with the current CAMA data vendors to establish work flows for providing and publishing the agreed-upon schema. CAMA vendors will be responsible for supplying the requested fields meeting standardized specifications (field length, content, data type, etc.) each month as either a read-only API, or as an extract of their data sent directly to VCGI. VCGI will be responsible for compiling data from all four vendors into a single database and performing any transformations needed to ensure data are standardized in format and content. VCGI will also make the dataset publicly through incorporation in the Parcel Viewer and for download via the Vermont Geodata Portal.

As CAMA data become more publicly accessible, it will be important to be explicit about specific and intended uses. Namely, CAMA data should not be used for non-assessment purposes including financing. VCGI and the Department of Tax recommend the following disclaimer accompany CAMA data wherever it becomes available:

>"the data on this cost sheet/CAMA data reference are based on the last inspection by the listers/assessor for the town. This information should not be used for financing, permitting, or any other non-assessment related purposes. Data observed by the listers/assessors will not be adjusted to serve any financing or other purpose."

Timing between an update to a property's CAMA data and availability in statewide geospatial datasets would be approximately six to eight weeks, depending on data collection by listers/assessors, recording in CAMA software, monthly transfer to VCGI, and final data compilation, transformation, and publish. A similar workflow currently exists for [Vermont Property Transfers](https://vcgi.vermont.gov/data-release/vermont-property-transfers-now-available-spatial-data), which include a weekly extract of [property transfer data as provided publicly](https://taxpttrpublicblob.z2.web.core.usgovcloudapi.net/?prefix=property_transfer_files/) by the Department of Tax. Under this model, 70% of property transfers appear in geospatial datasets within four to five weeks of their closing date. 


# Recommendation 4: Clarify Right-of-Way Mapping for Tax Purposes

## 4.1 Summary

- Create guidance for treatment of the area between road centerline and edge of right-of-way for taxation purposes
- Promote mapping guidance specifying that parcels should be mapped to the edge of the right-of-way, not the road centerline

## 4.2 Justification

A quote from a GIS map vendor practicing in Vermont speaks to this recommendation:

>With the more widespread use of the GIS parcel data, more and more Towns are using it to calculate taxable acreage. Without any clear legal direction of whether to include area within the public right-of-way for the calculation for taxable acreage, it will lead to further issues.

In Vermont there is no formally defined practice or requirement for the handling of public rights-of-way from a taxation perspective and its relation with parcel mapping. Public rights-of-way such as roads and highways are areas not to be obstructed by abutting private property owners, whether they are owned in fee or easements. State highways, for example, often involve the State purchasing lands between the road centerline and abutting parcel, whereas towns may or may not do the same for local roads. These differences can contribute to a lack of clarity when accounting for the area within a right-of-way and between an abutting private parcel and road centerline. Occasionally this discrepancy has led to differences in spatial representations and resulting acreage calculations. The Tax Department, with aid of partners, should develop guidance for considering these areas with regard to taxation and related parcel acreage calculations.

[Other states have attempted](#a41-example-row-statutes-in-other-states) to clarify treatment of rights-of-way in statute, which may also be an option for Vermont. However, these examples are arguably not clear for all conditions, and may be legally and administratively burdensome to enact and enforce. Given the relatively low frequency of ROWs that are out of compliance with the state data standard (see [Appendix 4](#appendix-4-clarify-right-of-way-mapping-for-tax-purposes-considerations) and [Section 4.2.1](#421-acreage-in-right-of-way)), these issues could likely be addressed through a review of listed vs. mapped acreage of ROW-abutting parcels (see [Recommendation 5](#recommendation-5-clarify-grand-list-vs-gis-acreage-guidance)), clear guidance within the Tax Department's Lister and Assessor Handbook, and [VCGI's reporting of parcel data submittals](https://maps.vcgi.vermont.gov/parcelstatus) that are out of compliance with the state data standard.

![ROW_Zones_Diagram](https://github.com/user-attachments/assets/086078d4-7da8-496a-b4bb-3d380ca477f7)
**Figure 7: Methods for Mapping Rights-of-Way.** *Mapping of ROWs may vary depending on road type. Recommended guidance is that all parcels be mapped to the edge of the ROW regardless of road type or ownership (diagram A).*

### 4.2.1 Acreage in Right-of-Way

Correct mapping of Rights-of-Way has important implications for taxation purposes. Based on the parcel data, over 133,000 acres in Vermont are classified as a Right-of-Way. [Explore ROW acreage by town here](https://www.arcgis.com/apps/mapviewer/index.html?webmap=710b9e14e2b04c4c85a2d6e3b9638e82) and in the images below. Acreage is based on the sum of parcels by town where the Property Type is classified as "ROW_ROAD", "ROW_RAIL", or "ROW_TRAIL". The second image provides an example of each ROW.  

While the majority (96%) of municipalities include ROWs, a small number do not. Parcels in these towns are generally mapped to centerlines where ROWs are missing. These municipalities include:

- Averill (only main roads)
- Bloomfield (only main roads)
- Eden (few road fragments)
- Johnson (only in town center)
- Norton (only main roads)

In addition, ROWs for the following municipalities are typically missing or incorrectly attributed when updated data are sent to VCGI: Canaan, Royalton, Saint Albans Town, West Windsor, and Wolcott. ROWs for these municipalities can often be restored, however, using the existing data. 

![ROW_acreage](https://github.com/user-attachments/assets/cd87c576-58a5-443e-8a3b-a31288008565)

**Figure 8: Total Right-of-Way Acreage by Town.** *ROW acreage, as summed by town for all parcels with a Property Type of ROW_Road, ROW_Rail, or ROW_Trail. Total statewide ROW acreage is 133,150 acres, average per town is 522 acres, maximum is 1,883 acres (Randolph), and minimum is 16 acres (Avery's Gore).*

![ROW_zoom](https://github.com/user-attachments/assets/6c4da9a4-2798-4ad9-89b9-ee3a0a5ff5e4)

**Figure 9: Rights-of-Way Types.** *Example of parcels with Property Type of ROW_Road (grey), ROW_Rail (red), and ROW_Trail (green) in Ferrisburgh.*

## 4.3 Implementation

Implementation of this recommendation is partially contingent on which jurisdiction or institution is ultimately responsible for maintaining parcel map data (see [Recommendation 2](#recommendation-2-support-digital-parcel-maintenance-and-submittal-to-the-state-of-vermont)). If municipalities are to remain responsible for mapping, the listed vs. mapped acreage review, Tax guidance, and GIS data standard-compliance reporting above, combined with existing education and professional development work via Tax's District Advisors and the Vermont Assessors and Listers Association (VALA) could be effective to bring all towns to uniformly map and calculate taxable acreage to edge of the ROW.

If either regional assessment districts or the State assume ultimate responsibility for mapping, efforts they complete or oversee would need to follow state GIS parcel data standard and map to the edge of right of way. Education via the District Advisors, VALA, and potentially via regional assessment district would still be needed to ensure consistency practices when calculating taxable acreage to the edge of ROW.

## 4.4 Related Statutes
[19 V.S.A. § 32 Assumed width of right-of-way](https://legislature.vermont.gov/statutes/section/19/001/00032)

[19 V.S.A. § 1111 Permitted use of the right-of-way relocation or adjustment orders](https://legislature.vermont.gov/statutes/section/19/011/01111)

[19 V.S.A. § 717 Highways / Laying Out, Discontinuing, and Reclassifying Highways](https://legislature.vermont.gov/statutes/section/19/007/00717)

# Recommendation 5: Clarify Grand List vs. GIS Acreage Guidance

## 5.1 Summary
- Develop criteria for when review of underlying legal property descriptions is needed given differences in listed and map acreage for the same parcel
- Specify actions to be taken in the Listers and Assessors handbook based on best available documentation for acreage discrepancies

## 5.2 Justification

In addition to acreage and resulting taxation associated with areas of property in road rights-of-way, acreage discrepancies between listed and mapped values are common. It is currently technically possible to easily display and compare differences between listed and mapped acreage. 

![Listed_Vs_Mapped_Acreage_Percent_Difference](https://github.com/user-attachments/assets/9af187d1-4f4f-4f22-b13a-8a84f47a2ed6)
![image](https://github.com/user-attachments/assets/d723529b-89de-43e8-915a-312fdfe6d9b6)

**Figure 10: Percent Difference Between Grand List Acreage and GIS Acreage.** *Visualized differences in listed acreage and GIS (drawn) acreage in Northfield, VT. The amount of percent difference is shown in five ranges and colors, as well as described in text on each parcel. [See an interactive map of these differences.](https://vcgi.maps.arcgis.com/apps/mapviewer/index.html?webmap=e452fa5505644e12b1bf8b6308f7b2e8)*

### 5.2.1 Discrepancies in Listed and Mapped Acreage

|                                              |Total Acreage             |
|----------------------------------------------|--------------------------|
|**Listed Acreage** (2023 Grand List)          |5,609,102 ac              |
|**Mapped Acreage** (statewide parcel dataset) |5,786,273 ac              |
|                                              |*177,171 ac difference*   |

**Table X: Statewide Discrepancy in Listed and Mapped Acreage.** *While some disagreement is expected, differences in listed and mapped acreage may warrant further investigation of Grand List recordings and/or mapping.*

- 42,162 grand list records had no listed acreage
- Mapped acreage was calculated for parcels only based on property type (PROPTYPE) field
- A small subset of grand list records represent railroad rights-of-way based on property description (DESCPROP) field

## 5.3 Implementation

The Tax Department, in collaboration with partners, should develop guidance for handling of these acreage discrepancies. This may include specifying when the difference is large enough to trigger review of the parcel(s) underlying recorded legal descriptions, and when updating the listed and/or as-drawn acreage should result. These recommendations may be included in an updated Listers and Assessors handbook and ensuing training/guidance for municipalities. VCGI should continue to make web applications that display acreage discrepancies on a per parcel basis statewide.

# Recommendation 6: Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract

## 6.1 Summary

-	Increase the frequency of aerial imagery collection to statewide annually
-	Make higher resolution (at least 15cm/6 inch), leaf-off, imagery available across entire state every other year
-	Include buy-up options for oblique imagery and higher resolution (7.5cm/3 inch) imagery

## 6.2 Justification

Aerial imagery provides a comprehensive view of a property and its surroundings, which is invaluable for evaluating land use, property boundaries, and changes over time. Benefits of using aerial imagery in the assessments include the following:

### 6.2.1 Improved Property Valuation Accuracy and Transparency

Annual access to aerial imagery provides up-to-date, high-resolution visuals of properties, allowing assessors to work with the most current information on structures, additions, and improvements, reducing reliance on outdated records. 

**Increased Equity:** By using accurate and consistent data, assessors ensure that taxpayers are charged fairly, with property values reflecting true market conditions, which builds trust in the process. 

**Enhanced Identification:** Imagery allows assessors to identify unreported property changes, such as new constructions or additions, ensuring all taxable improvements are included. 

**Transparency:** Access to updated imagery fosters public trust, as taxpayers can see the same data used for their assessments, demonstrating the fairness and objectivity of the process.

### 6.2.2 Cost Efficiency

**Reduced Field Visits:** High-quality aerial images allow assessors to conduct some of their work remotely, minimizing the need for costly and time-consuming on-site visits.

**Time Savings:** Detailed imagery enables faster and more efficient property analysis, increasing productivity and allowing assessors to cover more properties in less time. 

**Standardized Process:** Using consistent statewide imagery reduces reliance on multiple data sources, streamlining workflows, minimizing errors, and lowering overall costs.

![2023_15cm_SouthBurlingtonDev_close](https://github.com/user-attachments/assets/7b92eefb-6e1c-4239-be4f-fbb9f1b72f5d)
**Figure 11: High Resolution Imagery to Capture Development.** *High resolution imagery could improve the efficiency with which assessments are performed while providing up-to-date information.*

### 6.3.3 Resolution, Frequency, and Types that Speed the Process

**Resolution:** Higher resolution (15cm) leaf-off imagery acquisition in the state has primarily been collected in targeted areas, such as Chittenden County, where additional funds have been contributed by municipalities. Imagery at this resolution should be made available statewide at least every two years, consistent with the recommendations of the International Association of Assessing Officers (IAAO) and with the needs identified in user surveys in Vermont and elsewhere. Lower resolution (30cm) imagery should be made available on alternating years to support change detection. Statewide collections benefit from economies of scale and promote equity across the state.

**Frequency:** Annual collections enable the discovery of undocumented structures and unreported real property helps ensure fair and equitable taxation across the state. An example highlighting this outside of Vermont is a case study of a county in Arizona that recently used imagery in their assessing process to identify 9000 porches, 1200 garages, 1100 pools and 1200 additions missing from existing assessments, adding over $95 million in market value.  Vermont’s grand list totals over $100 billion dollars, if imagery was used to find 0.1% in unaccounted for value it would result in $100 million in currently untaxed property added to the grand list.

**Buy-Ups:** The state should make oblique imagery options available as part of the statewide imagery program to achieve economies of scale and limit duplicative efforts. Some municipalities have individually contracted to collect or access oblique imagery for assessment and planning purposes, likely incurring higher costs due to the lack of coordinated procurement. While collecting statewide oblique imagery should be considered in the future, the acquisition costs are significantly greater than current orthoimagery collections and the state should ensure that tools, infrastructure, and training, is in place to maximize the value of oblique imagery prior to making a major investment. By offering oblique imagery as an optional "buy-up" under the program, the state can address varying needs and capabilities while fostering collaboration and cost-sharing opportunities among municipalities. The utilization of oblique imagery by some municipalities also presents the opportunity to pilot the use new remote sensing methods before committing to a larger investment (see recommendation 7).

**Oblique Imagery:** Oblique imagery is aerial photographs taken at an angle, typically between 30 to 60 degrees from vertical. Unlike traditional ortho (or nadir) imagery, which captures a top-down view of the terrain and structures, oblique imagery provides a perspective that includes the sides of buildings, terrain contours, and other vertical features. Some parts of the country have used high-quality oblique imagery to replace physical inspections. 

Key characteristics of oblique imagery include: 

-	Multi-Angle Views: Often captured from four cardinal directions (north, south, east, west), oblique imagery offers comprehensive visual coverage.
-	Three-Dimensional Perspective: The angled view reveals details about the height, depth, and structure of objects.
-	Rich Detail: It captures features not visible from directly above, such as facades, overhangs, or property boundaries hidden by tree cover in nadir imagery.

![Obliques_01a_KY_From_Above](https://github.com/user-attachments/assets/6bc4a26b-3984-4b4c-9538-72860a1953ba)
![Obliques_01b_KY_From_Above](https://github.com/user-attachments/assets/a6a2951d-62ef-4690-8d07-6204dd7c15bf)
**Figure 12: Oblique Imagery.** *Screenshots from a viewer show oblique imagery with possible measurements and identifiable features for properties in Kentucky. The imagery is publicly available [here](https://explore.kyfromabove.ky.gov/?ll=36.738774,-83.737983) (Color_6052_19796, Right_6053_24171, Fwd_6052_19790, Left_6050_12120, and Bwd_6052_19804).*



## 6.3 Implementation

The Vermont Mapping Program (VMP), was established in 1968 under the Department of Taxes to collect aerial imagery to support tax equity and operational efficiency. Over the years, the program evolved to transition to digital photography in the 1990s, color in the 2000s, as well as a move toward higher resolution and frequency. The program is now managed by the Vermont Center for Geographic Information, a part of the Agency of Digital Services (10 V.S.A. § 123), and Vermont's aerial imagery is accessed in web applications by hundreds of thousands of individuals every year. 

The change to annual statewide collections and 15cm leaf-off imagery every two years is likely to be implemented by the state's existing imagery program, managed by ADS, beginning in the Spring of 2026. A 2023 survey of users expressed a strong need and the interagency imagery advisory group has recommended these specifications. In terms of leaf-off imagery, the change would represent a four-fold increase in resolution and double the collection frequency. The cost of the resolution and frequency upgrade is estimated to be approximately double the existing base program budget, which has remained the same for over two decades at $125k a year.  

# Recommendation 7: Pilot Remotely-Sensed Tools to Support Appraisals

## 7.1 Summary

- Pilot the use of ortho and oblique imagery along with automated feature extraction and artificial intelligence to support appraisals for an area of the state
- Assess and document results and viability for broader use, along with considerations for such use

## 7.2 Justification

The integration of ortho/oblique imagery and artificial intelligence (AI) in property appraisals represents a transformative approach to modernizing assessment practices. These tools have potential to accuracy, efficiency, and fairness while addressing limitations of traditional methods. 

Recent advancements in technology have enabled:

**Automated Change Detection:** AI algorithms can analyze imagery to identify changes in properties over time, such as new constructions, demolitions, or renovations, ensuring assessments remain current.

**Property Classification:** Machine learning models can automatically and reliably classify property types, assess conditions, and detect features like pools, decks, or accessory buildings, improving valuation accuracy.

**Scalability:** AI processes large datasets quickly, allowing jurisdictions to scale appraisal efforts to assist existing staff that may not have the capacity to meet existing demands.

**Error Reduction:** Automated systems minimize human error and bias, ensuring consistent application of appraisal standards across properties.

![Automated_Detection_01_Vexcel](https://github.com/user-attachments/assets/1c037e71-e185-4eaf-a64f-e4319b09e023)
**Figure 13: Automated Change Detection.** *AI algorithms can assess imagery to detect new construction and existing construction both with and without changes over time.*

![Automated_Attribute_01_Vexcel](https://github.com/user-attachments/assets/470fd5d9-8841-46fe-aef8-8be757c82d36)
**Figure 14: Detection of Specified Attributes.** *Using machine learning, models can detect the presence of solar panels on a roof in Texas. The ability to detect certain features will enhance valuation accuracy.*

![Automated_Id_Examples_Vexcel](https://github.com/user-attachments/assets/5d8e1d54-0d44-42ee-afe2-532a7ef9cc25)

**Figure 15: Summarized Building Attributes.** *In examples from Arizona and Florida, the presence or absence of property features and measurements are quickly assessed and provided.*

## 7.3 Implementation

The Tax Department should partner with willing jurisdictions to test and evaluate the use of these methods and tools. The partnership should leverage the imagery program managed by ADS to access ‘buy-up’ products (see recommendation 6), such as oblique imagery, that could be utilized for various purposes by departments for uses beyond assessments.

# Recommendation 8: Develop and Offer Updated Parcel Contract Guidance

## 8.1 Summary

- Updated mapping contract guidance that reflects current best practices may improve quality and currentness of parcel data
- Separation of standardized parcel data maintenance from town-specific derivatives (such as print maps and custom web applications) in contracts may ease uniform administration and reduce costs
- Updated contract guidance is contingent on the assessment jurisdiction extent

## 8.2 Justification

Per VCGI's records, about 90% of Vermont municipalities currently maintain parcel data. The vast majority of these towns do so via a GIS, allowing maintenance of map data with SPANs assigned to each parce. SPAN assignment meets basic compliance with the state data standard and permits joining with the annual grand list. A small number of towns continue to hire vendors using Computer-Aided Design (CAD) software to maintain parcels, but these are not capable of data integration like a GIS. CAD data are thus unusable for joining with the grand list, CAMA, and other related information. A small remainder of towns do not maintain parcel data in any way. In all cases, the town is the jurisdiction currently responsible for drafting and overseeing a contract for parcel data maintenance meeting their specific wants and needs.

Contracts commonly include print media products, often in the form of large format plots of keyed tax map sheets with parcel identifiers and owner names. Such static maps are generated from digital parcel data, which are able to rapidly and continuously reflect changes in geometry or attribution. As such, print parcel maps may be outdated and inaccurate shortly after they are made. Still, because parcel data maintenance and the creation of print maps both require GIS skills, the same vendor is typically paid for both services in the same contract. The creation of print map products represent a sizable portion of total funds for contracts that specify them. Ideally, print map products would not be covered by any per parcel payments. This specification could potentially reduce the overall cost of maintaining quality, current parcel data.

Towns are not limited to print products to provide access to current, accurate tax map information. Many towns also contract for custom web applications that display digital parcel data in a web map along with CAMA card integration for all properties. These web map applications provide citizens access to current information via underlying dynamic data sources. The [Vermont Parcel Viewer](https://maps.vcgi.vermont.gov/ParcelViewer/) provides access to best-available parcel data statewide and [offers much of the same functionality](https://github.com/VCGI/documentation/blob/main/parcelviewer4/User_Guide.md) for towns that do not individually contract for custom map applications.

![BarreCity_CAI_WebApp01](https://github.com/user-attachments/assets/95343fbf-8e25-414d-b9c4-3854bcd8d3cd)
**Figure 16: Municipal Parcel Web Map Application.** *Some towns contract for additional services such as web maps that display CAMA data for all properties.*

![BarreCity_ParcelViewer](https://github.com/user-attachments/assets/da32ee08-a992-42e2-9d43-9877518a622f)
**Figure 17: Statewide Parcel Viewer Web Map Application.** *All towns have access to best-available parcel data via the Vermont Parcel Viewer web map application. As of 2024 the viewer presents property transfers and submitted land surveys along with grand list information for all parcels. Future integration with CAMA data is possible should it become available per Recommendation 3.*

## 8.3 Implementation

Since 2017, VCGI has made [parcel mapping guidelines](https://vcgi.vermont.gov/document/vermont-gis-parcel-mapping-guideline) available that include contract templates and considerations. These may be updated to reflect current best practices and increase accessibility. However, tailoring updated contract guidance reflective of the above and more will depend on the jurisdiction ultimately responsible for tax assessments (see [section 2.3: Implementation](#23-implementation)). If towns are to remain the assessment jurisdiction, clarification of the importance and means of using current GIS as well as separation of parcel data maintenance from paying for print maps would be in focus. Updated guidance would ideally be combined with a requirement that any changes in per parcel payments associated with mapping would be limited to use for parcel data maintenance and not payment for derived products. Those print products or custom map applications may be purchased separately by towns should they continue to wish to do so.

It is assumed that one mapping contract per regional assessment district would be used if there is a change in assessment jurisdiction. From a mapping perspective, reducing 250+ separate contracts to approximately 14 would have advantages in ensuring that quality and timely data are maintained statewide. In this scenario, contract guidance could be designed to require standardized parcel data maintenance while permitting towns the option to "buy-up" additional services on their own should they wish to do so.

# Recommendation 9: Modernize Current Use Map Standards, Submittals, and Access

## 9.1 Summary

- There is no way to currently visualize the specific extents of all current use areas enrolled statewide, which are increasingly requested to support other mapping uses
- Recent changes in grand list maintenance via the Vermont Property Information Exchange (VTPIE) have improved internal data organization and access to current use information
- Web mapping tools can help modernize the mapping components of current use applications and visualizing specific enrolled areas
- Historical, analog map documents associated with enrolled lands could benefit from digitization efforts of other records

## 9.2 Justification

Vermont's [current use](https://tax.vermont.gov/property/current-use) program has been a cornerstone of the state's tax policy for several decades. As the program depends on the bounded extents of either forested or agricultural lands and associated acreage thresholds, mapping has been central to the program since its inception. Improved mapping accessibility and accuracy through digital tools and techniques has surpassed what was once sufficient in meeting the program's mapping requirements. As a result, the quality of the underlying maps supporting enrolled parcels varies widely.

Map storage needs range from to housing years of print-only documents with no digital equivalent to receiving modern GIS work submitted by qualified map preparers like county foresters. Forested parcels are much further along in their digitization with the Agency of Natural Resources (ANR) maintaining a [statewide GIS dataset of those records](#https://geodata.vermont.gov/datasets/VTANR::use-value-appraisal-parcels/explore). These parcels are simply joined to full parcel geometry rather than depicting specific enrolled extents. There is no digitally mapped equivalent for agricultural parcels, which represent 4,700+ records covering more than 320,000 acres.

The calculation of various current use statistics is made possible through the recent modernization of the state's grand list maintenance software, the Vermont Property Information Exchange (VTPIE). VTPIE has improved internal access to enrolled parcels statewide, at least as tabular data. This access is important as several other mapping requirements aim to depict current and complete current use lands statewide. For example, [Act No. 181 (H.687)](https://legislature.vermont.gov/bill/status/2024/H.687) of 2024 tasks Regional Planning Commissions (RPC's) to update regional plans and future land use maps to support an Act 250 tier system. RPC's understandably want to reflect current use lands within.

### 9.2.1 Lands in Current Use

In 2023 over 19,000 parcels were enrolled in current use, totaling over 2.5 million acres statewide. [Explore parcels enrolled in Current Use](https://www.arcgis.com/apps/mapviewer/index.html?webmap=6e82347c410d4c00bab809a8a6e5350b).

A meaningful detail and caveat to the map linked above is that current use parcels may only have a percentage of their acreage enrolled. The statewide average enrollment is 92.5%, with 75% of parcels between 92-100%.

![2023_CurrentUse](https://github.com/user-attachments/assets/4a0bf7fd-a32d-4217-9f63-b23782bb5f56)
**Figure 18: Parcels Enrolled in Current Use.** *Shaded parcels are enrolled in the current use program as of 2023 (left). A parcel may be fully or partially enrolled (right).*

## 9.3 Implementation

A near term improvement would be for VCGI, with the authorization of the Tax Department, to publish a publicly-accessible annual statewide layer of all enrolled current use lands joined with statewide parcel data. This process could be largely automated and meet many mapping needs, in addition to increasing transparency about the program and lands within.

A medium term improvement could involve developing a modern, public-facing map submittal tool to enable those without access to GIS to enter recent and accurate areas to be considered for enrollment. This map would be GIS-compatible at the source. Associated current use map standards, which were last updated in 2009 and still refer to outdated print-based mapping methods, could be updated at the same time.

A long term improvement would be to leverage any concurrent records digitization efforts or resources to consider digitizing print-only maps of enrolled areas. This would likely be a substantial effort but would ultimately lead to the most useful information. Automated digitization technology continues to evolve at a surprisingly quick pace and may also be applicable sooner than one may expect.

# Recommendation 10: Consider Updating and Moving Parcel Program in VT Statute

## 10.1 Summary

- Current statute is not reflective of actual oversight and operation of statewide parcel program
- Updating existing statute to reflect current and future practice could be completed with little to no impact on operations
- The current Parcel Advisory Board, developed in 2016, should be retired and rebuilt to better serve present and future program operations

## 10.2 Justification

In 2016 the Vermont Legislature passed a Transportation Bill which was led by the Vermont Agency of Transportation (VTrans) and the Agency of Commerce and Community Development. This bill contained language creating the Parcel Program, which was the product of a work group including multiple state agencies, regional planning commissions, nonprofits, and professional organizations. The initial phase, the Statewide Parcel Mapping Project, involved federal and state funding and occurred over a three year period from 2017-2019. Since then, parcel mapping maintenance has transitioned to the Parcel Program, which is the ongoing effort to maintain, publish, and improve existing statewide data. 

[Statutorily](https://legislature.vermont.gov/statutes/section/19/001/00010), the Parcel Program continues to reside under the supervision of VTrans. Practically, the program is entirely managed and staffed within VCGI (Agency of Digital Services). Transitioning the specified responsibilities and maintenance of the program to the appropriate stewards in statute will improve accuracy and clarity around work being performed and the duties of both agencies.

Relatedly, [19 V.S.A. § 44](https://legislature.vermont.gov/statutes/section/19/001/00044) specifies a Parcel Advisory Board to monitor the program and make recommendations for improvements. The Advisory Board is comprised of the following, or assigned designees:

- Secretary of Transportation (chair)
- Secretrary of Natural Resources
- Secretary of Commerce and Community Development
- Commissioner of Taxes
- Representative of the Vermont Association of Planning and Development Agencies
- Representative of the Vermont League of Cities and Towns
- Land Surveyor licensed under [26 V.S.A. § 45](https://legislature.vermont.gov/statutes/chapter/26/045)

While the Parcel Advisory Board [met regularly](https://vcgi.vermont.gov/data-and-programs/parcel-program/parcel-advisory-board) from 2016-2019, the needs and priorities of ongoing parcel maintenance have shifted since the transition to the Parcel Program. Since then, meetings have been infrequent and have primarily focused on updating the Board on the current Program status rather than identifying and enacting improvements. 
In addition, statute wording specifies VTrans as the agency receiving Board recommendations. Given the evolution of operations the need exists to update statute language and location, and to modernize the objective, role, and composition of the Advisory Board to better align with the future of the Program.

## 10.3 Implementation

Transferring ownership of the Parcel Program in statute should be relatively seamless and could happen without significant impact to current operations. [where will it go instead...?]

Given successful completion of the Parcel Project, the current Parcel Advisory Board should be retired and a new oversight body of similar composition could be established to guide the Parcel Program moving forward. This body could continue to provide insight and recommendations based on experience from a variety of users and stakeholders. The new advisory board should meet with VCGI on a pre-determined schedule once or twice a year at minimum. This schedule would allow the Parcel Program to remain responsive and attentive to issues and needed improvements, particularly in light of the prosposed operational changes.

## 10.4 Related Statutes

[19 V.S.A. § 10 Highways - State Highway Law; General Transportation Divisions](https://legislature.vermont.gov/statutes/section/19/001/00010)

> 19 V.S.A. § 10 (17) Administer the Statewide Property Parcel Mapping Program.

[19 V.S.A. § 44 Statewide Property Parcel Mapping Program](https://legislature.vermont.gov/statutes/section/19/001/00044)

[10 V.S.A. § 123 Geographic Information - Powers and Duties](https://legislature.vermont.gov/statutes/section/10/008/00123)

# Recommendation 11: Coordinate With Concurrent Efforts to Digitize Land Records

## 11.1 Summary

- If changes are made to assessment jurisdiction, digital land records become additionally important to minimize inefficiencies between tax administration and maintenance of authoritative land records
- Digital land records statewide would offer numerous benefits including integration with parcel data to increase transparency and ease access, regardless of assessment jurisdiction
- Integration with parcel data could potentially reduce the need for duplicative mapping needed by other state initiatives

## 11.2 Justification
Digital land records are X. Current efforts to digitize authoritative documents .
A parcel is the container by which land records could be joined, enabling easy, map-based access to associated documents.

[Act 171  of 2022](https://legislature.vermont.gov/Documents/2022/Docs/ACTS/ACT171/ACT171%20As%20Enacted.pdf) is focused on land records modernization through the Vermont State Archives and Records Administration office (VSARA) under the Secretary of State. VSARA was tasked with consulting the Joint Fiscal Office, Vermont League of Cities and Towns, Vermont Municipal Clerks' and Treasurers' Association, representatives from banking, bar, title insurance, and real industry industry, and other interested parties to assess the fiscal, governance, and operational sustainability of modernization. A [report](https://outside.vermont.gov/dept/sos/VSARA/Reports/VSARA_2024LegislativeReport_Act171_2022.pdf) was produced suggesting the benefits of an enterprise-wide systems approach to modernization, including consistency and uniformity. Digital land records offer many benefits similar to those above related to standardized statewide CAMA (see [Appendix C](https://outside.vermont.gov/dept/sos/VSARA/Reports/VSARA_2024LegislativeReport_Act171_2022.pdf#page=21), for example); efforts to make all of this information publicly available in a consistent format statewide would have far reaching applicability and long-term cost savings. 

As an example of utility, the [Protected Lands](https://geodata.vermont.gov/datasets/VCGI::vt-protected-lands-database/about) database could be enhanced through the inclusion of authoritative, digital land records indicating ownership and easements linked to parcel geometry. 

![ProtectedLands_Protection_Status_Jurisdiction_Access](https://github.com/user-attachments/assets/eb691607-3da6-4ed5-9057-e34acfbc0bcd)
**Figure 19: Protected Lands.** *Protected lands in Vermont, classified by Jurisdiction (top left), Public Access (top right), Primary Protection type (lower left), and GAP Status (lower right). Inclusion of digital land records could provide additional information for classification, including which parcels contain easements or the history of ownership.*

## 11.3 Implementation


## 11.4 Related Statutes and Bills

[H.512 (Act 171) of 2022 - An act relating to modernizing land records and notarial acts law](https://legislature.vermont.gov/bill/status/2022/H.512)

# Recommendation 12: Make Proposed Appraisal Districts Consistent and Compatible with Existing Administrative Boundaries

## 12.1 Summary

## 12.2 Justification
Text.

## 12.3 Implementation

# Additional Recommended Improvements

## Improve Submittal of Land Surveys to Vermont Land Survey Library

The Vermont [Land Survey Library](https://maps.vcgi.vermont.gov/landsurveylibrary/) is a repository for digital copies of land surveys maintained by VCGI as part of the Parcel Program but is maintained separately from parcel data. The library consists of a web map that displays the general location of a land survey with its related information.

The library was developed in accordance with the amendment of [27 V.S.A. § 341](https://legislature.vermont.gov/statutes/section/27/005/00341) by the passing of Act 38 in 2019 requiring a land survey for a property line change, including a boundary line adjustment or a subdivision, effective January 1, 2020. In addition to this mandatory practice for all Vermont municipalities, which includes those without development regulations, sections [27 V.S.A. §1401](https://legislature.vermont.gov/statutes/section/27/017/01401) and [27 V.S.A. §1403](https://legislature.vermont.gov/statutes/section/27/017/01403) require a digital copy of a land survey to be submitted to the library by a licensed land surveyor or a municipal official. While there is no legal requirement that applies to them, land surveys predating January 1, 2020 can also be submitted to the library by a licensed land surveyor or a municipal official. Others working in the public sector may submit a land survey to the library as well (e.g., the Vermont Agency of Transportation).

As of December 10, 2024:

- 3,121 land surveys have been published to the library, representing 215 towns (out of 256 total Vermont municipalities). About 55% of land surveys were submitted in accordance with the amendment (dated on or after January 1, 2020)

- 41 towns have no land surveys published in the library

- 143 towns have 10 or fewer land surveys published. Only 2 towns have more than 100 land surveys published

Mapping vendors typically receive the land surveys they need to complete a parcel data update directly from the town. Vendors have confirmed that the library does not currently reflect the total number of land surveys they receive. However, the two towns with over 100 land surveys published to the library demonstrate the potential value of the library. Now that the library is also integrated into the Vermont Parcel Viewer, increased participation the library may supplement preliminary research as part of a title search. From a town in Windham County: 

> This is a great resource once surveys are scanned, allowing towns to index their surveys and host them for free. I have been using this resource, realtors and title searchers know they can expect to see this information on this site.

Other uses include:

- Assist land surveyors with research prior to conducting field work 
- Identify and address discrepancies at town boundaries
- Create a digital copy to preserve historic land surveys

There is currently no enforcement around the survey submittal requirement, and additional measures could be used to encourage participation before considering more severe penalties for non-compliance. Any future work in land records digitization or realignment of assessment jurisdictions should consider leveraging this existing resource. The professional surveying, appraisal, and real estate communities, along with municipal officials who oversee local bylaws and development regulations, could be further engaged for improvements.
 
![SurveyLibraryStatus_Dec7_2024](https://github.com/user-attachments/assets/6f3e03ae-add5-4135-b70c-61bb4db4a356)
**Figure 20: Statistics from the Vermont Land Survey Library.** *Land surveyors are responsible for submitted new surveys to the Land Survey Library. Information about surveys including type, submittal date, survey year, town, and surveyor are tracked. These data can help assess patterns and completeness when compared to property transfers and new Grand List records, as well as between geographical areas.*

## Support Survey of Municipal Boundaries and/or Corner Points

Town boundaries form the basis of numerous administrative decisions, governance, and demographic analyses in Vermont. While most states are primarily organized and governed at the county level, Vermont continues to operate heavily at the town level. Even so, many boundaries between towns have not been officially surveyed. Charters often reference obscure landmarks or features that may have changed or disappeared over time, creating challenges and discrepancies in modern day mapping. It is common for data from VCGI, VTrans, E911, and other state agencies to differ on the exact location of various town boundaries. Where surveys do exist, they often only include one neighboring town or a portion of the town line. VCGI's current recommendation for resolving town boundaries is for towns to work with neighboring municipalities to establish agreed-upon lines and ideally have them surveyed. These surveys would then inform charter changes that then are reflected in boundary layers. Unsurprisingly, this is a cumbersome and often challenging effort for towns to undertake without additional support.

Massachusetts began [officially surveying corner points of municipalities in the 1890s](https://www.mass.gov/info-details/massgis-data-municipalities), and continues to update [surveyed points](https://gis.massdot.state.ma.us/towncorners/) and town boundaries statewide with any boundary changes approved by the state's legislature. Formally surveying all of Vermont's municipal boundaries and/or corner points would be a significant undertaking but ultimately help confirm and establish reliable, consistent, and permanent boundary designations that would improve all dependent mapping and policies.

![MuniLibrary_Survey_2](https://github.com/user-attachments/assets/6e6ad6d9-711e-4593-9c96-9109075fb448)
**Figure 21: Survey of Town Line Between Underhill and Westford.** *Town boundaries are not officially surveyed in many parts of the state. The Land Survey Library includes a specific designation for surveyors to indicate whether the survey is a municipal boundary. Ideally all town boundaries will be officially surveyed and formally documented in time.*

### Acreage Not Counted (Gaps) and Double Counted (Overlaps)
![WinooskiTopology_example](https://github.com/user-attachments/assets/c94e43ea-2df6-4d89-9d60-a22c4a7c611b)

**Figure 22: Gaps and Overlaps Between Municipal Boundaries.** *Example of gaps (red) and overlaps (blue) in parcel geometry at municipal boundaries between Winooski and bordering South Burlington, Burlington, and Colchester. Black lines represent town boundaries as reflected in the [town boundary dataset](https://geodata.vermont.gov/datasets/VCGI::vt-data-town-boundaries-1/about) maintained by VCGI. [Explore gaps and overlaps in parcel data along town boundaries](https://vcgi.maps.arcgis.com/apps/mapviewer/index.html?webmap=7972f2b2ab0646deae0fd8d8b79e138d).*

# Glossary

## Abutting

Sharing a contiguous border or boundary.

## Active Parcel

In cases where two or more abutting parcels have the same owner, parcel to which a single tax bill is associated with all the abutting parcels under the same ownership.

## Administrative Parcel

A parcel defined in boundaries and/or function by its tax or other administrative uses, not necessarily its legally documented boundaries. Often used in contrast to legal parcel.

## API (Application Programming Interface)

Digital tools and protocols that allow different software applications or systems to communicate and share information with each other.

## Assessment Jurisdiction

The bounded area in which a government or authorized entity has the authority to assess property for taxation. Typically also responsible for conducting appraisals, maintaining the grand list and associated property records, overseeing mapping of property within the area, and addressing appeals or disputes about property assessments. In Vermont, the current assessment jurisdiction is the municipality. In other states it is often the county.

## Attributes

Information associated with a map shape, found in fields, organized in a table.

## Calculated Acreage

The estimated acreage of a mapped parcel derived by using GIS. May or may not differ from listed acreage.

## CAMA (Computer Assisted Mass Appraisal)

Computer software that helps maintain property information. In Vermont, CAMA software platforms are currently handled on a town-by-town basis. These systems may be a source of some of, but ultimately are not the same as data provided by the statewide parcel dataset.

## Centerline

Applied to a street, road, right-of-way, or other strip of land of uniform width, defines the line midway between the side lines of said strip.

## Contiguous

Next to or close to one another; adjacent, having a common boundary, sharing an edge.

## Data Standard

A uniform way to manage digital information of a particular kind.

## Digital Land Records

Electronic storage, management, and distribution of land-related information. Includes details about properties, their ownership, boundaries, land uses, encumbrances, transactions, and other legal and administrative data. Used to refer to authoritative land records, in contrast with analog or paper-based land records.

## Domain

Rules that determine available values in fields. Keeps things tidy.

## Feature

A map shape that is a representation of a real-world object.

## Field

Like "column headers" in an excel table. Information organizers.

## Geometry

A GIS representation of spatial data using points, lines, and polygons.

## GIS (Geographic Information Systems)

Computer-based tools used to create, modify, store, visualize, and analyze spatial data.

## Inactive Parcel

In cases where two or more abutting parcels have the same owner, parcel(s) that does not receive a tax bill. May be represented as multiple parcels within a larger boundary with a single SPAN and owner, for example.

## Legal Parcel

A parcel defined in boundaries by deed, survey, or other official legal document. Often used in contrast to administrative parcel.

## Listed Acreage

The estimated acreage of a mapped parcel as presented within a Grand List. Often based on deeds within land records for a given property.

## Multi-Part Parcel

A non-contiguous geometry object (multi-part polygon) modeling one Grand List record as one record in the GIS data. For example, a single parcel split into two pieces by a water body or road but with a single SPAN and Grand List record.

## Parcel

A map representation of a bounded area of the Earth's surface. Often used to represent ownership of said area.

## Parcel Data

Parcel data consists of property ownership information (Grand List) joined with mapped property boundaries. Digital parcel data are easily distributed, are searchable and can be analyzed and applied for other uses. Not a survey but rather a map index of property ownership. 

## Private Right-of-Way (ROW) (or Ingress-Egress Easement): 

Arranged for access to locations by traversing one or more parcels. Ingress-egress easements that overlay underlying parcels are not considered to be public rights-of-way and are not considered to be parcels.

## Public Right-of-Way (ROW): 

An area that is legally dedicated to public right-of-way (access) purposes. Public rights-of-way areas do not have SPAN numbers, but are a type of parcel (bounded area).

## Schema

Format and rules of the content of spatial data. Uniformity here keeps decision-support tools running smoothly.

## SPAN (School Property Account Number)

Unique, statewide eleven-digit identification number assigned by a municipality to a property, per the Director of PVR via [32 V.S.A. § 5404](https://legislature.vermont.gov/statutes/section/32/135/05404).

## Spatial Data

Information that can be mapped and describes the location, shape, and/or relationships of objects or phenomena on the Earth's surface.

## Subdivision

Division of a lot, tract, or parcel of land into two or more lots, plats, sites, or other divisions of land for immediate or future sale or building development. 

## Survey

The process and resulting document of recording observations, making measurements, and marking the boundaries of tracts of land. 

## Unlanded Structures

A condominium unit, mobile home, camp, or other structure that is a unit of real estate which is separate from the underlying land surface. In some cases, the underlying land is rented.

## Vermont GIS Parcel Data Standard

The current Vermont GIS Parcel Data Standard ensures that all mapped properties statewide are linkable to their unique grand list record. This link between table record and its mapped area is enabled by the unique School Property Account Number (SPAN) assigned for every parcel. Parcel data adherent to the standard enables visualization of a statewide parcel data layer along with their respective grand list information for every property in the state. Standardized parcel data also enable other information to be related with properties on a map, such as weekly property transfers.

## VTPIE (Vermont Property Information Exchange)

An integrated system overseen by the Tax Department to collect Vermont’s statewide education grand list and to manage the statewide education property tax system, to be used by every municipality in the state. Integrates with parcel data served by the Vermont Parcel Program.

# Appendices

## Appendix 1: Update Parcel Definition in Vermont Statute Considerations
### A1.1 Current State of Mapped Inactive Parcels

Status of submitted parcel geometry, including counts of inactives and submittals by town, are published weekly at the [Town Parcel Status dashboard](https://maps.vcgi.vermont.gov/parcelstatus) maintained by VCGI. See the tab at the bottom titled "Inactives" to view current status. Inactives can also be found within the [Vermont Parcel Viewer](https://maps.vcgi.vermont.gov/parcelviewer) and as  GIS data at the [Vermont Open Geodata Portal](https://geodata.vermont.gov/pages/parcels). Those data are also updated weekly.

Inactive parcels are not managed consistently across towns; currently 178 towns (70%) submit inactive parcels. In addition, attribution of the parcel status field (active/inactive) is not complete or consistent for all submitting towns. As of November 2024, only 138 towns (54%) have submitted inactives with a populated and presumably accurate "STATUS" field. This means the parent parcel has an "ACTIVE" status and all associated "INACTIVE" status parcels have a PARENTSPAN matching the "ACTIVE" status SPAN.

![ActiveInactive](https://github.com/user-attachments/assets/9ebd72bc-9f34-4c54-aa2a-e930529b9803)

**Table X:** *Example of correct attribution in the inactive parcel layer. The parcel with an "ACTIVE" status has a SPAN entry, followed by the associated "INACTIVE" status parcels with PARENTSPAN entries linking them to the "ACTIVE" parcel. In the Active Parcels layer, these five parcels would be merged to a single parcel. In some cases, "INACTIVE" status parcels may also include a unique SPAN entry. Typically these are placeholders used by town officials.*

### A1.2 Comments on Maintaining Inactive Parcels at the Municipal Level

**From a municipality in Windham County:**

> As part of [the municipality's] reappraisal, we will review parcels previously classified as "inactive" to determine their contributory value. We believe that our [records] (similar to every town across the state) contain inactive parcels not represented in the Grand List or [in the parcel data]. Our goal is to identify and recreate these parcels through a thorough review of deeds, surveys, and historical grand lists.

**From a mapping vendor working with Vermont municipalities:**

> A property owner has to go through a subdivision process and approval with the town. Once approved, each lot becomes its own legal entity. That is the point at which the inactive lots legally exist and should be shown in the [parcel] data and entered in the inactive grand list. A 100 acre lot is a totally different situation than ten 10-acre lots. This info needs to be known.

The mapping vendor notes that when an individual purchases an abutting piece of land, listers will often make the new piece an inactive parcel. But if an individual were to create a subdivision while maintaining ownership, listers may not represent this in the parcel data at all. 

> The fallout from all this is that pieces of land get lost, revenue gets lost, and the picture of all the pieces of land is not accurate. We maintain one data layer of all parcels.  Each parcel has a parcel number, and what we call a link number. The link number is simply the parcel number of the active lot (if the parcel is active, the numbers are the same).

This last quote suggests that at least one parcel map vendor working in Vermont is already maintaining parcels in a way that is compatible with the proposed changes in this report.

### A1.3 Parcel Definition Alternatives

#### A1.3.1 Aggregate Mapped Unit Defined by Ownership (Contiguous)

Current Vermont Statute [32 V.S.A. § 4152 (a)(3)](https://legislature.vermont.gov/statutes/section/32/129/04152) defines a parcel. This is a "contiguous" parcel definition. Separate parcels are grouped together by ownership for administrative purposes.

Depicted visually, a contiguous parcel definition means that the two abutting parcels below, which have the same owner and are shown split with a dotted green line, are drawn as the single outer rectangle. This results as one "parcel" in the spatial data layer.

![image](https://github.com/user-attachments/assets/239c3a7e-e6f5-44cd-bb89-e8768e81a1da)

**Figure 23: Contiguous Parcel Schematic.** *In the current parcel dataset, abutting parcels with the same ownership are considered to be a single parcel.*

One of the individual parts is to be considered an "inactive" parcel, but this is not uniformly tracked across towns. The other part is to be considered "active", but its status is also not tracked uniformly across towns. These inconsistencies result in data incompleteness that impact analyses as well as long-term change tracking.

#### A1.3.2 Separate Mapped Unit, Defined by Practice

Example:
> A separately assessed lot or piece of real property - *New York State Property tax and assessment administration definitions / [guidance](https://www.tax.ny.gov/research/property/equal/assessrpt/b_define.htm)*

#### A1.3.3 Separate Mapped Unit, Defined by Unique Identifier

> "Parcel" means a separate plot of land as identified by the municipality tax map and lot number. - *[New Hampshire Admin. Code § Cub 301.15](https://casetext.com/regulation/new-hampshire-administrative-code/title-cub-chairman-current-use-board/chapter-cub-300-criteria-for-open-space-current-use-assessment/part-cub-301-definitions/section-cub-30115-parcel)*

#### A1.3.4 Separate Mapped Unit, Defined by Legal Document

> "Legal parcel" means any parcel of real property that may be separately sold in compliance with the Subdivision Map Act (Division 2 (commencing with Section 66410) of Title 7 of the Government Code). - *[California, Sierra County](http://sierracounty.ca.gov/AgendaCenter/ViewFile/Agenda/05052014-115). In Compliance with State Subdivision Law.*

This example is notable in that any **one** of the following must be met to define a legal parcel, per commentary by [CA Real Estate Law Firm](https://www.sandiegocounty.gov/pds/zoning/formfields/POLICY-G-3.pdf):
> - A lot shown on a Final Map. (Major Subdivision Map)
> - A lot or parcel shown on a Record of Survey approved by the Board of Supervisors or Planning Commission.
> - A parcel shown on a Parcel Map or Certificate of Compliance recorded in lieu of a Parcel Map.
> - A recorded Certificate of Compliance.
> - A parcel shown on an approved Division of Land Plat.
> - A parcel shown on a Lot legalization Plat used as evidence of legal parcel prior to a Certificate of Compliance.
> - A parcel shown on an approved Boundary Adjustment Plat.
> - A parcel described in a Grant Deed or other bona fide conveyance document recorded prior to February 1, 1972. The deed/document does not have to be in the name of the present owner. However, it must describe the perimeter boundaries only of the subject property and no other contiguous property. The legal description and County Recorder's information must be legible to County staff. The Deed need not be an original or certified copy.

There is no statewide subdivision requirement in Vermont, and not all municipalities require subdivisions. Thus, several instruments may be relied upon to help define a parcel (deed, subdivision plat where required by municipality, or property transfer or sale).

#### A1.3.5 Separate Mapped Unit, Defined by Combination 

Any combination of the examples above.

### A1.4 Proposed Parcel Layers and VT GIS Data Standard Schema Per Updated Parcel Definition

VCGI currently publishes and maintains two statewide parcel layers: Active Parcels and Inactive Parcels (as available). Following a change to the parcel definition, VCGI will continue to publish and maintain two layers, but with slightly modified purpose, content, and schema. The following describes the existing and proposed statewide parcel data layers:

#### 1. From Active Parcels To Administrative Parcels

|Criteria  |Existing                    |Proposed                       |
|:---------|:---------------------------|:------------------------------|
|Name      |Active Parcels              |Administrative Parcels         |
|Purpose   |Primary statewide parcel layer. Groups contiguous separate lots by common ownership to single parcel polygon, conforming to current parcel definition. Included for all municipalities. |Secondary statewide parcel layer. Continues to group separate lots by common ownership to facilitate tax administration, but does not represent new parcel definition of separate and sellable lots. Included for all municipalities. |
|Schema|- SPAN<br> - MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area<br>|- ADMINSPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area|

**Table X: Transition from Active Parcels to Administrative Parcels.** *The schema change for the Administrative Parcels layer is renaming "SPAN" to "ADMINSPAN". The ADMINSPAN is the common identifier for all contiguous lots with the same ownership. SPANs for other individual lots within an Administrative Parcel are not included in this layer.*

#### 2. From Inactive Parcels To Parcels

|Criteria  |Existing                    |Proposed                       |
|:---------|:---------------------------|:------------------------------|
|Name      |Inactive Parcels            |Parcels         |
|Purpose   |Secondary statewide parcel layer. Splits contiguous active parcels with common ownership into individual lots where applicable. Included for approximately two-thirds of municipalities. |Primary statewide parcel layer. Depicts parcels as separate and sellable lots or pieces of real property, regardless of contiguous ownership. Conforms to proposed new parcel definition. Included for all municipalities. |
|Schema|- STATUS<br> - PARENTSPAN<br>- SPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area<br>|- ADMINSPAN<br>- SPAN<br>- MAPID<br>- PROPTYPE<br>- YEAR<br>- TOWN<br>- SOURCENAME<br>- SOURCETYPE<br>- SOURCEDATE<br>- EDITMETHOD<br>- EDITOR<br>- EDITDATE<br>- MATCHSTAT<br>- EDITNOTE<br>- SHAPE_Length<br>- SHAPE_Area|

**Table X: Transition from Inactive Parcels to Parcels.** *The schema changes for the Parcels layer are removing the "STATUS" field and renaming "PARENTSPAN" to "ADMINSPAN". The ADMINSPAN is the common identifier for all contiguous parcels under the same ownership; this field can contain duplicates and can be used to aggregate parcels to the Administrative Parcel layer. The SPAN is the unique identifier for each separate and sellable lot (i.e., a parcel under the proposed new definition); this field should not contain duplicates. In many cases, and all instances where a parcel has no neighbors with the same owner/tax bill, the ADMINSPAN and SPAN fields will be the same.*

![AdminSPANs_SPANs](https://github.com/user-attachments/assets/cbb220fb-17ba-4a2a-bafb-6918cb4d5024)

**Figure 24: Tabular and Spatial Representation of Proposed Parcel Layers.** *Under the new parcel definition, the Parcels layer will represent parcels as single sellable units, each with a unique SPAN. The ADMINSPAN field will include duplicates for any abutting parcels with common ownership. The Administrative Parcels layer will combine any parcels with the same ADMINSPAN entries to a single geometry.*

### A1.5 Parcel Definitions and Interpretations in Existing Vermont Statute

This section lists existing Vermont statutes that define or interpret a definition of a parcel and/or have eligibility requirements dependent on such definition. It does not list those statutes that use the term "parcel" as an identifier to clarify an idea or specify the location or applicability of what is being discussed without area requirements, unless otherwise noted.

#### 6 V.S.A. Agriculture

[6 V.S.A. § 564 - Agriculture / Hemp](https://legislature.vermont.gov/statutes/section/06/034/00564)
> **§ 564. State hemp program; registration; application; administration.** (i) the location and acreage of all parcels where hemp will be grown;

[6 V.S.A. § 4871 - Agriculture / Agriculture Water Quality / Small Farm Certification](https://legislature.vermont.gov/statutes/section/06/215/04871)
> **§ 4871. Small farm certification.** (a) Small farm definition. As used in this section, “small farm” means a parcel or parcels of land: (1) on which 10 or more acres are used for farming;

#### 9 V.S.A. Uniform Commercial Code

[9A V.S.A. § 2A-103 - Uniform Commercial Code / Leases](https://legislature.vermont.gov/statutes/section/09a/002A/00002A)
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

[27A V.S.A. § 1-105 - Uniform Common Interest Ownership Act (1994) / General Provisions](https://legislature.vermont.gov/statutes/fullchapter/27A/001)
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

## Appendix 2: Support Digital Parcel Maintenance and Submittal to the State of Vermont Considerations

### A2.1 Current Shared Responsibility Model (Town Maintenance)
The success of the Parcel Program as a voluntary-based initiative is due to the collaboration between municipalities, state government, and mapping vendors in the private sector. This "Shared Responsibility" model relies on all parties contributing resources to maintain statewide parcel data.

![image](https://github.com/user-attachments/assets/57368cfe-eb6c-47b7-99ad-66c17cb00e3d)

**Figure 25: Current Parcel Data Maintenance Practices.** *Depending on the needs and resources of a municipality, several types of parcel data maintenance practices exist.*

The Shared Responsibility model identifies a municipality's ability to perform parcel geometry updates by contracting with a mapping vendor or completing updates internally. Municipalities unable to perform parcel geometry maintenance are updated by VCGI using any new land surveys available in the [Vermont Land Survey Library](https://landsurvey.vermont.gov/). This method does not typically capture all geometry changes due to the incomplete nature of the Land Stuvey Library, and updates do not happen on a regular schedule. While generally successful, the limitations of the Shared Responsibility model have emerged after five years of operation (2020-2024).

### A2.2 Funding During the Parcel Project (2017-2019)
The Statewide Property Parcel Mapping Project leveraged both state and federal funds with 80% coming from the Federal Highway Administration and the remaining 20% from several state agencies and departments. The Vermont Agency of Transportation contracted with several mapping vendor to update or create digital parcel data for each Vermont municipality over a three-year period. Each municipality was assigned  mapping vendor through a competitive bid process. 

The average cost per parcel during the Parcel Project was $8.45 compared to the national average of $5.20 reported 10 years prior by the National Research Council in *National Land Parcel Data: A Vision for the Future* (2007). The cost per parcel during the Parcel Project ranged from $0.42 to $166.67 with 185 municipalities falling at or below the average cost per parcel (74%). Based on our records, one municipality did not contract with a mapping vendor during the Parcel Project opting to standardize its parcel data internally (the total cost and cost per parcel for this municipality is listed as $0.00). The total cost as well as the cost per parcel for each municipality during the Parcel Project can be viewed in this [table](https://vcgi.maps.arcgis.com/home/item.html?id=33735911459d49e88553618642e9dcfd). 

### A2.3 Submittal Quality Criteria

Upon review by VCGI, new parcel submissions are published and assessed for how closely they meet the Parcel Data Standard. Data quality for a town's most recent data submission is available in the [Town Mapping Status](https://experience.arcgis.com/experience/d88b19e908a1460da8bcb7326f7c2ec6) application ("Submittal Quality" tab).

#### Fully Compliant
- Includes all towns that have not been updated since the Parcel Project (i.e., prior to 2020)
- Valid topology; no gaps or overlaps among parcels
- ROWs included and mapped correctly
- Unmatched parcels only comprised of land expected to have no SPAN (common land, town/state/federally-owned land, etc.)
- Multi-SPAN parcels (e.g., condos) are attributed correctly through the intersection table, if applicable

Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly; does not require edits that were made in the previous submission; any unmatched parcels are expected to be unmatched given their status as common land, government-owned land, etc.; any multi-SPAN parcels are accounted for correctly in the intersection table. Includes towns that are working with a vendor to maintain parcels but have not submitted updates to VCGI since January 1, 2020.

#### Compliant with Minor Edits
- Unmatched parcels (as received) are < 2%
- ROWs included and mapped correctly
- No/minimal repeated edits from prior submission during VCGI review
- No/minimal (<10) edits to intersection table to account for multi-SPAN parcels
- No topology errors

Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly. Requires minor editing to address unmatched parcels (<2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include <10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.

#### Compliant with Major Edits
- Unmatched parcels (as received) are > 2%
- Topology errors resulting in gaps/overlaps among parcels
- Incorrect or missing attribution of condos/multi-SPAN parcels in the intersection table
- ROWs are missing or incomplete (e.g., parcels are mapped to road centerlines)
- Repeated edits from prior submission during VCGI review

Summary: submission meets format and content requirements of the Parcel Data Standard to the extent that it can be incorporated into the statewide parcel dataset following revisions. May require significant edits to address topology errors, missing or invalid SPANs, missing or incomplete ROWs, and/or missing or incomplete multi-SPAN parcel representation in the intersection table. Requires editing to address unmatched parcels (>2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include >10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.

#### Not Compliant
- Includes all towns that are updated by VCGI/have no vendor or capacity to submit their own updates
- Submission does not include SPANs or Parcel/Map IDs that can be linked to the Grand List
- Submission is in an unusable format (e.g., CAD) that cannot be converted to a geodatabase
- Usable format (i.e., GIS files) but missing or invalid fields that do not allow conversion to usable schema/dataset, or require significant effort to update using existing data and external sources/map viewers (e.g., loading existing attribution into new geometry; using E911, AxisGIS, or other to validate/verify SPANs; merging/splitting active and inactive parcels, etc.)

Summary: submission does not meet format and/or content allowing for inclusion in the statewide parcel dataset. Data format may be unusable/unable to convert to GIS, and/or attribution does not include valid SPANs or Parcel/Map IDs for linking to Grand List. May sometimes include a workable data format that requires significant geometry (e.g., active and inactive parcels) and/or attribute manipulation using internal and external data sources (e.g., AxisGIS sites, surveys, E911 data, etc.) to create dataset with valid schema and attribution. Also includes towns that do not have a vendor or the capacity to make their own edits and are updated by VCGI using data available in the VT Land Survey Library.

### A2.4 Funding Estimates

In November 2024, VCGI organized a focus group of 12 municipalities selected based on parcel count, location, and mapping vendor. A municipal official (lister, assessor, or clerk) from each municipality was contacted by email and asked how much the municipality currently spends on parcel mapping. While sample size is a limiting factor, based on the information provided by the seven municipalities that responded the cost of ongoing parcel data maintenance is less than the initial cost during the Parcel Project. This is true even for municipalities that are no longer contracting with their Parcel Project mapping vendor. The current cost per parcel averaged $2.66 compared to $5.87 during the Parcel Project (55% cost reduction).

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

If not organized by town, funding could be allocated by the proposed assessment districts which could help account for any geographic variance between municipalities with respect to parcel mapping. VCGI would still continue to receive parcel data updates from municipalities. Using counties as an example, there is a significant range between cost per parcel during the Parcel Project:

|County     |2024 Grand List parcel count (preliminary)|Parcel Project cost|Parcel Project cost per parcel|
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

**Table X: Preliminary 2024 Parcel Count and Per Parcel Cost by County.** *Parcels counts from the preliminary 2024 Grand List are grouped and compared to county-based Parcel Project total and per-parcel costs.*

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
|**Average**|**$5.21**                          |                 |

**Table X: Estimated Statewide Financial Incentive Cost.** *Estimated funding needed to support a financial incentive is calculated by county, along with the estimated cost reduction compared to the cost of the Parcel Project.*

|              |Average cost per parcel|
|--------------|-----------------------|
|Focus Group   |$2.66                  |
|County-level  |$2.34                  |

**Table X: A summary of the average costs per parcel.** *The average cost per parcel for the seven towns that participated in the focus group is $2.66 which is 55% less than the cost per parcel during the Parcel Project. At the county-level, the average cost per parcel during the Parcel Project was $5.21. If the same 55% cost reduction was applied at the county-level, it can be estimated that the average cost per parcel would currently be around $2.34.*    

Each county could be assigned its own per parcel fee, or a single per parcel fee could be established for the state with some counties receiving an additional percentage above the per parcel fee based on financial capacity. While there are multiple ways to determine financial capacity, two methods using the Real Listed Value field from the 2023 Grand List are shown below. For both methods, counties that are **below** the average value are shown as receiving an adjusted per parcel fee. The remaining counties are shown as receiving the standard per parcel fee.

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

**Table X: Per Parcel Multiplier Using Real Listed Value per Capita.** *County-based adjustments are calculated based on county population. Counties below the average real listed value per capita would receive an adjusted payment based on the percent difference, while those at or above the average would receive the standard payment.*

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

**Table X: Per Parcel Multiplier Using Real Listed Value per Acre.** *County-based adjustments are calculated based on county acreage. Counties below the average real listed value per acre would receive an adjusted payment based on the percent difference, while those at or above the average would receive the standard payment.*

### A2.5 Eligibility for Per Parcel Payment

- VCGI will continue to accept and review parcel geometry updates on a rolling basis. A municipal official (or a contact from a municipality's mapping vendor) must send a standard-compliant parcel geometry update to VCGI by October 1st of a calendar year to be eligible to receive a financial incentive the following year
- No more than one standard-compliant parcel geometry update per municipality will be accepted each calendar year
- Parcel geometry updates will continued to be submitted to VCGI using the [Share Map Data](https://vcgi.vermont.gov/data-and-programs/share-map-data) form
- VCGI should be notified if a municipality has no changes to report. A municipality that reports no changes will not be eligible to receive a financial incentive
- Some municipalities may choose to “opt-out,” forgoing their eligibility in exchange for VCGI assisting in their parcel geometry update Municipalities that may be good candidates to opt-out include:
    - Municipalities not currently updating their parcel geometry, contracting with a non-GIS vendor, or having "low confidence" in their ability to conduct parcel geometry updated internally
    - Municipalities with a relatively small parcel count or relatively few parcel geometry updates

### A2.6 Additional Considerations for Per Parcel Payment

-	In addition to submittal compliance criteria, a timeframe component is needed when assessing a town's eligibility for a per parcel payment (e.g., annually). Some towns are technically “compliant” and are working with a vendor but have not submitted an update to VCGI since before 2020. For small towns that may not have any changes from year to year, and therefore do not submit an update, VCGI should still receive an annual confirmation that no changes or updates are needed to the existing data
-	Consider possible tiered system for payments to encourage compliance. For example: fully compliant or minor edit towns receive full payment amount, major edit town receive 50%, and non-compliant towns receive none
-	Based on discussions with vendors in 2024, it is not necessarily practical or feasible for vendors to directly use parcel data published by VCGI (e.g., vendors are not downloading the latest data for a town from VCGI prior to making their next round of edits). Often vendors are maintaining additional fields and formats beyond what is submitted and used by VCGI following the existing VT GIS Parcel Data Standard. This is likely a factor leading to repeated edits with each submission. Consider avenues to summarize and communicate submission issues or edits made by VCGI so vendors are aware and can correct for their subsequent submission, ideally without creating significant extra work for either VCGI or vendor. In addition or alternatively, VCGI should work with vendors to potentially update the current VT GIS Parcel Data Standard to be compatible with existing workflows.

## Appendix 3: Implement Vermont CAMA Data Standard and Require Submittal to State Considerations

### A3.1 Land Use Codes
 Vermont Department of Tax [Use of Property Codes](https://taxpttrpublicblob.blob.core.usgovcloudapi.net/taxpttrpublic/_Documentation/PTTR%20XML%20Documentation%20November%202024.pdf), updated August 2024:

| Category Code| Category                     |
|--------------|------------------------------|
| 01           | Domicile/Principal Residence |
| 02           | Non-Principal Residence: Fit for year-round |
| 03           | Non-Principal Residence: Not fit for year-round habitation |
| 04           | Non-Principal Residence: Long-term rental |
| 05           | Commercial                   |
| 06           | Government Use               |
| 07           | Industrial                   |
| 08           | Open Land                    |
| 09           | Timberland                   |
| 10           | Operating Farm               |
| 11           | Other                        |

**Table X: Vermont Department of Tax Use of Property Codes.** *Use codes could provide sufficient detail for information not currently or widely tracked in CAMA data.*

### A3.2 Standardized CAMA schema
The proposed standardized CAMA schema, based on example data from CAMA vendors in Vermont as well as a similar schema being developed in Connecticut, can be viewed [here](https://vermontgov.sharepoint.com/:x:/t/ADS.VCGIGroup/EZEBDpDNLNNHk_dhFOhtNW8BiiuDlzcCbWzOrxTXDUgO_g?e=3QqTMj). See 'PriorityFields_v1' for fields to standardize first following agreement between VT Department of Tax and all CAMA vendors.

### A3.3 Mapping of Unlanded Structures and Common Interest Parcels
**Background** 

Statewide standardized parcel data in Vermont is currently comprised of parcel geometry, the approximate parcel boundary lines drawn as closed multi-sided shapes (parcel polygons) as sourced from municipalities, and parcel attribution from the annual Grand List collected and published by the Tax Department. These two components are joined together by a matching School Property Account Number (SPAN) in the attribute table of the parcel polygons layer and in the Grand List. In most cases each polygon is joined to one Grand List record, but it is not uncommon for more than one Grand List record to be joined to the same polygon. This happens most often with condominiums as they are typically described by their percentage of undivided interest in the common area and facilities rather than discrete boundaries that can be easily represented by polygons. While VCGI has provided some guidance on mapping condominiums per the Vermont GIS Parcel Data Standard, a more comprehensive recommendation for mapping all types of unlanded structures is necessary to improve data quality, clarity, and ease of use.

#### A.3.3.1 Current Unlanded Structure and Common Interest Parcel Mapping Practices in Vermont

**Stacked Method - Recommended**

Stacked polygons use a standalone Intersection Table to relate multiple SPANs from the Grand List to the same “placeholder” SPAN assigned to a polygon in the parcel data. 

![image](https://github.com/user-attachments/assets/959a5b13-4dd0-484c-b064-758ae657ee00)

**Figure 26: Relationship Between GIS SPAN (Geometry) and Grand List SPAN.** *In Vermont parcel data, the stacked method is recommended. This method uses a placeholder GIS SPAN in the parcel geometry. In the Intersection Table, the GIS SPAN is listed for all corresponding Grand List SPANs at that parcel.*

This method creates identical polygons "stacked" on top of each other, which can be “flattened” to remove all but one polygon for each parcel for analytical purposes. Unlike the building footprints methods, there is no visual distinction between unlanded structures and the common land. Because of this, parcel geometry is simpler to maintain.

![image](https://github.com/user-attachments/assets/8da7e8ab-d3e0-4423-881a-1ce1e2a9d399)

**Figure 27: Stacked Method Mapping of Condos.** *The stacked method depicts multiple owners through parcel stacking; there is no distinction between common land and building footprints (source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)).*

Pros
- Geometry is easier to maintain when compared to the building footprints methods
- Geometry includes common land to reflect total, calculated acreage and is relatively easy to “flatten” stacked polygons for analysis purposes

Cons
- Requires the creation and maintenance of GIS SPANs in the Intersection Table

**Discrete and Distributed Methods**

Building footprints are often used to visually distinguish between unlanded structures and the common land, particularly as a paper tax map convention. The difference between the “Distributed” and “Discrete” building footprint methods is whether or not the common land has a SPAN. Per the Vermont GIS Parcel Data Standard, “in some instances, a deed specifies a percentage of common land ownership to each condominium unit and the common land does not have a SPAN number. In other instances, a deed does not allocate the common land, and the common land does have a SPAN number.”

![image](https://github.com/user-attachments/assets/2ff17158-461a-490d-8062-6c014960c6f0)

**Figure 28: Discrete Method Mapping of Condos.** *The discrete method depicts multiple owners through building footprints; common land does not have a SPAN (source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)).*

![image](https://github.com/user-attachments/assets/b39db8ec-ef97-477d-b394-b303d2ff0c4d)

**Figure 29: Distributed Method of Mapping Condos.** *The distributed method depicts multiple owners through building footprints; common land also has a SPAN (source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)).*

Pros
- Creates visual distinction between unlanded structures and common land
- Avoids potential confusion caused by the use of different GIS and Grand List SPANs in the Intersection Table
  
Cons
- Time intensive to create/maintain individual building footprints geometry

#### A.3.3.2 Other Unlanded Structures Mapping Practices from Other States

Parcel points are maintained by Dakota County in the State of Minnesota. This data layer is a compilation of tax parcel information, containing one record for each real estate/tax parcel identification number (PIN) within the county. Condominiums are included in this dataset (whereas they are not in the polygons).

![image](https://github.com/user-attachments/assets/3e0e0b19-c8eb-48ad-922e-44bcfc481928)

**Figure 30: Parcel Points Method Mapping of Condos.** *While parcel points are not currently maintained or available in Vermont, at least one mapping vendor does manage them for parcels with multiple owners (source: [Dakota County, Minnesota](https://gis.co.dakota.mn.us/DCGIS/)).*

Pros
- Already practiced by some Vermont municipalities internally
- Creates some visual distinction without subtracting from total, calculated acreage
  
Cons
- Requires the creation and maintenance of separate geometry layer

### A3.4 Example CAMA Submittal Statutes in Other States

Connecticut
[Sec. 7-100l. Transmission of digital parcel file. Annual report.](https://www.cga.ct.gov/current/pub/chap_096a.htm#sec_7-100l)

## Appendix 4: Clarify Right-of-Way Mapping for Tax Purposes Considerations

### A4.1 Example ROW Statutes in Other States

Washington
[RCW 84.36.210 Public right-of-way easements](https://app.leg.wa.gov/rcw/default.aspx?cite=84.36.210)

New Jersey
[N.J. Admin. Code § 18:23A-1.16 Rights-of-way and easements](https://www.law.cornell.edu/regulations/new-jersey/N-J-A-C-18-23A-1-16)

## Appendix 5: Clarify Grand List vs. GIS Acreage Guidance Considerations

### A5.1 Acreage in Common Ownership
A stacked polygon is a group of identical parcel features (polygons) stacked on top of each other with a different grand list record assigned to each. Stacked polygons often represent common ownership parcels like condominiums. [Explore common ownership parcels](https://vcgi.maps.arcgis.com/apps/mapviewer/index.html?webmap=01a6baaaf41d4667b2f9cce09d9c26a3).

- There are 27,239 grand list records represented as 3,254 stacked polygons statewide
- Stacked polygons account for 200,457 acres (about 3.5% of the total acres attributed to parcels)

![CommonOwnership_statewide](https://github.com/user-attachments/assets/2eecb05d-b610-4d0c-97e0-ab4c7a197e55)

**Figure 31: Common Ownership Parcels Statewide.** *Shaded areas represent stacked parcels.*

![CommonOwnership_Brattleboro](https://github.com/user-attachments/assets/9580c23e-579e-41fe-aa55-b9fc13aa058b)

**Figure 32: Stacked Parcels in Brattleboro.** *An example of stacked parcels (shaded) indicating a mobile home park with over 200 unique Grand List SPANs.*

### A5.2 Acreage within State Boundary

| Geography | Total Area |         |            | Land Area |         |            | Water Area |         |         |
|-----------|------------|---------|------------|-----------|---------|------------|------------|---------|---------|
|           | Sq. Mi.    | Sq. Km. | Acres      | Sq. Mi.   | Sq. Km. | Acres      | Sq.Mi.     | Sq. Km. | Acres   |
| Vermont   | 9,615      | 24,903  | 6,153,746  | 9,217     | 23,873  | 5,899,041  | 398        | 1,031   | 254,705 |
|           |            |         | 100%       |           |         | 96%        |            |         | 4%      |

**Table X: Statewide Total, Land, and Water Area.** *Areas calculated for the state of Vermont per U.S. Census Bureau's [2022 TIGER/Line Geodatabase File](https://www.census.gov/geographies/mapping-files/time-series/geo/tiger-geodatabase-file.2022.html).*

Notes:
1. The [NIST standard](http://www.nist.gov/system/files/documents/2023/01/30/appc-23-HB44.pdf) for converting square meters into square miles was used (1 square mile = 2,589,988.110336 square meters).
2. Acres were calculated by multiplying square miles by 640, per conversion factors in the [NIST Handbook 44 (2023)](https://www.nist.gov/system/files/documents/2023/01/30/appc-23-HB44.pdf), Appendix C: General Tables of Units of Measurement.
3. Area measurements are from the Census Bureau's master TIGER database. Land and water classifications reflect updates made to the TIGER database through August 2022. Values reflect the ALAND and AWATER fields. Water measurements include only perennial water. All other water (intermittent, glacier, marsh/swamp) is included in the table as part of land area calculations.

![Vermont Land and Water Area 02 Comp_1144px](https://github.com/user-attachments/assets/79b7d3cd-30c2-4238-bdde-57ac7de9957b)
**Figure 33: Vermont Land and Water Areas.** *Statewide land and water areas as depicted using BNDHASH and NHDPlus HR input layers.*
