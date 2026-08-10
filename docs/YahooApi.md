# ScrapeBadger.Api.YahooApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**YahooImageSearch**](YahooApi.md#yahooimagesearch) | **GET** /v1/yahoo/images | Image search |
| [**YahooListSupportedMarkets**](YahooApi.md#yahoolistsupportedmarkets) | **GET** /v1/yahoo/markets | List supported markets |
| [**YahooNewsSearch**](YahooApi.md#yahoonewssearch) | **GET** /v1/yahoo/news | News search |
| [**YahooSearchSuggestions**](YahooApi.md#yahoosearchsuggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions |
| [**YahooVideoSearch**](YahooApi.md#yahoovideosearch) | **GET** /v1/yahoo/videos | Video search |
| [**YahooWebSearch**](YahooApi.md#yahoowebsearch) | **GET** /v1/yahoo/search | Web search |
| [**YahooYahooScraperHealthCheck**](YahooApi.md#yahooyahooscraperhealthcheck) | **GET** /v1/yahoo/health | Yahoo scraper health check |
| [**YahooYahooScraperHealthCheckHead**](YahooApi.md#yahooyahooscraperhealthcheckhead) | **HEAD** /v1/yahoo/health | Yahoo scraper health check |

<a id="yahooimagesearch"></a>
# **YahooImageSearch**
> Object YahooImageSearch (string query, string market = null, int? count = null)

Image search

Yahoo Images — thumbnail, full-size and source URL per result.

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
    public class YahooImageSearchExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'golden retriever'
            var market = "\"us\"";  // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional)  (default to "us")
            var count = 30;  // int? | Results to return (optional)  (default to 30)

            try
            {
                // Image search
                Object result = apiInstance.YahooImageSearch(query, market, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Image search
    ApiResponse<Object> response = apiInstance.YahooImageSearchWithHttpInfo(query, market, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;golden retriever&#39; |  |
| **market** | **string** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;] |
| **count** | **int?** | Results to return | [optional] [default to 30] |

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

<a id="yahoolistsupportedmarkets"></a>
# **YahooListSupportedMarkets**
> Object YahooListSupportedMarkets ()

List supported markets

Supported Yahoo market codes. Free — costs no credits.

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
    public class YahooListSupportedMarketsExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);

            try
            {
                // List supported markets
                Object result = apiInstance.YahooListSupportedMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooListSupportedMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooListSupportedMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported markets
    ApiResponse<Object> response = apiInstance.YahooListSupportedMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooListSupportedMarketsWithHttpInfo: " + e.Message);
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

<a id="yahoonewssearch"></a>
# **YahooNewsSearch**
> Object YahooNewsSearch (string query, string market = null)

News search

Yahoo News — headline, source, published time and snippet per article.

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
    public class YahooNewsSearchExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'interest rates'
            var market = "\"us\"";  // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional)  (default to "us")

            try
            {
                // News search
                Object result = apiInstance.YahooNewsSearch(query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // News search
    ApiResponse<Object> response = apiInstance.YahooNewsSearchWithHttpInfo(query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;interest rates&#39; |  |
| **market** | **string** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;] |

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

<a id="yahoosearchsuggestions"></a>
# **YahooSearchSuggestions**
> Object YahooSearchSuggestions (string query, string market = null)

Search suggestions

Yahoo search-box query suggestions.

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
    public class YahooSearchSuggestionsExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term, e.g. 'coff'
            var market = "\"us\"";  // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional)  (default to "us")

            try
            {
                // Search suggestions
                Object result = apiInstance.YahooSearchSuggestions(query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.YahooSearchSuggestionsWithHttpInfo(query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term, e.g. &#39;coff&#39; |  |
| **market** | **string** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;] |

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

<a id="yahoovideosearch"></a>
# **YahooVideoSearch**
> Object YahooVideoSearch (string query, string market = null, int? count = null)

Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

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
    public class YahooVideoSearchExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'espresso tutorial'
            var market = "\"us\"";  // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional)  (default to "us")
            var count = 30;  // int? | Results to return (optional)  (default to 30)

            try
            {
                // Video search
                Object result = apiInstance.YahooVideoSearch(query, market, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooVideoSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooVideoSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Video search
    ApiResponse<Object> response = apiInstance.YahooVideoSearchWithHttpInfo(query, market, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooVideoSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;espresso tutorial&#39; |  |
| **market** | **string** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;] |
| **count** | **int?** | Results to return | [optional] [default to 30] |

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

<a id="yahoowebsearch"></a>
# **YahooWebSearch**
> Object YahooWebSearch (string query, string market = null, int? offset = null, string safeSearch = null)

Web search

Yahoo web SERP — organic results, ads, related searches and total count.

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
    public class YahooWebSearchExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'coffee machine'
            var market = "\"us\"";  // string | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets. (optional)  (default to "us")
            var offset = 0;  // int? | Zero-based result offset for pagination (optional)  (default to 0)
            var safeSearch = "safeSearch_example";  // string | off | moderate | strict (default moderate) (optional) 

            try
            {
                // Web search
                Object result = apiInstance.YahooWebSearch(query, market, offset, safeSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web search
    ApiResponse<Object> response = apiInstance.YahooWebSearchWithHttpInfo(query, market, offset, safeSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;coffee machine&#39; |  |
| **market** | **string** | Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to &quot;us&quot;] |
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

<a id="yahooyahooscraperhealthcheck"></a>
# **YahooYahooScraperHealthCheck**
> Object YahooYahooScraperHealthCheck ()

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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
    public class YahooYahooScraperHealthCheckExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);

            try
            {
                // Yahoo scraper health check
                Object result = apiInstance.YahooYahooScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooYahooScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooYahooScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Yahoo scraper health check
    ApiResponse<Object> response = apiInstance.YahooYahooScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooYahooScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="yahooyahooscraperhealthcheckhead"></a>
# **YahooYahooScraperHealthCheckHead**
> Object YahooYahooScraperHealthCheckHead ()

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

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
    public class YahooYahooScraperHealthCheckHeadExample
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
            var apiInstance = new YahooApi(httpClient, config, httpClientHandler);

            try
            {
                // Yahoo scraper health check
                Object result = apiInstance.YahooYahooScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YahooApi.YahooYahooScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YahooYahooScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Yahoo scraper health check
    ApiResponse<Object> response = apiInstance.YahooYahooScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YahooApi.YahooYahooScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

