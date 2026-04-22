# WorkEmailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**work_email** | **str** | Best-effort work email address. &#x60;null&#x60; if no public email was found and no email pattern could be inferred from the domain. | 

## Example

```python
from ninjapear.models.work_email_response import WorkEmailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WorkEmailResponse from a JSON string
work_email_response_instance = WorkEmailResponse.from_json(json)
# print the JSON string representation of the object
print(WorkEmailResponse.to_json())

# convert the object into a dict
work_email_response_dict = work_email_response_instance.to_dict()
# create an instance of WorkEmailResponse from a dict
work_email_response_from_dict = WorkEmailResponse.from_dict(work_email_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


