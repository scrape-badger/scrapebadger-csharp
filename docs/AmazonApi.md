# ScrapeBadger.Api.AmazonApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AmazonAmazonScraperHealthCheck**](AmazonApi.md#amazonamazonscraperhealthcheck) | **GET** /v1/amazon/health | Amazon scraper health check |
| [**AmazonAmazonScraperHealthCheckHead**](AmazonApi.md#amazonamazonscraperhealthcheckhead) | **HEAD** /v1/amazon/health | Amazon scraper health check |
| [**AmazonBestsellersByCategory**](AmazonApi.md#amazonbestsellersbycategory) | **GET** /v1/amazon/bestsellers | Bestsellers by category |
| [**AmazonBrowseNodeCategoryListing**](AmazonApi.md#amazonbrowsenodecategorylisting) | **GET** /v1/amazon/category | Browse-node category listing |
| [**AmazonGetAllSellerOffersBuybox**](AmazonApi.md#amazongetallselleroffersbuybox) | **GET** /v1/amazon/products/{asin}/offers | Get all seller offers (buybox) |
| [**AmazonGetProductDetail**](AmazonApi.md#amazongetproductdetail) | **GET** /v1/amazon/products/{asin} | Get product detail |
| [**AmazonGetProductReviews**](AmazonApi.md#amazongetproductreviews) | **GET** /v1/amazon/products/{asin}/reviews | Get product reviews |
| [**AmazonGetSellerFeedback**](AmazonApi.md#amazongetsellerfeedback) | **GET** /v1/amazon/sellers/{seller_id}/feedback | Get seller feedback |
| [**AmazonGetSellerProfile**](AmazonApi.md#amazongetsellerprofile) | **GET** /v1/amazon/sellers/{seller_id} | Get seller profile |
| [**AmazonGetSellerStorefrontProducts**](AmazonApi.md#amazongetsellerstorefrontproducts) | **GET** /v1/amazon/sellers/{seller_id}/products | Get seller storefront products |
| [**AmazonKeywordSuggestions**](AmazonApi.md#amazonkeywordsuggestions) | **GET** /v1/amazon/autocomplete | Keyword suggestions |
| [**AmazonListCategoryAliases**](AmazonApi.md#amazonlistcategoryaliases) | **GET** /v1/amazon/categories | List category aliases |
| [**AmazonListMarketplaces**](AmazonApi.md#amazonlistmarketplaces) | **GET** /v1/amazon/markets | List marketplaces |
| [**AmazonNewReleasesByCategory**](AmazonApi.md#amazonnewreleasesbycategory) | **GET** /v1/amazon/new-releases | New releases by category |
| [**AmazonSearchAmazonProducts**](AmazonApi.md#amazonsearchamazonproducts) | **GET** /v1/amazon/search | Search Amazon products |
| [**AmazonTodaySDeals**](AmazonApi.md#amazontodaysdeals) | **GET** /v1/amazon/deals | Today&#39;s deals |

<a id="amazonamazonscraperhealthcheck"></a>
# **AmazonAmazonScraperHealthCheck**
> Object AmazonAmazonScraperHealthCheck ()

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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
    public class AmazonAmazonScraperHealthCheckExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);

            try
            {
                // Amazon scraper health check
                Object result = apiInstance.AmazonAmazonScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonAmazonScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonAmazonScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Amazon scraper health check
    ApiResponse<Object> response = apiInstance.AmazonAmazonScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonAmazonScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="amazonamazonscraperhealthcheckhead"></a>
# **AmazonAmazonScraperHealthCheckHead**
> Object AmazonAmazonScraperHealthCheckHead ()

Amazon scraper health check

Check health of the Amazon scraper service (accepts HEAD for UptimeRobot).

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
    public class AmazonAmazonScraperHealthCheckHeadExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);

            try
            {
                // Amazon scraper health check
                Object result = apiInstance.AmazonAmazonScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonAmazonScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonAmazonScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Amazon scraper health check
    ApiResponse<Object> response = apiInstance.AmazonAmazonScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonAmazonScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="amazonbestsellersbycategory"></a>
# **AmazonBestsellersByCategory**
> Object AmazonBestsellersByCategory (string domain = null, string category = null, int? page = null)

Bestsellers by category

Top-selling products for a category (browse node).

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
    public class AmazonBestsellersByCategoryExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var category = "category_example";  // string | Bestsellers node id or slug (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Bestsellers by category
                Object result = apiInstance.AmazonBestsellersByCategory(domain, category, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonBestsellersByCategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonBestsellersByCategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Bestsellers by category
    ApiResponse<Object> response = apiInstance.AmazonBestsellersByCategoryWithHttpInfo(domain, category, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonBestsellersByCategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **category** | **string** | Bestsellers node id or slug | [optional]  |
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

<a id="amazonbrowsenodecategorylisting"></a>
# **AmazonBrowseNodeCategoryListing**
> Object AmazonBrowseNodeCategoryListing (string node, string domain = null, int? page = null, string sortBy = null)

Browse-node category listing

List products within an Amazon browse-node category.

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
    public class AmazonBrowseNodeCategoryListingExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var node = "node_example";  // string | Amazon browse-node id
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)
            var sortBy = "sortBy_example";  // string |  (optional) 

            try
            {
                // Browse-node category listing
                Object result = apiInstance.AmazonBrowseNodeCategoryListing(node, domain, page, sortBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonBrowseNodeCategoryListing: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonBrowseNodeCategoryListingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Browse-node category listing
    ApiResponse<Object> response = apiInstance.AmazonBrowseNodeCategoryListingWithHttpInfo(node, domain, page, sortBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonBrowseNodeCategoryListingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **node** | **string** | Amazon browse-node id |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **sortBy** | **string** |  | [optional]  |

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

<a id="amazongetallselleroffersbuybox"></a>
# **AmazonGetAllSellerOffersBuybox**
> Object AmazonGetAllSellerOffersBuybox (string asin, string domain = null, string zip = null)

Get all seller offers (buybox)

All third-party offers for an ASIN, including the Buy Box winner.

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
    public class AmazonGetAllSellerOffersBuyboxExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var asin = "asin_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var zip = "zip_example";  // string |  (optional) 

            try
            {
                // Get all seller offers (buybox)
                Object result = apiInstance.AmazonGetAllSellerOffersBuybox(asin, domain, zip);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetAllSellerOffersBuybox: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetAllSellerOffersBuyboxWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all seller offers (buybox)
    ApiResponse<Object> response = apiInstance.AmazonGetAllSellerOffersBuyboxWithHttpInfo(asin, domain, zip);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetAllSellerOffersBuyboxWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **asin** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **zip** | **string** |  | [optional]  |

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

<a id="amazongetproductdetail"></a>
# **AmazonGetProductDetail**
> Object AmazonGetProductDetail (string asin, string domain = null, string zip = null, string language = null)

Get product detail

Full product detail by ASIN (price, variants, badges, buybox, ranks…).

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
    public class AmazonGetProductDetailExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var asin = "asin_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var zip = "zip_example";  // string | Delivery postal/zip for localized buybox (optional) 
            var language = "language_example";  // string |  (optional) 

            try
            {
                // Get product detail
                Object result = apiInstance.AmazonGetProductDetail(asin, domain, zip, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product detail
    ApiResponse<Object> response = apiInstance.AmazonGetProductDetailWithHttpInfo(asin, domain, zip, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **asin** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **zip** | **string** | Delivery postal/zip for localized buybox | [optional]  |
| **language** | **string** |  | [optional]  |

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

<a id="amazongetproductreviews"></a>
# **AmazonGetProductReviews**
> Object AmazonGetProductReviews (string asin, string domain = null, int? page = null, string sortBy = null, string star = null, bool? verifiedOnly = null, bool? mediaOnly = null)

Get product reviews

Customer reviews for an ASIN (featured + paginated, with filters).

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
    public class AmazonGetProductReviewsExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var asin = "asin_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? | Review page (1-100, ~10 reviews/page) (optional)  (default to 1)
            var sortBy = "\"helpful\"";  // string | helpful | recent (optional)  (default to "helpful")
            var star = "star_example";  // string | one_star..five_star | positive | critical (optional) 
            var verifiedOnly = false;  // bool? |  (optional)  (default to false)
            var mediaOnly = false;  // bool? |  (optional)  (default to false)

            try
            {
                // Get product reviews
                Object result = apiInstance.AmazonGetProductReviews(asin, domain, page, sortBy, star, verifiedOnly, mediaOnly);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetProductReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetProductReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get product reviews
    ApiResponse<Object> response = apiInstance.AmazonGetProductReviewsWithHttpInfo(asin, domain, page, sortBy, star, verifiedOnly, mediaOnly);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetProductReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **asin** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **page** | **int?** | Review page (1-100, ~10 reviews/page) | [optional] [default to 1] |
| **sortBy** | **string** | helpful | recent | [optional] [default to &quot;helpful&quot;] |
| **star** | **string** | one_star..five_star | positive | critical | [optional]  |
| **verifiedOnly** | **bool?** |  | [optional] [default to false] |
| **mediaOnly** | **bool?** |  | [optional] [default to false] |

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

<a id="amazongetsellerfeedback"></a>
# **AmazonGetSellerFeedback**
> Object AmazonGetSellerFeedback (string sellerId, string domain = null, int? page = null)

Get seller feedback

Buyer feedback entries for a seller.

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
    public class AmazonGetSellerFeedbackExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get seller feedback
                Object result = apiInstance.AmazonGetSellerFeedback(sellerId, domain, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetSellerFeedback: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetSellerFeedbackWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller feedback
    ApiResponse<Object> response = apiInstance.AmazonGetSellerFeedbackWithHttpInfo(sellerId, domain, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetSellerFeedbackWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
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

<a id="amazongetsellerprofile"></a>
# **AmazonGetSellerProfile**
> Object AmazonGetSellerProfile (string sellerId, string domain = null)

Get seller profile

Seller profile, ratings and feedback summary.

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
    public class AmazonGetSellerProfileExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // Get seller profile
                Object result = apiInstance.AmazonGetSellerProfile(sellerId, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetSellerProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetSellerProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller profile
    ApiResponse<Object> response = apiInstance.AmazonGetSellerProfileWithHttpInfo(sellerId, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetSellerProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="amazongetsellerstorefrontproducts"></a>
# **AmazonGetSellerStorefrontProducts**
> Object AmazonGetSellerStorefrontProducts (string sellerId, string domain = null, int? page = null)

Get seller storefront products

Products listed in a seller's storefront.

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
    public class AmazonGetSellerStorefrontProductsExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var sellerId = "sellerId_example";  // string | 
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get seller storefront products
                Object result = apiInstance.AmazonGetSellerStorefrontProducts(sellerId, domain, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonGetSellerStorefrontProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonGetSellerStorefrontProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get seller storefront products
    ApiResponse<Object> response = apiInstance.AmazonGetSellerStorefrontProductsWithHttpInfo(sellerId, domain, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonGetSellerStorefrontProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **sellerId** | **string** |  |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
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

<a id="amazonkeywordsuggestions"></a>
# **AmazonKeywordSuggestions**
> Object AmazonKeywordSuggestions (string query, string domain = null)

Keyword suggestions

Get Amazon search autocomplete suggestions for keyword research.

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
    public class AmazonKeywordSuggestionsExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Partial search term
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // Keyword suggestions
                Object result = apiInstance.AmazonKeywordSuggestions(query, domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonKeywordSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonKeywordSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Keyword suggestions
    ApiResponse<Object> response = apiInstance.AmazonKeywordSuggestionsWithHttpInfo(query, domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonKeywordSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Partial search term |  |
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="amazonlistcategoryaliases"></a>
# **AmazonListCategoryAliases**
> Object AmazonListCategoryAliases (string domain = null)

List category aliases

List common Amazon department/category aliases and bestseller nodes.

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
    public class AmazonListCategoryAliasesExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var domain = "\"com\"";  // string |  (optional)  (default to "com")

            try
            {
                // List category aliases
                Object result = apiInstance.AmazonListCategoryAliases(domain);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonListCategoryAliases: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonListCategoryAliasesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List category aliases
    ApiResponse<Object> response = apiInstance.AmazonListCategoryAliasesWithHttpInfo(domain);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonListCategoryAliasesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |

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

<a id="amazonlistmarketplaces"></a>
# **AmazonListMarketplaces**
> Object AmazonListMarketplaces ()

List marketplaces

List all supported Amazon marketplaces.

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
    public class AmazonListMarketplacesExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);

            try
            {
                // List marketplaces
                Object result = apiInstance.AmazonListMarketplaces();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonListMarketplaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonListMarketplacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List marketplaces
    ApiResponse<Object> response = apiInstance.AmazonListMarketplacesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonListMarketplacesWithHttpInfo: " + e.Message);
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

<a id="amazonnewreleasesbycategory"></a>
# **AmazonNewReleasesByCategory**
> Object AmazonNewReleasesByCategory (string domain = null, string category = null, int? page = null)

New releases by category

Newly released products for a category (browse node).

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
    public class AmazonNewReleasesByCategoryExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var category = "category_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // New releases by category
                Object result = apiInstance.AmazonNewReleasesByCategory(domain, category, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonNewReleasesByCategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonNewReleasesByCategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // New releases by category
    ApiResponse<Object> response = apiInstance.AmazonNewReleasesByCategoryWithHttpInfo(domain, category, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonNewReleasesByCategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **category** | **string** |  | [optional]  |
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

<a id="amazonsearchamazonproducts"></a>
# **AmazonSearchAmazonProducts**
> Object AmazonSearchAmazonProducts (string query, string domain = null, int? page = null, string sortBy = null, string category = null, decimal? minPrice = null, decimal? maxPrice = null, string zip = null, string language = null)

Search Amazon products

Search the Amazon catalog with filters and sorting.

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
    public class AmazonSearchAmazonProductsExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Search keywords
            var domain = "\"com\"";  // string | Amazon marketplace TLD or code (com, co.uk, de…) (optional)  (default to "com")
            var page = 1;  // int? |  (optional)  (default to 1)
            var sortBy = "sortBy_example";  // string | relevance | price_low_to_high | price_high_to_low | avg_review | newest (optional) 
            var category = "category_example";  // string | Department/category alias (i= param) (optional) 
            var minPrice = 8.14D;  // decimal? |  (optional) 
            var maxPrice = 8.14D;  // decimal? |  (optional) 
            var zip = "zip_example";  // string | Delivery postal/zip code for localized pricing (optional) 
            var language = "language_example";  // string | Locale for results, e.g. en_US, fr_FR (optional) 

            try
            {
                // Search Amazon products
                Object result = apiInstance.AmazonSearchAmazonProducts(query, domain, page, sortBy, category, minPrice, maxPrice, zip, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonSearchAmazonProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonSearchAmazonProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Amazon products
    ApiResponse<Object> response = apiInstance.AmazonSearchAmazonProductsWithHttpInfo(query, domain, page, sortBy, category, minPrice, maxPrice, zip, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonSearchAmazonProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Search keywords |  |
| **domain** | **string** | Amazon marketplace TLD or code (com, co.uk, de…) | [optional] [default to &quot;com&quot;] |
| **page** | **int?** |  | [optional] [default to 1] |
| **sortBy** | **string** | relevance | price_low_to_high | price_high_to_low | avg_review | newest | [optional]  |
| **category** | **string** | Department/category alias (i&#x3D; param) | [optional]  |
| **minPrice** | **decimal?** |  | [optional]  |
| **maxPrice** | **decimal?** |  | [optional]  |
| **zip** | **string** | Delivery postal/zip code for localized pricing | [optional]  |
| **language** | **string** | Locale for results, e.g. en_US, fr_FR | [optional]  |

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

<a id="amazontodaysdeals"></a>
# **AmazonTodaySDeals**
> Object AmazonTodaySDeals (string domain = null, string category = null, int? page = null)

Today's deals

Current Amazon deals (lightning deals, best deals).

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
    public class AmazonTodaySDealsExample
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
            var apiInstance = new AmazonApi(httpClient, config, httpClientHandler);
            var domain = "\"com\"";  // string |  (optional)  (default to "com")
            var category = "category_example";  // string |  (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Today's deals
                Object result = apiInstance.AmazonTodaySDeals(domain, category, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AmazonApi.AmazonTodaySDeals: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AmazonTodaySDealsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Today's deals
    ApiResponse<Object> response = apiInstance.AmazonTodaySDealsWithHttpInfo(domain, category, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AmazonApi.AmazonTodaySDealsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **domain** | **string** |  | [optional] [default to &quot;com&quot;] |
| **category** | **string** |  | [optional]  |
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

