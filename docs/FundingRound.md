# FundingRound


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**round_type** | **str** | Type of funding round | [optional] 
**var_date** | **str** | Date of the funding round | [optional] 
**amount_usd** | **int** | Amount raised in USD | [optional] 
**investors** | [**List[Investor]**](Investor.md) | List of investors in this round | [optional] 

## Example

```python
from ninjapear.models.funding_round import FundingRound

# TODO update the JSON string below
json = "{}"
# create an instance of FundingRound from a JSON string
funding_round_instance = FundingRound.from_json(json)
# print the JSON string representation of the object
print(FundingRound.to_json())

# convert the object into a dict
funding_round_dict = funding_round_instance.to_dict()
# create an instance of FundingRound from a dict
funding_round_from_dict = FundingRound.from_dict(funding_round_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


