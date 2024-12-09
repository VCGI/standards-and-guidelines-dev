# Act 68 VCGI - Backup

This document is for backup or extra sections of the Act 68 Part II report by VCGI.

# Recommendation 1

# Recommendation 2: Support Digital Parcel Maintenance and Submittal to the State of Vermont
## 2.1 Summary

- The current model of town-based parcel maintenance with voluntary submittal to the state has reached its limits in data quality and currentness; further improvements will need new support
- The design of support for parcel data maintenance and submittal will depend on the jurisdiction ultimately responsible for mapping: town (current), region, or state
- If municipalities are to remain responsible for mapping: institute a per parcel payment to municipalities to aid costs associated with parcel data maintenance
- If Regional Appraisal District or the State is to assume responsibility for parcel mapping, those practices should be required to adhere to the state data standard, maintain and share with the state on a normalized schedule, and be funded accordingly

## 2.2 Justification

Vermont has 256 municipalities: 237 towns, 10 cities, 5 unincorporated towns, and 4 gores. Unlike other states with county government that oversee the task, in Vermont individual municipalities are responsible for parcel mapping of taxable lands in their jurisdiction. Most towns budget to hire a GIS vendor to maintain their digital parcel data and depend on them to reflect any changes to parcel geometry since the town's last update. Frequency of geometry updates varies depending on the needs and resources of the town, with some updates performed annually and others completed every two to three years or more. Some towns remain without any digital parcel geometry maintenance. Town oversight of parcel mapping is typically the responsibility of its listers or assessors.

The [Statewide Property Parcel Program](https://vcgi.vermont.gov/data-and-programs/parcel-program) publishes municipal parcel map data joined to the annual statewide grand list in a uniform, digital format. The Program relies on towns voluntarily sharing updated parcel geometry with VCGI, typically via their vendor. These data are then made publicly available by VCGI in a uniform, accessible way with [many capabilities](https://github.com/VCGI/documentation/blob/main/parcelviewer4/User_Guide.md). The data drive applications such as the [Vermont Parcel Viewer](https://maps.vcgi.vermont.gov/ParcelViewer/) that draws more than 500,000 unique views a year, and are offered as raw spatial data that sees more than 1 million unique views a year.

Parcel data sourced in this voluntary way are now one of the State of Vermont's most-used spatial datasets, supporting state, regional, and local efforts in emergency management, natural resources policy and planning, permitting and compliance, and transportation. Parcel data also support efforts to address pressing issues such as flood response, resilience planning, and housing. All municipalities may use these data and applications to display their digital parcel maps free of charge. Some towns pay vendors for additional map services such as custom web applications and print map production. The current overarching incentive for municipal parcel data maintenance is for towns to ensure the most accurate, consistent, and timely data exist across all representations of who owns which lands where and with what details, be that in grand list tables or on maps that see high use.

While relatively successful, improvements are needed in the current town-sourced model of parcel data maintenance and publishing. About 60% of municipalities have submitted updated parcel geometry to VCGI within the last year. In contrast, about 16% of municipalities have not submitted updated parcel geometry to VCGI in over three years, indicating a divide in participation in the Parcel Program and limitations to its voluntary model. Inaccurate, untimely data impacts downstream uses that are now dependent on this information.

### 2.2.1 Submittal Status
VCGI tracks municipal parcel data maintenance and voluntary submittals and presents this information via the [Parcel Program's Town Mapping Status application](https://maps.vcgi.vermont.gov/parcelstatus/), updated weekly. These statistics represent five years (2020 - 2024) of oversight of the Statewide Property Parcel Program. They highlight the need for improvements to the current data maintenance model.

As of October 24, 2024:
-	**90%** of towns are edited/updated by vendors or the town. 10% are edited/updated by VCGI (towns updated by VCGI are considered “not VT GIS Parcel Data Standard compliant”)
-	**10%** of submissions require edits to parcel topology (i.e., geometry) to address gaps and/or overlaps among parcels
-	**50%** of submissions required edits that were already made for the previous submission  (i.e., repeated revisions)
-	**70%** of submissions contain inactive parcels. Inactives exist for at least some towns that do not include them in their submissions
-	**96%** of towns include and represent rights-of-way. For those that do not, some map parcels to road centerlines, others only include main ROWs or those in the town/village center, and others have gaps in the parcel data where ROWs should be
-	**24%** of submissions are fully compliant with the current parcel data standard. 26% are compliant with minor edits, 37% are compliant with major edits, and 13% are not compliant (see [submittal criteria](#232-submittal-quality-criteria))
-	**11%** of towns have a mapping vendor (to the best of VCGI's knowledge) but have not submitted an update since the original Parcel Project data (prior to 2020). These towns are currently classified as “fully compliant” despite having stale data.
-	**12%** of submissions are/have been reviewed by towns prior to submittal; 64% have not, and 24% are unknown. Some vendors are working closely with towns as edits are being made (or edits are only being made at the direction of a town official), which may negate the need for a more formal review of the data prior to submission

## 2.3 Design

The design of a financial incentive to reward parcel data upkeep and quality improvements that is contingent on data submittal to the State should consider Municipal maintenance costs, be reflective of only those parcels that are changed (and thus need maintenance) since the last update, and potentially, account for cost differences by regional location and/or situation.

### 2.3.1 Support By Maintenance Type

- Make disbursement of this per parcel payment to municipalities contingent on submittal of [Vermont GIS Data Standard-compliant](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/02-k-VT_GIS_Parcel_Data_Standard.pdf) digital parcel data to VCGI, maximum payment once per year per town
- A payment should help compensate only for those parcels that are changed in geometry since the last update
- Per parcel payments may be administered and normalized by proposed Regional Appraisal Districts

A financial incentive to assist [JURISDICTION] with the cost of parcel mapping that is contingent on data standard-compliant parcel geometry submissions to VCGI could be designed to close this “participation gap” while improving data quality. An incentive is preferable to a submittal requirement as the latter may not be possible for some towns and could be challenging to enforce. An incentive, when combined with the fact that standardized GIS parcel data exist statewide (albeit with varied recency), may be enough to enable the remaining 10-15% of towns without GIS parcel data maintenance to begin upkeep and improvement. Creating incentives to increase data maintenance and sharing was also a recommended consideration in the [2015 Vermont Statewide Digital Parcel Lifecycle & Maintenance Plan](https://vcgi.vermont.gov/sites/vcgiupdate/files/doc_library/VT_Parcel%20Data%20Lifecycle%20and%20Maintenance%20Plan_2015_FINAL.pdf):

> As implementation shifts into a maintenance stage, Vermont will want to pay close attention to challenges to compliance. While some impediments may be more attitudinal than logistical or economic, the state may want to consider creating incentives to comply.

Other states have implemented similar contingent financial incentives to maintain foundational, local spatial data (Massachusetts, for example, [with their 911 addressing data](https://www.mass.gov/doc/standard-for-digital-parcels-and-related-data-sets-version-3/download)). Assuming that municipalities remain responsible for and the authoritative source of land records, 
[It is time to consider supporting Vermont municipalities in the upkeep of parcel data on which many State programs now depend.]

### 2.3.1 Eligibility

- VCGI will continue to accept and review parcel geometry updates on a rolling basis. A municipal official (or a contact from a municipality's mapping vendor) must send a standard-compliant parcel geometry update to VCGI by October 1st of a calendar year to be eligible to receive a financial incentive the following year
- No more than one standard-compliant parcel geometry update per municipality will be accepted each calendar year
- Parcel geometry updates will continued to be submitted to VCGI using the [Share Map Data](https://vcgi.vermont.gov/data-and-programs/share-map-data) form
- VCGI should be notified if a municipality has no changes to report. A municipality that reports no changes will not be eligible to receive a financial incentive
- Some municipalities may choose to “opt-out,” forgoing their eligibility in exchange for VCGI assisting in their parcel geometry update Municipalities that may be good candidates to opt-out include:
    - Municipalities not currently updating their parcel geometry, contracting with a non-GIS vendor, or having "low confidence" in their ability to conduct parcel geometry updated internally
    - Municipalities with a relatively small parcel count or relatively few parcel geometry updates

### 2.3.2 Submittal Quality Criteria

|**Criteria**                | **Description/Examples**|
|:---------------------------|:------------------------|
|Fully Compliant             | •	Includes all towns that have not been updated since the Parcel Project (i.e., prior to 2020)<br>•	Valid topology; no gaps or overlaps among parcels<br>•	ROWs included and mapped correctly<br>•	Unmatched parcels only comprised of land expected to have no SPAN (common land, town/state/federally-owned land, etc.)<br>•	Multi-SPAN parcels (e.g., condos) are attributed correctly through the intersection table, if applicable<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly; does not require edits that were made in the previous submission; any unmatched parcels are expected to be unmatched given their status as common land, government-owned land, etc.; any multi-SPAN parcels are accounted for correctly in the intersection table. Includes towns that are working with a vendor to maintain parcels but have not submitted updates to VCGI since January 1, 2020.
|Compliant with Minor Edits  |•	Unmatched parcels (as received) are < 2%<br>•	ROWs included and mapped correctly<br>•	No/minimal repeated edits from prior submission during VCGI review<br>•	No/minimal (<10) edits to intersection table to account for multi-SPAN parcels<br>•	No topology errors<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard. Includes valid topology, SPANs, and ROWs that are mapped correctly. Requires minor editing to address unmatched parcels (<2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include <10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Compliant with Major Edits  |•	Unmatched parcels (as received) are > 2%<br>•	Topology errors resulting in gaps/overlaps among parcels<br>•	Incorrect or missing attribution of condos/multi-SPAN parcels in the intersection table<br>•	ROWs are missing or incomplete (e.g., parcels are mapped to road centerlines)<br>•	Repeated edits from prior submission during VCGI review<br><br>Summary: submission meets format and content requirements of the Parcel Data Standard to the extent that it can be incorporated into the statewide parcel dataset following revisions. May require significant edits to address topology errors, missing or invalid SPANs, missing or incomplete ROWs, and/or missing or incomplete multi-SPAN parcel representation in the intersection table. Requires editing to address unmatched parcels (>2% of town's total parcels) that should have SPANs and a match in the annual Grand List. May include >10 edits that were made in the prior submission and/or to account for multi-SPAN parcels in the intersection table.
|Not Compliant               |•	Includes all towns that are updated by VCGI/have no vendor or capacity to submit their own updates<br>•	Submission does not include SPANs or Parcel/Map IDs that can be linked to the Grand List<br>•	Submission is in an unusable format (e.g., CAD) that cannot be converted to a geodatabase<br>•	Usable format (i.e., GIS files) but missing or invalid fields that do not allow conversion to usable schema/dataset, or require significant effort to update using existing data and external sources/map viewers (e.g., loading existing attribution into new geometry; using E911, AxisGIS, or other to validate/verify SPANs; merging/splitting active and inactive parcels, etc.)<br><br>Summary: submission does not meet format and/or content allowing for inclusion in the statewide parcel dataset. Data format may be unusable/unable to convert to GIS, and/or attribution does not include valid SPANs or Parcel/Map IDs for linking to Grand List. May sometimes include a workable data format that requires significant geometry (e.g., active and inactive parcels) and/or attribute manipulation using internal and external data sources (e.g., AxisGIS sites, surveys, E911 data, etc.) to create dataset with valid schema and attribution. Also includes towns that do not have a vendor or the capacity to make their own edits and are updated by VCGI using data available in the VT Land Survey Library.

### 2.3.3 Communication and Timing

Text.

### 2.3.4 Funding

In November 2024 VCGI organized a focus group of 12 municipalities selected based on parcel count, location, and mapping vendor. A municipal official (Lister, Assessor, or Town Clerk) from each municipality was contacted by email and asked how much the municipality currently spends on parcel mapping. While sample size is a limiting factor, based on the information provided by the seven municipalities that responded, the cost of ongoing parcel data maintenance is less than the initial cost during the Parcel Project. This is true even for municipalities that are no longer contracting with their Parcel Project mapping vendor. The current cost per parcel averaged $2.66 compared to $5.87 during the Parcel Project (55% cost reduction).

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
-	In addition to submittal compliance criteria, a timeframe component is needed when assessing a town's eligibility for a per parcel payment (likely annual). Some towns are technically “compliant” and are working with a vendor but have not submitted an update to VCGI since before 2020. For small towns that may not have any changes from year to year (and therefore do not submit an update), VCGI should still receive an annual confirmation that no changes or updates are needed to the existing data
-	Consider possible tiered system for payments to encourage compliance. For example: fully compliant or minor edit towns receive full amount, major edit town receive 50%, and non-compliant towns receive none
-	Based on vendor discussions, it is not necessarily practical or feasible for vendors to directly use parcel data published by VCGI (e.g., vendors are not downloading the latest data for a town from VCGI prior to making their next round of edits). Often vendors are maintaining additional fields and formats beyond what is submitted and used by VCGI. This is likely a factor leading to repeated edits with each submission. Consider a way to summarize and communicate submission issues or edits that VCGI makes so vendors are aware and can correct for their subsequent submission, ideally without creating significant extra work for either VCGI or vendor. 

## 2.4 Example Statute Update

Text.

## 2.5 Implementation

Text.

# Recommendation 3

# Recommendation 4

# Recommendation 5

# Recommendation 6

# Recommendation 7

# Recommendation 8

# Recommendation 9

![CU](https://github.com/user-attachments/assets/c43d6573-861f-4f47-9e32-6099e8c4bf77)
**Figure X:** *Parcels enrolled in Current Use statewide.*

In addition, Current Use parcels may only have a percentage of their acreage enrolled. The statewide average enrollment is 92.5%, with 75% of parcels between 92-100%.

![CUenrolled](https://github.com/user-attachments/assets/996dcba9-2c36-42b0-bb1d-adc21e6fcc26)
**Figure X:** *Example of parcels enrolled in Current Use, with percent of acreage enrolled.*

# Recommendation 10

# Recommendation 11

# Recommendation 12

# Future Improvements

# Appendices

## Appendix: Maps and Tables

### X.X Lands in Current Use Needing Administrative Definition for Acreage

A change to the parcel defintion would have impacts on parcels enrolled in [Current Use](https://tax.vermont.gov/property/current-use/property-types). A primary requirement for eligibility is at least 25 acres of contiguous land in active agricultural use or forested land managed to state standard and an approved forest management plan. Parcels containing inactives and enrolled in Current Use may become eligible based on acreage if a parcel is defined by separate and sellable pieces of real estate rather than by common ownership. In the example below, the green parcel contains four inactive parcels; the "ACTIVE" status parcel is 70.64 acres, however, so this parcel would still be eligible for Current Use. The red parcel, however, is comprised of two inactives where the "ACTIVE" status parcel is 10.28 acres. As such, it would no longer be eligibile for Current Use based on acreage. This example also highlights the implications associated with which parcel receives the "ACTIVE" status. Brown parcels are enrolled in Current Use but do not contain inactive(s). The eligibility of these parcels for Current Use would not be impacted by a change to the parcel defintion. [Explore parcels enrolled in Current Use](https://arcg.is/1vXL4u1) and potential eligibility impacts associated with a change to the parcel definition.

![CU_ActiveInactive](https://github.com/user-attachments/assets/5b8af80f-80aa-4dd3-811c-c13f350bfc14)

**Figure X:** *Example of parcels enrolled in Current Use and containing inactive parcels (red and green). Based on the status of a parcel ("ACTIVE" or "INACTIVE") and the acreage, eligibility for Current Use could be impacted with a change to the parcel definition. The acreage eligibility for parcels enrolled in Current Use and without any inactives (brown parcels) would not be impacted by a change to the parcel defintion.*

Examining Current Use parcels with inactives statewide, the following impacts are seen by town:

![Inactives_CU](https://github.com/user-attachments/assets/16d095e6-ec20-405c-b295-f8a07145bd24)

**Figure X:** *Count of parcels with at least one inactive parcel and enrolled in current use (2023), by town.*

Total bar count represents parcels per town enrolled in Current Use and with at least one inactive. Green count represents parcels whose parent parcel is >25 acres, deeming the parcel still eligible for Current Use under the new parcel definition. Red count represents parcels whose parent parcel is <25 acres and therefore no longer eligible for Current Use based on acreage. 

![image](https://github.com/user-attachments/assets/0364e196-1b06-429d-8f6b-58178a1cd86c)

**Table X:** *Count and percentage of parcels with at least one inactive parcel and enrolled in current use, by town. Approximately 32% of parcels statewide would lose their eligibility for current use based on acreage following a change to the parcel definition.*

Note: inactive parcels are not managed consistently across towns; currently 178 towns (70%) submit inactive parcels. In addition, attribution of the parcel status field (active/inactive) is not complete or consistent for all submitting towns. This analysis is based on a subset of 138 towns with inactives and a presumably accurate "STATUS" field. This means the parent parcel has an "ACTIVE" status and all associated "INACTIVE" status parcels have a PARENTSPAN matching the "ACTIVE" status SPAN. 

![ActiveInactive](https://github.com/user-attachments/assets/9ebd72bc-9f34-4c54-aa2a-e930529b9803)

**Table X:** *Example of correct attribution in the inactive parcel layer. The parcel with an "ACTIVE" status has a SPAN entry, followed by the associated "INACTIVE" status parcels with PARENTSPAN entries linking them to the "ACTIVE" parcel. In the Active Parcels layer, these five parcels would be merged to a single parcel. In some cases, "INACTIVE" status parcels may also include a unique SPAN entry. Typically these are placeholders used by town officials.*