# Investor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Investor name | [optional] 
**website** | **str** | Investor website URL | [optional] 
**type** | **str** | Type of investor | [optional] 
**amount_usd** | **int** | Amount invested in USD (if known) | [optional] 

## Example

```python
from ninjapear.models.investor import Investor

# TODO update the JSON string below
json = "{}"
# create an instance of Investor from a JSON string
investor_instance = Investor.from_json(json)
# print the JSON string representation of the object
print(Investor.to_json())

# convert the object into a dict
investor_dict = investor_instance.to_dict()
# create an instance of Investor from a dict
investor_from_dict = Investor.from_dict(investor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


