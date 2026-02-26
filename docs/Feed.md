# Feed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique feed identifier | [optional] 
**name** | **str** | Feed display name | [optional] 
**is_public** | **bool** | Whether the RSS feed is publicly accessible without a token | [optional] 
**is_suspended** | **bool** | Whether the feed is currently suspended (e.g. due to insufficient credits) | [optional] 
**suspension_reason** | **str** | Reason for suspension, if suspended | [optional] 
**rss_url** | **str** | URL to the RSS feed. Includes a token query parameter for private feeds. | [optional] 
**created_at** | **datetime** | When the feed was created | [optional] 
**targets** | [**List[Target]**](Target.md) | List of monitored targets in this feed | [optional] 

## Example

```python
from ninjapear.models.feed import Feed

# TODO update the JSON string below
json = "{}"
# create an instance of Feed from a JSON string
feed_instance = Feed.from_json(json)
# print the JSON string representation of the object
print(Feed.to_json())

# convert the object into a dict
feed_dict = feed_instance.to_dict()
# create an instance of Feed from a dict
feed_from_dict = Feed.from_dict(feed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


