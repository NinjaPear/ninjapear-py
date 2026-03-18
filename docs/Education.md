# Education


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**major** | **str** | Field of study | [optional] 
**school** | **str** | School/university name | [optional] 
**start_date** | **str** | Start date | [optional] 
**end_date** | **str** | End date | [optional] 

## Example

```python
from ninjapear.models.education import Education

# TODO update the JSON string below
json = "{}"
# create an instance of Education from a JSON string
education_instance = Education.from_json(json)
# print the JSON string representation of the object
print(Education.to_json())

# convert the object into a dict
education_dict = education_instance.to_dict()
# create an instance of Education from a dict
education_from_dict = Education.from_dict(education_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


