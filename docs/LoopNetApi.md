# ScrapeBadger.Api.LoopNetApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**LoopnetGetBrokerProfile**](LoopNetApi.md#loopnetgetbrokerprofile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile |
| [**LoopnetGetListingDetail**](LoopNetApi.md#loopnetgetlistingdetail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail |
| [**LoopnetListCoverageMarkets**](LoopNetApi.md#loopnetlistcoveragemarkets) | **GET** /v1/loopnet/markets | List coverage markets |
| [**LoopnetListPropertyTypes**](LoopNetApi.md#loopnetlistpropertytypes) | **GET** /v1/loopnet/property-types | List property types |
| [**LoopnetLoopnetScraperHealthCheck**](LoopNetApi.md#loopnetloopnetscraperhealthcheck) | **GET** /v1/loopnet/health | LoopNet scraper health check |
| [**LoopnetLoopnetScraperHealthCheckHead**](LoopNetApi.md#loopnetloopnetscraperhealthcheckhead) | **HEAD** /v1/loopnet/health | LoopNet scraper health check |
| [**LoopnetSearchCommercialRealEstate**](LoopNetApi.md#loopnetsearchcommercialrealestate) | **GET** /v1/loopnet/search | Search commercial real estate |

<a id="loopnetgetbrokerprofile"></a>
# **LoopnetGetBrokerProfile**
> Object LoopnetGetBrokerProfile (string slug, string brokerId, string market = null)

Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

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
    public class LoopnetGetBrokerProfileExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);
            var slug = "slug_example";  // string | 
            var brokerId = "brokerId_example";  // string | 
            var market = "\"us\"";  // string | us|ca|uk|fr|es (optional)  (default to "us")

            try
            {
                // Get broker profile
                Object result = apiInstance.LoopnetGetBrokerProfile(slug, brokerId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetGetBrokerProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetGetBrokerProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get broker profile
    ApiResponse<Object> response = apiInstance.LoopnetGetBrokerProfileWithHttpInfo(slug, brokerId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetGetBrokerProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **slug** | **string** |  |  |
| **brokerId** | **string** |  |  |
| **market** | **string** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;] |

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

<a id="loopnetgetlistingdetail"></a>
# **LoopnetGetListingDetail**
> Object LoopnetGetListingDetail (string listingId, string market = null)

Get listing detail

Get a single LoopNet listing's full detail by its numeric id.

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
    public class LoopnetGetListingDetailExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);
            var listingId = "listingId_example";  // string | 
            var market = "\"us\"";  // string | us|ca|uk|fr|es (optional)  (default to "us")

            try
            {
                // Get listing detail
                Object result = apiInstance.LoopnetGetListingDetail(listingId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetGetListingDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetGetListingDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing detail
    ApiResponse<Object> response = apiInstance.LoopnetGetListingDetailWithHttpInfo(listingId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetGetListingDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **string** |  |  |
| **market** | **string** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;] |

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

<a id="loopnetlistcoveragemarkets"></a>
# **LoopnetListCoverageMarkets**
> Object LoopnetListCoverageMarkets ()

List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

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
    public class LoopnetListCoverageMarketsExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);

            try
            {
                // List coverage markets
                Object result = apiInstance.LoopnetListCoverageMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetListCoverageMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetListCoverageMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List coverage markets
    ApiResponse<Object> response = apiInstance.LoopnetListCoverageMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetListCoverageMarketsWithHttpInfo: " + e.Message);
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

<a id="loopnetlistpropertytypes"></a>
# **LoopnetListPropertyTypes**
> Object LoopnetListPropertyTypes ()

List property types

List LoopNet property-type facets accepted by /search.

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
    public class LoopnetListPropertyTypesExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);

            try
            {
                // List property types
                Object result = apiInstance.LoopnetListPropertyTypes();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetListPropertyTypes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetListPropertyTypesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List property types
    ApiResponse<Object> response = apiInstance.LoopnetListPropertyTypesWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetListPropertyTypesWithHttpInfo: " + e.Message);
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

<a id="loopnetloopnetscraperhealthcheck"></a>
# **LoopnetLoopnetScraperHealthCheck**
> Object LoopnetLoopnetScraperHealthCheck ()

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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
    public class LoopnetLoopnetScraperHealthCheckExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);

            try
            {
                // LoopNet scraper health check
                Object result = apiInstance.LoopnetLoopnetScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetLoopnetScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetLoopnetScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // LoopNet scraper health check
    ApiResponse<Object> response = apiInstance.LoopnetLoopnetScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetLoopnetScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="loopnetloopnetscraperhealthcheckhead"></a>
# **LoopnetLoopnetScraperHealthCheckHead**
> Object LoopnetLoopnetScraperHealthCheckHead ()

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

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
    public class LoopnetLoopnetScraperHealthCheckHeadExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);

            try
            {
                // LoopNet scraper health check
                Object result = apiInstance.LoopnetLoopnetScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetLoopnetScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetLoopnetScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // LoopNet scraper health check
    ApiResponse<Object> response = apiInstance.LoopnetLoopnetScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetLoopnetScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="loopnetsearchcommercialrealestate"></a>
# **LoopnetSearchCommercialRealEstate**
> Object LoopnetSearchCommercialRealEstate (string location, string market = null, string listingType = null, string propertyType = null, int? page = null, int? minPrice = null, int? maxPrice = null, string priceType = null, int? minSize = null, int? maxSize = null)

Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

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
    public class LoopnetSearchCommercialRealEstateExample
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
            var apiInstance = new LoopNetApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | City/state, ZIP, state code, or 'usa'
            var market = "\"us\"";  // string | us|ca|uk|fr|es (optional)  (default to "us")
            var listingType = "\"for-lease\"";  // string | for-lease|for-sale|auctions (optional)  (default to "for-lease")
            var propertyType = "propertyType_example";  // string | Slug from /property-types (optional) 
            var page = 1;  // int? |  (optional)  (default to 1)
            var minPrice = 56;  // int? |  (optional) 
            var maxPrice = 56;  // int? |  (optional) 
            var priceType = "priceType_example";  // string | unit | sf | acre (optional) 
            var minSize = 56;  // int? |  (optional) 
            var maxSize = 56;  // int? |  (optional) 

            try
            {
                // Search commercial real estate
                Object result = apiInstance.LoopnetSearchCommercialRealEstate(location, market, listingType, propertyType, page, minPrice, maxPrice, priceType, minSize, maxSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LoopNetApi.LoopnetSearchCommercialRealEstate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoopnetSearchCommercialRealEstateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search commercial real estate
    ApiResponse<Object> response = apiInstance.LoopnetSearchCommercialRealEstateWithHttpInfo(location, market, listingType, propertyType, page, minPrice, maxPrice, priceType, minSize, maxSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LoopNetApi.LoopnetSearchCommercialRealEstateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | City/state, ZIP, state code, or &#39;usa&#39; |  |
| **market** | **string** | us|ca|uk|fr|es | [optional] [default to &quot;us&quot;] |
| **listingType** | **string** | for-lease|for-sale|auctions | [optional] [default to &quot;for-lease&quot;] |
| **propertyType** | **string** | Slug from /property-types | [optional]  |
| **page** | **int?** |  | [optional] [default to 1] |
| **minPrice** | **int?** |  | [optional]  |
| **maxPrice** | **int?** |  | [optional]  |
| **priceType** | **string** | unit | sf | acre | [optional]  |
| **minSize** | **int?** |  | [optional]  |
| **maxSize** | **int?** |  | [optional]  |

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

