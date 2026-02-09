# ninjapear.MetaAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_credit_balance**](MetaAPIApi.md#get_credit_balance) | **GET** /api/v1/meta/credit-balance | View Credit Balance


# **get_credit_balance**
> CreditBalanceResponse get_credit_balance()

View Credit Balance

Get your current credit balance.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.credit_balance_response import CreditBalanceResponse
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
    api_instance = ninjapear.MetaAPIApi(api_client)

    try:
        # View Credit Balance
        api_response = api_instance.get_credit_balance()
        print("The response of MetaAPIApi->get_credit_balance:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MetaAPIApi->get_credit_balance: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**CreditBalanceResponse**](CreditBalanceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current credit balance |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

