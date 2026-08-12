# ScrapeBadger.Api.AppStoreApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AppStoreGetAppDetail**](AppStoreApi.md#appstoregetappdetail) | **GET** /v1/app-store/apps/{app_id} | Get app detail |
| [**AppStoreGetAppReviews**](AppStoreApi.md#appstoregetappreviews) | **GET** /v1/app-store/apps/{app_id}/reviews | Get app reviews |
| [**AppStoreGetDeveloperApps**](AppStoreApi.md#appstoregetdeveloperapps) | **GET** /v1/app-store/developers/{artist_id} | Get developer apps |
| [**AppStoreListGenres**](AppStoreApi.md#appstorelistgenres) | **GET** /v1/app-store/genres | List genres |
| [**AppStoreListMarkets**](AppStoreApi.md#appstorelistmarkets) | **GET** /v1/app-store/markets | List markets |
| [**AppStoreSearchApps**](AppStoreApi.md#appstoresearchapps) | **GET** /v1/app-store/search | Search apps |
| [**AppStoreTopCharts**](AppStoreApi.md#appstoretopcharts) | **GET** /v1/app-store/charts | Top charts |

<a id="appstoregetappdetail"></a>
# **AppStoreGetAppDetail**
> Object AppStoreGetAppDetail (string appId, string country = null, string lang = null, bool? includeExtras = null)

Get app detail

App detail: bundle id, version, pricing, ratings, genres, min OS, size, languages, screenshots, in-app purchases and version history.

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
    public class AppStoreGetAppDetailExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Numeric trackId (e.g. '310633997') or bundle id (e.g. 'net.whatsapp.WhatsApp').
            var country = "\"us\"";  // string |  (optional)  (default to "us")
            var lang = "lang_example";  // string | Result language, e.g. 'en_us' (optional) 
            var includeExtras = true;  // bool? | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. (optional)  (default to true)

            try
            {
                // Get app detail
                Object result = apiInstance.AppStoreGetAppDetail(appId, country, lang, includeExtras);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreGetAppDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreGetAppDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get app detail
    ApiResponse<Object> response = apiInstance.AppStoreGetAppDetailWithHttpInfo(appId, country, lang, includeExtras);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreGetAppDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Numeric trackId (e.g. &#39;310633997&#39;) or bundle id (e.g. &#39;net.whatsapp.WhatsApp&#39;). |  |
| **country** | **string** |  | [optional] [default to &quot;us&quot;] |
| **lang** | **string** | Result language, e.g. &#39;en_us&#39; | [optional]  |
| **includeExtras** | **bool?** | Fetch the storefront page for rating histogram, IAP list, full-res screenshots and App Privacy. Set false to skip the 2nd fetch. | [optional] [default to true] |

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

<a id="appstoregetappreviews"></a>
# **AppStoreGetAppReviews**
> Object AppStoreGetAppReviews (string appId, string country = null, int? page = null, string sort = null)

Get app reviews

Paginated customer reviews (50 per page, up to 10 pages).

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
    public class AppStoreGetAppReviewsExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Numeric trackId, e.g. '310633997'
            var country = "\"us\"";  // string |  (optional)  (default to "us")
            var page = 1;  // int? | Apple caps reviews at 10 pages (optional)  (default to 1)
            var sort = "\"mostRecent\"";  // string | mostRecent | mostHelpful (optional)  (default to "mostRecent")

            try
            {
                // Get app reviews
                Object result = apiInstance.AppStoreGetAppReviews(appId, country, page, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreGetAppReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreGetAppReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get app reviews
    ApiResponse<Object> response = apiInstance.AppStoreGetAppReviewsWithHttpInfo(appId, country, page, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreGetAppReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Numeric trackId, e.g. &#39;310633997&#39; |  |
| **country** | **string** |  | [optional] [default to &quot;us&quot;] |
| **page** | **int?** | Apple caps reviews at 10 pages | [optional] [default to 1] |
| **sort** | **string** | mostRecent | mostHelpful | [optional] [default to &quot;mostRecent&quot;] |

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

<a id="appstoregetdeveloperapps"></a>
# **AppStoreGetDeveloperApps**
> Object AppStoreGetDeveloperApps (string artistId, string country = null)

Get developer apps

Developer info and their published apps.

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
    public class AppStoreGetDeveloperAppsExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);
            var artistId = "artistId_example";  // string | Numeric artistId (developer id)
            var country = "\"us\"";  // string |  (optional)  (default to "us")

            try
            {
                // Get developer apps
                Object result = apiInstance.AppStoreGetDeveloperApps(artistId, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreGetDeveloperApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreGetDeveloperAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get developer apps
    ApiResponse<Object> response = apiInstance.AppStoreGetDeveloperAppsWithHttpInfo(artistId, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreGetDeveloperAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **artistId** | **string** | Numeric artistId (developer id) |  |
| **country** | **string** |  | [optional] [default to &quot;us&quot;] |

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

<a id="appstorelistgenres"></a>
# **AppStoreListGenres**
> Object AppStoreListGenres ()

List genres

The Apple App Store genre/category ids.

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
    public class AppStoreListGenresExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);

            try
            {
                // List genres
                Object result = apiInstance.AppStoreListGenres();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreListGenres: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreListGenresWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List genres
    ApiResponse<Object> response = apiInstance.AppStoreListGenresWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreListGenresWithHttpInfo: " + e.Message);
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

<a id="appstorelistmarkets"></a>
# **AppStoreListMarkets**
> Object AppStoreListMarkets ()

List markets

Supported App Store country codes.

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
    public class AppStoreListMarketsExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.AppStoreListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.AppStoreListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreListMarketsWithHttpInfo: " + e.Message);
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

<a id="appstoresearchapps"></a>
# **AppStoreSearchApps**
> Object AppStoreSearchApps (string query, string country = null, string entity = null, int? limit = null, int? offset = null, string lang = null)

Search apps

Search the Apple App Store.

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
    public class AppStoreSearchAppsExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search term, e.g. 'chat'
            var country = "\"us\"";  // string | App Store country code (optional)  (default to "us")
            var entity = "\"software\"";  // string | software | iPadSoftware | macSoftware (optional)  (default to "software")
            var limit = 25;  // int? |  (optional)  (default to 25)
            var offset = 0;  // int? |  (optional)  (default to 0)
            var lang = "lang_example";  // string | Language, e.g. 'en_us' (optional) 

            try
            {
                // Search apps
                Object result = apiInstance.AppStoreSearchApps(query, country, entity, limit, offset, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreSearchApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreSearchAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search apps
    ApiResponse<Object> response = apiInstance.AppStoreSearchAppsWithHttpInfo(query, country, entity, limit, offset, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreSearchAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search term, e.g. &#39;chat&#39; |  |
| **country** | **string** | App Store country code | [optional] [default to &quot;us&quot;] |
| **entity** | **string** | software | iPadSoftware | macSoftware | [optional] [default to &quot;software&quot;] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **offset** | **int?** |  | [optional] [default to 0] |
| **lang** | **string** | Language, e.g. &#39;en_us&#39; | [optional]  |

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

<a id="appstoretopcharts"></a>
# **AppStoreTopCharts**
> Object AppStoreTopCharts (string country = null, string type = null, int? genre = null, int? limit = null, string entity = null)

Top charts

Top charts, optionally scoped to a genre.

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
    public class AppStoreTopChartsExample
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
            var apiInstance = new AppStoreApi(httpClient, config, httpClientHandler);
            var country = "\"us\"";  // string |  (optional)  (default to "us")
            var type = "\"top-free\"";  // string | top-free | top-paid | top-grossing (optional)  (default to "top-free")
            var genre = 56;  // int? | Apple genre id (optional), e.g. 6014 (optional) 
            var limit = 50;  // int? |  (optional)  (default to 50)
            var entity = "\"apps\"";  // string | apps (iPhone) | ipad (optional)  (default to "apps")

            try
            {
                // Top charts
                Object result = apiInstance.AppStoreTopCharts(country, type, genre, limit, entity);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AppStoreApi.AppStoreTopCharts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AppStoreTopChartsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Top charts
    ApiResponse<Object> response = apiInstance.AppStoreTopChartsWithHttpInfo(country, type, genre, limit, entity);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AppStoreApi.AppStoreTopChartsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **country** | **string** |  | [optional] [default to &quot;us&quot;] |
| **type** | **string** | top-free | top-paid | top-grossing | [optional] [default to &quot;top-free&quot;] |
| **genre** | **int?** | Apple genre id (optional), e.g. 6014 | [optional]  |
| **limit** | **int?** |  | [optional] [default to 50] |
| **entity** | **string** | apps (iPhone) | ipad | [optional] [default to &quot;apps&quot;] |

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

