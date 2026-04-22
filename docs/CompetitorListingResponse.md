# CompetitorListingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**competitors** | [**List[CompetitorCompany]**](CompetitorCompany.md) | List of competitors for the target company | [optional] 

## Example

```python
from ninjapear.models.competitor_listing_response import CompetitorListingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorListingResponse from a JSON string
competitor_listing_response_instance = CompetitorListingResponse.from_json(json)
# print the JSON string representation of the object
print(CompetitorListingResponse.to_json())

# convert the object into a dict
competitor_listing_response_dict = competitor_listing_response_instance.to_dict()
# create an instance of CompetitorListingResponse from a dict
competitor_listing_response_from_dict = CompetitorListingResponse.from_dict(competitor_listing_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


