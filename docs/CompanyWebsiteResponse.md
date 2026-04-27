# CompanyWebsiteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**website** | **str** | The resolved canonical website URL. | [optional] 

## Example

```python
from ninjapear.models.company_website_response import CompanyWebsiteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyWebsiteResponse from a JSON string
company_website_response_instance = CompanyWebsiteResponse.from_json(json)
# print the JSON string representation of the object
print(CompanyWebsiteResponse.to_json())

# convert the object into a dict
company_website_response_dict = company_website_response_instance.to_dict()
# create an instance of CompanyWebsiteResponse from a dict
company_website_response_from_dict = CompanyWebsiteResponse.from_dict(company_website_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


