# ScrapeBadger.Api.AirbnbApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AirbnbAirbnbScraperHealthCheck**](AirbnbApi.md#airbnbairbnbscraperhealthcheck) | **GET** /v1/airbnb/health | Airbnb scraper health check |
| [**AirbnbAirbnbScraperHealthCheckHead**](AirbnbApi.md#airbnbairbnbscraperhealthcheckhead) | **HEAD** /v1/airbnb/health | Airbnb scraper health check |
| [**AirbnbGetAvailabilityCalendar**](AirbnbApi.md#airbnbgetavailabilitycalendar) | **GET** /v1/airbnb/listings/{room_id}/calendar | Get availability calendar |
| [**AirbnbGetExperienceDetail**](AirbnbApi.md#airbnbgetexperiencedetail) | **GET** /v1/airbnb/experiences/{experience_id} | Get experience detail |
| [**AirbnbGetListingDetail**](AirbnbApi.md#airbnbgetlistingdetail) | **GET** /v1/airbnb/listings/{room_id} | Get listing detail |
| [**AirbnbGetListingReviews**](AirbnbApi.md#airbnbgetlistingreviews) | **GET** /v1/airbnb/listings/{room_id}/reviews | Get listing reviews |
| [**AirbnbSearchExperiences**](AirbnbApi.md#airbnbsearchexperiences) | **GET** /v1/airbnb/experiences | Search experiences |
| [**AirbnbSearchStays**](AirbnbApi.md#airbnbsearchstays) | **GET** /v1/airbnb/search | Search stays |

<a id="airbnbairbnbscraperhealthcheck"></a>
# **AirbnbAirbnbScraperHealthCheck**
> Object AirbnbAirbnbScraperHealthCheck ()

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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
    public class AirbnbAirbnbScraperHealthCheckExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);

            try
            {
                // Airbnb scraper health check
                Object result = apiInstance.AirbnbAirbnbScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbAirbnbScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbAirbnbScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Airbnb scraper health check
    ApiResponse<Object> response = apiInstance.AirbnbAirbnbScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbAirbnbScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="airbnbairbnbscraperhealthcheckhead"></a>
# **AirbnbAirbnbScraperHealthCheckHead**
> Object AirbnbAirbnbScraperHealthCheckHead ()

Airbnb scraper health check

Check health of the Airbnb scraper service (accepts HEAD).

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
    public class AirbnbAirbnbScraperHealthCheckHeadExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);

            try
            {
                // Airbnb scraper health check
                Object result = apiInstance.AirbnbAirbnbScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbAirbnbScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbAirbnbScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Airbnb scraper health check
    ApiResponse<Object> response = apiInstance.AirbnbAirbnbScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbAirbnbScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="airbnbgetavailabilitycalendar"></a>
# **AirbnbGetAvailabilityCalendar**
> Object AirbnbGetAvailabilityCalendar (string roomId, int? month = null, int? year = null, int? months = null, string currency = null, string locale = null)

Get availability calendar

Day-by-day availability for up to 12 months: bookable, check-in/out windows and min/max nights per date.

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
    public class AirbnbGetAvailabilityCalendarExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var roomId = "roomId_example";  // string | 
            var month = 1;  // int? | Start month (1-12) (optional)  (default to 1)
            var year = 2026;  // int? | Start year (optional)  (default to 2026)
            var months = 12;  // int? | Number of months (max 12) (optional)  (default to 12)
            var currency = "currency_example";  // string |  (optional) 
            var locale = "locale_example";  // string |  (optional) 

            try
            {
                // Get availability calendar
                Object result = apiInstance.AirbnbGetAvailabilityCalendar(roomId, month, year, months, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbGetAvailabilityCalendar: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbGetAvailabilityCalendarWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get availability calendar
    ApiResponse<Object> response = apiInstance.AirbnbGetAvailabilityCalendarWithHttpInfo(roomId, month, year, months, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbGetAvailabilityCalendarWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **roomId** | **string** |  |  |
| **month** | **int?** | Start month (1-12) | [optional] [default to 1] |
| **year** | **int?** | Start year | [optional] [default to 2026] |
| **months** | **int?** | Number of months (max 12) | [optional] [default to 12] |
| **currency** | **string** |  | [optional]  |
| **locale** | **string** |  | [optional]  |

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

<a id="airbnbgetexperiencedetail"></a>
# **AirbnbGetExperienceDetail**
> Object AirbnbGetExperienceDetail (string experienceId, int? adults = null, int? children = null, int? infants = null, string currency = null, string locale = null)

Get experience detail

Full detail for one experience: description, rating, host, location and photos.

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
    public class AirbnbGetExperienceDetailExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var experienceId = "experienceId_example";  // string | 
            var adults = 1;  // int? |  (optional)  (default to 1)
            var children = 0;  // int? |  (optional)  (default to 0)
            var infants = 0;  // int? |  (optional)  (default to 0)
            var currency = "currency_example";  // string |  (optional) 
            var locale = "locale_example";  // string |  (optional) 

            try
            {
                // Get experience detail
                Object result = apiInstance.AirbnbGetExperienceDetail(experienceId, adults, children, infants, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbGetExperienceDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbGetExperienceDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get experience detail
    ApiResponse<Object> response = apiInstance.AirbnbGetExperienceDetailWithHttpInfo(experienceId, adults, children, infants, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbGetExperienceDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **experienceId** | **string** |  |  |
| **adults** | **int?** |  | [optional] [default to 1] |
| **children** | **int?** |  | [optional] [default to 0] |
| **infants** | **int?** |  | [optional] [default to 0] |
| **currency** | **string** |  | [optional]  |
| **locale** | **string** |  | [optional]  |

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

<a id="airbnbgetlistingdetail"></a>
# **AirbnbGetListingDetail**
> Object AirbnbGetListingDetail (string roomId, int? adults = null, string currency = null, string locale = null)

Get listing detail

Full detail for one listing: amenities, house rules, host, ratings, coordinates and photos.

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
    public class AirbnbGetListingDetailExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var roomId = "roomId_example";  // string | 
            var adults = 1;  // int? |  (optional)  (default to 1)
            var currency = "currency_example";  // string |  (optional) 
            var locale = "locale_example";  // string |  (optional) 

            try
            {
                // Get listing detail
                Object result = apiInstance.AirbnbGetListingDetail(roomId, adults, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbGetListingDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbGetListingDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing detail
    ApiResponse<Object> response = apiInstance.AirbnbGetListingDetailWithHttpInfo(roomId, adults, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbGetListingDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **roomId** | **string** |  |  |
| **adults** | **int?** |  | [optional] [default to 1] |
| **currency** | **string** |  | [optional]  |
| **locale** | **string** |  | [optional]  |

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

<a id="airbnbgetlistingreviews"></a>
# **AirbnbGetListingReviews**
> Object AirbnbGetListingReviews (string roomId, int? limit = null, int? offset = null, string sort = null, string currency = null, string locale = null)

Get listing reviews

Paginated guest reviews with reviewer, rating, date, text and host response.

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
    public class AirbnbGetListingReviewsExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var roomId = "roomId_example";  // string | 
            var limit = 24;  // int? |  (optional)  (default to 24)
            var offset = 0;  // int? |  (optional)  (default to 0)
            var sort = "\"MOST_RECENT\"";  // string | MOST_RECENT | RATING_DESC | RATING_ASC (optional)  (default to "MOST_RECENT")
            var currency = "currency_example";  // string |  (optional) 
            var locale = "locale_example";  // string |  (optional) 

            try
            {
                // Get listing reviews
                Object result = apiInstance.AirbnbGetListingReviews(roomId, limit, offset, sort, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbGetListingReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbGetListingReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing reviews
    ApiResponse<Object> response = apiInstance.AirbnbGetListingReviewsWithHttpInfo(roomId, limit, offset, sort, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbGetListingReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **roomId** | **string** |  |  |
| **limit** | **int?** |  | [optional] [default to 24] |
| **offset** | **int?** |  | [optional] [default to 0] |
| **sort** | **string** | MOST_RECENT | RATING_DESC | RATING_ASC | [optional] [default to &quot;MOST_RECENT&quot;] |
| **currency** | **string** |  | [optional]  |
| **locale** | **string** |  | [optional]  |

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

<a id="airbnbsearchexperiences"></a>
# **AirbnbSearchExperiences**
> Object AirbnbSearchExperiences (string location, string cursor = null, string currency = null, string locale = null)

Search experiences

Search Airbnb Experiences by location.

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
    public class AirbnbSearchExperiencesExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Free-text place, e.g. 'Rome, Italy'
            var cursor = "cursor_example";  // string | next_page_cursor from a prior response (optional) 
            var currency = "currency_example";  // string |  (optional) 
            var locale = "locale_example";  // string |  (optional) 

            try
            {
                // Search experiences
                Object result = apiInstance.AirbnbSearchExperiences(location, cursor, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbSearchExperiences: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbSearchExperiencesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search experiences
    ApiResponse<Object> response = apiInstance.AirbnbSearchExperiencesWithHttpInfo(location, cursor, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbSearchExperiencesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Free-text place, e.g. &#39;Rome, Italy&#39; |  |
| **cursor** | **string** | next_page_cursor from a prior response | [optional]  |
| **currency** | **string** |  | [optional]  |
| **locale** | **string** |  | [optional]  |

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

<a id="airbnbsearchstays"></a>
# **AirbnbSearchStays**
> Object AirbnbSearchStays (string location = null, decimal? neLat = null, decimal? neLng = null, decimal? swLat = null, decimal? swLng = null, string checkIn = null, string checkOut = null, int? adults = null, int? children = null, int? infants = null, int? pets = null, int? priceMin = null, int? priceMax = null, int? minBedrooms = null, int? minBeds = null, int? minBathrooms = null, string roomType = null, string cursor = null, int? limit = null, string currency = null, string locale = null)

Search stays

Search Airbnb stays by place name and/or map bounding box, with dates, guests, price and property filters. Paginate with the `cursor`.

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
    public class AirbnbSearchStaysExample
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
            var apiInstance = new AirbnbApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Free-text place, e.g. 'Paris, France' (optional) 
            var neLat = 8.14D;  // decimal? | Map bounding-box NE latitude (optional) 
            var neLng = 8.14D;  // decimal? | Map bounding-box NE longitude (optional) 
            var swLat = 8.14D;  // decimal? | Map bounding-box SW latitude (optional) 
            var swLng = 8.14D;  // decimal? | Map bounding-box SW longitude (optional) 
            var checkIn = "checkIn_example";  // string | Check-in date YYYY-MM-DD (optional) 
            var checkOut = "checkOut_example";  // string | Check-out date YYYY-MM-DD (optional) 
            var adults = 1;  // int? |  (optional)  (default to 1)
            var children = 0;  // int? |  (optional)  (default to 0)
            var infants = 0;  // int? |  (optional)  (default to 0)
            var pets = 0;  // int? |  (optional)  (default to 0)
            var priceMin = 56;  // int? |  (optional) 
            var priceMax = 56;  // int? |  (optional) 
            var minBedrooms = 56;  // int? |  (optional) 
            var minBeds = 56;  // int? |  (optional) 
            var minBathrooms = 56;  // int? |  (optional) 
            var roomType = "roomType_example";  // string | e.g. 'Entire home/apt', 'Private room' (optional) 
            var cursor = "cursor_example";  // string | next_page_cursor from a prior response (optional) 
            var limit = 18;  // int? |  (optional)  (default to 18)
            var currency = "currency_example";  // string | ISO currency, e.g. USD, EUR (optional) 
            var locale = "locale_example";  // string | Locale, e.g. en, fr (optional) 

            try
            {
                // Search stays
                Object result = apiInstance.AirbnbSearchStays(location, neLat, neLng, swLat, swLng, checkIn, checkOut, adults, children, infants, pets, priceMin, priceMax, minBedrooms, minBeds, minBathrooms, roomType, cursor, limit, currency, locale);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AirbnbApi.AirbnbSearchStays: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AirbnbSearchStaysWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search stays
    ApiResponse<Object> response = apiInstance.AirbnbSearchStaysWithHttpInfo(location, neLat, neLng, swLat, swLng, checkIn, checkOut, adults, children, infants, pets, priceMin, priceMax, minBedrooms, minBeds, minBathrooms, roomType, cursor, limit, currency, locale);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AirbnbApi.AirbnbSearchStaysWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Free-text place, e.g. &#39;Paris, France&#39; | [optional]  |
| **neLat** | **decimal?** | Map bounding-box NE latitude | [optional]  |
| **neLng** | **decimal?** | Map bounding-box NE longitude | [optional]  |
| **swLat** | **decimal?** | Map bounding-box SW latitude | [optional]  |
| **swLng** | **decimal?** | Map bounding-box SW longitude | [optional]  |
| **checkIn** | **string** | Check-in date YYYY-MM-DD | [optional]  |
| **checkOut** | **string** | Check-out date YYYY-MM-DD | [optional]  |
| **adults** | **int?** |  | [optional] [default to 1] |
| **children** | **int?** |  | [optional] [default to 0] |
| **infants** | **int?** |  | [optional] [default to 0] |
| **pets** | **int?** |  | [optional] [default to 0] |
| **priceMin** | **int?** |  | [optional]  |
| **priceMax** | **int?** |  | [optional]  |
| **minBedrooms** | **int?** |  | [optional]  |
| **minBeds** | **int?** |  | [optional]  |
| **minBathrooms** | **int?** |  | [optional]  |
| **roomType** | **string** | e.g. &#39;Entire home/apt&#39;, &#39;Private room&#39; | [optional]  |
| **cursor** | **string** | next_page_cursor from a prior response | [optional]  |
| **limit** | **int?** |  | [optional] [default to 18] |
| **currency** | **string** | ISO currency, e.g. USD, EUR | [optional]  |
| **locale** | **string** | Locale, e.g. en, fr | [optional]  |

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

