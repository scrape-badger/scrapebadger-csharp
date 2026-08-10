# ScrapeBadger.Api.BingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BingBingScraperHealthCheck**](BingApi.md#bingbingscraperhealthcheck) | **GET** /v1/bing/health | Bing scraper health check |
| [**BingBingScraperHealthCheckHead**](BingApi.md#bingbingscraperhealthcheckhead) | **HEAD** /v1/bing/health | Bing scraper health check |
| [**BingImageSearch**](BingApi.md#bingimagesearch) | **GET** /v1/bing/images | Image search |
| [**BingListSupportedMarkets**](BingApi.md#binglistsupportedmarkets) | **GET** /v1/bing/markets | List supported markets |
| [**BingNewsSearch**](BingApi.md#bingnewssearch) | **GET** /v1/bing/news | News search |
| [**BingSearchSuggestions**](BingApi.md#bingsearchsuggestions) | **GET** /v1/bing/autocomplete | Search suggestions |
| [**BingVideoSearch**](BingApi.md#bingvideosearch) | **GET** /v1/bing/videos | Video search |
| [**BingWebSearch**](BingApi.md#bingwebsearch) | **GET** /v1/bing/search | Web search |

<a id="bingbingscraperhealthcheck"></a>
# **BingBingScraperHealthCheck**
> Object BingBingScraperHealthCheck ()

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingBingScraperHealthCheckExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);

            try
            {
                // Bing scraper health check
                Object result = apiInstance.BingBingScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingBingScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingBingScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bing scraper health check
    ApiResponse<Object> response = apiInstance.BingBingScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingBingScraperHealthCheckWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingbingscraperhealthcheckhead"></a>
# **BingBingScraperHealthCheckHead**
> Object BingBingScraperHealthCheckHead ()

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingBingScraperHealthCheckHeadExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);

            try
            {
                // Bing scraper health check
                Object result = apiInstance.BingBingScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingBingScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingBingScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bing scraper health check
    ApiResponse<Object> response = apiInstance.BingBingScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingBingScraperHealthCheckHeadWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingimagesearch"></a>
# **BingImageSearch**
> Object BingImageSearch (string query, string market = null, int? count = null, string safeSearch = null)

Image search

Bing Images — thumbnail, full-size and source URL per result.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingImageSearchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'golden retriever'
            var market = "\"en-US\"";  // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional)  (default to "en-US")
            var count = 35;  // int? | Results to return (optional)  (default to 35)
            var safeSearch = "safeSearch_example";  // string | off | moderate | strict (optional) 

            try
            {
                // Image search
                Object result = apiInstance.BingImageSearch(query, market, count, safeSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Image search
    ApiResponse<Object> response = apiInstance.BingImageSearchWithHttpInfo(query, market, count, safeSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;golden retriever&#39; |  |
| **market** | **string** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;] |
| **count** | **int?** | Results to return | [optional] [default to 35] |
| **safeSearch** | **string** | off | moderate | strict | [optional]  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="binglistsupportedmarkets"></a>
# **BingListSupportedMarkets**
> Object BingListSupportedMarkets ()

List supported markets

Supported Bing market codes. Free — costs no credits.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingListSupportedMarketsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);

            try
            {
                // List supported markets
                Object result = apiInstance.BingListSupportedMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingListSupportedMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingListSupportedMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported markets
    ApiResponse<Object> response = apiInstance.BingListSupportedMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingListSupportedMarketsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingnewssearch"></a>
# **BingNewsSearch**
> Object BingNewsSearch (string query, string market = null, string freshness = null)

News search

Bing News — headline, source, published time and snippet per article.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingNewsSearchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'interest rates'
            var market = "\"en-US\"";  // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional)  (default to "en-US")
            var freshness = "freshness_example";  // string | day | week | month — restrict to recent articles (optional) 

            try
            {
                // News search
                Object result = apiInstance.BingNewsSearch(query, market, freshness);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // News search
    ApiResponse<Object> response = apiInstance.BingNewsSearchWithHttpInfo(query, market, freshness);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;interest rates&#39; |  |
| **market** | **string** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;] |
| **freshness** | **string** | day | week | month — restrict to recent articles | [optional]  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingsearchsuggestions"></a>
# **BingSearchSuggestions**
> Object BingSearchSuggestions (string query, string market = null)

Search suggestions

Bing search-box query suggestions.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingSearchSuggestionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term, e.g. 'coff'
            var market = "\"en-US\"";  // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional)  (default to "en-US")

            try
            {
                // Search suggestions
                Object result = apiInstance.BingSearchSuggestions(query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.BingSearchSuggestionsWithHttpInfo(query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term, e.g. &#39;coff&#39; |  |
| **market** | **string** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;] |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingvideosearch"></a>
# **BingVideoSearch**
> Object BingVideoSearch (string query, string market = null, int? count = null, string safeSearch = null)

Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingVideoSearchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'espresso tutorial'
            var market = "\"en-US\"";  // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional)  (default to "en-US")
            var count = 35;  // int? | Results to return (optional)  (default to 35)
            var safeSearch = "safeSearch_example";  // string | off | moderate | strict (optional) 

            try
            {
                // Video search
                Object result = apiInstance.BingVideoSearch(query, market, count, safeSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingVideoSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingVideoSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Video search
    ApiResponse<Object> response = apiInstance.BingVideoSearchWithHttpInfo(query, market, count, safeSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingVideoSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;espresso tutorial&#39; |  |
| **market** | **string** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;] |
| **count** | **int?** | Results to return | [optional] [default to 35] |
| **safeSearch** | **string** | off | moderate | strict | [optional]  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="bingwebsearch"></a>
# **BingWebSearch**
> Object BingWebSearch (string query, string market = null, int? count = null, int? offset = null, string safeSearch = null)

Web search

Bing web SERP — organic results, ads, related searches and total count.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using System.Net.Http;
using ScrapeBadger.Api;
using ScrapeBadger.Client;
using ScrapeBadger.Model;

namespace Example
{
    public class BingWebSearchExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://scrapebadger.com";
            // Configure API key authorization: ApiKeyAuth
            config.AddApiKey("X-API-Key", "YOUR_API_KEY");
            // Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
            // config.AddApiKeyPrefix("X-API-Key", "Bearer");

            // create instances of HttpClient, HttpClientHandler to be reused later with different Api classes
            HttpClient httpClient = new HttpClient();
            HttpClientHandler httpClientHandler = new HttpClientHandler();
            var apiInstance = new BingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'coffee machine'
            var market = "\"en-US\"";  // string | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets. (optional)  (default to "en-US")
            var count = 10;  // int? | Results per page (1-50) (optional)  (default to 10)
            var offset = 0;  // int? | Zero-based result offset for pagination (optional)  (default to 0)
            var safeSearch = "safeSearch_example";  // string | off | moderate | strict (default moderate) (optional) 

            try
            {
                // Web search
                Object result = apiInstance.BingWebSearch(query, market, count, offset, safeSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BingApi.BingWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BingWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web search
    ApiResponse<Object> response = apiInstance.BingWebSearchWithHttpInfo(query, market, count, offset, safeSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BingApi.BingWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;coffee machine&#39; |  |
| **market** | **string** | Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to &quot;en-US&quot;] |
| **count** | **int?** | Results per page (1-50) | [optional] [default to 10] |
| **offset** | **int?** | Zero-based result offset for pagination | [optional] [default to 0] |
| **safeSearch** | **string** | off | moderate | strict (default moderate) | [optional]  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

