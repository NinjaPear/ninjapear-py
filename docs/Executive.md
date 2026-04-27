# Executive


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Full name of the executive | [optional] 
**title** | **str** | Job title | [optional] 
**role** | **str** | Normalized role type | [optional] 
**person_profile_url** | **str** | Pre-filled URL to the Person Profile endpoint. Authenticate with your bearer token to fetch the executive&#39;s full profile. Null when first name or company website is missing. | [optional] 

## Example

```python
from ninjapear.models.executive import Executive

# TODO update the JSON string below
json = "{}"
# create an instance of Executive from a JSON string
executive_instance = Executive.from_json(json)
# print the JSON string representation of the object
print(Executive.to_json())

# convert the object into a dict
executive_dict = executive_instance.to_dict()
# create an instance of Executive from a dict
executive_from_dict = Executive.from_dict(executive_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


