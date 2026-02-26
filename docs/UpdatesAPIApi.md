# ninjapear.UpdatesAPIApi

All URIs are relative to *https://nubela.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_target**](UpdatesAPIApi.md#add_target) | **POST** /api/v1/feeds/{feed_id}/targets | Add Target
[**create_feed**](UpdatesAPIApi.md#create_feed) | **POST** /api/v1/feeds | Create Feed
[**delete_feed**](UpdatesAPIApi.md#delete_feed) | **DELETE** /api/v1/feeds/{feed_id} | Delete Feed
[**delete_target**](UpdatesAPIApi.md#delete_target) | **DELETE** /api/v1/feeds/{feed_id}/targets/{target_id} | Delete Target
[**get_feed**](UpdatesAPIApi.md#get_feed) | **GET** /api/v1/feeds/{feed_id} | Get Feed
[**get_rss_feed**](UpdatesAPIApi.md#get_rss_feed) | **GET** /api/v1/feeds/{feed_id}/rss.xml | Get RSS Feed
[**list_feeds**](UpdatesAPIApi.md#list_feeds) | **GET** /api/v1/feeds | List Feeds
[**update_feed**](UpdatesAPIApi.md#update_feed) | **PATCH** /api/v1/feeds/{feed_id} | Update Feed
[**update_target**](UpdatesAPIApi.md#update_target) | **PATCH** /api/v1/feeds/{feed_id}/targets/{target_id} | Update Target


# **add_target**
> Target add_target(feed_id, add_target_request)

Add Target

Add a new company target to an existing feed.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.add_target_request import AddTargetRequest
from ninjapear.models.target import Target
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)
    add_target_request = ninjapear.AddTargetRequest() # AddTargetRequest | 

    try:
        # Add Target
        api_response = api_instance.add_target(feed_id, add_target_request)
        print("The response of UpdatesAPIApi->add_target:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->add_target: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 
 **add_target_request** | [**AddTargetRequest**](AddTargetRequest.md)|  | 

### Return type

[**Target**](Target.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Target added |  -  |
**404** | Feed not found |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_feed**
> Feed create_feed(create_feed_request)

Create Feed

Create a new monitoring feed with one or more company targets. Each target specifies a company website and which channels to monitor (blog, X/Twitter, website changes).

**Cost:** 3 credits

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.create_feed_request import CreateFeedRequest
from ninjapear.models.feed import Feed
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    create_feed_request = ninjapear.CreateFeedRequest() # CreateFeedRequest | 

    try:
        # Create Feed
        api_response = api_instance.create_feed(create_feed_request)
        print("The response of UpdatesAPIApi->create_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->create_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_feed_request** | [**CreateFeedRequest**](CreateFeedRequest.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Feed created successfully |  * X-NinjaPear-Credit-Cost - Total cost of credits for this API call <br>  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**403** | Insufficient credits |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_feed**
> MessageResponse delete_feed(feed_id)

Delete Feed

Soft-delete a feed and all its targets.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.message_response import MessageResponse
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)

    try:
        # Delete Feed
        api_response = api_instance.delete_feed(feed_id)
        print("The response of UpdatesAPIApi->delete_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->delete_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Feed deleted |  -  |
**404** | Feed not found |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_target**
> MessageResponse delete_target(feed_id, target_id)

Delete Target

Soft-delete a target from a feed.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.message_response import MessageResponse
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)
    target_id = 'target_id_example' # str | Target identifier (e.g. target_abc123xyz)

    try:
        # Delete Target
        api_response = api_instance.delete_target(feed_id, target_id)
        print("The response of UpdatesAPIApi->delete_target:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->delete_target: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 
 **target_id** | **str**| Target identifier (e.g. target_abc123xyz) | 

### Return type

[**MessageResponse**](MessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Target deleted |  -  |
**404** | Feed or target not found |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_feed**
> Feed get_feed(feed_id)

Get Feed

Get a feed with all its targets.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.feed import Feed
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)

    try:
        # Get Feed
        api_response = api_instance.get_feed(feed_id)
        print("The response of UpdatesAPIApi->get_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->get_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Feed details with targets |  -  |
**404** | Feed not found |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_rss_feed**
> str get_rss_feed(feed_id, token=token)

Get RSS Feed

Get the RSS 2.0 XML feed for a monitoring feed. Public feeds are accessible without authentication. Private feeds require the `token` query parameter.

**Cost:** FREE (0 credits)

**Authentication:** This endpoint does NOT use Bearer authentication. Private feeds are authenticated via the `token` query parameter, which is included in the `rss_url` returned when creating a feed.

### Example


```python
import ninjapear
from ninjapear.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://nubela.co
# See configuration.py for a list of all supported configuration parameters.
configuration = ninjapear.Configuration(
    host = "https://nubela.co"
)


# Enter a context with an instance of the API client
with ninjapear.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)
    token = 'token_example' # str | Access token for private feeds (included in rss_url) (optional)

    try:
        # Get RSS Feed
        api_response = api_instance.get_rss_feed(feed_id, token=token)
        print("The response of UpdatesAPIApi->get_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->get_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 
 **token** | **str**| Access token for private feeds (included in rss_url) | [optional] 

### Return type

**str**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | RSS 2.0 XML feed |  -  |
**403** | Token required for private feed |  -  |
**404** | Feed not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_feeds**
> FeedListResponse list_feeds()

List Feeds

List all feeds for the authenticated account.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.feed_list_response import FeedListResponse
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)

    try:
        # List Feeds
        api_response = api_instance.list_feeds()
        print("The response of UpdatesAPIApi->list_feeds:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->list_feeds: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**FeedListResponse**](FeedListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of feeds |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_feed**
> Feed update_feed(feed_id, update_feed_request)

Update Feed

Update feed metadata such as name, visibility, or suspension status.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.feed import Feed
from ninjapear.models.update_feed_request import UpdateFeedRequest
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)
    update_feed_request = ninjapear.UpdateFeedRequest() # UpdateFeedRequest | 

    try:
        # Update Feed
        api_response = api_instance.update_feed(feed_id, update_feed_request)
        print("The response of UpdatesAPIApi->update_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->update_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 
 **update_feed_request** | [**UpdateFeedRequest**](UpdateFeedRequest.md)|  | 

### Return type

[**Feed**](Feed.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated feed |  -  |
**404** | Feed not found |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_target**
> Target update_target(feed_id, target_id, update_target_request)

Update Target

Update monitoring settings for a target.

**Cost:** FREE (0 credits)

### Example

* Bearer Authentication (bearerAuth):

```python
import ninjapear
from ninjapear.models.target import Target
from ninjapear.models.update_target_request import UpdateTargetRequest
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
    api_instance = ninjapear.UpdatesAPIApi(api_client)
    feed_id = 'feed_id_example' # str | Feed identifier (e.g. feed_abc123xyz)
    target_id = 'target_id_example' # str | Target identifier (e.g. target_abc123xyz)
    update_target_request = ninjapear.UpdateTargetRequest() # UpdateTargetRequest | 

    try:
        # Update Target
        api_response = api_instance.update_target(feed_id, target_id, update_target_request)
        print("The response of UpdatesAPIApi->update_target:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UpdatesAPIApi->update_target: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **feed_id** | **str**| Feed identifier (e.g. feed_abc123xyz) | 
 **target_id** | **str**| Target identifier (e.g. target_abc123xyz) | 
 **update_target_request** | [**UpdateTargetRequest**](UpdateTargetRequest.md)|  | 

### Return type

[**Target**](Target.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated target |  -  |
**404** | Feed or target not found |  -  |
**400** | Invalid parameters provided |  -  |
**401** | Invalid API Key |  -  |
**429** | Rate limited |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

