# CompanyUpdatesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blogs** | **List[str]** | List of blog/RSS source URLs discovered for the company | [optional] 
**x_profile** | **str** | X/Twitter profile URL for the company | [optional] 
**updates** | [**List[CompanyUpdate]**](CompanyUpdate.md) | List of recent updates sorted by date descending | [optional] 
**timestamp** | **str** | Timestamp of the API response (ISO 8601 format) | [optional] 

## Example

```python
from ninjapear.models.company_updates_response import CompanyUpdatesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyUpdatesResponse from a JSON string
company_updates_response_instance = CompanyUpdatesResponse.from_json(json)
# print the JSON string representation of the object
print(CompanyUpdatesResponse.to_json())

# convert the object into a dict
company_updates_response_dict = company_updates_response_instance.to_dict()
# create an instance of CompanyUpdatesResponse from a dict
company_updates_response_from_dict = CompanyUpdatesResponse.from_dict(company_updates_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


