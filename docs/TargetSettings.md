# TargetSettings

Monitoring settings for a target.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**monitor_blog** | **bool** | Whether to monitor the company&#39;s blog RSS feeds | [optional] [default to True]
**monitor_x** | **bool** | Whether to monitor the company&#39;s X (Twitter) account | [optional] [default to True]
**monitor_website** | **bool** | Whether to monitor the company&#39;s website for content changes | [optional] [default to True]
**frequency_days** | **int** | How often to poll for updates (in days) | [optional] [default to 7]

## Example

```python
from ninjapear.models.target_settings import TargetSettings

# TODO update the JSON string below
json = "{}"
# create an instance of TargetSettings from a JSON string
target_settings_instance = TargetSettings.from_json(json)
# print the JSON string representation of the object
print(TargetSettings.to_json())

# convert the object into a dict
target_settings_dict = target_settings_instance.to_dict()
# create an instance of TargetSettings from a dict
target_settings_from_dict = TargetSettings.from_dict(target_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


