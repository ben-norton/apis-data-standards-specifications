# Value Domains
As defined in ISO 11179 [1], a value domain is a set of permissible values. Another way to think about value domains is within the concept of infinite space, which we define as every possible combination of Unicode alphanumeric characters. 
Each term contains values collectively derived from a specific combination(s) of characters within the larger infinite space. Values domains were created to address a need to define the combinations. Over time, commonalities between value domains provided the criteria to further categorize them based on the nature of the mechanism (e.g., fixed list and text pattern).

## Value Domain Properties 
1. All values must be the same data type in a value domain
2. Value domains are referenced by name or universal identifier
3. Individual values in an enumerated domain may be referenced using a number or abbreviation, referred to as an enumerated value code. Using a set of codes can significantly improve the performance and readability of a dataset and the associated API endpoint.

## Types of Value Domains
| Domain Type | Definition | Example(s) | Remarks |
| ----------- | ---------- | ---------- | ------- |
| Enumerated  | Fixed list of all permissible values | Gender: [m, f, o] Commonly referred to as lookup tables, picklists, and valid value sets |
| Described   | Value domain defined by one or more expressions, patterns, or formats that values must adhere too | date, URL, email address  | Also referred to as non-enumerated domains |
| Range | Defines the upper and lower bounds of a number using a maximum and minimum numeric value | -180 > n < 180 (latitude) | Only applies to numeric data types |
| Boolean | The specific pair of binary values used by a term with boolean data type | [0,1], [true/fals] | Where not explicitly defined, the boolean value domain is assumed to be true/false which adheres to the JSON Specification |

## Additional Information
1. Conceptual domains are sets of value meanings commonly presented using a list of concepts or descriptions. They describe the set of concepts that can be represented within a data element. 'US States' is an example, which describes the set of concepts (the geopolitical units comprising the United States) but does not specify their values (the actual state names or abbreviations). Most conceptual domains are associated with one or more value domains (e.g., US States by region, where the meaning remains the same, but the fixed list changes). In contrast, the associated value domain contains the actual names of the states (which is technically an enumerated domain since the list is fixed). [2]

## Resources
* Generic Statistical Information Mode (GSIM) (https://statswiki.unece.org/display/clickablegsim/GSIM+on+a+page)
* PDS 4 Data Dictionary Specification (https://pds.nasa.gov/datastandards/dictionaries/index-1.17.0.0.shtml)
* Data Dictionary for Preservation Metadata: PREMIS version 3.0 (2015) Preservation Metadata Maintenance Activity (PREMIS) Available Online at https://www.loc.gov/standards/premis/v3/premis-3-0-final.pdf.
* Monge, A. (2006) Database design with UML and SQL. 4th Edition. Available online at https://web.csulb.edu/colleges/coe/cecs/dbdesign/dbdesign.php?page=intro.html#maincontent.

## References  
[1] ISO/IEC 11179-1:2015(en) Information technology — Metadata registries (MDR) — Part 1: Framework (https://www.iso.org/obp/ui/#iso:std:iso-iec:11179:-1:ed-3:v1:en) 
[2] Loshin, D. (2011) The Practitioner's Guide to Data Quality Improvement. Morgan Kaufmann Publishers Inc. https://doi.org/10.1016/C2009-0-17212-4
