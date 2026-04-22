# CompetitorCompany


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**company_details_url** | **str** | URL to the Company Details API endpoint for this competitor | [optional] 
**website** | **str** | Company website URL | [optional] 
**competition_reason** | **str** | Why this company is considered a competitor | [optional] 

## Example

```python
from ninjapear.models.competitor_company import CompetitorCompany

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorCompany from a JSON string
competitor_company_instance = CompetitorCompany.from_json(json)
# print the JSON string representation of the object
print(CompetitorCompany.to_json())

# convert the object into a dict
competitor_company_dict = competitor_company_instance.to_dict()
# create an instance of CompetitorCompany from a dict
competitor_company_from_dict = CompetitorCompany.from_dict(competitor_company_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


