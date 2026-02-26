# FeedListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**feeds** | [**List[FeedSummary]**](FeedSummary.md) | List of feeds | [optional] 

## Example

```python
from ninjapear.models.feed_list_response import FeedListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FeedListResponse from a JSON string
feed_list_response_instance = FeedListResponse.from_json(json)
# print the JSON string representation of the object
print(FeedListResponse.to_json())

# convert the object into a dict
feed_list_response_dict = feed_list_response_instance.to_dict()
# create an instance of FeedListResponse from a dict
feed_list_response_from_dict = FeedListResponse.from_dict(feed_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


