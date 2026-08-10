# ScrapeBadger.Api.VintedApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**VintedGetItemDetails**](VintedApi.md#vintedgetitemdetails) | **GET** /v1/vinted/items/{item_id} | Get item details |
| [**VintedGetUserProfile**](VintedApi.md#vintedgetuserprofile) | **GET** /v1/vinted/users/{user_id} | Get user profile |
| [**VintedGetUserSListedItems**](VintedApi.md#vintedgetuserslisteditems) | **GET** /v1/vinted/users/{user_id}/items | Get user&#39;s listed items |
| [**VintedListColors**](VintedApi.md#vintedlistcolors) | **GET** /v1/vinted/colors | List colors |
| [**VintedListItemConditions**](VintedApi.md#vintedlistitemconditions) | **GET** /v1/vinted/statuses | List item conditions |
| [**VintedListMarkets**](VintedApi.md#vintedlistmarkets) | **GET** /v1/vinted/markets | List markets |
| [**VintedSearchBrands**](VintedApi.md#vintedsearchbrands) | **GET** /v1/vinted/brands | Search brands |
| [**VintedSearchVintedItems**](VintedApi.md#vintedsearchvinteditems) | **GET** /v1/vinted/search | Search Vinted items |
| [**VintedVintedScraperHealthCheck**](VintedApi.md#vintedvintedscraperhealthcheck) | **GET** /v1/vinted/health | Vinted scraper health check |
| [**VintedVintedScraperHealthCheckHead**](VintedApi.md#vintedvintedscraperhealthcheckhead) | **HEAD** /v1/vinted/health | Vinted scraper health check |

<a id="vintedgetitemdetails"></a>
# **VintedGetItemDetails**
> Object VintedGetItemDetails (int itemId, string market = null)

Get item details

Get detailed information about a Vinted item.

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
    public class VintedGetItemDetailsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var itemId = 56;  // int | 
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")

            try
            {
                // Get item details
                Object result = apiInstance.VintedGetItemDetails(itemId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedGetItemDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedGetItemDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get item details
    ApiResponse<Object> response = apiInstance.VintedGetItemDetailsWithHttpInfo(itemId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedGetItemDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **int** |  |  |
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |

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

<a id="vintedgetuserprofile"></a>
# **VintedGetUserProfile**
> Object VintedGetUserProfile (int userId, string market = null)

Get user profile

Get a Vinted user's profile.

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
    public class VintedGetUserProfileExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var userId = 56;  // int | 
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")

            try
            {
                // Get user profile
                Object result = apiInstance.VintedGetUserProfile(userId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedGetUserProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedGetUserProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user profile
    ApiResponse<Object> response = apiInstance.VintedGetUserProfileWithHttpInfo(userId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedGetUserProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **int** |  |  |
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |

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

<a id="vintedgetuserslisteditems"></a>
# **VintedGetUserSListedItems**
> Object VintedGetUserSListedItems (int userId, string market = null, int? page = null, int? perPage = null)

Get user's listed items

Get items listed by a Vinted user.

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
    public class VintedGetUserSListedItemsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var userId = 56;  // int | 
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 20;  // int? |  (optional)  (default to 20)

            try
            {
                // Get user's listed items
                Object result = apiInstance.VintedGetUserSListedItems(userId, market, page, perPage);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedGetUserSListedItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedGetUserSListedItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get user's listed items
    ApiResponse<Object> response = apiInstance.VintedGetUserSListedItemsWithHttpInfo(userId, market, page, perPage);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedGetUserSListedItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **userId** | **int** |  |  |
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** |  | [optional] [default to 20] |

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

<a id="vintedlistcolors"></a>
# **VintedListColors**
> Object VintedListColors (string market = null)

List colors

Get available Vinted colors for filtering.

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
    public class VintedListColorsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")

            try
            {
                // List colors
                Object result = apiInstance.VintedListColors(market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedListColors: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedListColorsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List colors
    ApiResponse<Object> response = apiInstance.VintedListColorsWithHttpInfo(market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedListColorsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |

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

<a id="vintedlistitemconditions"></a>
# **VintedListItemConditions**
> Object VintedListItemConditions (string market = null)

List item conditions

Get available item condition statuses.

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
    public class VintedListItemConditionsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")

            try
            {
                // List item conditions
                Object result = apiInstance.VintedListItemConditions(market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedListItemConditions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedListItemConditionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List item conditions
    ApiResponse<Object> response = apiInstance.VintedListItemConditionsWithHttpInfo(market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedListItemConditionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |

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

<a id="vintedlistmarkets"></a>
# **VintedListMarkets**
> Object VintedListMarkets ()

List markets

List all supported Vinted markets.

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
    public class VintedListMarketsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.VintedListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.VintedListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedListMarketsWithHttpInfo: " + e.Message);
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

<a id="vintedsearchbrands"></a>
# **VintedSearchBrands**
> Object VintedSearchBrands (string keyword, string market = null)

Search brands

Search Vinted brands.

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
    public class VintedSearchBrandsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var keyword = "keyword_example";  // string | Brand search keyword
            var market = "\"fr\"";  // string |  (optional)  (default to "fr")

            try
            {
                // Search brands
                Object result = apiInstance.VintedSearchBrands(keyword, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedSearchBrands: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedSearchBrandsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search brands
    ApiResponse<Object> response = apiInstance.VintedSearchBrandsWithHttpInfo(keyword, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedSearchBrandsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **keyword** | **string** | Brand search keyword |  |
| **market** | **string** |  | [optional] [default to &quot;fr&quot;] |

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

<a id="vintedsearchvinteditems"></a>
# **VintedSearchVintedItems**
> Object VintedSearchVintedItems (string query, string market = null, string sellerCountry = null, int? page = null, int? perPage = null, decimal? priceFrom = null, decimal? priceTo = null, string brandIds = null, string catalogIds = null, string colorIds = null, string statusIds = null, string order = null)

Search Vinted items

Search Vinted catalog items with filters.

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
    public class VintedSearchVintedItemsExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search text
            var market = "\"fr\"";  // string | Market code (optional)  (default to "fr")
            var sellerCountry = "sellerCountry_example";  // string | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. 'fr' or 'fr,be'). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller's country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var perPage = 20;  // int? |  (optional)  (default to 20)
            var priceFrom = 8.14D;  // decimal? |  (optional) 
            var priceTo = 8.14D;  // decimal? |  (optional) 
            var brandIds = "brandIds_example";  // string |  (optional) 
            var catalogIds = "catalogIds_example";  // string | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. '1904' or '1904,79'. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the `catalog[]` value in a Vinted category URL (vinted.fr/catalog?catalog[]=1904). (optional) 
            var colorIds = "colorIds_example";  // string | Comma-separated color IDs (optional) 
            var statusIds = "statusIds_example";  // string | Comma-separated condition/status IDs (optional) 
            var order = "order_example";  // string |  (optional) 

            try
            {
                // Search Vinted items
                Object result = apiInstance.VintedSearchVintedItems(query, market, sellerCountry, page, perPage, priceFrom, priceTo, brandIds, catalogIds, colorIds, statusIds, order);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedSearchVintedItems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedSearchVintedItemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Vinted items
    ApiResponse<Object> response = apiInstance.VintedSearchVintedItemsWithHttpInfo(query, market, sellerCountry, page, perPage, priceFrom, priceTo, brandIds, catalogIds, colorIds, statusIds, order);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedSearchVintedItemsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search text |  |
| **market** | **string** | Market code | [optional] [default to &quot;fr&quot;] |
| **sellerCountry** | **string** | Filter to items whose seller is physically located in one of these comma-separated ISO-2 country codes (e.g. &#39;fr&#39; or &#39;fr,be&#39;). Market domains federate cross-border EU listings and Vinted has no native country filter, so each item is enriched with its seller&#39;s country and non-matching ones are dropped. Adds 1 credit per uncached seller looked up (cached for 7 days). | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **perPage** | **int?** |  | [optional] [default to 20] |
| **priceFrom** | **decimal?** |  | [optional]  |
| **priceTo** | **decimal?** |  | [optional]  |
| **brandIds** | **string** |  | [optional]  |
| **catalogIds** | **string** | Comma-separated Vinted catalog (category) IDs to restrict the search to, e.g. &#39;1904&#39; or &#39;1904,79&#39;. Vinted applies this before searching, so pagination totals reflect the filtered set. A catalog ID is the &#x60;catalog[]&#x60; value in a Vinted category URL (vinted.fr/catalog?catalog[]&#x3D;1904). | [optional]  |
| **colorIds** | **string** | Comma-separated color IDs | [optional]  |
| **statusIds** | **string** | Comma-separated condition/status IDs | [optional]  |
| **order** | **string** |  | [optional]  |

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

<a id="vintedvintedscraperhealthcheck"></a>
# **VintedVintedScraperHealthCheck**
> Object VintedVintedScraperHealthCheck ()

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class VintedVintedScraperHealthCheckExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);

            try
            {
                // Vinted scraper health check
                Object result = apiInstance.VintedVintedScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedVintedScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedVintedScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Vinted scraper health check
    ApiResponse<Object> response = apiInstance.VintedVintedScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedVintedScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="vintedvintedscraperhealthcheckhead"></a>
# **VintedVintedScraperHealthCheckHead**
> Object VintedVintedScraperHealthCheckHead ()

Vinted scraper health check

Check health of the Vinted scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class VintedVintedScraperHealthCheckHeadExample
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
            var apiInstance = new VintedApi(httpClient, config, httpClientHandler);

            try
            {
                // Vinted scraper health check
                Object result = apiInstance.VintedVintedScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling VintedApi.VintedVintedScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VintedVintedScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Vinted scraper health check
    ApiResponse<Object> response = apiInstance.VintedVintedScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling VintedApi.VintedVintedScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

