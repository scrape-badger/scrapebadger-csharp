# ScrapeBadger.Api.ApartmentsApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ApartmentsApartmentsScraperHealthCheck**](ApartmentsApi.md#apartmentsapartmentsscraperhealthcheck) | **GET** /v1/apartments/health | Apartments scraper health check |
| [**ApartmentsApartmentsScraperHealthCheckHead**](ApartmentsApi.md#apartmentsapartmentsscraperhealthcheckhead) | **HEAD** /v1/apartments/health | Apartments scraper health check |
| [**ApartmentsGetPropertyDetailBySlugId**](ApartmentsApi.md#apartmentsgetpropertydetailbyslugid) | **GET** /v1/apartments/properties/{slug}/{property_id} | Get property detail by slug + id |
| [**ApartmentsGetPropertyDetailByUrl**](ApartmentsApi.md#apartmentsgetpropertydetailbyurl) | **GET** /v1/apartments/property | Get property detail by URL |
| [**ApartmentsSearchRentalListings**](ApartmentsApi.md#apartmentssearchrentallistings) | **GET** /v1/apartments/search | Search rental listings |

<a id="apartmentsapartmentsscraperhealthcheck"></a>
# **ApartmentsApartmentsScraperHealthCheck**
> Object ApartmentsApartmentsScraperHealthCheck ()

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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
    public class ApartmentsApartmentsScraperHealthCheckExample
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
            var apiInstance = new ApartmentsApi(httpClient, config, httpClientHandler);

            try
            {
                // Apartments scraper health check
                Object result = apiInstance.ApartmentsApartmentsScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApartmentsApi.ApartmentsApartmentsScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApartmentsApartmentsScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Apartments scraper health check
    ApiResponse<Object> response = apiInstance.ApartmentsApartmentsScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApartmentsApi.ApartmentsApartmentsScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="apartmentsapartmentsscraperhealthcheckhead"></a>
# **ApartmentsApartmentsScraperHealthCheckHead**
> Object ApartmentsApartmentsScraperHealthCheckHead ()

Apartments scraper health check

Check health of the Apartments scraper service (accepts HEAD for UptimeRobot).

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
    public class ApartmentsApartmentsScraperHealthCheckHeadExample
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
            var apiInstance = new ApartmentsApi(httpClient, config, httpClientHandler);

            try
            {
                // Apartments scraper health check
                Object result = apiInstance.ApartmentsApartmentsScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApartmentsApi.ApartmentsApartmentsScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApartmentsApartmentsScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Apartments scraper health check
    ApiResponse<Object> response = apiInstance.ApartmentsApartmentsScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApartmentsApi.ApartmentsApartmentsScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="apartmentsgetpropertydetailbyslugid"></a>
# **ApartmentsGetPropertyDetailBySlugId**
> Object ApartmentsGetPropertyDetailBySlugId (string slug, string propertyId)

Get property detail by slug + id

Get a property by its SEO slug and 7-character listing id.

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
    public class ApartmentsGetPropertyDetailBySlugIdExample
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
            var apiInstance = new ApartmentsApi(httpClient, config, httpClientHandler);
            var slug = "slug_example";  // string | 
            var propertyId = "propertyId_example";  // string | 

            try
            {
                // Get property detail by slug + id
                Object result = apiInstance.ApartmentsGetPropertyDetailBySlugId(slug, propertyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApartmentsApi.ApartmentsGetPropertyDetailBySlugId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApartmentsGetPropertyDetailBySlugIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail by slug + id
    ApiResponse<Object> response = apiInstance.ApartmentsGetPropertyDetailBySlugIdWithHttpInfo(slug, propertyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApartmentsApi.ApartmentsGetPropertyDetailBySlugIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **slug** | **string** |  |  |
| **propertyId** | **string** |  |  |

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

<a id="apartmentsgetpropertydetailbyurl"></a>
# **ApartmentsGetPropertyDetailByUrl**
> Object ApartmentsGetPropertyDetailByUrl (string url)

Get property detail by URL

Get an apartments.com property with full per-unit pricing and availability.

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
    public class ApartmentsGetPropertyDetailByUrlExample
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
            var apiInstance = new ApartmentsApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/

            try
            {
                // Get property detail by URL
                Object result = apiInstance.ApartmentsGetPropertyDetailByUrl(url);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApartmentsApi.ApartmentsGetPropertyDetailByUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApartmentsGetPropertyDetailByUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail by URL
    ApiResponse<Object> response = apiInstance.ApartmentsGetPropertyDetailByUrlWithHttpInfo(url);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApartmentsApi.ApartmentsGetPropertyDetailByUrlWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Full apartments.com property URL, e.g. https://www.apartments.com/urbane-kansas-city-mo/wcd6e5k/ |  |

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

<a id="apartmentssearchrentallistings"></a>
# **ApartmentsSearchRentalListings**
> Object ApartmentsSearchRentalListings (string location, int? page = null, int? beds = null, int? minPrice = null, int? maxPrice = null)

Search rental listings

Search apartments.com for rental properties. 40 cards per page.

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
    public class ApartmentsSearchRentalListingsExample
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
            var apiInstance = new ApartmentsApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | apartments.com location slug, e.g. 'kansas-city-mo'
            var page = 1;  // int? |  (optional)  (default to 1)
            var beds = 56;  // int? | 0=studio, 1-4 bedrooms (optional) 
            var minPrice = 56;  // int? |  (optional) 
            var maxPrice = 56;  // int? |  (optional) 

            try
            {
                // Search rental listings
                Object result = apiInstance.ApartmentsSearchRentalListings(location, page, beds, minPrice, maxPrice);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApartmentsApi.ApartmentsSearchRentalListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ApartmentsSearchRentalListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search rental listings
    ApiResponse<Object> response = apiInstance.ApartmentsSearchRentalListingsWithHttpInfo(location, page, beds, minPrice, maxPrice);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApartmentsApi.ApartmentsSearchRentalListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | apartments.com location slug, e.g. &#39;kansas-city-mo&#39; |  |
| **page** | **int?** |  | [optional] [default to 1] |
| **beds** | **int?** | 0&#x3D;studio, 1-4 bedrooms | [optional]  |
| **minPrice** | **int?** |  | [optional]  |
| **maxPrice** | **int?** |  | [optional]  |

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

