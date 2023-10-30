# API Data Types  
## Notes regarding the usage of data type field in API JSON responses.  
Status: <code style="color : name_color">DRAFT</code>

## Defining a Set of Data Types
A well-defined, robust, and consistent set of data types is essential for well-designed Web APIs, metadata schematics, and data dictionaries. When designing an API, 
one of the key challenges is to select a suite of data types that simultaneously adhere to the following principles: maximize specificity, maintain interoperability, 
accommodate third party datasets, and sustain strict adherence once established. Nearly every programming language and database technology uses different data types. 
Interoperability is highly variable. Beginning with a simple common set of primitive data types, many types are further refined by specifying a standard set of formats, 
such as specific strings and composite types (e.g., arrays, dict). These difficulties are amplified when a wide array of datasets adopts a single response schema. A 
standardized response requires that data types in existing third-party datasets map to the standard set utilized by the API prior to ingesting.

## NCMNS API Data Types
The data types in the NCMNS API are an extended set that is mainly based on the RFC Standards, OpenAPI Specification and the JSON Schema Specification. In addition, an extensive amount of literature and web-based resources were assessed to assure interoperability, refine format specifications, and create a comprehensive terminology taking ideas from across data communities. References to the support publications and resources are provided in the table labeled Resources.
The table below outlines the NCMNS API data types, followed by a list of additional resources and source information.

The table below outlines the NCMNS API data types followed by a list of additional resources and source information.  

### Core (Primitive) Data Types
| Data Type | Definition | Type | Remarks |
| --------- | ---------- | ---- | ------- |
| String  | An alphanumeric sequence of zero or more unicode characters | Primitive | |
| Number  | Any number with or without decimals | Primitive | |
| Integer | A whole number, may be positive or negative | Primitive | |
| Boolean | A binary value (true/false, 0/1) | Primitive | |


### Format Specifications 
Several data types may be further defined using an optional format option. These are extensions of the primitive core data type in the table above. Accordingly, they inherit the characteristics of the primitive then extended by a defined format usually by a globally recognized standard (RFC). The purpose for the format extesnions is to provide an additional level of specificty to a given attribute. 
| Data Type | Format | Definition | Reference |
| --------- | ------ | ---------- | --------- |
| Number  | float | Single-precision floating point number (number with decimal fractions or not a whole number) | IEEE 754 |
| Number  | double | Double-precision floating point number (number with decimal fractions or not a whole number) | IEEE 754 |
| Integer | int32 | 32-bit integer (whole number stored as 32 zeros and ones) that ranges from -2147483648 to 2147483647 | |
| Integer | int64 | 64-bit integer (whole number stored as 64 zeros and ones) that ranges from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | |
| string 	| date 	| Fully defined date (day, month, and year) | RFC3339 |
| string 	| date-time |	Concatenated value of a fully-defined date (day, month, and year) and time (hour, minute, second (optional) | RFC3339 |
| string 	| URI |	Uniform Resource Identifier according to RFC 3986 that uses US-ASCII characters only | RFC3339 |
| string 	| URL |	Uniform Resource Locator, a URI for the web allowing the URI to be located using standard web protocols | RFC3339 |
| string | IRI | Internationalized Resource Identifier, Expanded version of URI to include all unicode characters | RFC 3987 |

## Structural/Composite/Complex Data Types
| Name | Definition | Remarks |
| ---- | ---- | ---------- |
| Value Domain | The set of valid textural values defined by one or more constraints within infite space | Types of Value Domains: Enumerated Domains, |
| Enumerated Domain | A type of value domain that contains a finite set of valid values | All values are string data type, also refered to as picklists, valid value sets |
| Array   | An ordered (indexed), fixed-length set of values | Complex | | |
