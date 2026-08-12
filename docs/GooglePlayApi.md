# ScrapeBadger.Api.GooglePlayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GooglePlayBrowseACategory**](GooglePlayApi.md#googleplaybrowseacategory) | **GET** /v1/google-play/categories/{category_id} | Browse a category |
| [**GooglePlayGetAppDetail**](GooglePlayApi.md#googleplaygetappdetail) | **GET** /v1/google-play/apps/{app_id} | Get app detail |
| [**GooglePlayGetAppPermissions**](GooglePlayApi.md#googleplaygetapppermissions) | **GET** /v1/google-play/apps/{app_id}/permissions | Get app permissions |
| [**GooglePlayGetAppReviews**](GooglePlayApi.md#googleplaygetappreviews) | **GET** /v1/google-play/apps/{app_id}/reviews | Get app reviews |
| [**GooglePlayGetDeveloperApps**](GooglePlayApi.md#googleplaygetdeveloperapps) | **GET** /v1/google-play/developers/{developer} | Get developer apps |
| [**GooglePlayGetSimilarApps**](GooglePlayApi.md#googleplaygetsimilarapps) | **GET** /v1/google-play/apps/{app_id}/similar | Get similar apps |
| [**GooglePlayListCategories**](GooglePlayApi.md#googleplaylistcategories) | **GET** /v1/google-play/categories | List categories |
| [**GooglePlayListMarkets**](GooglePlayApi.md#googleplaylistmarkets) | **GET** /v1/google-play/markets | List markets |
| [**GooglePlaySearchApps**](GooglePlayApi.md#googleplaysearchapps) | **GET** /v1/google-play/search | Search apps |
| [**GooglePlayTopCharts**](GooglePlayApi.md#googleplaytopcharts) | **GET** /v1/google-play/collections/{collection} | Top charts |

<a id="googleplaybrowseacategory"></a>
# **GooglePlayBrowseACategory**
> Object GooglePlayBrowseACategory (string categoryId, string country = null, string lang = null)

Browse a category

The top apps within a Play category.

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
    public class GooglePlayBrowseACategoryExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var categoryId = "categoryId_example";  // string | Play category id, e.g. 'GAME_PUZZLE' or 'SOCIAL'
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Browse a category
                Object result = apiInstance.GooglePlayBrowseACategory(categoryId, country, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayBrowseACategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayBrowseACategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Browse a category
    ApiResponse<Object> response = apiInstance.GooglePlayBrowseACategoryWithHttpInfo(categoryId, country, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayBrowseACategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **categoryId** | **string** | Play category id, e.g. &#39;GAME_PUZZLE&#39; or &#39;SOCIAL&#39; |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

<a id="googleplaygetappdetail"></a>
# **GooglePlayGetAppDetail**
> Object GooglePlayGetAppDetail (string appId, string country = null, string lang = null)

Get app detail

Full app detail: ratings histogram, installs, pricing, IAP, developer, screenshots, version metadata and what's-new.

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
    public class GooglePlayGetAppDetailExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Android package id, e.g. 'com.whatsapp'.
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Get app detail
                Object result = apiInstance.GooglePlayGetAppDetail(appId, country, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayGetAppDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get app detail
    ApiResponse<Object> response = apiInstance.GooglePlayGetAppDetailWithHttpInfo(appId, country, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

<a id="googleplaygetapppermissions"></a>
# **GooglePlayGetAppPermissions**
> Object GooglePlayGetAppPermissions (string appId, string lang = null)

Get app permissions

The app's requested Android permissions, grouped.

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
    public class GooglePlayGetAppPermissionsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Android package id, e.g. 'com.whatsapp'.
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Get app permissions
                Object result = apiInstance.GooglePlayGetAppPermissions(appId, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppPermissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayGetAppPermissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get app permissions
    ApiResponse<Object> response = apiInstance.GooglePlayGetAppPermissionsWithHttpInfo(appId, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppPermissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

<a id="googleplaygetappreviews"></a>
# **GooglePlayGetAppReviews**
> Object GooglePlayGetAppReviews (string appId, string country = null, string lang = null, string sort = null, int? count = null, string pageToken = null)

Get app reviews

Paginated app reviews via the Play batchexecute RPC.

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
    public class GooglePlayGetAppReviewsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Android package id, e.g. 'com.whatsapp'.
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")
            var sort = "\"newest\"";  // string | newest | rating | helpfulness (optional)  (default to "newest")
            var count = 40;  // int? |  (optional)  (default to 40)
            var pageToken = "pageToken_example";  // string | Pagination token (optional) 

            try
            {
                // Get app reviews
                Object result = apiInstance.GooglePlayGetAppReviews(appId, country, lang, sort, count, pageToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayGetAppReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get app reviews
    ApiResponse<Object> response = apiInstance.GooglePlayGetAppReviewsWithHttpInfo(appId, country, lang, sort, count, pageToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetAppReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |
| **sort** | **string** | newest | rating | helpfulness | [optional] [default to &quot;newest&quot;] |
| **count** | **int?** |  | [optional] [default to 40] |
| **pageToken** | **string** | Pagination token | [optional]  |

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

<a id="googleplaygetdeveloperapps"></a>
# **GooglePlayGetDeveloperApps**
> Object GooglePlayGetDeveloperApps (string developer, string country = null, string lang = null)

Get developer apps

A developer's published apps.

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
    public class GooglePlayGetDeveloperAppsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var developer = "developer_example";  // string | Developer name or numeric id
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Get developer apps
                Object result = apiInstance.GooglePlayGetDeveloperApps(developer, country, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetDeveloperApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayGetDeveloperAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get developer apps
    ApiResponse<Object> response = apiInstance.GooglePlayGetDeveloperAppsWithHttpInfo(developer, country, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetDeveloperAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **developer** | **string** | Developer name or numeric id |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

<a id="googleplaygetsimilarapps"></a>
# **GooglePlayGetSimilarApps**
> Object GooglePlayGetSimilarApps (string appId, string country = null, string lang = null)

Get similar apps

Apps Google Play lists as similar to this one.

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
    public class GooglePlayGetSimilarAppsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var appId = "appId_example";  // string | Android package id, e.g. 'com.whatsapp'.
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Get similar apps
                Object result = apiInstance.GooglePlayGetSimilarApps(appId, country, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetSimilarApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayGetSimilarAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get similar apps
    ApiResponse<Object> response = apiInstance.GooglePlayGetSimilarAppsWithHttpInfo(appId, country, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayGetSimilarAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **appId** | **string** | Android package id, e.g. &#39;com.whatsapp&#39;. |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

<a id="googleplaylistcategories"></a>
# **GooglePlayListCategories**
> Object GooglePlayListCategories ()

List categories

The Google Play app/game category ids.

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
    public class GooglePlayListCategoriesExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);

            try
            {
                // List categories
                Object result = apiInstance.GooglePlayListCategories();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayListCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayListCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List categories
    ApiResponse<Object> response = apiInstance.GooglePlayListCategoriesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayListCategoriesWithHttpInfo: " + e.Message);
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

<a id="googleplaylistmarkets"></a>
# **GooglePlayListMarkets**
> Object GooglePlayListMarkets ()

List markets

Supported Google Play store countries and languages.

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
    public class GooglePlayListMarketsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.GooglePlayListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.GooglePlayListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayListMarketsWithHttpInfo: " + e.Message);
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

<a id="googleplaysearchapps"></a>
# **GooglePlaySearchApps**
> Object GooglePlaySearchApps (string query, string country = null, string lang = null, string price = null)

Search apps

Search Google Play for apps and games (the ~30 server-rendered results; Play exposes no page parameter).

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
    public class GooglePlaySearchAppsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'puzzle'
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")
            var price = "price_example";  // string | free | paid | all (optional) 

            try
            {
                // Search apps
                Object result = apiInstance.GooglePlaySearchApps(query, country, lang, price);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlaySearchApps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlaySearchAppsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search apps
    ApiResponse<Object> response = apiInstance.GooglePlaySearchAppsWithHttpInfo(query, country, lang, price);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlaySearchAppsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;puzzle&#39; |  |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |
| **price** | **string** | free | paid | all | [optional]  |

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

<a id="googleplaytopcharts"></a>
# **GooglePlayTopCharts**
> Object GooglePlayTopCharts (string collection, string category = null, string country = null, string lang = null)

Top charts

Top charts for a collection, optionally scoped to a category.

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
    public class GooglePlayTopChartsExample
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
            var apiInstance = new GooglePlayApi(httpClient, config, httpClientHandler);
            var collection = "collection_example";  // string | topselling_free | topselling_paid | topgrossing
            var category = "\"APPLICATION\"";  // string | Play category, e.g. 'GAME' (optional)  (default to "APPLICATION")
            var country = "\"US\"";  // string | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. 'US' (optional)  (default to "US")
            var lang = "\"en\"";  // string | Play content language (hl), e.g. 'en' or 'pt-BR' (optional)  (default to "en")

            try
            {
                // Top charts
                Object result = apiInstance.GooglePlayTopCharts(collection, category, country, lang);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GooglePlayApi.GooglePlayTopCharts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePlayTopChartsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Top charts
    ApiResponse<Object> response = apiInstance.GooglePlayTopChartsWithHttpInfo(collection, category, country, lang);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GooglePlayApi.GooglePlayTopChartsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **collection** | **string** | topselling_free | topselling_paid | topgrossing |  |
| **category** | **string** | Play category, e.g. &#39;GAME&#39; | [optional] [default to &quot;APPLICATION&quot;] |
| **country** | **string** | Play storefront country (gl), ISO 3166-1 alpha-2, e.g. &#39;US&#39; | [optional] [default to &quot;US&quot;] |
| **lang** | **string** | Play content language (hl), e.g. &#39;en&#39; or &#39;pt-BR&#39; | [optional] [default to &quot;en&quot;] |

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

