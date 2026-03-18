# CompanyUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | URL of the update/post | [optional] 
**title** | **str** | Title of the update | [optional] 
**description** | **str** | Brief description or excerpt | [optional] 
**image_url** | **str** | Associated image URL (if any) | [optional] 
**timestamp** | **str** | Publication timestamp (ISO 8601 format) | [optional] 
**source** | **str** | Source of the update | [optional] 

## Example

```python
from ninjapear.models.company_update import CompanyUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyUpdate from a JSON string
company_update_instance = CompanyUpdate.from_json(json)
# print the JSON string representation of the object
print(CompanyUpdate.to_json())

# convert the object into a dict
company_update_dict = company_update_instance.to_dict()
# create an instance of CompanyUpdate from a dict
company_update_from_dict = CompanyUpdate.from_dict(company_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


