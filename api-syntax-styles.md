# API Syntax and Style

\- Document Status: DRAFT

## Summary
This page contains information regarding the programmatic syntax specifications, coding styles, and best practices for an API.

## Request Endpoints  
### Structure  
[base url]/api/[version number]/[path]?parameters  
Example: https://domain.org/api/v2/resource?id=64fab1bd-1fa0-4cc7-b4de-6b0c2d306195

| Component | Definition |
| --- | --- |
| **base_url** | The root domain (and subdomain) in a URL. Base URLs are shared by every request https://data.naturalsciences.org) |
| **version_number** |  API Version. Endpoints are grouped and versioned at the resource class level. Currently, service endpoints use version 1.0. Data product and vocabulary endpoints use version 2.0. |
| **path** |  The hierarchical scheme used to generate paths is as follows: [resource class]/[resource type]/[resource name], which includes everything between the API version number and an optional 
trailing question mark to distinguish URL parameters from the path. |
| **parameters** |  Key-value pairs used to narrow the scope of an API request, parameters are separated from the path using a question mark (e.g., https://domain.org/api/v2/vocabularies?guid=|

**Specifications and Guidelines**

1. The path in the request URL reflects the hierarchical relationships in the underlying structure of the API (API Version > Resource Class > Resource Type > Resource)
2. Components ('subdirectories') in a path bound by two forward slashes are hyphenated, lowercase, and plural
3. The final part of a path (not bounded by a trailing forward slash) can be singular or plural depending on the nature of the requested resource.
4. Numeric or UUID identifiers are specified as URL parameters in the form key-value pairs for GET requests (e.g., https://domain.org/api/v1/users?id=23)
~~ 5. Numeric identifiers for POST, PATCH, and DELETE requests are path components (exceptions do occur) (e.g., https://domain.org/api/v1/users/23/update) ~~
5. UUID identifiers for POST, PATCH, and DELETE requests (exceptions do occur) (e.g., https://domain.org/api/v1/users/update?id=24e6c60d-d821-4b76-9c51-53b48cb3c983)
6. If two endpoints share a response body, then only one endpoint is needed. Every endpoint should return a unique response body.
7. Fewer endpoints are always better than more endpoints

## Responses

JSON datasets are hierarchical sets of key-value pairs in the following form:  "key": "value." Keys are commonly referenced as 'response parameters'.

### Keys

1. JSON keys are camel-cased and begin with a lowercase letter (camelCase)
2. Keys should not contain any reference to units of measurement (e.g., weight_g, weight_grams)
3. Keys with boolean data type are preceded with 'is' (e.g., isNullable, isEnumerated)
4. JSON arrays are special objects used to store collections at the same hierarchical level that can be indexed numerically. JSON arrays should only be used when structural
5. conditions meet the aforementioned special case in response bodies. Otherwise, nested information is annotated as objects.

### Values

1. Values should be of the corresponding key. For example, values for the key "gender" should not contain *?* or NA, those are not genders
2. Data types should not be mixed and preserved as defined. In JSON, strings are wrapped in double quotation marks. Integers are not. Accordingly, keys that contain
3. values that belong to the integer data type should not be wrapped in double quotation marks.

### Tabulated Conventions
### Resource Classes and Types  

| Use | Form | Casing | Separation | Example |
| -- | -- | -- | -- | -- |
| Formal (Preferred) Name | Singular | Proper | Whitespace | Data Dictionary |
| Path Identifier | Plural | Lowercase (all) | Hyphenated | data-dictionaries |
| JSON Key/Parameter | Plural | Camel-cased (first letter lowercase) | Capital Letter | dataDictionaries |
| Database Table | Plural | Lowercase (all) | Snake-casing | data_dictionaries |
| Database Column | Singular | Lowercase (all) | Snake-casing | last_modified |
| Database Table -Column Association | Not Applicable | Lowercase (all) | Dot (period) | data_dictionaries.last_modified |

Last Updated: 2022-04-25
