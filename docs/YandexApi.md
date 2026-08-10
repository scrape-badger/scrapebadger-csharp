# ScrapeBadger.Api.YandexApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**YandexImageSearch**](YandexApi.md#yandeximagesearch) | **GET** /v1/yandex/images/search | Image search |
| [**YandexListSupportedMarkets**](YandexApi.md#yandexlistsupportedmarkets) | **GET** /v1/yandex/markets | List supported markets |
| [**YandexReverseImageSearch**](YandexApi.md#yandexreverseimagesearch) | **GET** /v1/yandex/images/reverse | Reverse image search |
| [**YandexWebSearch**](YandexApi.md#yandexwebsearch) | **GET** /v1/yandex/search | Web search |
| [**YandexYandexScraperHealthCheck**](YandexApi.md#yandexyandexscraperhealthcheck) | **GET** /v1/yandex/health | Yandex scraper health check |
| [**YandexYandexScraperHealthCheckHead**](YandexApi.md#yandexyandexscraperhealthcheckhead) | **HEAD** /v1/yandex/health | Yandex scraper health check |

<a id="yandeximagesearch"></a>
# **YandexImageSearch**
> Object YandexImageSearch (string query, string domain = null, int? page = null)

Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

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
    public class YandexImageSearchExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Image search query, e.g. 'coffee machine'
            var domain = "\"tr\"";  // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional)  (default to "tr")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Image search
                Object result = apiInstance.YandexImageSearch(query, domain, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Image search
    ApiResponse<Object> response = apiInstance.YandexImageSearchWithHttpInfo(query, domain, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Image search query, e.g. &#39;coffee machine&#39; |  |
| **domain** | **string** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |

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

<a id="yandexlistsupportedmarkets"></a>
# **YandexListSupportedMarkets**
> Object YandexListSupportedMarkets ()

List supported markets

Supported Yandex markets (domains, default region and language).

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
    public class YandexListSupportedMarketsExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);

            try
            {
                // List supported markets
                Object result = apiInstance.YandexListSupportedMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexListSupportedMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexListSupportedMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported markets
    ApiResponse<Object> response = apiInstance.YandexListSupportedMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexListSupportedMarketsWithHttpInfo: " + e.Message);
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

<a id="yandexreverseimagesearch"></a>
# **YandexReverseImageSearch**
> Object YandexReverseImageSearch (string imageUrl, string domain = null)

Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

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
    public class YandexReverseImageSearchExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);
            var imageUrl = "imageUrl_example";  // string | Public URL of the image to reverse-search
            var domain = "\"tr\"";  // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional)  (default to "tr")

            try
            {
                // Reverse image search
                Object result = apiInstance.YandexReverseImageSearch(imageUrl, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexReverseImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexReverseImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reverse image search
    ApiResponse<Object> response = apiInstance.YandexReverseImageSearchWithHttpInfo(imageUrl, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexReverseImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **imageUrl** | **string** | Public URL of the image to reverse-search |  |
| **domain** | **string** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;] |

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

<a id="yandexwebsearch"></a>
# **YandexWebSearch**
> Object YandexWebSearch (string query, string domain = null, int? page = null, int? lr = null, string lang = null)

Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

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
    public class YandexWebSearchExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search query, e.g. 'coffee machine'
            var domain = "\"tr\"";  // string | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate. (optional)  (default to "tr")
            var page = 1;  // int? |  (optional)  (default to 1)
            var lr = 56;  // int? | Yandex region id, e.g. 213=Moscow, 84=USA (optional) 
            var lang = "lang_example";  // string | UI language: ru, en, tr, be, kk, uk (optional) 

            try
            {
                // Web search
                Object result = apiInstance.YandexWebSearch(query, domain, page, lr, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web search
    ApiResponse<Object> response = apiInstance.YandexWebSearchWithHttpInfo(query, domain, page, lr, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search query, e.g. &#39;coffee machine&#39; |  |
| **domain** | **string** | Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to &quot;tr&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **lr** | **int?** | Yandex region id, e.g. 213&#x3D;Moscow, 84&#x3D;USA | [optional]  |
| **lang** | **string** | UI language: ru, en, tr, be, kk, uk | [optional]  |

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

<a id="yandexyandexscraperhealthcheck"></a>
# **YandexYandexScraperHealthCheck**
> Object YandexYandexScraperHealthCheck ()

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

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
    public class YandexYandexScraperHealthCheckExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);

            try
            {
                // Yandex scraper health check
                Object result = apiInstance.YandexYandexScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexYandexScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexYandexScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Yandex scraper health check
    ApiResponse<Object> response = apiInstance.YandexYandexScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexYandexScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="yandexyandexscraperhealthcheckhead"></a>
# **YandexYandexScraperHealthCheckHead**
> Object YandexYandexScraperHealthCheckHead ()

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

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
    public class YandexYandexScraperHealthCheckHeadExample
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
            var apiInstance = new YandexApi(httpClient, config, httpClientHandler);

            try
            {
                // Yandex scraper health check
                Object result = apiInstance.YandexYandexScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YandexApi.YandexYandexScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YandexYandexScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Yandex scraper health check
    ApiResponse<Object> response = apiInstance.YandexYandexScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YandexApi.YandexYandexScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

