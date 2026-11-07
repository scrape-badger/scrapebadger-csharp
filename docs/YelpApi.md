# ScrapeBadger.Api.YelpApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**YelpListMarkets**](YelpApi.md#yelplistmarkets) | **GET** /v1/yelp/markets | List markets |
| [**YelpSearchBusinesses**](YelpApi.md#yelpsearchbusinesses) | **GET** /v1/yelp/search | Search businesses |

<a id="yelplistmarkets"></a>
# **YelpListMarkets**
> YelpMarketsResponse YelpListMarkets ()

List markets

Yelp sites this API verifiably searches. Free.

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
    public class YelpListMarketsExample
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
            var apiInstance = new YelpApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                YelpMarketsResponse result = apiInstance.YelpListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YelpApi.YelpListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YelpListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<YelpMarketsResponse> response = apiInstance.YelpListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YelpApi.YelpListMarketsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters
This endpoint does not need any parameter.
### Return type

[**YelpMarketsResponse**](YelpMarketsResponse.md)

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

<a id="yelpsearchbusinesses"></a>
# **YelpSearchBusinesses**
> YelpSearchResponse YelpSearchBusinesses (string location, string query = null, string market = null, string category = null, string sortBy = null, string price = null, string features = null, int? page = null)

Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

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
    public class YelpSearchBusinessesExample
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
            var apiInstance = new YelpApi(httpClient, config, httpClientHandler);
            var location = "location_example";  // string | Where to search, as typed into Yelp: city, neighbourhood, address or postcode.
            var query = "query_example";  // string | What to search for (e.g. pizza, plumbers). Optional when category is set. (optional) 
            var market = "us";  // string | Yelp site to search; see /markets. (optional)  (default to us)
            var category = "category_example";  // string | Yelp category alias, e.g. pizza, coffee, plumbing. (optional) 
            var sortBy = "recommended";  // string |  (optional)  (default to recommended)
            var price = "price_example";  // string | Comma-separated price levels 1-4 ($ to $$$$). (optional) 
            var features = "features_example";  // string | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. (optional) 
            var page = 1;  // int? | 1-based page, ten businesses each; pages 1-11. (optional)  (default to 1)

            try
            {
                // Search businesses
                YelpSearchResponse result = apiInstance.YelpSearchBusinesses(location, query, market, category, sortBy, price, features, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling YelpApi.YelpSearchBusinesses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the YelpSearchBusinessesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search businesses
    ApiResponse<YelpSearchResponse> response = apiInstance.YelpSearchBusinessesWithHttpInfo(location, query, market, category, sortBy, price, features, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling YelpApi.YelpSearchBusinessesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **location** | **string** | Where to search, as typed into Yelp: city, neighbourhood, address or postcode. |  |
| **query** | **string** | What to search for (e.g. pizza, plumbers). Optional when category is set. | [optional]  |
| **market** | **string** | Yelp site to search; see /markets. | [optional] [default to us] |
| **category** | **string** | Yelp category alias, e.g. pizza, coffee, plumbing. | [optional]  |
| **sortBy** | **string** |  | [optional] [default to recommended] |
| **price** | **string** | Comma-separated price levels 1-4 ($ to $$$$). | [optional]  |
| **features** | **string** | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. | [optional]  |
| **page** | **int?** | 1-based page, ten businesses each; pages 1-11. | [optional] [default to 1] |

### Return type

[**YelpSearchResponse**](YelpSearchResponse.md)

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

