# FeedSummary

Feed summary returned in list endpoints (without individual targets).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique feed identifier | [optional] 
**name** | **str** | Feed display name | [optional] 
**is_public** | **bool** | Whether the RSS feed is publicly accessible without a token | [optional] 
**is_suspended** | **bool** | Whether the feed is currently suspended | [optional] 
**suspension_reason** | **str** | Reason for suspension, if suspended | [optional] 
**rss_url** | **str** | URL to the RSS feed | [optional] 
**created_at** | **datetime** | When the feed was created | [optional] 
**target_count** | **int** | Number of active targets in this feed | [optional] 

## Example

```python
from ninjapear.models.feed_summary import FeedSummary

# TODO update the JSON string below
json = "{}"
# create an instance of FeedSummary from a JSON string
feed_summary_instance = FeedSummary.from_json(json)
# print the JSON string representation of the object
print(FeedSummary.to_json())

# convert the object into a dict
feed_summary_dict = feed_summary_instance.to_dict()
# create an instance of FeedSummary from a dict
feed_summary_from_dict = FeedSummary.from_dict(feed_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


