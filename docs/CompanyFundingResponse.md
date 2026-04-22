# CompanyFundingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website** | **str** | The company domain the response describes, echoed from the request. | [optional] 
**total_funds_raised_usd** | **int** | Total funds raised across all rounds in USD | [optional] 
**funding_rounds** | [**List[FundingRound]**](FundingRound.md) | List of funding rounds. Empty array on fresh-path failures (see &#x60;error_code&#x60;). | [optional] 
**credit_cost** | **int** | Total credits charged for this call (2 base + 1 per unique investor). Delivered in the response body rather than the &#x60;X-NinjaPear-Credit-Cost&#x60; header on cache misses, because streaming responses cannot set HTTP trailers. | [optional] 
**error** | **str** | Error message when funding data could not be extracted. Only present alongside &#x60;error_code&#x60;. | [optional] 
**error_code** | **str** | Present only on fresh-path failures (HTTP 200, streaming). Clients that previously branched on &#x60;status_code &#x3D;&#x3D; 404&#x60; should branch on this field. &#x60;no_funding_data&#x60; still charges the 2-credit base; &#x60;service_temp_unavailable&#x60; is not charged. | [optional] 

## Example

```python
from ninjapear.models.company_funding_response import CompanyFundingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyFundingResponse from a JSON string
company_funding_response_instance = CompanyFundingResponse.from_json(json)
# print the JSON string representation of the object
print(CompanyFundingResponse.to_json())

# convert the object into a dict
company_funding_response_dict = company_funding_response_instance.to_dict()
# create an instance of CompanyFundingResponse from a dict
company_funding_response_from_dict = CompanyFundingResponse.from_dict(company_funding_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


