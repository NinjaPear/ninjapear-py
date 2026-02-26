# AddTargetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **str** | Website URL of the company to monitor | 
**settings** | [**TargetSettings**](TargetSettings.md) |  | [optional] 

## Example

```python
from ninjapear.models.add_target_request import AddTargetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddTargetRequest from a JSON string
add_target_request_instance = AddTargetRequest.from_json(json)
# print the JSON string representation of the object
print(AddTargetRequest.to_json())

# convert the object into a dict
add_target_request_dict = add_target_request_instance.to_dict()
# create an instance of AddTargetRequest from a dict
add_target_request_from_dict = AddTargetRequest.from_dict(add_target_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


