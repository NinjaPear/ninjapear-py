# Target


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique target identifier | [optional] 
**website_url** | **str** | The website URL being monitored | [optional] 
**settings** | [**TargetSettings**](TargetSettings.md) |  | [optional] 
**last_polled_at** | **datetime** | When the target was last polled for updates | [optional] 
**is_baseline_complete** | **bool** | Whether the initial baseline poll has completed. Items are only generated after the baseline. | [optional] 
**created_at** | **datetime** | When the target was created | [optional] 

## Example

```python
from ninjapear.models.target import Target

# TODO update the JSON string below
json = "{}"
# create an instance of Target from a JSON string
target_instance = Target.from_json(json)
# print the JSON string representation of the object
print(Target.to_json())

# convert the object into a dict
target_dict = target_instance.to_dict()
# create an instance of Target from a dict
target_from_dict = Target.from_dict(target_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


