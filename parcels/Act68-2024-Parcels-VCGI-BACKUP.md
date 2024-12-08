# Act 68 VCGI - Backup

This document is for backup or extra sections of the Act 68 Part II report by VCGI.

# Recommendation 1

# Recommendation 2

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