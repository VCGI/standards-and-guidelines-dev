# Purpose and Goals

Text.

# Overview of All Recommendations

| **Recommendation**                                                                      | **Statute Change** | **Payment** | **Technical Guidance** | **New Technology** |
|:---------------------------------------------------------------------------------------:|:------------------:|:-----------:|:----------------------:|:------------------:|
| [1. Update Parcel Definition in VT Statute](#recommendation-1-update-parcel-definition-in-vt-statute)                                              | X                  |             |                        |                    |
| [2. Reward Standardized Digital Parcel Data Submittal to SoV via Per Parcel Fee](#recommendation-2-reward-digital-parcel-submittal-to-sov-via-per-parcel-fee)          | X                  | X           |                        |                    |
| 3. Implement VT CAMA Data Standard and Require Submittal to SoV                       | (X)                |             | X                      |                    |
| 4. Clarify Right-of-Way Mapping for Tax Purposes in VT Statute                          | X                  |             |                        |                    |
| 5. Clarify Grand List vs. GIS Acreage Guidance                                          |                    |             | X                      |                    |
| 6. Acquire and Publish Annual High Resolution Imagery and Offer Buy-Up Imagery Contract |                    |             | X                      | X                  |
| 7. Offer Updated Statewide Parcel Contract Guidance for Municipalities                  |                    |             | X                      | X                  |
| 8. Pilot Remotely-Sensed Tools to Support Appraisals                                    |                    |             |                        | X                  |
| 9. Modernize Current Use Map Standards and Submittals                                   |                    |             |                        | X                  |
| 10. Consider Updating and Moving Parcel Program in VT Statute                           | X                  |             |                        |                    |
| 11. Coordinate With Concurrent Efforts to Digitize Land Records                         |                   |             |                        | X                   |

# Recommendation 1: Update Parcel Definition in VT Statute

Text.

## Related VT Statutes

Text.

# Recommendation 2: Reward Digital Parcel Submittal to SoV via Per Parcel Fee

Text.

# Recommendation 3: Implement VT CAMA Data Standard and Require Submittal to SoV

Text.

## CAMA Data Standard Components

### Implement Changes to Parcel Definition

### Normalize Attribution and Mapping of Unlanded Structures

**Background**

Statewide standardized parcel data in Vermont is currently comprised of parcel geometry, the approximate parcel boundary lines drawn as closed multi-sided shapes (parcel polygons) as sourced from municipalities, and parcel attribution from the annual Grand List collected and published by the Tax Department. These two components are joined together by a matching School Property Account Number (SPAN) in the attribute table of the parcel polygons layer and in the Grand List. In most cases, each polygon is joined to one Grand List record but it’s not uncommon for more than one Grand List record to be joined to the same polygon. This happens most often with condominiums as they are typically described by their percentage of undivided interest in the common area and facilities rather than discrete boundaries that can be easily represented by polygons. While VCGI has provided some guidance on mapping condominiums per the Vermont GIS Parcel Data Standard, a more comprehensive recommendation for mapping all types of unlanded structures is necessary to improve data quality, clarity, and ease of use.

**Current Unlanded Structure Mapping Practices in Vermont**

***
**Discrete and Distributed Methods**

Building footprints  are often used to visually distinguish between unlanded structures and the common land, particularly as a paper tax map convention. The difference between the “Distributed” and “Discrete” building footprint methods is whether or not the common land has a SPAN. Per the Vermont GIS Parcel Data Standard, “in some instances, a deed specifies a percentage of common land ownership to each condominium unit and the common land does not have a SPAN number. In other instances, a deed does not allocate the common land, and the common land does have a SPAN number.”

Image 1: Discrete Method Mapping of Condos

![image](https://github.com/user-attachments/assets/2ff17158-461a-490d-8062-6c014960c6f0)

Image 2: Distributed Method of Mapping Condos

![image](https://github.com/user-attachments/assets/b39db8ec-ef97-477d-b394-b303d2ff0c4d)

Image 1 and 2 Source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)

Pros
- Creates visual distinction between unlanded structures and common land
- Avoids potential confusion caused by the use of different GIS and Grand List SPANs in the Intersection Table
  
Cons
- Time intensive to create/maintain individual building footprints geometry

***
**Stacked Method**

Stacked polygons use a standalone Intersection Table to relate multiple SPANs from the Grand List to the same “placeholder” SPAN assigned to a polygon in the parcel data. 

Image 3: Relationship of Grand List SPANs and GIS (drawing) SPANs in Vermont Parcel Data

![image](https://github.com/user-attachments/assets/959a5b13-4dd0-484c-b064-758ae657ee00)

This creates identical polygons "stacked" on top of each other, which can be “flattened” to remove all but one polygon for each parcel for analytical purposes. Unlike the building footprints methods, there is no visual distinction between unlanded structures and the common land. Because to this, parcel geometry is simpler to maintain.

Image 4: Stacked Method Mapping of Condos

![image](https://github.com/user-attachments/assets/8da7e8ab-d3e0-4423-881a-1ce1e2a9d399)

Image 4 Source: [Wisconsin Condo Stack Tool Guide](https://www.sco.wisc.edu/parcels/tools/CondoStack/Condo_Stack_Tool_Guide.pdf)

Pros
- Geometry is easier to maintain when compared to the building footprints methods
- Geometry includes common land to reflect total, calculated acreage and is relatively easy to “flatten” stacked polygons for analysis purposes

Cons
- Requires the creation and maintenance of GIS SPANs in the Intersection Table

***
**Other Unlanded Structures Mapping Practices from Other States**

Parcel points are maintained by Dakota County in the State of Minnesota. This data layer is a compilation of tax parcel information, containing one record for each real estate/tax parcel identification number (PIN) within the county. Condominiums are included in this dataset (whereas they are not in the polygons).

Image 5: Parcel Points Method Mapping of Condos

![image](https://github.com/user-attachments/assets/3e0e0b19-c8eb-48ad-922e-44bcfc481928)

Image 5 Source: [Dakota County, Minnesota](https://gis.co.dakota.mn.us/DCGIS/)

Pros
- Already practiced by some Vermont municipalities internally
- Creates some visual distinction without subtracting from total, calculated acreage
  
Cons
- Requires the creation and maintenance of separate geometry layer

### Normalize Land Use Classification Codes

### Normalize Actual Year Built, Effective Year Built, and Unit Count Information 

## Require Standardized CAMA Data Submittal to SoV

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

# Appendices
