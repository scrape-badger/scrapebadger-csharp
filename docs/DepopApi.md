# ScrapeBadger.Api.DepopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DepopDepopScraperHealthCheck**](DepopApi.md#depopdepopscraperhealthcheck) | **GET** /v1/depop/health | Depop scraper health check |
| [**DepopDepopScraperHealthCheckHead**](DepopApi.md#depopdepopscraperhealthcheckhead) | **HEAD** /v1/depop/health | Depop scraper health check |
| [**DepopGetAUserSProducts**](DepopApi.md#depopgetausersproducts) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products |
| [**DepopGetProductDetail**](DepopApi.md#depopgetproductdetail) | **GET** /v1/depop/products/{product_id} | Get product detail |
| [**DepopGetShopUserProfile**](DepopApi.md#depopgetshopuserprofile) | **GET** /v1/depop/users/{username} | Get shop/user profile |
| [**DepopListMarkets**](DepopApi.md#depoplistmarkets) | **GET** /v1/depop/markets | List markets |
| [**DepopSearchDepopProducts**](DepopApi.md#depopsearchdepopproducts) | **GET** /v1/depop/search | Search Depop products |

<a id="depopdepopscraperhealthcheck"></a>
# **DepopDepopScraperHealthCheck**
> Object DepopDepopScraperHealthCheck ()

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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
    public class DepopDepopScraperHealthCheckExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);

            try
            {
                // Depop scraper health check
                Object result = apiInstance.DepopDepopScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopDepopScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopDepopScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Depop scraper health check
    ApiResponse<Object> response = apiInstance.DepopDepopScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopDepopScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="depopdepopscraperhealthcheckhead"></a>
# **DepopDepopScraperHealthCheckHead**
> Object DepopDepopScraperHealthCheckHead ()

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

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
    public class DepopDepopScraperHealthCheckHeadExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);

            try
            {
                // Depop scraper health check
                Object result = apiInstance.DepopDepopScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopDepopScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopDepopScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Depop scraper health check
    ApiResponse<Object> response = apiInstance.DepopDepopScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopDepopScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="depopgetausersproducts"></a>
# **DepopGetAUserSProducts**
> Object DepopGetAUserSProducts (string username, string market = null, int? perPage = null, string cursor = null)

Get a user's products

A user's active listings (cursor-paginated).

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
    public class DepopGetAUserSProductsExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var market = "\"us\"";  // string | Market code (optional)  (default to "us")
            var perPage = 24;  // int? |  (optional)  (default to 24)
            var cursor = "cursor_example";  // string | Pagination cursor (optional) 

            try
            {
                // Get a user's products
                Object result = apiInstance.DepopGetAUserSProducts(username, market, perPage, cursor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopGetAUserSProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopGetAUserSProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a user's products
    ApiResponse<Object> response = apiInstance.DepopGetAUserSProductsWithHttpInfo(username, market, perPage, cursor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopGetAUserSProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **market** | **string** | Market code | [optional] [default to &quot;us&quot;] |
| **perPage** | **int?** |  | [optional] [default to 24] |
| **cursor** | **string** | Pagination cursor | [optional]  |

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

<a id="depopgetproductdetail"></a>
# **DepopGetProductDetail**
> Object DepopGetProductDetail (string productId, string market = null)

Get product detail

Full detail for a single product (by numeric id or slug).

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
    public class DepopGetProductDetailExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | 
            var market = "\"us\"";  // string | Market code (optional)  (default to "us")

            try
            {
                // Get product detail
                Object result = apiInstance.DepopGetProductDetail(productId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopGetProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopGetProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product detail
    ApiResponse<Object> response = apiInstance.DepopGetProductDetailWithHttpInfo(productId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopGetProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** |  |  |
| **market** | **string** | Market code | [optional] [default to &quot;us&quot;] |

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

<a id="depopgetshopuserprofile"></a>
# **DepopGetShopUserProfile**
> Object DepopGetShopUserProfile (string username, string market = null)

Get shop/user profile

Public shop/user profile by username.

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
    public class DepopGetShopUserProfileExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);
            var username = "username_example";  // string | 
            var market = "\"us\"";  // string | Market code (optional)  (default to "us")

            try
            {
                // Get shop/user profile
                Object result = apiInstance.DepopGetShopUserProfile(username, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopGetShopUserProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopGetShopUserProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get shop/user profile
    ApiResponse<Object> response = apiInstance.DepopGetShopUserProfileWithHttpInfo(username, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopGetShopUserProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **username** | **string** |  |  |
| **market** | **string** | Market code | [optional] [default to &quot;us&quot;] |

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

<a id="depoplistmarkets"></a>
# **DepopListMarkets**
> Object DepopListMarkets ()

List markets

List supported Depop markets (country + currency).

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
    public class DepopListMarketsExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.DepopListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.DepopListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopListMarketsWithHttpInfo: " + e.Message);
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

<a id="depopsearchdepopproducts"></a>
# **DepopSearchDepopProducts**
> Object DepopSearchDepopProducts (string query, string market = null, int? perPage = null, string cursor = null, decimal? priceMin = null, decimal? priceMax = null, string brands = null, string categories = null, string sizes = null, string conditions = null, string gender = null, string sort = null)

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

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
    public class DepopSearchDepopProductsExample
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
            var apiInstance = new DepopApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search text, e.g. 'nike vintage'
            var market = "\"us\"";  // string | Market code (us, gb, au, it, fr, ...) (optional)  (default to "us")
            var perPage = 24;  // int? | Results per page (optional)  (default to 24)
            var cursor = "cursor_example";  // string | Pagination cursor (from previous page) (optional) 
            var priceMin = 8.14D;  // decimal? | Minimum price (optional) 
            var priceMax = 8.14D;  // decimal? | Maximum price (optional) 
            var brands = "brands_example";  // string | Comma-separated brand IDs (optional) 
            var categories = "categories_example";  // string | Comma-separated category IDs (optional) 
            var sizes = "sizes_example";  // string | Comma-separated size IDs (optional) 
            var conditions = "conditions_example";  // string | Comma-separated condition slugs (brand_new, used_excellent, ...) (optional) 
            var gender = "gender_example";  // string | male | female (optional) 
            var sort = "sort_example";  // string | relevance | newlyListed | priceAscending | priceDescending (optional) 

            try
            {
                // Search Depop products
                Object result = apiInstance.DepopSearchDepopProducts(query, market, perPage, cursor, priceMin, priceMax, brands, categories, sizes, conditions, gender, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DepopApi.DepopSearchDepopProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DepopSearchDepopProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Depop products
    ApiResponse<Object> response = apiInstance.DepopSearchDepopProductsWithHttpInfo(query, market, perPage, cursor, priceMin, priceMax, brands, categories, sizes, conditions, gender, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DepopApi.DepopSearchDepopProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search text, e.g. &#39;nike vintage&#39; |  |
| **market** | **string** | Market code (us, gb, au, it, fr, ...) | [optional] [default to &quot;us&quot;] |
| **perPage** | **int?** | Results per page | [optional] [default to 24] |
| **cursor** | **string** | Pagination cursor (from previous page) | [optional]  |
| **priceMin** | **decimal?** | Minimum price | [optional]  |
| **priceMax** | **decimal?** | Maximum price | [optional]  |
| **brands** | **string** | Comma-separated brand IDs | [optional]  |
| **categories** | **string** | Comma-separated category IDs | [optional]  |
| **sizes** | **string** | Comma-separated size IDs | [optional]  |
| **conditions** | **string** | Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional]  |
| **gender** | **string** | male | female | [optional]  |
| **sort** | **string** | relevance | newlyListed | priceAscending | priceDescending | [optional]  |

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

