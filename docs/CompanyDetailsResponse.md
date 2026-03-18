# CompanyDetailsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**websites** | **List[str]** | List of all company website URLs | [optional] 
**description** | **str** | A brief description of the company | [optional] 
**industry** | **int** | GICS 8-digit industry code | [optional] 
**company_type** | **str** | Type of company | [optional] 
**founded_year** | **int** | Year the company was founded | [optional] 
**specialties** | **List[str]** | List of company specialties | [optional] 
**name** | **str** | Company name | [optional] 
**tagline** | **str** | Company tagline or slogan | [optional] 
**logo_url** | **str** | URL to the company logo endpoint | [optional] 
**cover_pic_url** | **str** | URL to the company&#39;s cover/banner image | [optional] 
**facebook_url** | **str** | Facebook profile URL | [optional] 
**twitter_url** | **str** | Twitter/X profile URL | [optional] 
**instagram_url** | **str** | Instagram profile URL | [optional] 
**employee_count** | **int** | Estimated number of employees | [optional] 
**employee_count_range_min** | **int** | Lower bound of employee count range (only with include_employee_count&#x3D;true) | [optional] 
**employee_count_range_max** | **int** | Upper bound of employee count range (only with include_employee_count&#x3D;true) | [optional] 
**addresses** | [**List[Address]**](Address.md) | List of company addresses | [optional] 
**executives** | [**List[Executive]**](Executive.md) | List of company executives and board members | [optional] 
**public_listing** | [**PublicListing**](PublicListing.md) | Public company data. Null for private companies. | [optional] 
**follower_count** | **int** | Twitter/X follower count (only included when follower_count&#x3D;include query param is used) | [optional] 
**following_count** | **int** | Twitter/X following count (only included when follower_count&#x3D;include query param is used) | [optional] 
**similar_companies** | **str** | URL to the competitor listing endpoint for this company | [optional] 
**updates** | **str** | URL to the company updates endpoint for this company | [optional] 
**funding** | **str** | URL to the company funding endpoint for this company | [optional] 

## Example

```python
from ninjapear.models.company_details_response import CompanyDetailsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CompanyDetailsResponse from a JSON string
company_details_response_instance = CompanyDetailsResponse.from_json(json)
# print the JSON string representation of the object
print(CompanyDetailsResponse.to_json())

# convert the object into a dict
company_details_response_dict = company_details_response_instance.to_dict()
# create an instance of CompanyDetailsResponse from a dict
company_details_response_from_dict = CompanyDetailsResponse.from_dict(company_details_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


