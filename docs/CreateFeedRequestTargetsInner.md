# CreateFeedRequestTargetsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website_url** | **str** | Website URL of the company to monitor | 
**settings** | [**TargetSettings**](TargetSettings.md) |  | [optional] 

## Example

```python
from ninjapear.models.create_feed_request_targets_inner import CreateFeedRequestTargetsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFeedRequestTargetsInner from a JSON string
create_feed_request_targets_inner_instance = CreateFeedRequestTargetsInner.from_json(json)
# print the JSON string representation of the object
print(CreateFeedRequestTargetsInner.to_json())

# convert the object into a dict
create_feed_request_targets_inner_dict = create_feed_request_targets_inner_instance.to_dict()
# create an instance of CreateFeedRequestTargetsInner from a dict
create_feed_request_targets_inner_from_dict = CreateFeedRequestTargetsInner.from_dict(create_feed_request_targets_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


