# CustomerCompany


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Company name | [optional] 
**description** | **str** | A brief description of the company | [optional] 
**tagline** | **str** | Company tagline or slogan | [optional] 
**website** | **str** | Company website URL | [optional] 
**company_logo_url** | **str** | URL to the Company Logo API for this company | [optional] 
**id** | **str** | Unique identifier | [optional] 
**industry** | **int** | GICS 8-digit industry code | [optional] 
**specialties** | **List[str]** | List of company specialties | [optional] 
**x_profile** | **str** | X (Twitter) profile URL | [optional] 

## Example

```python
from ninjapear.models.customer_company import CustomerCompany

# TODO update the JSON string below
json = "{}"
# create an instance of CustomerCompany from a JSON string
customer_company_instance = CustomerCompany.from_json(json)
# print the JSON string representation of the object
print(CustomerCompany.to_json())

# convert the object into a dict
customer_company_dict = customer_company_instance.to_dict()
# create an instance of CustomerCompany from a dict
customer_company_from_dict = CustomerCompany.from_dict(customer_company_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


