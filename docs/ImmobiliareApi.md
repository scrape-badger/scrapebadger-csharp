# ScrapeBadger.Api.ImmobiliareApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ImmobiliareGetAgencyProfile**](ImmobiliareApi.md#immobiliaregetagencyprofile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile |
| [**ImmobiliareGetAnAgencySListings**](ImmobiliareApi.md#immobiliaregetanagencyslistings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings |
| [**ImmobiliareGetListingDetail**](ImmobiliareApi.md#immobiliaregetlistingdetail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail |
| [**ImmobiliareImmobiliareScraperHealthCheck**](ImmobiliareApi.md#immobiliareimmobiliarescraperhealthcheck) | **GET** /v1/immobiliare/health | Immobiliare scraper health check |
| [**ImmobiliareImmobiliareScraperHealthCheckHead**](ImmobiliareApi.md#immobiliareimmobiliarescraperhealthcheckhead) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check |
| [**ImmobiliareListFilterEnums**](ImmobiliareApi.md#immobiliarelistfilterenums) | **GET** /v1/immobiliare/reference | List filter enums |
| [**ImmobiliareListMarkets**](ImmobiliareApi.md#immobiliarelistmarkets) | **GET** /v1/immobiliare/markets | List markets |
| [**ImmobiliareLocationAutocomplete**](ImmobiliareApi.md#immobiliarelocationautocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete |
| [**ImmobiliarePriceMTimeSeries**](ImmobiliareApi.md#immobiliarepricemtimeseries) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series |
| [**ImmobiliareSearchListings**](ImmobiliareApi.md#immobiliaresearchlistings) | **GET** /v1/immobiliare/search | Search listings |

<a id="immobiliaregetagencyprofile"></a>
# **ImmobiliareGetAgencyProfile**
> Object ImmobiliareGetAgencyProfile (int agencyId, string market = null)

Get agency profile

Public agency/advertiser profile.

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
    public class ImmobiliareGetAgencyProfileExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var agencyId = 56;  // int | 
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")

            try
            {
                // Get agency profile
                Object result = apiInstance.ImmobiliareGetAgencyProfile(agencyId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetAgencyProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareGetAgencyProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get agency profile
    ApiResponse<Object> response = apiInstance.ImmobiliareGetAgencyProfileWithHttpInfo(agencyId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetAgencyProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agencyId** | **int** |  |  |
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |

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

<a id="immobiliaregetanagencyslistings"></a>
# **ImmobiliareGetAnAgencySListings**
> Object ImmobiliareGetAnAgencySListings (int agencyId, string market = null, string contract = null, int? page = null)

Get an agency's listings

An agency's active listings.

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
    public class ImmobiliareGetAnAgencySListingsExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var agencyId = 56;  // int | 
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")
            var contract = "\"sale\"";  // string | sale | rent (optional)  (default to "sale")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Get an agency's listings
                Object result = apiInstance.ImmobiliareGetAnAgencySListings(agencyId, market, contract, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetAnAgencySListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareGetAnAgencySListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an agency's listings
    ApiResponse<Object> response = apiInstance.ImmobiliareGetAnAgencySListingsWithHttpInfo(agencyId, market, contract, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetAnAgencySListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **agencyId** | **int** |  |  |
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |
| **contract** | **string** | sale | rent | [optional] [default to &quot;sale&quot;] |
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

<a id="immobiliaregetlistingdetail"></a>
# **ImmobiliareGetListingDetail**
> Object ImmobiliareGetListingDetail (int listingId, string market = null)

Get listing detail

Full detail for a single listing.

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
    public class ImmobiliareGetListingDetailExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var listingId = 56;  // int | 
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")

            try
            {
                // Get listing detail
                Object result = apiInstance.ImmobiliareGetListingDetail(listingId, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetListingDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareGetListingDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get listing detail
    ApiResponse<Object> response = apiInstance.ImmobiliareGetListingDetailWithHttpInfo(listingId, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareGetListingDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **listingId** | **int** |  |  |
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |

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

<a id="immobiliareimmobiliarescraperhealthcheck"></a>
# **ImmobiliareImmobiliareScraperHealthCheck**
> Object ImmobiliareImmobiliareScraperHealthCheck ()

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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
    public class ImmobiliareImmobiliareScraperHealthCheckExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);

            try
            {
                // Immobiliare scraper health check
                Object result = apiInstance.ImmobiliareImmobiliareScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareImmobiliareScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareImmobiliareScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Immobiliare scraper health check
    ApiResponse<Object> response = apiInstance.ImmobiliareImmobiliareScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareImmobiliareScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="immobiliareimmobiliarescraperhealthcheckhead"></a>
# **ImmobiliareImmobiliareScraperHealthCheckHead**
> Object ImmobiliareImmobiliareScraperHealthCheckHead ()

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

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
    public class ImmobiliareImmobiliareScraperHealthCheckHeadExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);

            try
            {
                // Immobiliare scraper health check
                Object result = apiInstance.ImmobiliareImmobiliareScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareImmobiliareScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareImmobiliareScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Immobiliare scraper health check
    ApiResponse<Object> response = apiInstance.ImmobiliareImmobiliareScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareImmobiliareScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="immobiliarelistfilterenums"></a>
# **ImmobiliareListFilterEnums**
> Object ImmobiliareListFilterEnums ()

List filter enums

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
    public class ImmobiliareListFilterEnumsExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);

            try
            {
                // List filter enums
                Object result = apiInstance.ImmobiliareListFilterEnums();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareListFilterEnums: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareListFilterEnumsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List filter enums
    ApiResponse<Object> response = apiInstance.ImmobiliareListFilterEnumsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareListFilterEnumsWithHttpInfo: " + e.Message);
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

<a id="immobiliarelistmarkets"></a>
# **ImmobiliareListMarkets**
> Object ImmobiliareListMarkets ()

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
    public class ImmobiliareListMarketsExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);

            try
            {
                // List markets
                Object result = apiInstance.ImmobiliareListMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareListMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareListMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List markets
    ApiResponse<Object> response = apiInstance.ImmobiliareListMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareListMarketsWithHttpInfo: " + e.Message);
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

<a id="immobiliarelocationautocomplete"></a>
# **ImmobiliareLocationAutocomplete**
> Object ImmobiliareLocationAutocomplete (string query, string market = null)

Location autocomplete

Resolve a place name to region/province/city ids usable in search.

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
    public class ImmobiliareLocationAutocompleteExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Free-text place name, e.g. 'Milano'
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")

            try
            {
                // Location autocomplete
                Object result = apiInstance.ImmobiliareLocationAutocomplete(query, market);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareLocationAutocomplete: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareLocationAutocompleteWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Location autocomplete
    ApiResponse<Object> response = apiInstance.ImmobiliareLocationAutocompleteWithHttpInfo(query, market);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareLocationAutocompleteWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Free-text place name, e.g. &#39;Milano&#39; |  |
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |

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

<a id="immobiliarepricemtimeseries"></a>
# **ImmobiliarePriceMTimeSeries**
> Object ImmobiliarePriceMTimeSeries (string regionId, string market = null, string provinceId = null, string cityId = null, string contract = null)

Price €/m² time series

Historical €/m² price statistics for an area.

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
    public class ImmobiliarePriceMTimeSeriesExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var regionId = "regionId_example";  // string | Region id, e.g. 'lom'
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")
            var provinceId = "provinceId_example";  // string | Province id, e.g. 'MI' (optional) 
            var cityId = "cityId_example";  // string | City id (idComune) (optional) 
            var contract = "\"sale\"";  // string | sale | rent (optional)  (default to "sale")

            try
            {
                // Price €/m² time series
                Object result = apiInstance.ImmobiliarePriceMTimeSeries(regionId, market, provinceId, cityId, contract);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliarePriceMTimeSeries: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliarePriceMTimeSeriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Price €/m² time series
    ApiResponse<Object> response = apiInstance.ImmobiliarePriceMTimeSeriesWithHttpInfo(regionId, market, provinceId, cityId, contract);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliarePriceMTimeSeriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **regionId** | **string** | Region id, e.g. &#39;lom&#39; |  |
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |
| **provinceId** | **string** | Province id, e.g. &#39;MI&#39; | [optional]  |
| **cityId** | **string** | City id (idComune) | [optional]  |
| **contract** | **string** | sale | rent | [optional] [default to &quot;sale&quot;] |

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

<a id="immobiliaresearchlistings"></a>
# **ImmobiliareSearchListings**
> Object ImmobiliareSearchListings (string market = null, string location = null, string regionId = null, string provinceId = null, string cityId = null, string contract = null, string category = null, int? priceMin = null, int? priceMax = null, int? surfaceMin = null, int? surfaceMax = null, int? roomsMin = null, int? roomsMax = null, int? bathroomsMin = null, string sort = null, int? page = null)

Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

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
    public class ImmobiliareSearchListingsExample
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
            var apiInstance = new ImmobiliareApi(httpClient, config, httpClientHandler);
            var market = "\"it\"";  // string | it | es | gr | lu (optional)  (default to "it")
            var location = "location_example";  // string | Free-text place (auto-resolved) (optional) 
            var regionId = "regionId_example";  // string | fkRegione (from /autocomplete) (optional) 
            var provinceId = "provinceId_example";  // string | idProvincia (from /autocomplete) (optional) 
            var cityId = "cityId_example";  // string | idComune (from /autocomplete) (optional) 
            var contract = "\"sale\"";  // string | sale | rent (optional)  (default to "sale")
            var category = "\"residential\"";  // string | see /reference (optional)  (default to "residential")
            var priceMin = 56;  // int? |  (optional) 
            var priceMax = 56;  // int? |  (optional) 
            var surfaceMin = 56;  // int? |  (optional) 
            var surfaceMax = 56;  // int? |  (optional) 
            var roomsMin = 56;  // int? |  (optional) 
            var roomsMax = 56;  // int? |  (optional) 
            var bathroomsMin = 56;  // int? |  (optional) 
            var sort = "\"relevance\"";  // string | see /reference (optional)  (default to "relevance")
            var page = 1;  // int? |  (optional)  (default to 1)

            try
            {
                // Search listings
                Object result = apiInstance.ImmobiliareSearchListings(market, location, regionId, provinceId, cityId, contract, category, priceMin, priceMax, surfaceMin, surfaceMax, roomsMin, roomsMax, bathroomsMin, sort, page);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareSearchListings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ImmobiliareSearchListingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search listings
    ApiResponse<Object> response = apiInstance.ImmobiliareSearchListingsWithHttpInfo(market, location, regionId, provinceId, cityId, contract, category, priceMin, priceMax, surfaceMin, surfaceMax, roomsMin, roomsMax, bathroomsMin, sort, page);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ImmobiliareApi.ImmobiliareSearchListingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **market** | **string** | it | es | gr | lu | [optional] [default to &quot;it&quot;] |
| **location** | **string** | Free-text place (auto-resolved) | [optional]  |
| **regionId** | **string** | fkRegione (from /autocomplete) | [optional]  |
| **provinceId** | **string** | idProvincia (from /autocomplete) | [optional]  |
| **cityId** | **string** | idComune (from /autocomplete) | [optional]  |
| **contract** | **string** | sale | rent | [optional] [default to &quot;sale&quot;] |
| **category** | **string** | see /reference | [optional] [default to &quot;residential&quot;] |
| **priceMin** | **int?** |  | [optional]  |
| **priceMax** | **int?** |  | [optional]  |
| **surfaceMin** | **int?** |  | [optional]  |
| **surfaceMax** | **int?** |  | [optional]  |
| **roomsMin** | **int?** |  | [optional]  |
| **roomsMax** | **int?** |  | [optional]  |
| **bathroomsMin** | **int?** |  | [optional]  |
| **sort** | **string** | see /reference | [optional] [default to &quot;relevance&quot;] |
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

