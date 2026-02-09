# ninjapear.CompanyAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_company_logo**](CompanyAPIApi.md#get_company_logo) | **GET** /api/v1/company/logo | Company Logo


# **get_company_logo**
> bytearray get_company_logo(website)

Company Logo

Retrieve the logo of a company given its website URL. Returns the logo as a PNG image (128x128).

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
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
    api_instance = ninjapear.CompanyAPIApi(api_client)
    website = 'https://www.stripe.com' # str | The website URL of the target company

    try:
        # Company Logo
        api_response = api_instance.get_company_logo(website)
        print("The response of CompanyAPIApi->get_company_logo:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompanyAPIApi->get_company_logo: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL of the target company | 

### Return type

**bytearray**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/png, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Company logo as PNG image |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**404** | No logo found for the given domain |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

