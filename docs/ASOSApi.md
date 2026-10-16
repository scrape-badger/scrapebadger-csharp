# ScrapeBadger.Api.ASOSApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AsosGetProductDetail**](ASOSApi.md#asosgetproductdetail) | **GET** /v1/asos/products/{product_id} | Get product detail |
| [**AsosGetStockAndPrices**](ASOSApi.md#asosgetstockandprices) | **GET** /v1/asos/stock-price | Get stock and prices |
| [**AsosListCategories**](ASOSApi.md#asoslistcategories) | **GET** /v1/asos/categories | List categories |
| [**AsosListMarkets**](ASOSApi.md#asoslistmarkets) | **GET** /v1/asos/markets | List markets |
| [**AsosListSearchFilters**](ASOSApi.md#asoslistsearchfilters) | **GET** /v1/asos/filters | List search filters |
| [**AsosSearchProducts**](ASOSApi.md#asossearchproducts) | **GET** /v1/asos/search | Search products |
| [**AsosSearchSuggestions**](ASOSApi.md#asossearchsuggestions) | **GET** /v1/asos/autocomplete | Search suggestions |

<a id="asosgetproductdetail"></a>
# **AsosGetProductDetail**
> ProductResponse AsosGetProductDetail (int productId, string market = null, string store = null, string country = null, string currency = null, string language = null)

Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

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
    public class AsosGetProductDetailExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var productId = 56;  // int | 
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // Get product detail
                ProductResponse result = apiInstance.AsosGetProductDetail(productId, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosGetProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosGetProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product detail
    ApiResponse<ProductResponse> response = apiInstance.AsosGetProductDetailWithHttpInfo(productId, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosGetProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **int** |  |  |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

### Return type

[**ProductResponse**](ProductResponse.md)

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

<a id="asosgetstockandprices"></a>
# **AsosGetStockAndPrices**
> StockResponse AsosGetStockAndPrices (string productIds, string market = null, string store = null, string country = null, string currency = null, string language = null)

Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

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
    public class AsosGetStockAndPricesExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var productIds = "productIds_example";  // string | 1–50 comma-separated product ids
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // Get stock and prices
                StockResponse result = apiInstance.AsosGetStockAndPrices(productIds, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosGetStockAndPrices: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosGetStockAndPricesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get stock and prices
    ApiResponse<StockResponse> response = apiInstance.AsosGetStockAndPricesWithHttpInfo(productIds, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosGetStockAndPricesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productIds** | **string** | 1–50 comma-separated product ids |  |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

### Return type

[**StockResponse**](StockResponse.md)

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

<a id="asoslistcategories"></a>
# **AsosListCategories**
> Object AsosListCategories (string gender = null, string market = null, string store = null, string country = null, string currency = null, string language = null)

List categories

Full nested navigation with category ids, names, images and links.

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
    public class AsosListCategoriesExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var gender = "men";  // string |  (optional)  (default to men)
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // List categories
                Object result = apiInstance.AsosListCategories(gender, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosListCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosListCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List categories
    ApiResponse<Object> response = apiInstance.AsosListCategoriesWithHttpInfo(gender, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosListCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **gender** | **string** |  | [optional] [default to men] |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

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

<a id="asoslistmarkets"></a>
# **AsosListMarkets**
> Object AsosListMarkets ()

List markets

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
    public class AsosListMarketsExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.AsosListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.AsosListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosListMarketsWithHttpInfo: " + e.Message);
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

<a id="asoslistsearchfilters"></a>
# **AsosListSearchFilters**
> Object AsosListSearchFilters (string query = null, int? categoryId = null, string market = null, string store = null, string country = null, string currency = null, string language = null)

List search filters

Facet ids, labels, option counts and selections for a query or category.

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
    public class AsosListSearchFiltersExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string |  (optional) 
            var categoryId = 56;  // int? |  (optional) 
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // List search filters
                Object result = apiInstance.AsosListSearchFilters(query, categoryId, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosListSearchFilters: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosListSearchFiltersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List search filters
    ApiResponse<Object> response = apiInstance.AsosListSearchFiltersWithHttpInfo(query, categoryId, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosListSearchFiltersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  | [optional]  |
| **categoryId** | **int?** |  | [optional]  |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

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

<a id="asossearchproducts"></a>
# **AsosSearchProducts**
> PortalApiRoutersV1AsosSearchResponse AsosSearchProducts (string query = null, int? categoryId = null, int? offset = null, int? limit = null, string sort = null, string brand = null, string colour = null, string size = null, decimal? minPrice = null, decimal? maxPrice = null, string market = null, string store = null, string country = null, string currency = null, string language = null)

Search products

Search by query, category_id, or both. Includes price, images and filter facets.

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
    public class AsosSearchProductsExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Keyword, e.g. shoes (optional) 
            var categoryId = 56;  // int? | Category id from navigation (optional) 
            var offset = 0;  // int? |  (optional)  (default to 0)
            var limit = 48;  // int? |  (optional)  (default to 48)
            var sort = "recommended";  // string |  (optional)  (default to recommended)
            var brand = "brand_example";  // string | Comma-separated brand facet ids (optional) 
            var colour = "colour_example";  // string | Comma-separated colour facet ids (optional) 
            var size = "size_example";  // string | Comma-separated size facet ids (optional) 
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // Search products
                PortalApiRoutersV1AsosSearchResponse result = apiInstance.AsosSearchProducts(query, categoryId, offset, limit, sort, brand, colour, size, minPrice, maxPrice, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosSearchProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosSearchProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search products
    ApiResponse<PortalApiRoutersV1AsosSearchResponse> response = apiInstance.AsosSearchProductsWithHttpInfo(query, categoryId, offset, limit, sort, brand, colour, size, minPrice, maxPrice, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosSearchProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Keyword, e.g. shoes | [optional]  |
| **categoryId** | **int?** | Category id from navigation | [optional]  |
| **offset** | **int?** |  | [optional] [default to 0] |
| **limit** | **int?** |  | [optional] [default to 48] |
| **sort** | **string** |  | [optional] [default to recommended] |
| **brand** | **string** | Comma-separated brand facet ids | [optional]  |
| **colour** | **string** | Comma-separated colour facet ids | [optional]  |
| **size** | **string** | Comma-separated size facet ids | [optional]  |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

### Return type

[**PortalApiRoutersV1AsosSearchResponse**](PortalApiRoutersV1AsosSearchResponse.md)

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

<a id="asossearchsuggestions"></a>
# **AsosSearchSuggestions**
> Object AsosSearchSuggestions (string query, string market = null, string store = null, string country = null, string currency = null, string language = null)

Search suggestions

Search suggestions with result counts.

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
    public class AsosSearchSuggestionsExample
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
            var apiInstance = new ASOSApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var market = "\"uk\"";  // string | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl (optional)  (default to "uk")
            var store = "store_example";  // string | Override store, e.g. COM or US (optional) 
            var country = "country_example";  // string | ISO country override (optional) 
            var currency = "currency_example";  // string | Currency override (optional) 
            var language = "language_example";  // string | Locale override, e.g. en-GB (optional) 

            try
            {
                // Search suggestions
                Object result = apiInstance.AsosSearchSuggestions(query, market, store, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ASOSApi.AsosSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AsosSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.AsosSearchSuggestionsWithHttpInfo(query, market, store, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ASOSApi.AsosSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **market** | **string** | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to &quot;uk&quot;] |
| **store** | **string** | Override store, e.g. COM or US | [optional]  |
| **country** | **string** | ISO country override | [optional]  |
| **currency** | **string** | Currency override | [optional]  |
| **language** | **string** | Locale override, e.g. en-GB | [optional]  |

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

