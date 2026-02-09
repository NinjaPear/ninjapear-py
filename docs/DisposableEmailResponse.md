# DisposableEmailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** | The email address that was checked | [optional] 
**is_disposable_email** | **bool** | Whether the email domain is a known disposable/temporary email provider | [optional] 
**is_free_email** | **bool** | Whether the email domain is a free email provider | [optional] 

## Example

```python
from ninjapear.models.disposable_email_response import DisposableEmailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DisposableEmailResponse from a JSON string
disposable_email_response_instance = DisposableEmailResponse.from_json(json)
# print the JSON string representation of the object
print(DisposableEmailResponse.to_json())

# convert the object into a dict
disposable_email_response_dict = disposable_email_response_instance.to_dict()
# create an instance of DisposableEmailResponse from a dict
disposable_email_response_from_dict = DisposableEmailResponse.from_dict(disposable_email_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


