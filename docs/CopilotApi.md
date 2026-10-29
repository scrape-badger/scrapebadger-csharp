# ScrapeBadger.Api.CopilotApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CopilotAskCopilotAQuestion**](CopilotApi.md#copilotaskcopilotaquestion) | **GET** /v1/copilot/ask | Ask Copilot a question |
| [**CopilotAskCopilotAQuestionPost**](CopilotApi.md#copilotaskcopilotaquestionpost) | **POST** /v1/copilot/ask | Ask Copilot a question (POST) |
| [**CopilotCopilotScraperHealthCheck**](CopilotApi.md#copilotcopilotscraperhealthcheck) | **GET** /v1/copilot/health | Copilot scraper health check |
| [**CopilotCopilotScraperHealthCheckHead**](CopilotApi.md#copilotcopilotscraperhealthcheckhead) | **HEAD** /v1/copilot/health | Copilot scraper health check |
| [**CopilotListCopilotMarkets**](CopilotApi.md#copilotlistcopilotmarkets) | **GET** /v1/copilot/markets | List Copilot markets |
| [**CopilotMeasureABrandSVisibilityInACopilotAnswer**](CopilotApi.md#copilotmeasureabrandsvisibilityinacopilotanswer) | **GET** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer |
| [**CopilotMeasureABrandSVisibilityInACopilotAnswerPost**](CopilotApi.md#copilotmeasureabrandsvisibilityinacopilotanswerpost) | **POST** /v1/copilot/brand-visibility | Measure a brand&#39;s visibility in a Copilot answer (POST) |

<a id="copilotaskcopilotaquestion"></a>
# **CopilotAskCopilotAQuestion**
> Object CopilotAskCopilotAQuestion (string prompt, string country = null, string market = null, bool? strictCountry = null)

Ask Copilot a question

Ask Microsoft Copilot (Copilot Search in Bing) and get the answer plus its cited sources.

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
    public class CopilotAskCopilotAQuestionExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to send to Copilot (max 2000 characters).
            var country = "country_example";  // string | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. (optional) 
            var market = "market_example";  // string | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. (optional) 
            var strictCountry = false;  // bool? | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. (optional)  (default to false)

            try
            {
                // Ask Copilot a question
                Object result = apiInstance.CopilotAskCopilotAQuestion(prompt, country, market, strictCountry);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotAskCopilotAQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotAskCopilotAQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Copilot a question
    ApiResponse<Object> response = apiInstance.CopilotAskCopilotAQuestionWithHttpInfo(prompt, country, market, strictCountry);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotAskCopilotAQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to send to Copilot (max 2000 characters). |  |
| **country** | **string** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional]  |
| **market** | **string** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional]  |
| **strictCountry** | **bool?** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

<a id="copilotaskcopilotaquestionpost"></a>
# **CopilotAskCopilotAQuestionPost**
> Object CopilotAskCopilotAQuestionPost ()

Ask Copilot a question (POST)

POST form of `/ask`, for prompts too long for a query string.

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
    public class CopilotAskCopilotAQuestionPostExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);

            try
            {
                // Ask Copilot a question (POST)
                Object result = apiInstance.CopilotAskCopilotAQuestionPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotAskCopilotAQuestionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotAskCopilotAQuestionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Copilot a question (POST)
    ApiResponse<Object> response = apiInstance.CopilotAskCopilotAQuestionPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotAskCopilotAQuestionPostWithHttpInfo: " + e.Message);
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

<a id="copilotcopilotscraperhealthcheck"></a>
# **CopilotCopilotScraperHealthCheck**
> Object CopilotCopilotScraperHealthCheck ()

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

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
    public class CopilotCopilotScraperHealthCheckExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);

            try
            {
                // Copilot scraper health check
                Object result = apiInstance.CopilotCopilotScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotCopilotScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotCopilotScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Copilot scraper health check
    ApiResponse<Object> response = apiInstance.CopilotCopilotScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotCopilotScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="copilotcopilotscraperhealthcheckhead"></a>
# **CopilotCopilotScraperHealthCheckHead**
> Object CopilotCopilotScraperHealthCheckHead ()

Copilot scraper health check

Check health of the Copilot scraper service (accepts HEAD).

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
    public class CopilotCopilotScraperHealthCheckHeadExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);

            try
            {
                // Copilot scraper health check
                Object result = apiInstance.CopilotCopilotScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotCopilotScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotCopilotScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Copilot scraper health check
    ApiResponse<Object> response = apiInstance.CopilotCopilotScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotCopilotScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="copilotlistcopilotmarkets"></a>
# **CopilotListCopilotMarkets**
> Object CopilotListCopilotMarkets ()

List Copilot markets

The Bing markets Copilot can be asked in.

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
    public class CopilotListCopilotMarketsExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);

            try
            {
                // List Copilot markets
                Object result = apiInstance.CopilotListCopilotMarkets();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotListCopilotMarkets: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotListCopilotMarketsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List Copilot markets
    ApiResponse<Object> response = apiInstance.CopilotListCopilotMarketsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotListCopilotMarketsWithHttpInfo: " + e.Message);
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

<a id="copilotmeasureabrandsvisibilityinacopilotanswer"></a>
# **CopilotMeasureABrandSVisibilityInACopilotAnswer**
> Object CopilotMeasureABrandSVisibilityInACopilotAnswer (string prompt, string brand, string domain = null, string aliases = null, string competitors = null, string country = null, string market = null, bool? strictCountry = null)

Measure a brand's visibility in a Copilot answer

Ask Copilot, then report whether the brand is mentioned, cited and how prominently.

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
    public class CopilotMeasureABrandSVisibilityInACopilotAnswerExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to ask Copilot.
            var brand = "brand_example";  // string | Brand name to look for in the answer.
            var domain = "domain_example";  // string | Brand domain, for citation matching. (optional) 
            var aliases = "aliases_example";  // string | Comma-separated alternative names. (optional) 
            var competitors = "competitors_example";  // string | Comma-separated competitor names. (optional) 
            var country = "country_example";  // string | ISO-3166 alpha-2 country to ask from, e.g. 'JP', 'US', 'GB'. Unless `market` is set, Copilot also answers in that country's market. (optional) 
            var market = "market_example";  // string | Bing market (language-COUNTRY), e.g. 'ja-JP', 'en-GB'. Defaults to the country's. (optional) 
            var strictCountry = false;  // bool? | Answer only from an exit in `country`, never another one; 503 `country_unavailable` (not billed) when none answers. Requires `country`. (optional)  (default to false)

            try
            {
                // Measure a brand's visibility in a Copilot answer
                Object result = apiInstance.CopilotMeasureABrandSVisibilityInACopilotAnswer(prompt, brand, domain, aliases, competitors, country, market, strictCountry);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotMeasureABrandSVisibilityInACopilotAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotMeasureABrandSVisibilityInACopilotAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Copilot answer
    ApiResponse<Object> response = apiInstance.CopilotMeasureABrandSVisibilityInACopilotAnswerWithHttpInfo(prompt, brand, domain, aliases, competitors, country, market, strictCountry);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotMeasureABrandSVisibilityInACopilotAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to ask Copilot. |  |
| **brand** | **string** | Brand name to look for in the answer. |  |
| **domain** | **string** | Brand domain, for citation matching. | [optional]  |
| **aliases** | **string** | Comma-separated alternative names. | [optional]  |
| **competitors** | **string** | Comma-separated competitor names. | [optional]  |
| **country** | **string** | ISO-3166 alpha-2 country to ask from, e.g. &#39;JP&#39;, &#39;US&#39;, &#39;GB&#39;. Unless &#x60;market&#x60; is set, Copilot also answers in that country&#39;s market. | [optional]  |
| **market** | **string** | Bing market (language-COUNTRY), e.g. &#39;ja-JP&#39;, &#39;en-GB&#39;. Defaults to the country&#39;s. | [optional]  |
| **strictCountry** | **bool?** | Answer only from an exit in &#x60;country&#x60;, never another one; 503 &#x60;country_unavailable&#x60; (not billed) when none answers. Requires &#x60;country&#x60;. | [optional] [default to false] |

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

<a id="copilotmeasureabrandsvisibilityinacopilotanswerpost"></a>
# **CopilotMeasureABrandSVisibilityInACopilotAnswerPost**
> Object CopilotMeasureABrandSVisibilityInACopilotAnswerPost ()

Measure a brand's visibility in a Copilot answer (POST)

POST form, for longer prompts and larger competitor sets.

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
    public class CopilotMeasureABrandSVisibilityInACopilotAnswerPostExample
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
            var apiInstance = new CopilotApi(httpClient, config, httpClientHandler);

            try
            {
                // Measure a brand's visibility in a Copilot answer (POST)
                Object result = apiInstance.CopilotMeasureABrandSVisibilityInACopilotAnswerPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CopilotApi.CopilotMeasureABrandSVisibilityInACopilotAnswerPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CopilotMeasureABrandSVisibilityInACopilotAnswerPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Copilot answer (POST)
    ApiResponse<Object> response = apiInstance.CopilotMeasureABrandSVisibilityInACopilotAnswerPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CopilotApi.CopilotMeasureABrandSVisibilityInACopilotAnswerPostWithHttpInfo: " + e.Message);
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

