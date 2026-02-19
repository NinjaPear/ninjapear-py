# Address


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address_type** | **str** | Type of address | [optional] 
**line1** | **str** | Street address line 1 | [optional] 
**line2** | **str** | Street address line 2 | [optional] 
**city** | **str** | City name | [optional] 
**state** | **str** | State, province, or region | [optional] 
**postal_code** | **str** | Postal/ZIP code | [optional] 
**country_code** | **str** | ISO 3166-1 alpha-2 country code | [optional] 
**country** | **str** | Full country name | [optional] 
**is_primary** | **bool** | Whether this is the primary address | [optional] 

## Example

```python
from ninjapear.models.address import Address

# TODO update the JSON string below
json = "{}"
# create an instance of Address from a JSON string
address_instance = Address.from_json(json)
# print the JSON string representation of the object
print(Address.to_json())

# convert the object into a dict
address_dict = address_instance.to_dict()
# create an instance of Address from a dict
address_from_dict = Address.from_dict(address_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


