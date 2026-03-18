# PersonProfileResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique person identifier | [optional] 
**slug** | **str** | Person&#39;s slug identifier | [optional] 
**profile_pic_url** | **str** | Profile picture URL | [optional] 
**first_name** | **str** | First name | [optional] 
**middle_name** | **str** | Middle name | [optional] 
**last_name** | **str** | Last name | [optional] 
**full_name** | **str** | Full name | [optional] 
**bio** | **str** | Professional bio/summary | [optional] 
**follower_count** | **int** | X/Twitter follower count | [optional] 
**following_count** | **int** | X/Twitter following count | [optional] 
**country** | **str** | Country | [optional] 
**city** | **str** | City | [optional] 
**state** | **str** | State/province | [optional] 
**x_handle** | **str** | X/Twitter handle | [optional] 
**x_profile_url** | **str** | X/Twitter profile URL | [optional] 
**personal_website** | **str** | Personal website URL | [optional] 
**work_experience** | [**List[WorkExperience]**](WorkExperience.md) | Work experience history | [optional] 
**education** | [**List[Education]**](Education.md) | Education history | [optional] 

## Example

```python
from ninjapear.models.person_profile_response import PersonProfileResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PersonProfileResponse from a JSON string
person_profile_response_instance = PersonProfileResponse.from_json(json)
# print the JSON string representation of the object
print(PersonProfileResponse.to_json())

# convert the object into a dict
person_profile_response_dict = person_profile_response_instance.to_dict()
# create an instance of PersonProfileResponse from a dict
person_profile_response_from_dict = PersonProfileResponse.from_dict(person_profile_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


