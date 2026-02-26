# UpdateTargetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**settings** | [**TargetSettings**](TargetSettings.md) |  | 

## Example

```python
from ninjapear.models.update_target_request import UpdateTargetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTargetRequest from a JSON string
update_target_request_instance = UpdateTargetRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateTargetRequest.to_json())

# convert the object into a dict
update_target_request_dict = update_target_request_instance.to_dict()
# create an instance of UpdateTargetRequest from a dict
update_target_request_from_dict = UpdateTargetRequest.from_dict(update_target_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


