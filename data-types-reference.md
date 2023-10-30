# Data Types Reference
---
## XSD Data Types
### Primitive Built-in 
| datatype | label | definition | source |
| -- | -- | -- | -- |
| duration | Duration | Length of a time interval defined using six components in order of decreasing significance year, month, day, hour, minute, and second (ISO 8601) |  |
| dateTime | Date and Time  | Represents instants of time, optionally marked with a particular time zone offset. Values may be viewed as objects with integer-valued year, month, day, hour and minute properties, a decimal-valued second property, and a boolean timezoned property. |  |
| time | Time |  |  |
| date | Date | Represents the date component of a datetime field where the values may be viewed as objects with integer-valued year, month, day, hour and minute properties, a decimal-valued second property, and a boolean timezoned property. |  |
| gYear | Year | A specific gregorian month in a specific gregorian year represented numerically (1999) |  |
| gDay | Day | a gregorian day that recurs, specifically a day of the month such as the 5th of the month. Arbitrary recurring days are not supported by this datatype. |  |
| gMonth | Month | A specific gregorian month that occurs every year (12) |  |
| gYearMonth | Month-Year | A specific gregorian month in a specific gregorian year represented numerically (1999-12) |  |
| gMonthDay | Month-Day | a gregorian date that recurs, specifically a day of the year such as the third of May. Arbitrary recurring dates are not supported by this datatype. |  |
| boolean |  | Boolean | Represents values of two-valued logic (true/false) |  |
| base64binary | Base64 Binary | Represents Base64-encoded arbitrary binary data with a value domain consisting of the set of finite-length sequences of binary octets. For base64Binary data the entire binary stream is encoded using the Base64 Alphabet in [RFC 2045].  |  |
| hexBinary |  HEX binary | Represents arbitrary hex-encoded binary data. The value domain is the set of finite-length sequences of binary octets.  |  |
| float |  Float | Numeric values that belong to the value domain consisting of values m × 2^e, where m is an integer whose absolute value is less than 2^24, and e is an integer between -149 and 104, inclusive, Patterned after the IEEE single-precision 32-bit floating point type  |  |
| double | Double | Numeric values that belong to the domain consisting of values m × 2^e, where m is an integer whose absolute value is less than 2^53, and e is an integer between -1075 and 970, inclusive |  |
| anyURI | Any URI |  a Uniform Resource Identifier Reference (URI). An anyURI value can be absolute or relative, and may have an optional fragment identifier |  |
| QName | QName | Represents XML qualified names. |  |
| NOTATION | XML Notation | Represents the Notation Attribute Type as defined in XML 1.0 with a value domain consisting of the QNames declarations in the XML document (https://www.w3.org/TR/xmlschema-2/#XML) |  |
| string  | Character String | Combination of one or more unicode characters |  |
| decimal | Decimal  | A subset of the real numbers, which can be represented by decimal numerals. | |



## JSON Schema

| Type | Definition |
| -- | -- |
| string  | Contains one of more unicode characters that includes letter, numbers, and puncutation marks |
| number  | Any numeric type, either integers or floating point numbers |
| integer | Numeric types that does not include floating point numbers  |
| object  | Set of one or more key-value pairs, keys are always strings, each pair is referred to as a property |
| array   | Ordered collections of elements, where each element may belong to a different data type |
| boolean | Binary set of values represented by true or false |
| null    | Missing values (not the same as an empty value) |  

Source: [http://json-schema.org/](http://json-schema.org/)  

## JSON
| Data Type | Category | Definition |
| -- | -- | -- |
| string | simple | Zero or more unicode characters that are wrapped with double quotation marks to distinquish strings from other data types |
| number | simple | Double-precision float-point numbers, not enclosed with quotation marks |
| boolean | simple | binary value represented using true and false, not enclosed with quotation marks |
| null | simple | Indicates that no value is assigned to the corresponding key (an empty string is not a null value), repsented by the word null without quotation marks |
| object | complex | unordered set of zero or more key/value pairs enclosed with braces, key-value pairs within a single object are separated with commas |
| array | complex | Ordered list of one or more objects enclosed with square brackets and separated by commas |  

Source: [https://www.json.org/json-en.html](https://www.json.org/json-en.html)  

## Mappings
### JSON - Python
| JSON | Python |
| -- | -- |
| string 	| string [4]	|
| number 	| int/float [5] |
| object 	| dict |
| array 	| list |
| boolean | bool |
| null		| None |


