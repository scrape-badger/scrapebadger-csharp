# ScrapeBadger.Api.AliExpressApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AliexpressGetCategoryNavigation**](AliExpressApi.md#aliexpressgetcategorynavigation) | **GET** /v1/aliexpress/categories | Get category navigation |
| [**AliexpressGetProductDetail**](AliExpressApi.md#aliexpressgetproductdetail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail |
| [**AliexpressGetProductReviews**](AliExpressApi.md#aliexpressgetproductreviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews |
| [**AliexpressGetSearchSuggestions**](AliExpressApi.md#aliexpressgetsearchsuggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions |
| [**AliexpressGetStoreProductCategories**](AliExpressApi.md#aliexpressgetstoreproductcategories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories |
| [**AliexpressGetStoreProducts**](AliExpressApi.md#aliexpressgetstoreproducts) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products |
| [**AliexpressGetStoreProfile**](AliExpressApi.md#aliexpressgetstoreprofile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile |
| [**AliexpressSearchProducts**](AliExpressApi.md#aliexpresssearchproducts) | **GET** /v1/aliexpress/search | Search products |

<a id="aliexpressgetcategorynavigation"></a>
# **AliexpressGetCategoryNavigation**
> Object AliexpressGetCategoryNavigation ()

Get category navigation

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
    public class AliexpressGetCategoryNavigationExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);

            try
            {
                // Get category navigation
                Object result = apiInstance.AliexpressGetCategoryNavigation();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetCategoryNavigation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetCategoryNavigationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get category navigation
    ApiResponse<Object> response = apiInstance.AliexpressGetCategoryNavigationWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetCategoryNavigationWithHttpInfo: " + e.Message);
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

<a id="aliexpressgetproductdetail"></a>
# **AliexpressGetProductDetail**
> Object AliexpressGetProductDetail (string productId, string country = null, string currency = null, string language = null)

Get product detail

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
    public class AliexpressGetProductDetailExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en_US\"";  // string |  (optional)  (default to "en_US")

            try
            {
                // Get product detail
                Object result = apiInstance.AliexpressGetProductDetail(productId, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product detail
    ApiResponse<Object> response = apiInstance.AliexpressGetProductDetailWithHttpInfo(productId, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en_US&quot;] |

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

<a id="aliexpressgetproductreviews"></a>
# **AliexpressGetProductReviews**
> Object AliexpressGetProductReviews (string productId, int? page = null, int? pageSize = null, string sort = null)

Get product reviews

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
    public class AliexpressGetProductReviewsExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 10;  // int? |  (optional)  (default to 10)
            var sort = "complex_default";  // string |  (optional)  (default to complex_default)

            try
            {
                // Get product reviews
                Object result = apiInstance.AliexpressGetProductReviews(productId, page, pageSize, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetProductReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetProductReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product reviews
    ApiResponse<Object> response = apiInstance.AliexpressGetProductReviewsWithHttpInfo(productId, page, pageSize, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetProductReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 10] |
| **sort** | **string** |  | [optional] [default to complex_default] |

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

<a id="aliexpressgetsearchsuggestions"></a>
# **AliexpressGetSearchSuggestions**
> Object AliexpressGetSearchSuggestions (string query, string country = null, string language = null)

Get search suggestions

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
    public class AliexpressGetSearchSuggestionsExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var language = "\"en\"";  // string |  (optional)  (default to "en")

            try
            {
                // Get search suggestions
                Object result = apiInstance.AliexpressGetSearchSuggestions(query, country, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get search suggestions
    ApiResponse<Object> response = apiInstance.AliexpressGetSearchSuggestionsWithHttpInfo(query, country, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en&quot;] |

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

<a id="aliexpressgetstoreproductcategories"></a>
# **AliexpressGetStoreProductCategories**
> Object AliexpressGetStoreProductCategories (string storeId, string country = null)

Get store product categories

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
    public class AliexpressGetStoreProductCategoriesExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var storeId = "storeId_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Get store product categories
                Object result = apiInstance.AliexpressGetStoreProductCategories(storeId, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProductCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetStoreProductCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store product categories
    ApiResponse<Object> response = apiInstance.AliexpressGetStoreProductCategoriesWithHttpInfo(storeId, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProductCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **storeId** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="aliexpressgetstoreproducts"></a>
# **AliexpressGetStoreProducts**
> Object AliexpressGetStoreProducts (string storeId, int? page = null, int? pageSize = null, string country = null, string currency = null, string language = null, string query = null, string sort = null)

Get store products

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
    public class AliexpressGetStoreProductsExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var storeId = "storeId_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var pageSize = 24;  // int? |  (optional)  (default to 24)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en\"";  // string |  (optional)  (default to "en")
            var query = "\"\"";  // string |  (optional)  (default to "")
            var sort = "bestmatch_sort";  // string |  (optional)  (default to bestmatch_sort)

            try
            {
                // Get store products
                Object result = apiInstance.AliexpressGetStoreProducts(storeId, page, pageSize, country, currency, language, query, sort);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetStoreProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store products
    ApiResponse<Object> response = apiInstance.AliexpressGetStoreProductsWithHttpInfo(storeId, page, pageSize, country, currency, language, query, sort);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **storeId** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **pageSize** | **int?** |  | [optional] [default to 24] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en&quot;] |
| **query** | **string** |  | [optional] [default to &quot;&quot;] |
| **sort** | **string** |  | [optional] [default to bestmatch_sort] |

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

<a id="aliexpressgetstoreprofile"></a>
# **AliexpressGetStoreProfile**
> Object AliexpressGetStoreProfile (string storeId, string country = null, string currency = null, string language = null)

Get store profile

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
    public class AliexpressGetStoreProfileExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var storeId = "storeId_example";  // string | 
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en\"";  // string |  (optional)  (default to "en")

            try
            {
                // Get store profile
                Object result = apiInstance.AliexpressGetStoreProfile(storeId, country, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressGetStoreProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get store profile
    ApiResponse<Object> response = apiInstance.AliexpressGetStoreProfileWithHttpInfo(storeId, country, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressGetStoreProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **storeId** | **string** |  |  |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en&quot;] |

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

<a id="aliexpresssearchproducts"></a>
# **AliexpressSearchProducts**
> Object AliexpressSearchProducts (string query, int? page = null, string country = null, string currency = null, string language = null, string sort = null, decimal? minPrice = null, decimal? maxPrice = null)

Search products

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
    public class AliexpressSearchProductsExample
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
            var apiInstance = new AliExpressApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | 
            var page = 1;  // int? |  (optional)  (default to 1)
            var country = "\"US\"";  // string |  (optional)  (default to "US")
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var language = "\"en\"";  // string |  (optional)  (default to "en")
            var sort = "default";  // string |  (optional)  (default to default)
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 

            try
            {
                // Search products
                Object result = apiInstance.AliexpressSearchProducts(query, page, country, currency, language, sort, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AliExpressApi.AliexpressSearchProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AliexpressSearchProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search products
    ApiResponse<Object> response = apiInstance.AliexpressSearchProductsWithHttpInfo(query, page, country, currency, language, sort, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AliExpressApi.AliexpressSearchProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** |  |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **country** | **string** |  | [optional] [default to &quot;US&quot;] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **language** | **string** |  | [optional] [default to &quot;en&quot;] |
| **sort** | **string** |  | [optional] [default to default] |
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

