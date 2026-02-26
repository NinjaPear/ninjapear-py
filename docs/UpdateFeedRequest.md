# UpdateFeedRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | New feed name | [optional] 
**is_public** | **bool** | Whether the RSS feed should be publicly accessible | [optional] 
**is_suspended** | **bool** | Manually suspend or resume the feed | [optional] 
**suspension_reason** | **str** | Reason for suspension (required when is_suspended&#x3D;true) | [optional] 

## Example

```python
from ninjapear.models.update_feed_request import UpdateFeedRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFeedRequest from a JSON string
update_feed_request_instance = UpdateFeedRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateFeedRequest.to_json())

# convert the object into a dict
update_feed_request_dict = update_feed_request_instance.to_dict()
# create an instance of UpdateFeedRequest from a dict
update_feed_request_from_dict = UpdateFeedRequest.from_dict(update_feed_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


