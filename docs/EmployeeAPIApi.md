# ninjapear.EmployeeAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_person_profile**](EmployeeAPIApi.md#get_person_profile) | **GET** /api/v1/employee/profile | Person Profile Enrichment
[**get_work_email**](EmployeeAPIApi.md#get_work_email) | **GET** /api/v1/employee/work-email | Work Email Lookup


# **get_person_profile**
> PersonProfileResponse get_person_profile(work_email=work_email, first_name=first_name, middle_name=middle_name, last_name=last_name, employer_website=employer_website, role=role, slug=slug, id=id)

Person Profile Enrichment

Enrich a person's professional profile including work experience, education, and social media presence. Provide at least one of the following combinations:
- `work_email`
- `first_name` + `employer_website`
- `employer_website` + `role`
- `slug` or `id` for direct lookup

**Cost:** 3 credits

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.person_profile_response import PersonProfileResponse
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
    api_instance = ninjapear.EmployeeAPIApi(api_client)
    work_email = 'john@stripe.com' # str | Person's work email address (optional)
    first_name = 'first_name_example' # str | Person's first name (optional)
    middle_name = 'middle_name_example' # str | Person's middle name (optional)
    last_name = 'last_name_example' # str | Person's last name (optional)
    employer_website = 'https://stripe.com' # str | Employer's website URL or company name. A website URL (e.g. `https://stripe.com`) is strongly recommended for precision. (optional)
    role = 'CEO' # str | Job role/title (optional)
    slug = 'slug_example' # str | Person's unique slug identifier (direct lookup) (optional)
    id = 'id_example' # str | Person's unique ID (direct lookup) (optional)

    try:
        # Person Profile Enrichment
        api_response = api_instance.get_person_profile(work_email=work_email, first_name=first_name, middle_name=middle_name, last_name=last_name, employer_website=employer_website, role=role, slug=slug, id=id)
        print("The response of EmployeeAPIApi->get_person_profile:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmployeeAPIApi->get_person_profile: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **work_email** | **str**| Person&#39;s work email address | [optional] 
 **first_name** | **str**| Person&#39;s first name | [optional] 
 **middle_name** | **str**| Person&#39;s middle name | [optional] 
 **last_name** | **str**| Person&#39;s last name | [optional] 
 **employer_website** | **str**| Employer&#39;s website URL or company name. A website URL (e.g. &#x60;https://stripe.com&#x60;) is strongly recommended for precision. | [optional] 
 **role** | **str**| Job role/title | [optional] 
 **slug** | **str**| Person&#39;s unique slug identifier (direct lookup) | [optional] 
 **id** | **str**| Person&#39;s unique ID (direct lookup) | [optional] 

### Return type

[**PersonProfileResponse**](PersonProfileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Person profile data |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**404** | Person not found or no profile data found |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_work_email**
> WorkEmailResponse get_work_email(first_name, domain, last_name=last_name, force_refresh=force_refresh)

Work Email Lookup

Makes a best-effort attempt to return a person's public work email address given their first name (optional last name) and a company domain. Searches public sources for the specific email first; if none is found, infers the address from observed employee email patterns at the domain. Returns `work_email: null` if no evidence is available.

**Cost:** 2 credits per API call, charged regardless of whether an email is returned.

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.work_email_response import WorkEmailResponse
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
    api_instance = ninjapear.EmployeeAPIApi(api_client)
    first_name = 'Patrick' # str | Person's first name
    domain = 'stripe.com' # str | Company domain. Scheme, www, and trailing slash are stripped if present.
    last_name = 'Collison' # str | Person's last name. Improves accuracy when the email pattern needs it. (optional)
    force_refresh = True # bool | If `true`, bypass the cache and re-run the AI lookup. (optional)

    try:
        # Work Email Lookup
        api_response = api_instance.get_work_email(first_name, domain, last_name=last_name, force_refresh=force_refresh)
        print("The response of EmployeeAPIApi->get_work_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EmployeeAPIApi->get_work_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **first_name** | **str**| Person&#39;s first name | 
 **domain** | **str**| Company domain. Scheme, www, and trailing slash are stripped if present. | 
 **last_name** | **str**| Person&#39;s last name. Improves accuracy when the email pattern needs it. | [optional] 
 **force_refresh** | **bool**| If &#x60;true&#x60;, bypass the cache and re-run the AI lookup. | [optional] 

### Return type

[**WorkEmailResponse**](WorkEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Best-effort work email lookup result |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**503** | Upstream AI / LLM provider temporarily unavailable. Retry later. No credits charged. |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

