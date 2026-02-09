# ninjapear.CustomerAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_customer_listing**](CustomerAPIApi.md#get_customer_listing) | **GET** /api/v1/customer/listing | Customer Listing


# **get_customer_listing**
> CustomerListingResponse get_customer_listing(website, cursor=cursor, page_size=page_size, quality_filter=quality_filter)

Customer Listing

Get a list of highly-probable customers, investors, and partners/platforms of a target company, categorized by relationship type.

**Cost:** 1 credit/request + 2 credits/company returned. Credits are charged even when the request returns an empty result.

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.customer_listing_response import CustomerListingResponse
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
    api_instance = ninjapear.CustomerAPIApi(api_client)
    website = 'https://www.stripe.com' # str | The website URL of the target company
    cursor = 'cursor_example' # str | Pagination cursor from `next_page` in a previous response (optional)
    page_size = 200 # int | Number of results per page (1-200, default 200) (optional) (default to 200)
    quality_filter = True # bool | Filter out low-quality results (junk TLDs and unreachable websites) (optional) (default to True)

    try:
        # Customer Listing
        api_response = api_instance.get_customer_listing(website, cursor=cursor, page_size=page_size, quality_filter=quality_filter)
        print("The response of CustomerAPIApi->get_customer_listing:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CustomerAPIApi->get_customer_listing: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL of the target company | 
 **cursor** | **str**| Pagination cursor from &#x60;next_page&#x60; in a previous response | [optional] 
 **page_size** | **int**| Number of results per page (1-200, default 200) | [optional] [default to 200]
 **quality_filter** | **bool**| Filter out low-quality results (junk TLDs and unreachable websites) | [optional] [default to True]

### Return type

[**CustomerListingResponse**](CustomerListingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response with customer listing |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

