# EmployeeCountResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**employee_count** | **int** | Estimated employee count | [optional] 

## Example

```python
from ninjapear.models.employee_count_response import EmployeeCountResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EmployeeCountResponse from a JSON string
employee_count_response_instance = EmployeeCountResponse.from_json(json)
# print the JSON string representation of the object
print(EmployeeCountResponse.to_json())

# convert the object into a dict
employee_count_response_dict = employee_count_response_instance.to_dict()
# create an instance of EmployeeCountResponse from a dict
employee_count_response_from_dict = EmployeeCountResponse.from_dict(employee_count_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


