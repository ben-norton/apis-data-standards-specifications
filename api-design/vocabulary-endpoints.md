# Vocabulary Reference URLs
<span style="color:red">Status: **Draft** </span>

Design specifications for the provision of data dictionaries/vocabularies through APIs. The URLs are maintained as static properties associated with every resource in the Vocabulary Resource Class. 
Each resource is identifiable through a pair of URLs with differing schemas: a GUID based URL that is machine-readable and a name-based URL that's human-readable
  
## Data Dictionary  
| Type | URL Pattern |
| -- | -- |
| GUID | https://domain.org/api/v2/vocabularies/defined-term-set?guid=xxxx |
| Name | https://domain.org/api/v2/vocabularies/defined-term-set/{data-dictionary-name} |
  
## Dictionary Terms  
| Type | URL Pattern |
| -- | -- |
| GUID | https://domain.org/api/v2/vocabularies/defined-term?guid=xxxx |
| Term Name | https://domain.org/api/v2/vocabularies/defined-term/{data-dictionary-name}/{term-name |
  
## Notes
- DefinedTermSet and DefinedTerm belong to the schema.org specifications
- All data dictionaries are types of DefinedTermSets (Resource Type: Data Dictionary = Defined Term Set)
- All terms that belong to a data dictionary equivalent to the schema.org object DefinedTerms and belong to a DefinedTermSet (Resource Type: Dictionary Term = DefinedTerm)

- Term names are not globally unique. Therefore, a URL that references only the term name is not a viable reference URL.
- Term names are always unique within the scope of the parent data dictionary. Therefore, URLs referenced by the term name must include the name of the parent data dictionary in the URL

Name Format
Lowercase form of model name with words separated by hyphens
Example: ReptileDatabaseDataDictionary
{data-dictionary-name} = {reptile-database-data-dictionary} or https://domain.org/api/v2/vocabularies/defined-term-set/reptile-database-data-dictionary




