# CustomerListingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customers** | [**List[CustomerCompany]**](CustomerCompany.md) | Companies that are probable customers of the target company | [optional] 
**investors** | [**List[CustomerCompany]**](CustomerCompany.md) | VC firms, PE funds, angel networks that have invested in the target company | [optional] 
**partner_platforms** | [**List[CustomerCompany]**](CustomerCompany.md) | Partners, platforms, or service providers the target company uses | [optional] 
**next_page** | **str** | Pagination URL for the next page of results | [optional] 

## Example

```python
from ninjapear.models.customer_listing_response import CustomerListingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerListingResponse from a JSON string
customer_listing_response_instance = CustomerListingResponse.from_json(json)
# print the JSON string representation of the object
print(CustomerListingResponse.to_json())

# convert the object into a dict
customer_listing_response_dict = customer_listing_response_instance.to_dict()
# create an instance of CustomerListingResponse from a dict
customer_listing_response_from_dict = CustomerListingResponse.from_dict(customer_listing_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


