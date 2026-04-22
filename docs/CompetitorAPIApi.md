# ninjapear.CompetitorAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_competitor_listing**](CompetitorAPIApi.md#get_competitor_listing) | **GET** /api/v1/competitor/listing | Competitor Listing


# **get_competitor_listing**
> CompetitorListingResponse get_competitor_listing(website)

Competitor Listing

Discover direct business competitors of a target company. Competitors are identified via organic keyword overlap and AI-powered product comparison.

**Cost:** 2 credits/competitor returned. Minimum 5 credits per request.

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.competitor_listing_response import CompetitorListingResponse
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
    api_instance = ninjapear.CompetitorAPIApi(api_client)
    website = 'https://www.stripe.com' # str | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.

    try:
        # Competitor Listing
        api_response = api_instance.get_competitor_listing(website)
        print("The response of CompetitorAPIApi->get_competitor_listing:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompetitorAPIApi->get_competitor_listing: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 

### Return type

[**CompetitorListingResponse**](CompetitorListingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response with competitor listing |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

