# ScrapeBadger.Api.GeminiApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GeminiAskGeminiAQuestion**](GeminiApi.md#geminiaskgeminiaquestion) | **GET** /v1/gemini/ask | Ask Gemini a question |
| [**GeminiAskGeminiAQuestionPost**](GeminiApi.md#geminiaskgeminiaquestionpost) | **POST** /v1/gemini/ask | Ask Gemini a question (POST) |
| [**GeminiGeminiScraperHealthCheck**](GeminiApi.md#geminigeminiscraperhealthcheck) | **GET** /v1/gemini/health | Gemini scraper health check |
| [**GeminiGeminiScraperHealthCheckHead**](GeminiApi.md#geminigeminiscraperhealthcheckhead) | **HEAD** /v1/gemini/health | Gemini scraper health check |
| [**GeminiMeasureABrandSVisibilityInAGeminiAnswer**](GeminiApi.md#geminimeasureabrandsvisibilityinageminianswer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer |
| [**GeminiMeasureABrandSVisibilityInAGeminiAnswerPost**](GeminiApi.md#geminimeasureabrandsvisibilityinageminianswerpost) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST) |

<a id="geminiaskgeminiaquestion"></a>
# **GeminiAskGeminiAQuestion**
> Object GeminiAskGeminiAQuestion (string prompt, string country = null, string webSearch = null, string imageUrl = null)

Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

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
    public class GeminiAskGeminiAQuestionExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to send to Gemini (max 4096 characters).
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional) 
            var webSearch = "\"auto\"";  // string | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. (optional)  (default to "auto")
            var imageUrl = "imageUrl_example";  // string | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts `image_base64`. Exactly one of the two. (optional) 

            try
            {
                // Ask Gemini a question
                Object result = apiInstance.GeminiAskGeminiAQuestion(prompt, country, webSearch, imageUrl);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiAskGeminiAQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiAskGeminiAQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Gemini a question
    ApiResponse<Object> response = apiInstance.GeminiAskGeminiAQuestionWithHttpInfo(prompt, country, webSearch, imageUrl);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiAskGeminiAQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to send to Gemini (max 4096 characters). |  |
| **country** | **string** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional]  |
| **webSearch** | **string** | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &quot;auto&quot;] |
| **imageUrl** | **string** | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts &#x60;image_base64&#x60;. Exactly one of the two. | [optional]  |

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

<a id="geminiaskgeminiaquestionpost"></a>
# **GeminiAskGeminiAQuestionPost**
> Object GeminiAskGeminiAQuestionPost ()

Ask Gemini a question (POST)

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
    public class GeminiAskGeminiAQuestionPostExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);

            try
            {
                // Ask Gemini a question (POST)
                Object result = apiInstance.GeminiAskGeminiAQuestionPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiAskGeminiAQuestionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiAskGeminiAQuestionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask Gemini a question (POST)
    ApiResponse<Object> response = apiInstance.GeminiAskGeminiAQuestionPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiAskGeminiAQuestionPostWithHttpInfo: " + e.Message);
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

<a id="geminigeminiscraperhealthcheck"></a>
# **GeminiGeminiScraperHealthCheck**
> Object GeminiGeminiScraperHealthCheck ()

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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
    public class GeminiGeminiScraperHealthCheckExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);

            try
            {
                // Gemini scraper health check
                Object result = apiInstance.GeminiGeminiScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiGeminiScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiGeminiScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gemini scraper health check
    ApiResponse<Object> response = apiInstance.GeminiGeminiScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiGeminiScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="geminigeminiscraperhealthcheckhead"></a>
# **GeminiGeminiScraperHealthCheckHead**
> Object GeminiGeminiScraperHealthCheckHead ()

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

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
    public class GeminiGeminiScraperHealthCheckHeadExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);

            try
            {
                // Gemini scraper health check
                Object result = apiInstance.GeminiGeminiScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiGeminiScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiGeminiScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gemini scraper health check
    ApiResponse<Object> response = apiInstance.GeminiGeminiScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiGeminiScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="geminimeasureabrandsvisibilityinageminianswer"></a>
# **GeminiMeasureABrandSVisibilityInAGeminiAnswer**
> Object GeminiMeasureABrandSVisibilityInAGeminiAnswer (string prompt, string brand, string domain = null, string aliases = null, string competitors = null, string country = null, string webSearch = null)

Measure a brand's visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

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
    public class GeminiMeasureABrandSVisibilityInAGeminiAnswerExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to ask Gemini.
            var brand = "brand_example";  // string | Brand name to look for in the answer.
            var domain = "domain_example";  // string | Brand domain, for citation matching. (optional) 
            var aliases = "aliases_example";  // string | Comma-separated alternative names. (optional) 
            var competitors = "competitors_example";  // string | Comma-separated competitor names. (optional) 
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country. (optional) 
            var webSearch = "\"force\"";  // string | auto | force | off (optional)  (default to "force")

            try
            {
                // Measure a brand's visibility in a Gemini answer
                Object result = apiInstance.GeminiMeasureABrandSVisibilityInAGeminiAnswer(prompt, brand, domain, aliases, competitors, country, webSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiMeasureABrandSVisibilityInAGeminiAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiMeasureABrandSVisibilityInAGeminiAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Gemini answer
    ApiResponse<Object> response = apiInstance.GeminiMeasureABrandSVisibilityInAGeminiAnswerWithHttpInfo(prompt, brand, domain, aliases, competitors, country, webSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiMeasureABrandSVisibilityInAGeminiAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to ask Gemini. |  |
| **brand** | **string** | Brand name to look for in the answer. |  |
| **domain** | **string** | Brand domain, for citation matching. | [optional]  |
| **aliases** | **string** | Comma-separated alternative names. | [optional]  |
| **competitors** | **string** | Comma-separated competitor names. | [optional]  |
| **country** | **string** | ISO-3166 alpha-2 egress country. | [optional]  |
| **webSearch** | **string** | auto | force | off | [optional] [default to &quot;force&quot;] |

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

<a id="geminimeasureabrandsvisibilityinageminianswerpost"></a>
# **GeminiMeasureABrandSVisibilityInAGeminiAnswerPost**
> Object GeminiMeasureABrandSVisibilityInAGeminiAnswerPost ()

Measure a brand's visibility in a Gemini answer (POST)

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
    public class GeminiMeasureABrandSVisibilityInAGeminiAnswerPostExample
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
            var apiInstance = new GeminiApi(httpClient, config, httpClientHandler);

            try
            {
                // Measure a brand's visibility in a Gemini answer (POST)
                Object result = apiInstance.GeminiMeasureABrandSVisibilityInAGeminiAnswerPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GeminiApi.GeminiMeasureABrandSVisibilityInAGeminiAnswerPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GeminiMeasureABrandSVisibilityInAGeminiAnswerPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a Gemini answer (POST)
    ApiResponse<Object> response = apiInstance.GeminiMeasureABrandSVisibilityInAGeminiAnswerPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GeminiApi.GeminiMeasureABrandSVisibilityInAGeminiAnswerPostWithHttpInfo: " + e.Message);
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

