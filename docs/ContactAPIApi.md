# ninjapear.ContactAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_disposable_email**](ContactAPIApi.md#check_disposable_email) | **GET** /api/v1/contact/disposable-email | Disposable Email Checker


# **check_disposable_email**
> DisposableEmailResponse check_disposable_email(email)

Disposable Email Checker

Check if an email address is a disposable (temporary/throwaway) email or a free email provider.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.disposable_email_response import DisposableEmailResponse
from ninjapear.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://nubela.co
# See configuration.py for a list of all supported configuration parameters.
configuration = ninjapear.Configuration(
    host = "https://nubela.co"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = ninjapear.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with ninjapear.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ninjapear.ContactAPIApi(api_client)
    email = 'test@mailinator.com' # str | The email address to check

    try:
        # Disposable Email Checker
        api_response = api_instance.check_disposable_email(email)
        print("The response of ContactAPIApi->check_disposable_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContactAPIApi->check_disposable_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **str**| The email address to check | 

### Return type

[**DisposableEmailResponse**](DisposableEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email check result |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

