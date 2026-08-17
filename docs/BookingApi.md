# ScrapeBadger.Api.BookingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**BookingBookingScraperHealthCheck**](BookingApi.md#bookingbookingscraperhealthcheck) | **GET** /v1/booking/health | Booking scraper health check |
| [**BookingBookingScraperHealthCheckHead**](BookingApi.md#bookingbookingscraperhealthcheckhead) | **HEAD** /v1/booking/health | Booking scraper health check |
| [**BookingGetPropertyDetail**](BookingApi.md#bookinggetpropertydetail) | **GET** /v1/booking/properties/{country_code}/{slug} | Get property detail |
| [**BookingGetPropertyReviews**](BookingApi.md#bookinggetpropertyreviews) | **GET** /v1/booking/properties/{country_code}/{slug}/reviews | Get property reviews |
| [**BookingSearchDestinations**](BookingApi.md#bookingsearchdestinations) | **GET** /v1/booking/destinations | Search destinations |
| [**BookingSearchProperties**](BookingApi.md#bookingsearchproperties) | **GET** /v1/booking/search | Search properties |

<a id="bookingbookingscraperhealthcheck"></a>
# **BookingBookingScraperHealthCheck**
> Object BookingBookingScraperHealthCheck ()

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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
    public class BookingBookingScraperHealthCheckExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);

            try
            {
                // Booking scraper health check
                Object result = apiInstance.BookingBookingScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingBookingScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingBookingScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Booking scraper health check
    ApiResponse<Object> response = apiInstance.BookingBookingScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingBookingScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="bookingbookingscraperhealthcheckhead"></a>
# **BookingBookingScraperHealthCheckHead**
> Object BookingBookingScraperHealthCheckHead ()

Booking scraper health check

Check health of the Booking scraper service (accepts HEAD).

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
    public class BookingBookingScraperHealthCheckHeadExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);

            try
            {
                // Booking scraper health check
                Object result = apiInstance.BookingBookingScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingBookingScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingBookingScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Booking scraper health check
    ApiResponse<Object> response = apiInstance.BookingBookingScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingBookingScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="bookinggetpropertydetail"></a>
# **BookingGetPropertyDetail**
> Object BookingGetPropertyDetail (string countryCode, string slug, int? photos = null, int? questions = null, string language = null)

Get property detail

Full detail for one property: description, address and coordinates, star rating, review score with per-category breakdown, facilities, house rules, room types with occupancy and beds, photos and guest Q&A.

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
    public class BookingGetPropertyDetailExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);
            var countryCode = "countryCode_example";  // string | Two-letter country code, e.g. 'it'
            var slug = "slug_example";  // string | Booking page name, e.g. 'hotel-artemide'
            var photos = 40;  // int? | Gallery photos to return (optional)  (default to 40)
            var questions = 10;  // int? | Guest Q&A pairs to return (optional)  (default to 10)
            var language = "language_example";  // string | Locale, e.g. en-us, fr (optional) 

            try
            {
                // Get property detail
                Object result = apiInstance.BookingGetPropertyDetail(countryCode, slug, photos, questions, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingGetPropertyDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingGetPropertyDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property detail
    ApiResponse<Object> response = apiInstance.BookingGetPropertyDetailWithHttpInfo(countryCode, slug, photos, questions, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingGetPropertyDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **countryCode** | **string** | Two-letter country code, e.g. &#39;it&#39; |  |
| **slug** | **string** | Booking page name, e.g. &#39;hotel-artemide&#39; |  |
| **photos** | **int?** | Gallery photos to return | [optional] [default to 40] |
| **questions** | **int?** | Guest Q&amp;A pairs to return | [optional] [default to 10] |
| **language** | **string** | Locale, e.g. en-us, fr | [optional]  |

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

<a id="bookinggetpropertyreviews"></a>
# **BookingGetPropertyReviews**
> Object BookingGetPropertyReviews (string countryCode, string slug, int? limit = null, int? offset = null, string sort = null, string reviewLanguage = null, string guestType = null, string language = null)

Get property reviews

Paginated guest reviews with score, positive and negative text, stay dates, room type, guest country and type, photos and the partner's reply.

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
    public class BookingGetPropertyReviewsExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);
            var countryCode = "countryCode_example";  // string | Two-letter country code, e.g. 'it'
            var slug = "slug_example";  // string | Booking page name, e.g. 'hotel-artemide'
            var limit = 25;  // int? |  (optional)  (default to 25)
            var offset = 0;  // int? |  (optional)  (default to 0)
            var sort = "\"MOST_RELEVANT\"";  // string | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC (optional)  (default to "MOST_RELEVANT")
            var reviewLanguage = "reviewLanguage_example";  // string | Only reviews written in this language, e.g. 'fr' (optional) 
            var guestType = "guestType_example";  // string | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS (optional) 
            var language = "language_example";  // string | Locale for labels, e.g. en-us (optional) 

            try
            {
                // Get property reviews
                Object result = apiInstance.BookingGetPropertyReviews(countryCode, slug, limit, offset, sort, reviewLanguage, guestType, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingGetPropertyReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingGetPropertyReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get property reviews
    ApiResponse<Object> response = apiInstance.BookingGetPropertyReviewsWithHttpInfo(countryCode, slug, limit, offset, sort, reviewLanguage, guestType, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingGetPropertyReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **countryCode** | **string** | Two-letter country code, e.g. &#39;it&#39; |  |
| **slug** | **string** | Booking page name, e.g. &#39;hotel-artemide&#39; |  |
| **limit** | **int?** |  | [optional] [default to 25] |
| **offset** | **int?** |  | [optional] [default to 0] |
| **sort** | **string** | MOST_RELEVANT | NEWEST_FIRST | OLDEST_FIRST | SCORE_DESC | SCORE_ASC | [optional] [default to &quot;MOST_RELEVANT&quot;] |
| **reviewLanguage** | **string** | Only reviews written in this language, e.g. &#39;fr&#39; | [optional]  |
| **guestType** | **string** | FAMILIES | COUPLES | GROUP_OF_FRIENDS | SOLO_TRAVELLERS | BUSINESS_TRAVELLERS | [optional]  |
| **language** | **string** | Locale for labels, e.g. en-us | [optional]  |

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

<a id="bookingsearchdestinations"></a>
# **BookingSearchDestinations**
> Object BookingSearchDestinations (string query, int? limit = null, string language = null)

Search destinations

Resolve a place name to Booking's `dest_id`/`dest_type`, with coordinates and country — feed the pair back into /search for an exact match.

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
    public class BookingSearchDestinationsExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Free-text place, e.g. 'amsterd'
            var limit = 8;  // int? |  (optional)  (default to 8)
            var language = "language_example";  // string | Locale, e.g. en-us, fr (optional) 

            try
            {
                // Search destinations
                Object result = apiInstance.BookingSearchDestinations(query, limit, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingSearchDestinations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingSearchDestinationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search destinations
    ApiResponse<Object> response = apiInstance.BookingSearchDestinationsWithHttpInfo(query, limit, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingSearchDestinationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Free-text place, e.g. &#39;amsterd&#39; |  |
| **limit** | **int?** |  | [optional] [default to 8] |
| **language** | **string** | Locale, e.g. en-us, fr | [optional]  |

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

<a id="bookingsearchproperties"></a>
# **BookingSearchProperties**
> Object BookingSearchProperties (string location = null, int? destId = null, string destType = null, string checkin = null, string checkout = null, int? adults = null, string children = null, int? rooms = null, int? offset = null, int? limit = null, string sort = null, string filters = null, string currency = null, string language = null)

Search properties

Search Booking.com properties by destination, with dates, occupancy, sorting and filters. Returns prices, review scores, coordinates, room configuration and photos. Paginate with `offset`.

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
    public class BookingSearchPropertiesExample
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
            var apiInstance = new BookingApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Free-text destination, e.g. 'Rome' (optional) 
            var destId = 56;  // int? | Exact destination id (ufi) from /destinations (optional) 
            var destType = "\"NO_DEST_TYPE\"";  // string | Destination type, e.g. CITY (optional)  (default to "NO_DEST_TYPE")
            var checkin = "checkin_example";  // string | Check-in date YYYY-MM-DD (optional) 
            var checkout = "checkout_example";  // string | Check-out date YYYY-MM-DD (optional) 
            var adults = 2;  // int? |  (optional)  (default to 2)
            var children = "children_example";  // string | Comma-separated children ages, e.g. '4,9' (optional) 
            var rooms = 1;  // int? |  (optional)  (default to 1)
            var offset = 0;  // int? | Result offset for pagination (optional)  (default to 0)
            var limit = 25;  // int? |  (optional)  (default to 25)
            var sort = "sort_example";  // string | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh (optional) 
            var filters = "filters_example";  // string | Semicolon-separated Booking filter ids, e.g. 'class=4' (optional) 
            var currency = "currency_example";  // string | ISO currency, e.g. EUR, USD, GBP (optional) 
            var language = "language_example";  // string | Locale, e.g. en-us, fr, de, es (optional) 

            try
            {
                // Search properties
                Object result = apiInstance.BookingSearchProperties(location, destId, destType, checkin, checkout, adults, children, rooms, offset, limit, sort, filters, currency, language);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling BookingApi.BookingSearchProperties: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the BookingSearchPropertiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search properties
    ApiResponse<Object> response = apiInstance.BookingSearchPropertiesWithHttpInfo(location, destId, destType, checkin, checkout, adults, children, rooms, offset, limit, sort, filters, currency, language);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling BookingApi.BookingSearchPropertiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Free-text destination, e.g. &#39;Rome&#39; | [optional]  |
| **destId** | **int?** | Exact destination id (ufi) from /destinations | [optional]  |
| **destType** | **string** | Destination type, e.g. CITY | [optional] [default to &quot;NO_DEST_TYPE&quot;] |
| **checkin** | **string** | Check-in date YYYY-MM-DD | [optional]  |
| **checkout** | **string** | Check-out date YYYY-MM-DD | [optional]  |
| **adults** | **int?** |  | [optional] [default to 2] |
| **children** | **string** | Comma-separated children ages, e.g. &#39;4,9&#39; | [optional]  |
| **rooms** | **int?** |  | [optional] [default to 1] |
| **offset** | **int?** | Result offset for pagination | [optional] [default to 0] |
| **limit** | **int?** |  | [optional] [default to 25] |
| **sort** | **string** | popularity | price | class_descending | class_ascending | distance_from_search | bayesian_review_score | review_score_and_price | upsort_bh | [optional]  |
| **filters** | **string** | Semicolon-separated Booking filter ids, e.g. &#39;class&#x3D;4&#39; | [optional]  |
| **currency** | **string** | ISO currency, e.g. EUR, USD, GBP | [optional]  |
| **language** | **string** | Locale, e.g. en-us, fr, de, es | [optional]  |

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

