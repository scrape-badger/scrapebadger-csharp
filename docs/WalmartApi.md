# ScrapeBadger.Api.WalmartApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**WalmartBrowseACategory**](WalmartApi.md#walmartbrowseacategory) | **GET** /v1/walmart/category | Browse a category |
| [**WalmartDealsRollbacksAndClearance**](WalmartApi.md#walmartdealsrollbacksandclearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance |
| [**WalmartGetASellerSCatalogue**](WalmartApi.md#walmartgetasellerscatalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue |
| [**WalmartGetProductDetail**](WalmartApi.md#walmartgetproductdetail) | **GET** /v1/walmart/products/{item_id} | Get product detail |
| [**WalmartGetProductReviews**](WalmartApi.md#walmartgetproductreviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews |
| [**WalmartGetSellerProfile**](WalmartApi.md#walmartgetsellerprofile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile |
| [**WalmartGetStoreNearbyStores**](WalmartApi.md#walmartgetstorenearbystores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores |
| [**WalmartListSupportedMarkets**](WalmartApi.md#walmartlistsupportedmarkets) | **GET** /v1/walmart/markets | List supported markets |
| [**WalmartSearchProducts**](WalmartApi.md#walmartsearchproducts) | **GET** /v1/walmart/search | Search products |
| [**WalmartSearchSuggestions**](WalmartApi.md#walmartsearchsuggestions) | **GET** /v1/walmart/autocomplete | Search suggestions |
| [**WalmartWalmartScraperHealthCheck**](WalmartApi.md#walmartwalmartscraperhealthcheck) | **GET** /v1/walmart/health | Walmart scraper health check |
| [**WalmartWalmartScraperHealthCheckHead**](WalmartApi.md#walmartwalmartscraperhealthcheckhead) | **HEAD** /v1/walmart/health | Walmart scraper health check |

<a id="walmartbrowseacategory"></a>
# **WalmartBrowseACategory**
> Object WalmartBrowseACategory (string path, int? page = null, decimal? minPrice = null, decimal? maxPrice = null, string facet = null)

Browse a category

Browse a Walmart category. Same result shape as search.  No `sort`: Walmart's browse pages ignore it. Sort on `/search` instead.

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
    public class WalmartBrowseACategoryExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var path = "path_example";  // string | Browse path, e.g. 'electronics/3944', or a '/cp/...' path
            var page = 1;  // int? |  (optional)  (default to 1)
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var facet = "facet_example";  // string |  (optional) 

            try
            {
                // Browse a category
                Object result = apiInstance.WalmartBrowseACategory(path, page, minPrice, maxPrice, facet);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartBrowseACategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartBrowseACategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Browse a category
    ApiResponse<Object> response = apiInstance.WalmartBrowseACategoryWithHttpInfo(path, page, minPrice, maxPrice, facet);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartBrowseACategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **path** | **string** | Browse path, e.g. &#39;electronics/3944&#39;, or a &#39;/cp/...&#39; path |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **facet** | **string** |  | [optional]  |

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

<a id="walmartdealsrollbacksandclearance"></a>
# **WalmartDealsRollbacksAndClearance**
> Object WalmartDealsRollbacksAndClearance (int? page = null, decimal? minPrice = null, decimal? maxPrice = null)

Deals, rollbacks and clearance

Walmart's current deals, rollbacks and clearance.

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
    public class WalmartDealsRollbacksAndClearanceExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var page = 1;  // int? |  (optional)  (default to 1)
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Deals, rollbacks and clearance
                Object result = apiInstance.WalmartDealsRollbacksAndClearance(page, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartDealsRollbacksAndClearance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartDealsRollbacksAndClearanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deals, rollbacks and clearance
    ApiResponse<Object> response = apiInstance.WalmartDealsRollbacksAndClearanceWithHttpInfo(page, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartDealsRollbacksAndClearanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **page** | **int?** |  | [optional] [default to 1] |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |

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

<a id="walmartgetasellerscatalogue"></a>
# **WalmartGetASellerSCatalogue**
> Object WalmartGetASellerSCatalogue (string sellerId, string query, int? page = null, string sort = null)

Get a seller's catalogue

A marketplace seller's catalogue, scoped by a search term.

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
    public class WalmartGetASellerSCatalogueExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
            var query = "query_example";  // string | Required — Walmart returns nothing for a seller facet alone
            var page = 1;  // int? |  (optional)  (default to 1)
            var sort = "sort_example";  // string |  (optional) 

            try
            {
                // Get a seller's catalogue
                Object result = apiInstance.WalmartGetASellerSCatalogue(sellerId, query, page, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartGetASellerSCatalogue: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartGetASellerSCatalogueWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a seller's catalogue
    ApiResponse<Object> response = apiInstance.WalmartGetASellerSCatalogueWithHttpInfo(sellerId, query, page, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartGetASellerSCatalogueWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). |  |
| **query** | **string** | Required — Walmart returns nothing for a seller facet alone |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **sort** | **string** |  | [optional]  |

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

<a id="walmartgetproductdetail"></a>
# **WalmartGetProductDetail**
> Object WalmartGetProductDetail (string itemId)

Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

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
    public class WalmartGetProductDetailExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var itemId = "itemId_example";  // string | Walmart usItemId, e.g. '5689919121'

            try
            {
                // Get product detail
                Object result = apiInstance.WalmartGetProductDetail(itemId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartGetProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartGetProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product detail
    ApiResponse<Object> response = apiInstance.WalmartGetProductDetailWithHttpInfo(itemId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartGetProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **string** | Walmart usItemId, e.g. &#39;5689919121&#39; |  |

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

<a id="walmartgetproductreviews"></a>
# **WalmartGetProductReviews**
> Object WalmartGetProductReviews (string itemId, int? page = null, string sort = null)

Get product reviews

Paginated reviews with the full star histogram. 10 per page.

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
    public class WalmartGetProductReviewsExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var itemId = "itemId_example";  // string | Walmart usItemId, e.g. '5689919121'
            var page = 1;  // int? |  (optional)  (default to 1)
            var sort = "sort_example";  // string | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful (optional) 

            try
            {
                // Get product reviews
                Object result = apiInstance.WalmartGetProductReviews(itemId, page, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartGetProductReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartGetProductReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product reviews
    ApiResponse<Object> response = apiInstance.WalmartGetProductReviewsWithHttpInfo(itemId, page, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartGetProductReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **itemId** | **string** | Walmart usItemId, e.g. &#39;5689919121&#39; |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **sort** | **string** | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful | [optional]  |

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

<a id="walmartgetsellerprofile"></a>
# **WalmartGetSellerProfile**
> Object WalmartGetSellerProfile (string sellerId)

Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No `page`: adding one makes Walmart's own SSR throw. Use `/sellers/{id}/products` for the catalogue.

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
    public class WalmartGetSellerProfileExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).

            try
            {
                // Get seller profile
                Object result = apiInstance.WalmartGetSellerProfile(sellerId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartGetSellerProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartGetSellerProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller profile
    ApiResponse<Object> response = apiInstance.WalmartGetSellerProfileWithHttpInfo(sellerId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartGetSellerProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** | Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). |  |

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

<a id="walmartgetstorenearbystores"></a>
# **WalmartGetStoreNearbyStores**
> Object WalmartGetStoreNearbyStores (string storeId)

Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

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
    public class WalmartGetStoreNearbyStoresExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var storeId = "storeId_example";  // string | Walmart store number, e.g. '100'

            try
            {
                // Get store + nearby stores
                Object result = apiInstance.WalmartGetStoreNearbyStores(storeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartGetStoreNearbyStores: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartGetStoreNearbyStoresWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store + nearby stores
    ApiResponse<Object> response = apiInstance.WalmartGetStoreNearbyStoresWithHttpInfo(storeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartGetStoreNearbyStoresWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **storeId** | **string** | Walmart store number, e.g. &#39;100&#39; |  |

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

<a id="walmartlistsupportedmarkets"></a>
# **WalmartListSupportedMarkets**
> Object WalmartListSupportedMarkets ()

List supported markets

Supported Walmart markets.

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
    public class WalmartListSupportedMarketsExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);

            try
            {
                // List supported markets
                Object result = apiInstance.WalmartListSupportedMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartListSupportedMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartListSupportedMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List supported markets
    ApiResponse<Object> response = apiInstance.WalmartListSupportedMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartListSupportedMarketsWithHttpInfo: " + e.Message);
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

<a id="walmartsearchproducts"></a>
# **WalmartSearchProducts**
> Object WalmartSearchProducts (string query, int? page = null, string sort = null, decimal? minPrice = null, decimal? maxPrice = null, string facet = null)

Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

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
    public class WalmartSearchProductsExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords, e.g. 'laptop'
            var page = 1;  // int? | Results dry up after page 10 (optional)  (default to 1)
            var sort = "sort_example";  // string | best_match | best_seller | price_low | price_high | rating_high | new (optional) 
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var facet = "facet_example";  // string | Facet filter, e.g. 'brand:HP' (optional) 

            try
            {
                // Search products
                Object result = apiInstance.WalmartSearchProducts(query, page, sort, minPrice, maxPrice, facet);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartSearchProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartSearchProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search products
    ApiResponse<Object> response = apiInstance.WalmartSearchProductsWithHttpInfo(query, page, sort, minPrice, maxPrice, facet);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartSearchProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords, e.g. &#39;laptop&#39; |  |
| **page** | **int?** | Results dry up after page 10 | [optional] [default to 1] |
| **sort** | **string** | best_match | best_seller | price_low | price_high | rating_high | new | [optional]  |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **facet** | **string** | Facet filter, e.g. &#39;brand:HP&#39; | [optional]  |

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

<a id="walmartsearchsuggestions"></a>
# **WalmartSearchSuggestions**
> Object WalmartSearchSuggestions (string query)

Search suggestions

Walmart search-box suggestions.

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
    public class WalmartSearchSuggestionsExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term, e.g. 'lapt'

            try
            {
                // Search suggestions
                Object result = apiInstance.WalmartSearchSuggestions(query);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search suggestions
    ApiResponse<Object> response = apiInstance.WalmartSearchSuggestionsWithHttpInfo(query);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term, e.g. &#39;lapt&#39; |  |

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

<a id="walmartwalmartscraperhealthcheck"></a>
# **WalmartWalmartScraperHealthCheck**
> Object WalmartWalmartScraperHealthCheck ()

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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
    public class WalmartWalmartScraperHealthCheckExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);

            try
            {
                // Walmart scraper health check
                Object result = apiInstance.WalmartWalmartScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartWalmartScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartWalmartScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Walmart scraper health check
    ApiResponse<Object> response = apiInstance.WalmartWalmartScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartWalmartScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="walmartwalmartscraperhealthcheckhead"></a>
# **WalmartWalmartScraperHealthCheckHead**
> Object WalmartWalmartScraperHealthCheckHead ()

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

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
    public class WalmartWalmartScraperHealthCheckHeadExample
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
            var apiInstance = new WalmartApi(httpClient, config, httpClientHandler);

            try
            {
                // Walmart scraper health check
                Object result = apiInstance.WalmartWalmartScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WalmartApi.WalmartWalmartScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WalmartWalmartScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Walmart scraper health check
    ApiResponse<Object> response = apiInstance.WalmartWalmartScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WalmartApi.WalmartWalmartScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

