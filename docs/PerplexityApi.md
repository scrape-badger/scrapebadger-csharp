# ScrapeBadger.Api.PerplexityApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**PerplexityAskPerplexityAQuestion**](PerplexityApi.md#perplexityaskperplexityaquestion) | **GET** /v1/perplexity/ask | Ask Perplexity a question |
| [**PerplexityAskPerplexityAQuestionPost**](PerplexityApi.md#perplexityaskperplexityaquestionpost) | **POST** /v1/perplexity/ask | Ask Perplexity a question (POST) |
| [**PerplexityMeasureABrandSVisibilityInAPerplexityAnswer**](PerplexityApi.md#perplexitymeasureabrandsvisibilityinaperplexityanswer) | **GET** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer |
| [**PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**](PerplexityApi.md#perplexitymeasureabrandsvisibilityinaperplexityanswerpost) | **POST** /v1/perplexity/brand-visibility | Measure a brand&#39;s visibility in a Perplexity answer (POST) |
| [**PerplexityPerplexityScraperHealthCheck**](PerplexityApi.md#perplexityperplexityscraperhealthcheck) | **GET** /v1/perplexity/health | Perplexity scraper health check |
| [**PerplexityPerplexityScraperHealthCheckHead**](PerplexityApi.md#perplexityperplexityscraperhealthcheckhead) | **HEAD** /v1/perplexity/health | Perplexity scraper health check |

<a id="perplexityaskperplexityaquestion"></a>
# **PerplexityAskPerplexityAQuestion**
> Object PerplexityAskPerplexityAQuestion (string prompt, string country = null)

Ask Perplexity a question

Send a prompt to Perplexity and get the answer plus the web sources it cited.

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
    public class PerplexityAskPerplexityAQuestionExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to send to Perplexity (max 4096 characters).
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional) 

            try
            {
                // Ask Perplexity a question
                Object result = apiInstance.PerplexityAskPerplexityAQuestion(prompt, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityAskPerplexityAQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityAskPerplexityAQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Perplexity a question
    ApiResponse<Object> response = apiInstance.PerplexityAskPerplexityAQuestionWithHttpInfo(prompt, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityAskPerplexityAQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to send to Perplexity (max 4096 characters). |  |
| **country** | **string** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional]  |

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

<a id="perplexityaskperplexityaquestionpost"></a>
# **PerplexityAskPerplexityAQuestionPost**
> Object PerplexityAskPerplexityAQuestionPost ()

Ask Perplexity a question (POST)

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
    public class PerplexityAskPerplexityAQuestionPostExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);

            try
            {
                // Ask Perplexity a question (POST)
                Object result = apiInstance.PerplexityAskPerplexityAQuestionPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityAskPerplexityAQuestionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityAskPerplexityAQuestionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Perplexity a question (POST)
    ApiResponse<Object> response = apiInstance.PerplexityAskPerplexityAQuestionPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityAskPerplexityAQuestionPostWithHttpInfo: " + e.Message);
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

<a id="perplexitymeasureabrandsvisibilityinaperplexityanswer"></a>
# **PerplexityMeasureABrandSVisibilityInAPerplexityAnswer**
> Object PerplexityMeasureABrandSVisibilityInAPerplexityAnswer (string prompt, string brand, string domain = null, string aliases = null, string competitors = null, string country = null)

Measure a brand's visibility in a Perplexity answer

Ask Perplexity, then report whether the brand is mentioned, cited and how prominently.

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
    public class PerplexityMeasureABrandSVisibilityInAPerplexityAnswerExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to ask Perplexity.
            var brand = "brand_example";  // string | Brand name to look for in the answer.
            var domain = "domain_example";  // string | Brand domain, for citation matching. (optional) 
            var aliases = "aliases_example";  // string | Comma-separated alternative names. (optional) 
            var competitors = "competitors_example";  // string | Comma-separated competitor names. (optional) 
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country. (optional) 

            try
            {
                // Measure a brand's visibility in a Perplexity answer
                Object result = apiInstance.PerplexityMeasureABrandSVisibilityInAPerplexityAnswer(prompt, brand, domain, aliases, competitors, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityMeasureABrandSVisibilityInAPerplexityAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityMeasureABrandSVisibilityInAPerplexityAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Perplexity answer
    ApiResponse<Object> response = apiInstance.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerWithHttpInfo(prompt, brand, domain, aliases, competitors, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to ask Perplexity. |  |
| **brand** | **string** | Brand name to look for in the answer. |  |
| **domain** | **string** | Brand domain, for citation matching. | [optional]  |
| **aliases** | **string** | Comma-separated alternative names. | [optional]  |
| **competitors** | **string** | Comma-separated competitor names. | [optional]  |
| **country** | **string** | ISO-3166 alpha-2 egress country. | [optional]  |

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

<a id="perplexitymeasureabrandsvisibilityinaperplexityanswerpost"></a>
# **PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPost**
> Object PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPost ()

Measure a brand's visibility in a Perplexity answer (POST)

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
    public class PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPostExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);

            try
            {
                // Measure a brand's visibility in a Perplexity answer (POST)
                Object result = apiInstance.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Perplexity answer (POST)
    ApiResponse<Object> response = apiInstance.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityMeasureABrandSVisibilityInAPerplexityAnswerPostWithHttpInfo: " + e.Message);
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

<a id="perplexityperplexityscraperhealthcheck"></a>
# **PerplexityPerplexityScraperHealthCheck**
> Object PerplexityPerplexityScraperHealthCheck ()

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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
    public class PerplexityPerplexityScraperHealthCheckExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);

            try
            {
                // Perplexity scraper health check
                Object result = apiInstance.PerplexityPerplexityScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityPerplexityScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityPerplexityScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perplexity scraper health check
    ApiResponse<Object> response = apiInstance.PerplexityPerplexityScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityPerplexityScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="perplexityperplexityscraperhealthcheckhead"></a>
# **PerplexityPerplexityScraperHealthCheckHead**
> Object PerplexityPerplexityScraperHealthCheckHead ()

Perplexity scraper health check

Check health of the Perplexity scraper service (accepts HEAD).

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
    public class PerplexityPerplexityScraperHealthCheckHeadExample
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
            var apiInstance = new PerplexityApi(httpClient, config, httpClientHandler);

            try
            {
                // Perplexity scraper health check
                Object result = apiInstance.PerplexityPerplexityScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PerplexityApi.PerplexityPerplexityScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PerplexityPerplexityScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Perplexity scraper health check
    ApiResponse<Object> response = apiInstance.PerplexityPerplexityScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PerplexityApi.PerplexityPerplexityScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

