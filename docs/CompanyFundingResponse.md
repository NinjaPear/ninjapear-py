# CompanyFundingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_funds_raised_usd** | **int** | Total funds raised across all rounds in USD | [optional] 
**funding_rounds** | [**List[FundingRound]**](FundingRound.md) | List of funding rounds | [optional] 

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


