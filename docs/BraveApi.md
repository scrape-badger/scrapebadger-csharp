# ScrapeBadger.Api.BraveApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BraveAutocomplete**](BraveApi.md#braveautocomplete) | **GET** /v1/brave/autocomplete | Autocomplete |
| [**BraveImageSearch**](BraveApi.md#braveimagesearch) | **GET** /v1/brave/images | Image search |
| [**BraveListSupportedLocales**](BraveApi.md#bravelistsupportedlocales) | **GET** /v1/brave/locales | List supported locales |
| [**BraveNewsSearch**](BraveApi.md#bravenewssearch) | **GET** /v1/brave/news | News search |
| [**BraveVideoSearch**](BraveApi.md#bravevideosearch) | **GET** /v1/brave/videos | Video search |
| [**BraveWebSearch**](BraveApi.md#bravewebsearch) | **GET** /v1/brave/search | Web search |

<a id="braveautocomplete"></a>
# **BraveAutocomplete**
> BraveAutocompleteResponse BraveAutocomplete (string query, string country = null)

Autocomplete

Native search-box suggestions with entity descriptions and images. Two credits.

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
    public class BraveAutocompleteExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var country = "us";  // string |  (optional)  (default to us)

            try
            {
                // Autocomplete
                BraveAutocompleteResponse result = apiInstance.BraveAutocomplete(query, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveAutocomplete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveAutocompleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Autocomplete
    ApiResponse<BraveAutocompleteResponse> response = apiInstance.BraveAutocompleteWithHttpInfo(query, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveAutocompleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **country** | **string** |  | [optional] [default to us] |

### Return type

[**BraveAutocompleteResponse**](BraveAutocompleteResponse.md)

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

<a id="braveimagesearch"></a>
# **BraveImageSearch**
> BraveResponse BraveImageSearch (string query, string country = null, string uiLanguage = null, string safeSearch = null, int? count = null)

Image search

Native image batch with original URLs, source pages, thumbnails and dimensions.

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
    public class BraveImageSearchExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Native Brave search query
            var country = "us";  // string | Native result region; see /locales (optional)  (default to us)
            var uiLanguage = "en-us";  // string | UI labels/date language; does not restrict result language (optional)  (default to en-us)
            var safeSearch = "off";  // string |  (optional)  (default to moderate)
            var count = 50;  // int? | Slice the initial native image batch (optional)  (default to 50)

            try
            {
                // Image search
                BraveResponse result = apiInstance.BraveImageSearch(query, country, uiLanguage, safeSearch, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveImageSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveImageSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Image search
    ApiResponse<BraveResponse> response = apiInstance.BraveImageSearchWithHttpInfo(query, country, uiLanguage, safeSearch, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveImageSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Native Brave search query |  |
| **country** | **string** | Native result region; see /locales | [optional] [default to us] |
| **uiLanguage** | **string** | UI labels/date language; does not restrict result language | [optional] [default to en-us] |
| **safeSearch** | **string** |  | [optional] [default to moderate] |
| **count** | **int?** | Slice the initial native image batch | [optional] [default to 50] |

### Return type

[**BraveResponse**](BraveResponse.md)

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

<a id="bravelistsupportedlocales"></a>
# **BraveListSupportedLocales**
> BraveLocalesResponse BraveListSupportedLocales ()

List supported locales

Native country and UI-language choices. Free; result language is a separate preference.

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
    public class BraveListSupportedLocalesExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);

            try
            {
                // List supported locales
                BraveLocalesResponse result = apiInstance.BraveListSupportedLocales();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveListSupportedLocales: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveListSupportedLocalesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported locales
    ApiResponse<BraveLocalesResponse> response = apiInstance.BraveListSupportedLocalesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveListSupportedLocalesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**BraveLocalesResponse**](BraveLocalesResponse.md)

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

<a id="bravenewssearch"></a>
# **BraveNewsSearch**
> BraveResponse BraveNewsSearch (string query, string country = null, string uiLanguage = null, string safeSearch = null, int? count = null)

News search

Native news batch; relative source dates stay display strings.

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
    public class BraveNewsSearchExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Native Brave search query
            var country = "us";  // string | Native result region; see /locales (optional)  (default to us)
            var uiLanguage = "en-us";  // string | UI labels/date language; does not restrict result language (optional)  (default to en-us)
            var safeSearch = "off";  // string |  (optional)  (default to moderate)
            var count = 35;  // int? | Slice the initial native news batch (optional)  (default to 35)

            try
            {
                // News search
                BraveResponse result = apiInstance.BraveNewsSearch(query, country, uiLanguage, safeSearch, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveNewsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveNewsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // News search
    ApiResponse<BraveResponse> response = apiInstance.BraveNewsSearchWithHttpInfo(query, country, uiLanguage, safeSearch, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveNewsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Native Brave search query |  |
| **country** | **string** | Native result region; see /locales | [optional] [default to us] |
| **uiLanguage** | **string** | UI labels/date language; does not restrict result language | [optional] [default to en-us] |
| **safeSearch** | **string** |  | [optional] [default to moderate] |
| **count** | **int?** | Slice the initial native news batch | [optional] [default to 35] |

### Return type

[**BraveResponse**](BraveResponse.md)

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

<a id="bravevideosearch"></a>
# **BraveVideoSearch**
> BravePagedResponse BraveVideoSearch (string query, string country = null, string uiLanguage = null, string safeSearch = null, int? page = null, int? count = null)

Video search

Native video results with duration, creator, publisher and verified page ordinals.

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
    public class BraveVideoSearchExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Native Brave search query
            var country = "us";  // string | Native result region; see /locales (optional)  (default to us)
            var uiLanguage = "en-us";  // string | UI labels/date language; does not restrict result language (optional)  (default to en-us)
            var safeSearch = "off";  // string |  (optional)  (default to moderate)
            var page = 1;  // int? | 1-based native page ordinal (optional)  (default to 1)
            var count = 50;  // int? |  (optional)  (default to 50)

            try
            {
                // Video search
                BravePagedResponse result = apiInstance.BraveVideoSearch(query, country, uiLanguage, safeSearch, page, count);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveVideoSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveVideoSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Video search
    ApiResponse<BravePagedResponse> response = apiInstance.BraveVideoSearchWithHttpInfo(query, country, uiLanguage, safeSearch, page, count);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveVideoSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Native Brave search query |  |
| **country** | **string** | Native result region; see /locales | [optional] [default to us] |
| **uiLanguage** | **string** | UI labels/date language; does not restrict result language | [optional] [default to en-us] |
| **safeSearch** | **string** |  | [optional] [default to moderate] |
| **page** | **int?** | 1-based native page ordinal | [optional] [default to 1] |
| **count** | **int?** |  | [optional] [default to 50] |

### Return type

[**BravePagedResponse**](BravePagedResponse.md)

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

<a id="bravewebsearch"></a>
# **BraveWebSearch**
> BraveSearchResponse BraveWebSearch (string query, string country = null, string uiLanguage = null, string safeSearch = null, int? page = null, int? count = null, string freshness = null, bool? spellcheck = null)

Web search

Native Brave organic results, rich source blocks and page metadata. Seven credits.

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
    public class BraveWebSearchExample
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
            var apiInstance = new BraveApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Native Brave search query
            var country = "us";  // string | Native result region; see /locales (optional)  (default to us)
            var uiLanguage = "en-us";  // string | UI labels/date language; does not restrict result language (optional)  (default to en-us)
            var safeSearch = "off";  // string |  (optional)  (default to moderate)
            var page = 1;  // int? | 1-based native page ordinal (optional)  (default to 1)
            var count = 20;  // int? | Slice one native page; does not change native page boundaries (optional)  (default to 20)
            var freshness = "any";  // string |  (optional)  (default to any)
            var spellcheck = false;  // bool? | Allow native spelling correction (optional)  (default to false)

            try
            {
                // Web search
                BraveSearchResponse result = apiInstance.BraveWebSearch(query, country, uiLanguage, safeSearch, page, count, freshness, spellcheck);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BraveApi.BraveWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BraveWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web search
    ApiResponse<BraveSearchResponse> response = apiInstance.BraveWebSearchWithHttpInfo(query, country, uiLanguage, safeSearch, page, count, freshness, spellcheck);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BraveApi.BraveWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Native Brave search query |  |
| **country** | **string** | Native result region; see /locales | [optional] [default to us] |
| **uiLanguage** | **string** | UI labels/date language; does not restrict result language | [optional] [default to en-us] |
| **safeSearch** | **string** |  | [optional] [default to moderate] |
| **page** | **int?** | 1-based native page ordinal | [optional] [default to 1] |
| **count** | **int?** | Slice one native page; does not change native page boundaries | [optional] [default to 20] |
| **freshness** | **string** |  | [optional] [default to any] |
| **spellcheck** | **bool?** | Allow native spelling correction | [optional] [default to false] |

### Return type

[**BraveSearchResponse**](BraveSearchResponse.md)

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

