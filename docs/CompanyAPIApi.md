# ninjapear.CompanyAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_company_details**](CompanyAPIApi.md#get_company_details) | **GET** /api/v1/company/details | Company Details
[**get_company_funding**](CompanyAPIApi.md#get_company_funding) | **GET** /api/v1/company/funding | Company Funding
[**get_company_logo**](CompanyAPIApi.md#get_company_logo) | **GET** /api/v1/company/logo | Company Logo
[**get_company_updates**](CompanyAPIApi.md#get_company_updates) | **GET** /api/v1/company/updates | Company Updates
[**get_employee_count**](CompanyAPIApi.md#get_employee_count) | **GET** /api/v1/company/employee-count | Employee Count


# **get_company_details**
> CompanyDetailsResponse get_company_details(website, include_employee_count=include_employee_count, follower_count=follower_count)

Company Details

Retrieve detailed company information including description, industry, executives, addresses, and for public companies: financials and stock info.

**Cost:** 2 credits (4 credits if include_employee_count=true, +1 credit if follower_count=include)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.company_details_response import CompanyDetailsResponse
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
    website = 'https://www.stripe.com' # str | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.
    include_employee_count = False # bool | Fetch fresh employee count data via web search. Adds 2 credits. (optional) (default to False)
    follower_count = 'follower_count_example' # str | Set to 'include' to fetch Twitter/X follower and following counts. Adds 1 credit. (optional)

    try:
        # Company Details
        api_response = api_instance.get_company_details(website, include_employee_count=include_employee_count, follower_count=follower_count)
        print("The response of CompanyAPIApi->get_company_details:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompanyAPIApi->get_company_details: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 
 **include_employee_count** | **bool**| Fetch fresh employee count data via web search. Adds 2 credits. | [optional] [default to False]
 **follower_count** | **str**| Set to &#39;include&#39; to fetch Twitter/X follower and following counts. Adds 1 credit. | [optional] 

### Return type

[**CompanyDetailsResponse**](CompanyDetailsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Company details |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**404** | No company data found for the given website |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_company_funding**
> CompanyFundingResponse get_company_funding(website)

Company Funding

Retrieve the funding history of a company including all funding rounds and investors.

On cache miss this endpoint streams a single JSON object with whitespace heartbeats while Google AI Mode and LLM extraction run; set your HTTP client read timeout to at least 180 seconds. Cache hits return immediately. Fresh-path failures are delivered as HTTP 200 with `error` and `error_code` fields in the response body (see `CompanyFundingResponse`) because streaming responses cannot set late status codes.

**Cost:** 2 credits + 1 credit per unique investor returned

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.company_funding_response import CompanyFundingResponse
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
    website = 'https://www.stripe.com' # str | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.

    try:
        # Company Funding
        api_response = api_instance.get_company_funding(website)
        print("The response of CompanyAPIApi->get_company_funding:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompanyAPIApi->get_company_funding: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 

### Return type

[**CompanyFundingResponse**](CompanyFundingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Company funding data. On cache hit this is a standard JSON response; on cache miss the body is streamed as a single JSON object with whitespace heartbeats and may carry &#x60;error&#x60;/&#x60;error_code&#x60; fields instead of &#x60;funding_rounds&#x60;. |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call. Present on cache hits only — on streaming cache-miss responses the credit cost is delivered in the response body as &#x60;credit_cost&#x60; because streaming responses cannot set HTTP trailers. <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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

# **get_company_updates**
> CompanyUpdatesResponse get_company_updates(website)

Company Updates

Retrieve recent blog posts and X/Twitter updates for a company.

**Cost:** 2 credits

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.company_updates_response import CompanyUpdatesResponse
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
    website = 'https://www.stripe.com' # str | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.

    try:
        # Company Updates
        api_response = api_instance.get_company_updates(website)
        print("The response of CompanyAPIApi->get_company_updates:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompanyAPIApi->get_company_updates: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 

### Return type

[**CompanyUpdatesResponse**](CompanyUpdatesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Company updates |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_employee_count**
> EmployeeCountResponse get_employee_count(website)

Employee Count

Get the employee count for a company. Uses web search to find the most recent employee count information.

**Cost:** 2 credits

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.employee_count_response import EmployeeCountResponse
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
    website = 'https://www.stripe.com' # str | The website URL or company name of the target company. A website URL (e.g. `https://www.stripe.com`) is strongly recommended for precision.

    try:
        # Employee Count
        api_response = api_instance.get_employee_count(website)
        print("The response of CompanyAPIApi->get_employee_count:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompanyAPIApi->get_employee_count: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **website** | **str**| The website URL or company name of the target company. A website URL (e.g. &#x60;https://www.stripe.com&#x60;) is strongly recommended for precision. | 

### Return type

[**EmployeeCountResponse**](EmployeeCountResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Employee count data |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**404** | No employee count data found for the given website |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

