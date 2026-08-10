# ScrapeBadger.Api.GoogleApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GoogleGetAuthorCitationsPerYearChart**](GoogleApi.md#googlegetauthorcitationsperyearchart) | **GET** /v1/google/scholar/author/citation | Get author citations-per-year chart |
| [**GoogleGetBusinessPosts**](GoogleApi.md#googlegetbusinessposts) | **GET** /v1/google/maps/posts | Get business posts |
| [**GoogleGetCitationFormatsForAScholarPaper**](GoogleApi.md#googlegetcitationformatsforascholarpaper) | **GET** /v1/google/scholar/cite | Get citation formats for a Scholar paper |
| [**GoogleGetPlaceDetails**](GoogleApi.md#googlegetplacedetails) | **GET** /v1/google/maps/place | Get place details |
| [**GoogleGetPlacePhotos**](GoogleApi.md#googlegetplacephotos) | **GET** /v1/google/maps/photos | Get place photos |
| [**GoogleGetPlaceReviews**](GoogleApi.md#googlegetplacereviews) | **GET** /v1/google/maps/reviews | Get place reviews |
| [**GoogleGetScholarAuthorProfile**](GoogleApi.md#googlegetscholarauthorprofile) | **GET** /v1/google/scholar/author | Get Scholar author profile |
| [**GoogleGetStockIndexQuote**](GoogleApi.md#googlegetstockindexquote) | **GET** /v1/google/finance/quote | Get stock/index quote |
| [**GoogleGoogleAiModeSearch**](GoogleApi.md#googlegoogleaimodesearch) | **GET** /v1/google/ai-mode/search | Google AI Mode search |
| [**GoogleGoogleAiOverviewInlineSerpBlock**](GoogleApi.md#googlegoogleaioverviewinlineserpblock) | **GET** /v1/google/ai-overview | Google AI Overview (inline SERP block) |
| [**GoogleGoogleFlightsCalendarCheapestFarePerDate**](GoogleApi.md#googlegoogleflightscalendarcheapestfareperdate) | **GET** /v1/google/flights/calendar | Google Flights calendar — cheapest fare per date |
| [**GoogleGoogleFlightsSearch**](GoogleApi.md#googlegoogleflightssearch) | **GET** /v1/google/flights/search | Google Flights search |
| [**GoogleGoogleLensVisualSearch**](GoogleApi.md#googlegooglelensvisualsearch) | **GET** /v1/google/lens/search | Google Lens visual search |
| [**GoogleGoogleScraperHealthCheck**](GoogleApi.md#googlegooglescraperhealthcheck) | **GET** /v1/google/health | Google scraper health check |
| [**GoogleGoogleScraperHealthCheckHead**](GoogleApi.md#googlegooglescraperhealthcheckhead) | **HEAD** /v1/google/health | Google scraper health check |
| [**GoogleGoogleSearchSuggestions**](GoogleApi.md#googlegooglesearchsuggestions) | **GET** /v1/google/autocomplete | Google search suggestions |
| [**GoogleGoogleShortsSearch**](GoogleApi.md#googlegoogleshortssearch) | **GET** /v1/google/shorts/search | Google Shorts search |
| [**GoogleGoogleWebSearch**](GoogleApi.md#googlegooglewebsearch) | **GET** /v1/google/search | Google web search |
| [**GoogleHotelDetails**](GoogleApi.md#googlehoteldetails) | **GET** /v1/google/hotels/details | Hotel details |
| [**GoogleImmersiveProductDetail**](GoogleApi.md#googleimmersiveproductdetail) | **GET** /v1/google/products/detail | Immersive product detail |
| [**GoogleInterestByRegion**](GoogleApi.md#googleinterestbyregion) | **GET** /v1/google/trends/regions | Interest by region |
| [**GoogleInterestOverTime**](GoogleApi.md#googleinterestovertime) | **GET** /v1/google/trends/interest | Interest over time |
| [**GoogleMultiSellerOffersByBarcode**](GoogleApi.md#googlemultiselleroffersbybarcode) | **GET** /v1/google/shopping/offers | Multi-seller offers by barcode |
| [**GoogleNewsByTopic**](GoogleApi.md#googlenewsbytopic) | **GET** /v1/google/news/topics | News by topic |
| [**GooglePatentDetails**](GoogleApi.md#googlepatentdetails) | **GET** /v1/google/patents/detail | Patent details |
| [**GoogleRelatedTopicsQueries**](GoogleApi.md#googlerelatedtopicsqueries) | **GET** /v1/google/trends/related | Related topics &amp; queries |
| [**GoogleSearchGoogleImages**](GoogleApi.md#googlesearchgoogleimages) | **GET** /v1/google/images/search | Search Google Images |
| [**GoogleSearchGoogleJobs**](GoogleApi.md#googlesearchgooglejobs) | **GET** /v1/google/jobs/search | Search Google Jobs |
| [**GoogleSearchGoogleMapsPlaces**](GoogleApi.md#googlesearchgooglemapsplaces) | **GET** /v1/google/maps/search | Search Google Maps places |
| [**GoogleSearchGoogleNews**](GoogleApi.md#googlesearchgooglenews) | **GET** /v1/google/news/search | Search Google News |
| [**GoogleSearchGoogleScholar**](GoogleApi.md#googlesearchgooglescholar) | **GET** /v1/google/scholar/search | Search Google Scholar |
| [**GoogleSearchGoogleVideos**](GoogleApi.md#googlesearchgooglevideos) | **GET** /v1/google/videos/search | Search Google Videos |
| [**GoogleSearchHotels**](GoogleApi.md#googlesearchhotels) | **GET** /v1/google/hotels/search | Search hotels |
| [**GoogleSearchPatents**](GoogleApi.md#googlesearchpatents) | **GET** /v1/google/patents/search | Search patents |
| [**GoogleSearchProducts**](GoogleApi.md#googlesearchproducts) | **GET** /v1/google/shopping/search | Search products |
| [**GoogleSearchScholarAuthorProfiles**](GoogleApi.md#googlesearchscholarauthorprofiles) | **GET** /v1/google/scholar/profiles | Search Scholar author profiles |
| [**GoogleTrendingNews**](GoogleApi.md#googletrendingnews) | **GET** /v1/google/news/trending | Trending news |
| [**GoogleTrendingSearches**](GoogleApi.md#googletrendingsearches) | **GET** /v1/google/trends/trending | Trending searches |
| [**GoogleTrendsTopicAutocomplete**](GoogleApi.md#googletrendstopicautocomplete) | **GET** /v1/google/trends/autocomplete | Trends topic autocomplete |

<a id="googlegetauthorcitationsperyearchart"></a>
# **GoogleGetAuthorCitationsPerYearChart**
> Object GoogleGetAuthorCitationsPerYearChart (string authorId, string hl = null)

Get author citations-per-year chart

Return the citations-per-year chart for a Google Scholar author.

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
    public class GoogleGetAuthorCitationsPerYearChartExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var authorId = "authorId_example";  // string | Scholar user ID
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")

            try
            {
                // Get author citations-per-year chart
                Object result = apiInstance.GoogleGetAuthorCitationsPerYearChart(authorId, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetAuthorCitationsPerYearChart: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetAuthorCitationsPerYearChartWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get author citations-per-year chart
    ApiResponse<Object> response = apiInstance.GoogleGetAuthorCitationsPerYearChartWithHttpInfo(authorId, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetAuthorCitationsPerYearChartWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authorId** | **string** | Scholar user ID |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |

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

<a id="googlegetbusinessposts"></a>
# **GoogleGetBusinessPosts**
> Object GoogleGetBusinessPosts (string dataId, string nextPageToken = null)

Get business posts

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
    public class GoogleGetBusinessPostsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var dataId = "dataId_example";  // string | Maps data ID
            var nextPageToken = "nextPageToken_example";  // string |  (optional) 

            try
            {
                // Get business posts
                Object result = apiInstance.GoogleGetBusinessPosts(dataId, nextPageToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetBusinessPosts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetBusinessPostsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get business posts
    ApiResponse<Object> response = apiInstance.GoogleGetBusinessPostsWithHttpInfo(dataId, nextPageToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetBusinessPostsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dataId** | **string** | Maps data ID |  |
| **nextPageToken** | **string** |  | [optional]  |

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

<a id="googlegetcitationformatsforascholarpaper"></a>
# **GoogleGetCitationFormatsForAScholarPaper**
> Object GoogleGetCitationFormatsForAScholarPaper (string q, string hl = null)

Get citation formats for a Scholar paper

Return MLA, APA, Chicago, Harvard, and Vancouver citation formats for a paper.

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
    public class GoogleGetCitationFormatsForAScholarPaperExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Cluster ID from a search result
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")

            try
            {
                // Get citation formats for a Scholar paper
                Object result = apiInstance.GoogleGetCitationFormatsForAScholarPaper(q, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetCitationFormatsForAScholarPaper: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetCitationFormatsForAScholarPaperWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get citation formats for a Scholar paper
    ApiResponse<Object> response = apiInstance.GoogleGetCitationFormatsForAScholarPaperWithHttpInfo(q, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetCitationFormatsForAScholarPaperWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Cluster ID from a search result |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |

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

<a id="googlegetplacedetails"></a>
# **GoogleGetPlaceDetails**
> Object GoogleGetPlaceDetails (string placeId = null, string dataId = null, string hl = null, string gl = null)

Get place details

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
    public class GoogleGetPlaceDetailsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var placeId = "placeId_example";  // string |  (optional) 
            var dataId = "dataId_example";  // string |  (optional) 
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var gl = "\"us\"";  // string |  (optional)  (default to "us")

            try
            {
                // Get place details
                Object result = apiInstance.GoogleGetPlaceDetails(placeId, dataId, hl, gl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetPlaceDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetPlaceDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get place details
    ApiResponse<Object> response = apiInstance.GoogleGetPlaceDetailsWithHttpInfo(placeId, dataId, hl, gl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetPlaceDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **placeId** | **string** |  | [optional]  |
| **dataId** | **string** |  | [optional]  |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |

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

<a id="googlegetplacephotos"></a>
# **GoogleGetPlacePhotos**
> Object GoogleGetPlacePhotos (string dataId, string hl = null, string nextPageToken = null)

Get place photos

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
    public class GoogleGetPlacePhotosExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var dataId = "dataId_example";  // string | Maps data ID
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var nextPageToken = "nextPageToken_example";  // string |  (optional) 

            try
            {
                // Get place photos
                Object result = apiInstance.GoogleGetPlacePhotos(dataId, hl, nextPageToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetPlacePhotos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetPlacePhotosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get place photos
    ApiResponse<Object> response = apiInstance.GoogleGetPlacePhotosWithHttpInfo(dataId, hl, nextPageToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetPlacePhotosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dataId** | **string** | Maps data ID |  |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **nextPageToken** | **string** |  | [optional]  |

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

<a id="googlegetplacereviews"></a>
# **GoogleGetPlaceReviews**
> Object GoogleGetPlaceReviews (string dataId, string sortBy = null, string hl = null, string nextPageToken = null, int? results = null)

Get place reviews

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
    public class GoogleGetPlaceReviewsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var dataId = "dataId_example";  // string | Maps data ID
            var sortBy = "\"qualityScore\"";  // string |  (optional)  (default to "qualityScore")
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var nextPageToken = "nextPageToken_example";  // string |  (optional) 
            var results = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // Get place reviews
                Object result = apiInstance.GoogleGetPlaceReviews(dataId, sortBy, hl, nextPageToken, results);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetPlaceReviews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetPlaceReviewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get place reviews
    ApiResponse<Object> response = apiInstance.GoogleGetPlaceReviewsWithHttpInfo(dataId, sortBy, hl, nextPageToken, results);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetPlaceReviewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **dataId** | **string** | Maps data ID |  |
| **sortBy** | **string** |  | [optional] [default to &quot;qualityScore&quot;] |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **nextPageToken** | **string** |  | [optional]  |
| **results** | **int?** |  | [optional] [default to 10] |

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

<a id="googlegetscholarauthorprofile"></a>
# **GoogleGetScholarAuthorProfile**
> Object GoogleGetScholarAuthorProfile (string authorId, string hl = null, int? cstart = null, int? pagesize = null)

Get Scholar author profile

Get detailed Google Scholar author profile including articles, stats, co-authors.

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
    public class GoogleGetScholarAuthorProfileExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var authorId = "authorId_example";  // string | Scholar user ID (the `user` query parameter)
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var cstart = 0;  // int? | Articles pagination offset (optional)  (default to 0)
            var pagesize = 20;  // int? | Articles per page (optional)  (default to 20)

            try
            {
                // Get Scholar author profile
                Object result = apiInstance.GoogleGetScholarAuthorProfile(authorId, hl, cstart, pagesize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetScholarAuthorProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetScholarAuthorProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Scholar author profile
    ApiResponse<Object> response = apiInstance.GoogleGetScholarAuthorProfileWithHttpInfo(authorId, hl, cstart, pagesize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetScholarAuthorProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **authorId** | **string** | Scholar user ID (the &#x60;user&#x60; query parameter) |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **cstart** | **int?** | Articles pagination offset | [optional] [default to 0] |
| **pagesize** | **int?** | Articles per page | [optional] [default to 20] |

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

<a id="googlegetstockindexquote"></a>
# **GoogleGetStockIndexQuote**
> Object GoogleGetStockIndexQuote (string q, string hl = null)

Get stock/index quote

Get a stock or index quote from Google Finance.

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
    public class GoogleGetStockIndexQuoteExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Ticker and exchange (e.g. \"AAPL:NASDAQ\", \"BTC-USD\")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")

            try
            {
                // Get stock/index quote
                Object result = apiInstance.GoogleGetStockIndexQuote(q, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGetStockIndexQuote: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGetStockIndexQuoteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get stock/index quote
    ApiResponse<Object> response = apiInstance.GoogleGetStockIndexQuoteWithHttpInfo(q, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGetStockIndexQuoteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Ticker and exchange (e.g. \&quot;AAPL:NASDAQ\&quot;, \&quot;BTC-USD\&quot;) |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |

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

<a id="googlegoogleaimodesearch"></a>
# **GoogleGoogleAiModeSearch**
> Object GoogleGoogleAiModeSearch (string q, string gl = null, string hl = null, bool? includeHtml = null)

Google AI Mode search

Get AI-generated search results from Google AI Mode.  Returns the structured `text_blocks` (paragraphs, headings, comparison `table` blocks and lists), a flat `references` source list, a compact `markdown` rendering of the whole answer and — unless `include_html` is false — the raw `answer_html` body.

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
    public class GoogleGoogleAiModeSearchExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query for AI-generated response
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var includeHtml = true;  // bool? | Include the raw `answer_html` (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured `text_blocks` + `markdown`. (optional)  (default to true)

            try
            {
                // Google AI Mode search
                Object result = apiInstance.GoogleGoogleAiModeSearch(q, gl, hl, includeHtml);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleAiModeSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleAiModeSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google AI Mode search
    ApiResponse<Object> response = apiInstance.GoogleGoogleAiModeSearchWithHttpInfo(q, gl, hl, includeHtml);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleAiModeSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query for AI-generated response |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **includeHtml** | **bool?** | Include the raw &#x60;answer_html&#x60; (full answer body HTML) in the response for maximum parity. It can be 100s of KB — set false when you only need the structured &#x60;text_blocks&#x60; + &#x60;markdown&#x60;. | [optional] [default to true] |

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

<a id="googlegoogleaioverviewinlineserpblock"></a>
# **GoogleGoogleAiOverviewInlineSerpBlock**
> Object GoogleGoogleAiOverviewInlineSerpBlock (string q, string gl = null, string hl = null)

Google AI Overview (inline SERP block)

Get the AI Overview block Google renders inline at the top of a SERP.  Deferred overviews (where Google lazy-loads the block via a follow-up ``page_token``) are chased automatically.

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
    public class GoogleGoogleAiOverviewInlineSerpBlockExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query — same shape as a Google Search query
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")

            try
            {
                // Google AI Overview (inline SERP block)
                Object result = apiInstance.GoogleGoogleAiOverviewInlineSerpBlock(q, gl, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleAiOverviewInlineSerpBlock: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleAiOverviewInlineSerpBlockWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google AI Overview (inline SERP block)
    ApiResponse<Object> response = apiInstance.GoogleGoogleAiOverviewInlineSerpBlockWithHttpInfo(q, gl, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleAiOverviewInlineSerpBlockWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query — same shape as a Google Search query |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |

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

<a id="googlegoogleflightscalendarcheapestfareperdate"></a>
# **GoogleGoogleFlightsCalendarCheapestFarePerDate**
> Object GoogleGoogleFlightsCalendarCheapestFarePerDate (string departureId, string arrivalId, string outboundDateFrom, string outboundDateTo, string tripType = null, int? tripLengthDays = null, string returnDateFrom = null, string returnDateTo = null, int? adults = null, int? children = null, int? infantsInSeat = null, int? infantsOnLap = null, string travelClass = null, string currency = null, string gl = null, string hl = null)

Google Flights calendar — cheapest fare per date

Price a whole range of dates in one call — up to 200 dates per request.  Google Flights' own price graph / date grid: the cheapest fare per departure date instead of one search per date. Prices match `/flights/search` exactly.

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
    public class GoogleGoogleFlightsCalendarCheapestFarePerDateExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var departureId = "departureId_example";  // string | Departure airport IATA code or location ID
            var arrivalId = "arrivalId_example";  // string | Arrival airport IATA code or location ID
            var outboundDateFrom = "outboundDateFrom_example";  // string | First outbound date to price (YYYY-MM-DD)
            var outboundDateTo = "outboundDateTo_example";  // string | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode.
            var tripType = "\"one_way\"";  // string | one_way | round_trip (optional)  (default to "one_way")
            var tripLengthDays = 56;  // int? | Round-trip stay length in nights (price-graph mode). Defaults to 7. (optional) 
            var returnDateFrom = "returnDateFrom_example";  // string | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. (optional) 
            var returnDateTo = "returnDateTo_example";  // string | Date-grid mode: last return date (optional) 
            var adults = 1;  // int? |  (optional)  (default to 1)
            var children = 0;  // int? |  (optional)  (default to 0)
            var infantsInSeat = 0;  // int? |  (optional)  (default to 0)
            var infantsOnLap = 0;  // int? |  (optional)  (default to 0)
            var travelClass = "\"economy\"";  // string |  (optional)  (default to "economy")
            var currency = "\"USD\"";  // string | ISO-4217 currency (optional)  (default to "USD")
            var gl = "\"us\"";  // string |  (optional)  (default to "us")
            var hl = "\"en\"";  // string |  (optional)  (default to "en")

            try
            {
                // Google Flights calendar — cheapest fare per date
                Object result = apiInstance.GoogleGoogleFlightsCalendarCheapestFarePerDate(departureId, arrivalId, outboundDateFrom, outboundDateTo, tripType, tripLengthDays, returnDateFrom, returnDateTo, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleFlightsCalendarCheapestFarePerDate: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleFlightsCalendarCheapestFarePerDateWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google Flights calendar — cheapest fare per date
    ApiResponse<Object> response = apiInstance.GoogleGoogleFlightsCalendarCheapestFarePerDateWithHttpInfo(departureId, arrivalId, outboundDateFrom, outboundDateTo, tripType, tripLengthDays, returnDateFrom, returnDateTo, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleFlightsCalendarCheapestFarePerDateWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **departureId** | **string** | Departure airport IATA code or location ID |  |
| **arrivalId** | **string** | Arrival airport IATA code or location ID |  |
| **outboundDateFrom** | **string** | First outbound date to price (YYYY-MM-DD) |  |
| **outboundDateTo** | **string** | Last outbound date to price (YYYY-MM-DD). At most 200 days from outbound_date_from, or 14 in date-grid mode. |  |
| **tripType** | **string** | one_way | round_trip | [optional] [default to &quot;one_way&quot;] |
| **tripLengthDays** | **int?** | Round-trip stay length in nights (price-graph mode). Defaults to 7. | [optional]  |
| **returnDateFrom** | **string** | Date-grid mode: first return date. With return_date_to, returns the full outbound x return matrix (each range at most 14 days). Round-trip only. | [optional]  |
| **returnDateTo** | **string** | Date-grid mode: last return date | [optional]  |
| **adults** | **int?** |  | [optional] [default to 1] |
| **children** | **int?** |  | [optional] [default to 0] |
| **infantsInSeat** | **int?** |  | [optional] [default to 0] |
| **infantsOnLap** | **int?** |  | [optional] [default to 0] |
| **travelClass** | **string** |  | [optional] [default to &quot;economy&quot;] |
| **currency** | **string** | ISO-4217 currency | [optional] [default to &quot;USD&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |

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

<a id="googlegoogleflightssearch"></a>
# **GoogleGoogleFlightsSearch**
> Object GoogleGoogleFlightsSearch (string departureId, string arrivalId, string outboundDate, string returnDate = null, string tripType = null, int? adults = null, int? children = null, int? infantsInSeat = null, int? infantsOnLap = null, string travelClass = null, string currency = null, string gl = null, string hl = null, string stops = null, int? maxPrice = null, string departureToken = null)

Google Flights search

Search Google Flights for available itineraries.

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
    public class GoogleGoogleFlightsSearchExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var departureId = "departureId_example";  // string | Departure airport IATA code or location ID
            var arrivalId = "arrivalId_example";  // string | Arrival airport IATA code or location ID
            var outboundDate = "outboundDate_example";  // string | Outbound date (YYYY-MM-DD)
            var returnDate = "returnDate_example";  // string | Return date (round-trip only) (optional) 
            var tripType = "\"round_trip\"";  // string | round_trip | one_way | multi_city (optional)  (default to "round_trip")
            var adults = 1;  // int? |  (optional)  (default to 1)
            var children = 0;  // int? |  (optional)  (default to 0)
            var infantsInSeat = 0;  // int? |  (optional)  (default to 0)
            var infantsOnLap = 0;  // int? |  (optional)  (default to 0)
            var travelClass = "\"economy\"";  // string |  (optional)  (default to "economy")
            var currency = "\"USD\"";  // string | ISO-4217 currency (optional)  (default to "USD")
            var gl = "\"us\"";  // string |  (optional)  (default to "us")
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var stops = "\"any\"";  // string |  (optional)  (default to "any")
            var maxPrice = 56;  // int? |  (optional) 
            var departureToken = "departureToken_example";  // string | A round-trip offer's departure_token; returns the return-leg flights for that selected outbound (round-trip only). (optional) 

            try
            {
                // Google Flights search
                Object result = apiInstance.GoogleGoogleFlightsSearch(departureId, arrivalId, outboundDate, returnDate, tripType, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl, stops, maxPrice, departureToken);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleFlightsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleFlightsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google Flights search
    ApiResponse<Object> response = apiInstance.GoogleGoogleFlightsSearchWithHttpInfo(departureId, arrivalId, outboundDate, returnDate, tripType, adults, children, infantsInSeat, infantsOnLap, travelClass, currency, gl, hl, stops, maxPrice, departureToken);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleFlightsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **departureId** | **string** | Departure airport IATA code or location ID |  |
| **arrivalId** | **string** | Arrival airport IATA code or location ID |  |
| **outboundDate** | **string** | Outbound date (YYYY-MM-DD) |  |
| **returnDate** | **string** | Return date (round-trip only) | [optional]  |
| **tripType** | **string** | round_trip | one_way | multi_city | [optional] [default to &quot;round_trip&quot;] |
| **adults** | **int?** |  | [optional] [default to 1] |
| **children** | **int?** |  | [optional] [default to 0] |
| **infantsInSeat** | **int?** |  | [optional] [default to 0] |
| **infantsOnLap** | **int?** |  | [optional] [default to 0] |
| **travelClass** | **string** |  | [optional] [default to &quot;economy&quot;] |
| **currency** | **string** | ISO-4217 currency | [optional] [default to &quot;USD&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **stops** | **string** |  | [optional] [default to &quot;any&quot;] |
| **maxPrice** | **int?** |  | [optional]  |
| **departureToken** | **string** | A round-trip offer&#39;s departure_token; returns the return-leg flights for that selected outbound (round-trip only). | [optional]  |

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

<a id="googlegooglelensvisualsearch"></a>
# **GoogleGoogleLensVisualSearch**
> Object GoogleGoogleLensVisualSearch (string url, string query = null, string country = null, string language = null, string gl = null, string hl = null, bool? product = null, bool? visualMatches = null, bool? exactMatches = null)

Google Lens visual search

Google Lens visual search.  Response carries ``lens_results`` (Scrapingdog parity alias) with ``title`` / ``source`` / ``source_favicon`` / ``thumbnail`` / ``original_thumbnail`` / ``rating`` / ``reviews`` / ``in_stock``, plus ``price`` (``{value, currency, extracted}``) and the raw ``tag`` chip it is parsed from, on shoppable matches. ``related_searches`` chips come alongside. Legacy ``results`` alias kept for backwards compat.

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
    public class GoogleGoogleLensVisualSearchExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var url = "url_example";  // string | Public URL of the image to search visually
            var query = "query_example";  // string | Optional text refinement (e.g. 'pizza') (optional) 
            var country = "country_example";  // string | ISO country code (alias for gl) (optional) 
            var language = "language_example";  // string | Language code (alias for hl) (optional) 
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var product = false;  // bool? | Bias towards shoppable product matches (optional)  (default to false)
            var visualMatches = true;  // bool? | Include the visual-matches carousel (optional)  (default to true)
            var exactMatches = false;  // bool? | Restrict to exact-match results (optional)  (default to false)

            try
            {
                // Google Lens visual search
                Object result = apiInstance.GoogleGoogleLensVisualSearch(url, query, country, language, gl, hl, product, visualMatches, exactMatches);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleLensVisualSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleLensVisualSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google Lens visual search
    ApiResponse<Object> response = apiInstance.GoogleGoogleLensVisualSearchWithHttpInfo(url, query, country, language, gl, hl, product, visualMatches, exactMatches);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleLensVisualSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **url** | **string** | Public URL of the image to search visually |  |
| **query** | **string** | Optional text refinement (e.g. &#39;pizza&#39;) | [optional]  |
| **country** | **string** | ISO country code (alias for gl) | [optional]  |
| **language** | **string** | Language code (alias for hl) | [optional]  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **product** | **bool?** | Bias towards shoppable product matches | [optional] [default to false] |
| **visualMatches** | **bool?** | Include the visual-matches carousel | [optional] [default to true] |
| **exactMatches** | **bool?** | Restrict to exact-match results | [optional] [default to false] |

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

<a id="googlegooglescraperhealthcheck"></a>
# **GoogleGoogleScraperHealthCheck**
> Object GoogleGoogleScraperHealthCheck ()

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class GoogleGoogleScraperHealthCheckExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);

            try
            {
                // Google scraper health check
                Object result = apiInstance.GoogleGoogleScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google scraper health check
    ApiResponse<Object> response = apiInstance.GoogleGoogleScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="googlegooglescraperhealthcheckhead"></a>
# **GoogleGoogleScraperHealthCheckHead**
> Object GoogleGoogleScraperHealthCheckHead ()

Google scraper health check

Check health of the Google scraper service.  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class GoogleGoogleScraperHealthCheckHeadExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);

            try
            {
                // Google scraper health check
                Object result = apiInstance.GoogleGoogleScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google scraper health check
    ApiResponse<Object> response = apiInstance.GoogleGoogleScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="googlegooglesearchsuggestions"></a>
# **GoogleGoogleSearchSuggestions**
> Object GoogleGoogleSearchSuggestions (string q, string hl = null, string gl = null)

Google search suggestions

Get Google search autocomplete suggestions.

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
    public class GoogleGoogleSearchSuggestionsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query to get suggestions for
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")

            try
            {
                // Google search suggestions
                Object result = apiInstance.GoogleGoogleSearchSuggestions(q, hl, gl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleSearchSuggestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleSearchSuggestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google search suggestions
    ApiResponse<Object> response = apiInstance.GoogleGoogleSearchSuggestionsWithHttpInfo(q, hl, gl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleSearchSuggestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query to get suggestions for |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |

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

<a id="googlegoogleshortssearch"></a>
# **GoogleGoogleShortsSearch**
> Object GoogleGoogleShortsSearch (string q, string gl = null, string hl = null, string domain = null, int? num = null, int? start = null)

Google Shorts search

Return short-form video results (YouTube Shorts, TikToks) from Google Shorts mode.

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
    public class GoogleGoogleShortsSearchExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var domain = "\"google.com\"";  // string | Google domain (optional)  (default to "google.com")
            var num = 20;  // int? | Results per page (optional)  (default to 20)
            var start = 0;  // int? | Pagination offset (optional)  (default to 0)

            try
            {
                // Google Shorts search
                Object result = apiInstance.GoogleGoogleShortsSearch(q, gl, hl, domain, num, start);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleShortsSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleShortsSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google Shorts search
    ApiResponse<Object> response = apiInstance.GoogleGoogleShortsSearchWithHttpInfo(q, gl, hl, domain, num, start);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleShortsSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **domain** | **string** | Google domain | [optional] [default to &quot;google.com&quot;] |
| **num** | **int?** | Results per page | [optional] [default to 20] |
| **start** | **int?** | Pagination offset | [optional] [default to 0] |

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

<a id="googlegooglewebsearch"></a>
# **GoogleGoogleWebSearch**
> Object GoogleGoogleWebSearch (string q, string gl = null, string hl = null, int? num = null, int? start = null, string domain = null, string device = null, string userAgent = null, string output = null, string location = null, string lr = null, string tbs = null, string safe = null, string uule = null, int? filter = null, int? nfpr = null, string cr = null, string ludocid = null, string lsig = null, string kgmid = null, string si = null, string ibp = null, string uds = null, bool? aiOverview = null)

Google web search

Search Google and get structured results (organic, ads, KG, AI overview, PAA).

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
    public class GoogleGoogleWebSearchExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query (supports Google operators)
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var num = 10;  // int? |  (optional)  (default to 10)
            var start = 0;  // int? | Page offset (0, 10, 20...) (optional)  (default to 0)
            var domain = "\"google.com\"";  // string | Google domain (optional)  (default to "google.com")
            var device = "desktop";  // string | Device target: desktop, mobile, iphone, android, tablet (optional)  (default to desktop)
            var userAgent = "userAgent_example";  // string | Custom User-Agent (overrides device) (optional) 
            var output = "json";  // string | Response format: json (parsed) or html (raw SERP) (optional)  (default to json)
            var location = "location_example";  // string | City-level geo-targeting (optional) 
            var lr = "lr_example";  // string | Language restrict (e.g. lang_en) (optional) 
            var tbs = "tbs_example";  // string | Time filter (e.g. qdr:d) (optional) 
            var safe = "\"off\"";  // string |  (optional)  (default to "off")
            var uule = "uule_example";  // string | UULE encoded location (optional) 
            var filter = 56;  // int? | Show omitted results (optional) 
            var nfpr = 0;  // int? | Disable auto-correction (optional)  (default to 0)
            var cr = "cr_example";  // string | Country restrict (optional) 
            var ludocid = "ludocid_example";  // string | Google Place CID (optional) 
            var lsig = "lsig_example";  // string | Knowledge Graph map ID (optional) 
            var kgmid = "kgmid_example";  // string | Knowledge Graph entity ID (optional) 
            var si = "si_example";  // string | Cached search params (optional) 
            var ibp = "ibp_example";  // string | Layout control (optional) 
            var uds = "uds_example";  // string | Google filter string (optional) 
            var aiOverview = false;  // bool? | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. (optional)  (default to false)

            try
            {
                // Google web search
                Object result = apiInstance.GoogleGoogleWebSearch(q, gl, hl, num, start, domain, device, userAgent, output, location, lr, tbs, safe, uule, filter, nfpr, cr, ludocid, lsig, kgmid, si, ibp, uds, aiOverview);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleGoogleWebSearch: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleGoogleWebSearchWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Google web search
    ApiResponse<Object> response = apiInstance.GoogleGoogleWebSearchWithHttpInfo(q, gl, hl, num, start, domain, device, userAgent, output, location, lr, tbs, safe, uule, filter, nfpr, cr, ludocid, lsig, kgmid, si, ibp, uds, aiOverview);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleGoogleWebSearchWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query (supports Google operators) |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **num** | **int?** |  | [optional] [default to 10] |
| **start** | **int?** | Page offset (0, 10, 20...) | [optional] [default to 0] |
| **domain** | **string** | Google domain | [optional] [default to &quot;google.com&quot;] |
| **device** | **string** | Device target: desktop, mobile, iphone, android, tablet | [optional] [default to desktop] |
| **userAgent** | **string** | Custom User-Agent (overrides device) | [optional]  |
| **output** | **string** | Response format: json (parsed) or html (raw SERP) | [optional] [default to json] |
| **location** | **string** | City-level geo-targeting | [optional]  |
| **lr** | **string** | Language restrict (e.g. lang_en) | [optional]  |
| **tbs** | **string** | Time filter (e.g. qdr:d) | [optional]  |
| **safe** | **string** |  | [optional] [default to &quot;off&quot;] |
| **uule** | **string** | UULE encoded location | [optional]  |
| **filter** | **int?** | Show omitted results | [optional]  |
| **nfpr** | **int?** | Disable auto-correction | [optional] [default to 0] |
| **cr** | **string** | Country restrict | [optional]  |
| **ludocid** | **string** | Google Place CID | [optional]  |
| **lsig** | **string** | Knowledge Graph map ID | [optional]  |
| **kgmid** | **string** | Knowledge Graph entity ID | [optional]  |
| **si** | **string** | Cached search params | [optional]  |
| **ibp** | **string** | Layout control | [optional]  |
| **uds** | **string** | Google filter string | [optional]  |
| **aiOverview** | **bool?** | Chase deferred AI Overview page_token with a follow-up fetch and merge the result. Adds ~1s and 1 credit when the SERP defers the overview. | [optional] [default to false] |

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

<a id="googlehoteldetails"></a>
# **GoogleHotelDetails**
> Object GoogleHotelDetails (string propertyToken, string checkIn, string checkOut)

Hotel details

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
    public class GoogleHotelDetailsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var propertyToken = "propertyToken_example";  // string | Property token
            var checkIn = "checkIn_example";  // string | YYYY-MM-DD
            var checkOut = "checkOut_example";  // string | YYYY-MM-DD

            try
            {
                // Hotel details
                Object result = apiInstance.GoogleHotelDetails(propertyToken, checkIn, checkOut);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleHotelDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleHotelDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Hotel details
    ApiResponse<Object> response = apiInstance.GoogleHotelDetailsWithHttpInfo(propertyToken, checkIn, checkOut);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleHotelDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **propertyToken** | **string** | Property token |  |
| **checkIn** | **string** | YYYY-MM-DD |  |
| **checkOut** | **string** | YYYY-MM-DD |  |

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

<a id="googleimmersiveproductdetail"></a>
# **GoogleImmersiveProductDetail**
> Object GoogleImmersiveProductDetail (string productId, string q, string gl = null, string hl = null, string catalogId = null, string imageDocid = null, string headlineOfferDocid = null, string mid = null, bool? includeOffers = null, bool? includeVariants = null)

Immersive product detail

Get deep product details from Google's immersive product page.

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
    public class GoogleImmersiveProductDetailExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var productId = "productId_example";  // string | Google Shopping ``gpcid`` — the product_id returned on ``/shopping/search`` tiles. Scrapingdog-compatible.
            var q = "q_example";  // string | Original search query that surfaced the product. Required by Google's ``/async/oapv`` RPC.
            var gl = "\"us\"";  // string | Country code (ISO 3166 alpha-2) (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var catalogId = "catalogId_example";  // string | Optional ``catalogid`` from the Shopping tile (improves parity). (optional) 
            var imageDocid = "imageDocid_example";  // string | Optional ``imageDocid`` for higher-fidelity images. (optional) 
            var headlineOfferDocid = "headlineOfferDocid_example";  // string | Optional ``headlineOfferDocid`` to pin the featured seller. (optional) 
            var mid = "mid_example";  // string | Optional Google Knowledge-Graph ``mid``. (optional) 
            var includeOffers = false;  // bool? | When true, fetch the full merchant-offer list via a secondary RPC (``/async/piu_ps``). Adds ~1 s. (optional)  (default to false)
            var includeVariants = false;  // bool? | When true, fetch size/colour variants via a secondary RPC (``/async/toy_v``). Adds ~1 s. (optional)  (default to false)

            try
            {
                // Immersive product detail
                Object result = apiInstance.GoogleImmersiveProductDetail(productId, q, gl, hl, catalogId, imageDocid, headlineOfferDocid, mid, includeOffers, includeVariants);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleImmersiveProductDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleImmersiveProductDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Immersive product detail
    ApiResponse<Object> response = apiInstance.GoogleImmersiveProductDetailWithHttpInfo(productId, q, gl, hl, catalogId, imageDocid, headlineOfferDocid, mid, includeOffers, includeVariants);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleImmersiveProductDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **string** | Google Shopping &#x60;&#x60;gpcid&#x60;&#x60; — the product_id returned on &#x60;&#x60;/shopping/search&#x60;&#x60; tiles. Scrapingdog-compatible. |  |
| **q** | **string** | Original search query that surfaced the product. Required by Google&#39;s &#x60;&#x60;/async/oapv&#x60;&#x60; RPC. |  |
| **gl** | **string** | Country code (ISO 3166 alpha-2) | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **catalogId** | **string** | Optional &#x60;&#x60;catalogid&#x60;&#x60; from the Shopping tile (improves parity). | [optional]  |
| **imageDocid** | **string** | Optional &#x60;&#x60;imageDocid&#x60;&#x60; for higher-fidelity images. | [optional]  |
| **headlineOfferDocid** | **string** | Optional &#x60;&#x60;headlineOfferDocid&#x60;&#x60; to pin the featured seller. | [optional]  |
| **mid** | **string** | Optional Google Knowledge-Graph &#x60;&#x60;mid&#x60;&#x60;. | [optional]  |
| **includeOffers** | **bool?** | When true, fetch the full merchant-offer list via a secondary RPC (&#x60;&#x60;/async/piu_ps&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |
| **includeVariants** | **bool?** | When true, fetch size/colour variants via a secondary RPC (&#x60;&#x60;/async/toy_v&#x60;&#x60;). Adds ~1 s. | [optional] [default to false] |

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

<a id="googleinterestbyregion"></a>
# **GoogleInterestByRegion**
> Object GoogleInterestByRegion (string q, string geo = null)

Interest by region

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
    public class GoogleInterestByRegionExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search term
            var geo = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Interest by region
                Object result = apiInstance.GoogleInterestByRegion(q, geo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleInterestByRegion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleInterestByRegionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Interest by region
    ApiResponse<Object> response = apiInstance.GoogleInterestByRegionWithHttpInfo(q, geo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleInterestByRegionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search term |  |
| **geo** | **string** |  | [optional] [default to &quot;&quot;] |

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

<a id="googleinterestovertime"></a>
# **GoogleInterestOverTime**
> Object GoogleInterestOverTime (string q, string geo = null, string date = null)

Interest over time

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
    public class GoogleInterestOverTimeExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search terms
            var geo = "\"\"";  // string |  (optional)  (default to "")
            var date = "\"today 12-m\"";  // string |  (optional)  (default to "today 12-m")

            try
            {
                // Interest over time
                Object result = apiInstance.GoogleInterestOverTime(q, geo, date);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleInterestOverTime: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleInterestOverTimeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Interest over time
    ApiResponse<Object> response = apiInstance.GoogleInterestOverTimeWithHttpInfo(q, geo, date);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleInterestOverTimeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search terms |  |
| **geo** | **string** |  | [optional] [default to &quot;&quot;] |
| **date** | **string** |  | [optional] [default to &quot;today 12-m&quot;] |

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

<a id="googlemultiselleroffersbybarcode"></a>
# **GoogleMultiSellerOffersByBarcode**
> Object GoogleMultiSellerOffersByBarcode (string barcode, string gl = null, string hl = null)

Multi-seller offers by barcode

Resolve a barcode to a product via Google web search, then return its Google Shopping seller offers (source + price per merchant).

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
    public class GoogleMultiSellerOffersByBarcodeExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var barcode = "barcode_example";  // string | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14
            var gl = "gl_example";  // string | Country code (ISO 3166 alpha-2) (optional) 
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")

            try
            {
                // Multi-seller offers by barcode
                Object result = apiInstance.GoogleMultiSellerOffersByBarcode(barcode, gl, hl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleMultiSellerOffersByBarcode: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleMultiSellerOffersByBarcodeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Multi-seller offers by barcode
    ApiResponse<Object> response = apiInstance.GoogleMultiSellerOffersByBarcodeWithHttpInfo(barcode, gl, hl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleMultiSellerOffersByBarcodeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **barcode** | **string** | Product barcode — GTIN-8 / UPC-A / EAN-13 / GTIN-14 |  |
| **gl** | **string** | Country code (ISO 3166 alpha-2) | [optional]  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |

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

<a id="googlenewsbytopic"></a>
# **GoogleNewsByTopic**
> Object GoogleNewsByTopic (string topic, string hl = null, string gl = null, int? maxResults = null)

News by topic

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
    public class GoogleNewsByTopicExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var topic = "topic_example";  // string | Topic name
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var gl = "\"US\"";  // string |  (optional)  (default to "US")
            var maxResults = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // News by topic
                Object result = apiInstance.GoogleNewsByTopic(topic, hl, gl, maxResults);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleNewsByTopic: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleNewsByTopicWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // News by topic
    ApiResponse<Object> response = apiInstance.GoogleNewsByTopicWithHttpInfo(topic, hl, gl, maxResults);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleNewsByTopicWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **topic** | **string** | Topic name |  |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;US&quot;] |
| **maxResults** | **int?** |  | [optional] [default to 10] |

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

<a id="googlepatentdetails"></a>
# **GooglePatentDetails**
> Object GooglePatentDetails (string patentId)

Patent details

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
    public class GooglePatentDetailsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var patentId = "patentId_example";  // string | Patent number

            try
            {
                // Patent details
                Object result = apiInstance.GooglePatentDetails(patentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GooglePatentDetails: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GooglePatentDetailsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Patent details
    ApiResponse<Object> response = apiInstance.GooglePatentDetailsWithHttpInfo(patentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GooglePatentDetailsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **patentId** | **string** | Patent number |  |

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

<a id="googlerelatedtopicsqueries"></a>
# **GoogleRelatedTopicsQueries**
> Object GoogleRelatedTopicsQueries (string q, string geo = null)

Related topics & queries

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
    public class GoogleRelatedTopicsQueriesExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search term
            var geo = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Related topics & queries
                Object result = apiInstance.GoogleRelatedTopicsQueries(q, geo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleRelatedTopicsQueries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleRelatedTopicsQueriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Related topics & queries
    ApiResponse<Object> response = apiInstance.GoogleRelatedTopicsQueriesWithHttpInfo(q, geo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleRelatedTopicsQueriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search term |  |
| **geo** | **string** |  | [optional] [default to &quot;&quot;] |

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

<a id="googlesearchgoogleimages"></a>
# **GoogleSearchGoogleImages**
> Object GoogleSearchGoogleImages (string q, string gl = null, string hl = null, string tbs = null, string imgsz = null, string imgcolor = null, string imgtype = null, string safe = null, int? page = null)

Search Google Images

Search Google Images for visual content.

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
    public class GoogleSearchGoogleImagesExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Image search query
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var tbs = "tbs_example";  // string | Time/filter string (e.g. qdr:d) (optional) 
            var imgsz = "imgsz_example";  // string | Image size: l, m, i, xXl (optional) 
            var imgcolor = "imgcolor_example";  // string | Image color filter (optional) 
            var imgtype = "imgtype_example";  // string | Image type: face, photo, clipart (optional) 
            var safe = "\"off\"";  // string | Safe search (optional)  (default to "off")
            var page = 0;  // int? | Page number (optional)  (default to 0)

            try
            {
                // Search Google Images
                Object result = apiInstance.GoogleSearchGoogleImages(q, gl, hl, tbs, imgsz, imgcolor, imgtype, safe, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleImages: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleImagesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google Images
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleImagesWithHttpInfo(q, gl, hl, tbs, imgsz, imgcolor, imgtype, safe, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleImagesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Image search query |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **tbs** | **string** | Time/filter string (e.g. qdr:d) | [optional]  |
| **imgsz** | **string** | Image size: l, m, i, xXl | [optional]  |
| **imgcolor** | **string** | Image color filter | [optional]  |
| **imgtype** | **string** | Image type: face, photo, clipart | [optional]  |
| **safe** | **string** | Safe search | [optional] [default to &quot;off&quot;] |
| **page** | **int?** | Page number | [optional] [default to 0] |

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

<a id="googlesearchgooglejobs"></a>
# **GoogleSearchGoogleJobs**
> Object GoogleSearchGoogleJobs (string q, string location = null, string gl = null, string jobType = null, string datePosted = null)

Search Google Jobs

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
    public class GoogleSearchGoogleJobsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Job title, keywords
            var location = "location_example";  // string |  (optional) 
            var gl = "\"us\"";  // string |  (optional)  (default to "us")
            var jobType = "jobType_example";  // string |  (optional) 
            var datePosted = "datePosted_example";  // string |  (optional) 

            try
            {
                // Search Google Jobs
                Object result = apiInstance.GoogleSearchGoogleJobs(q, location, gl, jobType, datePosted);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleJobs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleJobsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google Jobs
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleJobsWithHttpInfo(q, location, gl, jobType, datePosted);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleJobsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Job title, keywords |  |
| **location** | **string** |  | [optional]  |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |
| **jobType** | **string** |  | [optional]  |
| **datePosted** | **string** |  | [optional]  |

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

<a id="googlesearchgooglemapsplaces"></a>
# **GoogleSearchGoogleMapsPlaces**
> Object GoogleSearchGoogleMapsPlaces (string q, string ll = null, string gl = null, string hl = null, int? start = null)

Search Google Maps places

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
    public class GoogleSearchGoogleMapsPlacesExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var ll = "ll_example";  // string |  (optional) 
            var gl = "\"us\"";  // string |  (optional)  (default to "us")
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var start = 0;  // int? |  (optional)  (default to 0)

            try
            {
                // Search Google Maps places
                Object result = apiInstance.GoogleSearchGoogleMapsPlaces(q, ll, gl, hl, start);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleMapsPlaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleMapsPlacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google Maps places
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleMapsPlacesWithHttpInfo(q, ll, gl, hl, start);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleMapsPlacesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **ll** | **string** |  | [optional]  |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **start** | **int?** |  | [optional] [default to 0] |

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

<a id="googlesearchgooglenews"></a>
# **GoogleSearchGoogleNews**
> Object GoogleSearchGoogleNews (string q, string hl = null, string gl = null, int? maxResults = null)

Search Google News

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
    public class GoogleSearchGoogleNewsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var gl = "\"US\"";  // string |  (optional)  (default to "US")
            var maxResults = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // Search Google News
                Object result = apiInstance.GoogleSearchGoogleNews(q, hl, gl, maxResults);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleNews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleNewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google News
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleNewsWithHttpInfo(q, hl, gl, maxResults);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleNewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query |  |
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;US&quot;] |
| **maxResults** | **int?** |  | [optional] [default to 10] |

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

<a id="googlesearchgooglescholar"></a>
# **GoogleSearchGoogleScholar**
> Object GoogleSearchGoogleScholar (string q, string hl = null, int? asYlo = null, int? asYhi = null, string asSdt = null, int? page = null, int? num = null)

Search Google Scholar

Search Google Scholar for scholarly articles.  Each result ships with its doc ``id``, ``type`` badge ([BOOK]/[PDF]/...), wrapped ``inline_links`` (versions + cited_by + related), PDF ``resources`` list, and structured ``authors`` (with ``author_id`` for profiled authors — pipe straight into ``/scholar/author``). Envelope carries ``scholar_results`` alias (Scrapingdog parity), ``related_searches``, and matched ``profiles`` cards.

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
    public class GoogleSearchGoogleScholarExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query for scholarly articles
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var asYlo = 56;  // int? | Year from (e.g. 2020) (optional) 
            var asYhi = 56;  // int? | Year to (e.g. 2024) (optional) 
            var asSdt = "\"0\"";  // string | Search type: 0=exclude patents, 7=include (optional)  (default to "0")
            var page = 0;  // int? | Page number (0-based) (optional)  (default to 0)
            var num = 10;  // int? | Results per page (max 20) (optional)  (default to 10)

            try
            {
                // Search Google Scholar
                Object result = apiInstance.GoogleSearchGoogleScholar(q, hl, asYlo, asYhi, asSdt, page, num);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleScholar: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleScholarWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google Scholar
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleScholarWithHttpInfo(q, hl, asYlo, asYhi, asSdt, page, num);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleScholarWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query for scholarly articles |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **asYlo** | **int?** | Year from (e.g. 2020) | [optional]  |
| **asYhi** | **int?** | Year to (e.g. 2024) | [optional]  |
| **asSdt** | **string** | Search type: 0&#x3D;exclude patents, 7&#x3D;include | [optional] [default to &quot;0&quot;] |
| **page** | **int?** | Page number (0-based) | [optional] [default to 0] |
| **num** | **int?** | Results per page (max 20) | [optional] [default to 10] |

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

<a id="googlesearchgooglevideos"></a>
# **GoogleSearchGoogleVideos**
> Object GoogleSearchGoogleVideos (string q, string gl = null, string hl = null, string tbs = null, string safe = null, int? page = null)

Search Google Videos

Search Google for video results.

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
    public class GoogleSearchGoogleVideosExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Video search query
            var gl = "\"us\"";  // string | Country code (optional)  (default to "us")
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var tbs = "tbs_example";  // string | Time filter (e.g. qdr:d) (optional) 
            var safe = "\"off\"";  // string | Safe search (optional)  (default to "off")
            var page = 0;  // int? | Page number (optional)  (default to 0)

            try
            {
                // Search Google Videos
                Object result = apiInstance.GoogleSearchGoogleVideos(q, gl, hl, tbs, safe, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleVideos: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchGoogleVideosWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Google Videos
    ApiResponse<Object> response = apiInstance.GoogleSearchGoogleVideosWithHttpInfo(q, gl, hl, tbs, safe, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchGoogleVideosWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Video search query |  |
| **gl** | **string** | Country code | [optional] [default to &quot;us&quot;] |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **tbs** | **string** | Time filter (e.g. qdr:d) | [optional]  |
| **safe** | **string** | Safe search | [optional] [default to &quot;off&quot;] |
| **page** | **int?** | Page number | [optional] [default to 0] |

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

<a id="googlesearchhotels"></a>
# **GoogleSearchHotels**
> Object GoogleSearchHotels (string q, string checkIn, string checkOut, int? adults = null, string currency = null, string gl = null)

Search hotels

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
    public class GoogleSearchHotelsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Location or hotel name
            var checkIn = "checkIn_example";  // string | YYYY-MM-DD
            var checkOut = "checkOut_example";  // string | YYYY-MM-DD
            var adults = 2;  // int? |  (optional)  (default to 2)
            var currency = "\"USD\"";  // string |  (optional)  (default to "USD")
            var gl = "\"us\"";  // string |  (optional)  (default to "us")

            try
            {
                // Search hotels
                Object result = apiInstance.GoogleSearchHotels(q, checkIn, checkOut, adults, currency, gl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchHotels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchHotelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search hotels
    ApiResponse<Object> response = apiInstance.GoogleSearchHotelsWithHttpInfo(q, checkIn, checkOut, adults, currency, gl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchHotelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Location or hotel name |  |
| **checkIn** | **string** | YYYY-MM-DD |  |
| **checkOut** | **string** | YYYY-MM-DD |  |
| **adults** | **int?** |  | [optional] [default to 2] |
| **currency** | **string** |  | [optional] [default to &quot;USD&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |

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

<a id="googlesearchpatents"></a>
# **GoogleSearchPatents**
> Object GoogleSearchPatents (string q, int? page = null, int? num = null, string sort = null, string inventor = null, string assignee = null, string country = null, string language = null, string status = null, string patentType = null, string before = null, string after = null)

Search patents

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
    public class GoogleSearchPatentsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Search query (Boolean logic supported)
            var page = 0;  // int? |  (optional)  (default to 0)
            var num = 10;  // int? |  (optional)  (default to 10)
            var sort = "sort_example";  // string | 'new' or 'old' (optional) 
            var inventor = "inventor_example";  // string | Inventor name(s) (optional) 
            var assignee = "assignee_example";  // string | Assignee / company name(s) (optional) 
            var country = "country_example";  // string | Country code (US, EP, WO, …) (optional) 
            var language = "language_example";  // string | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH (optional) 
            var status = "status_example";  // string | GRANT or APPLICATION (optional) 
            var patentType = "patentType_example";  // string | PATENT or DESIGN (optional) 
            var before = "before_example";  // string | Before date YYYYMMDD (optional) 
            var after = "after_example";  // string | After date YYYYMMDD (optional) 

            try
            {
                // Search patents
                Object result = apiInstance.GoogleSearchPatents(q, page, num, sort, inventor, assignee, country, language, status, patentType, before, after);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchPatents: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchPatentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search patents
    ApiResponse<Object> response = apiInstance.GoogleSearchPatentsWithHttpInfo(q, page, num, sort, inventor, assignee, country, language, status, patentType, before, after);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchPatentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Search query (Boolean logic supported) |  |
| **page** | **int?** |  | [optional] [default to 0] |
| **num** | **int?** |  | [optional] [default to 10] |
| **sort** | **string** | &#39;new&#39; or &#39;old&#39; | [optional]  |
| **inventor** | **string** | Inventor name(s) | [optional]  |
| **assignee** | **string** | Assignee / company name(s) | [optional]  |
| **country** | **string** | Country code (US, EP, WO, …) | [optional]  |
| **language** | **string** | Patent language: ENGLISH, GERMAN, CHINESE, FRENCH, JAPANESE, KOREAN, SPANISH | [optional]  |
| **status** | **string** | GRANT or APPLICATION | [optional]  |
| **patentType** | **string** | PATENT or DESIGN | [optional]  |
| **before** | **string** | Before date YYYYMMDD | [optional]  |
| **after** | **string** | After date YYYYMMDD | [optional]  |

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

<a id="googlesearchproducts"></a>
# **GoogleSearchProducts**
> Object GoogleSearchProducts (string q, string gl = null, int? minPrice = null, int? maxPrice = null, string sortBy = null)

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
    public class GoogleSearchProductsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Product search query
            var gl = "\"us\"";  // string |  (optional)  (default to "us")
            var minPrice = 56;  // int? |  (optional) 
            var maxPrice = 56;  // int? |  (optional) 
            var sortBy = "sortBy_example";  // string |  (optional) 

            try
            {
                // Search products
                Object result = apiInstance.GoogleSearchProducts(q, gl, minPrice, maxPrice, sortBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchProducts: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchProductsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search products
    ApiResponse<Object> response = apiInstance.GoogleSearchProductsWithHttpInfo(q, gl, minPrice, maxPrice, sortBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchProductsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Product search query |  |
| **gl** | **string** |  | [optional] [default to &quot;us&quot;] |
| **minPrice** | **int?** |  | [optional]  |
| **maxPrice** | **int?** |  | [optional]  |
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

<a id="googlesearchscholarauthorprofiles"></a>
# **GoogleSearchScholarAuthorProfiles**
> Object GoogleSearchScholarAuthorProfiles (string mauthors, string hl = null, string afterAuthor = null, string beforeAuthor = null)

Search Scholar author profiles

Search Google Scholar for author profiles by name.

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
    public class GoogleSearchScholarAuthorProfilesExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var mauthors = "mauthors_example";  // string | Author name query (e.g. 'Geoffrey Hinton')
            var hl = "\"en\"";  // string | Language code (optional)  (default to "en")
            var afterAuthor = "afterAuthor_example";  // string | Pagination token (next page) (optional) 
            var beforeAuthor = "beforeAuthor_example";  // string | Pagination token (previous page) (optional) 

            try
            {
                // Search Scholar author profiles
                Object result = apiInstance.GoogleSearchScholarAuthorProfiles(mauthors, hl, afterAuthor, beforeAuthor);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleSearchScholarAuthorProfiles: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleSearchScholarAuthorProfilesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Scholar author profiles
    ApiResponse<Object> response = apiInstance.GoogleSearchScholarAuthorProfilesWithHttpInfo(mauthors, hl, afterAuthor, beforeAuthor);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleSearchScholarAuthorProfilesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **mauthors** | **string** | Author name query (e.g. &#39;Geoffrey Hinton&#39;) |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en&quot;] |
| **afterAuthor** | **string** | Pagination token (next page) | [optional]  |
| **beforeAuthor** | **string** | Pagination token (previous page) | [optional]  |

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

<a id="googletrendingnews"></a>
# **GoogleTrendingNews**
> Object GoogleTrendingNews (string hl = null, string gl = null, int? maxResults = null)

Trending news

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
    public class GoogleTrendingNewsExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var hl = "\"en\"";  // string |  (optional)  (default to "en")
            var gl = "\"US\"";  // string |  (optional)  (default to "US")
            var maxResults = 10;  // int? |  (optional)  (default to 10)

            try
            {
                // Trending news
                Object result = apiInstance.GoogleTrendingNews(hl, gl, maxResults);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleTrendingNews: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleTrendingNewsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trending news
    ApiResponse<Object> response = apiInstance.GoogleTrendingNewsWithHttpInfo(hl, gl, maxResults);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleTrendingNewsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **hl** | **string** |  | [optional] [default to &quot;en&quot;] |
| **gl** | **string** |  | [optional] [default to &quot;US&quot;] |
| **maxResults** | **int?** |  | [optional] [default to 10] |

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

<a id="googletrendingsearches"></a>
# **GoogleTrendingSearches**
> Object GoogleTrendingSearches (string geo = null)

Trending searches

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
    public class GoogleTrendingSearchesExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var geo = "\"US\"";  // string |  (optional)  (default to "US")

            try
            {
                // Trending searches
                Object result = apiInstance.GoogleTrendingSearches(geo);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleTrendingSearches: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleTrendingSearchesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trending searches
    ApiResponse<Object> response = apiInstance.GoogleTrendingSearchesWithHttpInfo(geo);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleTrendingSearchesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **geo** | **string** |  | [optional] [default to &quot;US&quot;] |

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

<a id="googletrendstopicautocomplete"></a>
# **GoogleTrendsTopicAutocomplete**
> Object GoogleTrendsTopicAutocomplete (string q, string hl = null, string tz = null)

Trends topic autocomplete

Return categorized Knowledge Graph topic entities (mid, type) for a query.

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
    public class GoogleTrendsTopicAutocompleteExample
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
            var apiInstance = new GoogleApi(httpClient, config, httpClientHandler);
            var q = "q_example";  // string | Query prefix to resolve into Trends topics
            var hl = "\"en-US\"";  // string | Language code (optional)  (default to "en-US")
            var tz = "\"0\"";  // string | Timezone offset in minutes (optional)  (default to "0")

            try
            {
                // Trends topic autocomplete
                Object result = apiInstance.GoogleTrendsTopicAutocomplete(q, hl, tz);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GoogleApi.GoogleTrendsTopicAutocomplete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GoogleTrendsTopicAutocompleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Trends topic autocomplete
    ApiResponse<Object> response = apiInstance.GoogleTrendsTopicAutocompleteWithHttpInfo(q, hl, tz);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GoogleApi.GoogleTrendsTopicAutocompleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **q** | **string** | Query prefix to resolve into Trends topics |  |
| **hl** | **string** | Language code | [optional] [default to &quot;en-US&quot;] |
| **tz** | **string** | Timezone offset in minutes | [optional] [default to &quot;0&quot;] |

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

