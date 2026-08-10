# ScrapeBadger.Api.ChatGPTApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ChatgptAskChatgptAQuestion**](ChatGPTApi.md#chatgptaskchatgptaquestion) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question |
| [**ChatgptAskChatgptAQuestionPost**](ChatGPTApi.md#chatgptaskchatgptaquestionpost) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST) |
| [**ChatgptChatgptScraperHealthCheck**](ChatGPTApi.md#chatgptchatgptscraperhealthcheck) | **GET** /v1/chatgpt/health | ChatGPT scraper health check |
| [**ChatgptChatgptScraperHealthCheckHead**](ChatGPTApi.md#chatgptchatgptscraperhealthcheckhead) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check |
| [**ChatgptListChatgptModels**](ChatGPTApi.md#chatgptlistchatgptmodels) | **GET** /v1/chatgpt/models | List ChatGPT models |
| [**ChatgptMeasureABrandSVisibilityInAChatgptAnswer**](ChatGPTApi.md#chatgptmeasureabrandsvisibilityinachatgptanswer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer |
| [**ChatgptMeasureABrandSVisibilityInAChatgptAnswerPost**](ChatGPTApi.md#chatgptmeasureabrandsvisibilityinachatgptanswerpost) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST) |

<a id="chatgptaskchatgptaquestion"></a>
# **ChatgptAskChatgptAQuestion**
> Object ChatgptAskChatgptAQuestion (string prompt, string country = null, string webSearch = null)

Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

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
    public class ChatgptAskChatgptAQuestionExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to send to ChatGPT (max 4096 characters).
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'. (optional) 
            var webSearch = "\"auto\"";  // string | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened. (optional)  (default to "auto")

            try
            {
                // Ask ChatGPT a question
                Object result = apiInstance.ChatgptAskChatgptAQuestion(prompt, country, webSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptAskChatgptAQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptAskChatgptAQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask ChatGPT a question
    ApiResponse<Object> response = apiInstance.ChatgptAskChatgptAQuestionWithHttpInfo(prompt, country, webSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptAskChatgptAQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to send to ChatGPT (max 4096 characters). |  |
| **country** | **string** | ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional]  |
| **webSearch** | **string** | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to &quot;auto&quot;] |

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

<a id="chatgptaskchatgptaquestionpost"></a>
# **ChatgptAskChatgptAQuestionPost**
> Object ChatgptAskChatgptAQuestionPost ()

Ask ChatGPT a question (POST)

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
    public class ChatgptAskChatgptAQuestionPostExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);

            try
            {
                // Ask ChatGPT a question (POST)
                Object result = apiInstance.ChatgptAskChatgptAQuestionPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptAskChatgptAQuestionPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptAskChatgptAQuestionPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Ask ChatGPT a question (POST)
    ApiResponse<Object> response = apiInstance.ChatgptAskChatgptAQuestionPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptAskChatgptAQuestionPostWithHttpInfo: " + e.Message);
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

<a id="chatgptchatgptscraperhealthcheck"></a>
# **ChatgptChatgptScraperHealthCheck**
> Object ChatgptChatgptScraperHealthCheck ()

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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
    public class ChatgptChatgptScraperHealthCheckExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);

            try
            {
                // ChatGPT scraper health check
                Object result = apiInstance.ChatgptChatgptScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptChatgptScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptChatgptScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // ChatGPT scraper health check
    ApiResponse<Object> response = apiInstance.ChatgptChatgptScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptChatgptScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="chatgptchatgptscraperhealthcheckhead"></a>
# **ChatgptChatgptScraperHealthCheckHead**
> Object ChatgptChatgptScraperHealthCheckHead ()

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

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
    public class ChatgptChatgptScraperHealthCheckHeadExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);

            try
            {
                // ChatGPT scraper health check
                Object result = apiInstance.ChatgptChatgptScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptChatgptScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptChatgptScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // ChatGPT scraper health check
    ApiResponse<Object> response = apiInstance.ChatgptChatgptScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptChatgptScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="chatgptlistchatgptmodels"></a>
# **ChatgptListChatgptModels**
> Object ChatgptListChatgptModels (string country = null)

List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

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
    public class ChatgptListChatgptModelsExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country. (optional) 

            try
            {
                // List ChatGPT models
                Object result = apiInstance.ChatgptListChatgptModels(country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptListChatgptModels: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptListChatgptModelsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // List ChatGPT models
    ApiResponse<Object> response = apiInstance.ChatgptListChatgptModelsWithHttpInfo(country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptListChatgptModelsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
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

<a id="chatgptmeasureabrandsvisibilityinachatgptanswer"></a>
# **ChatgptMeasureABrandSVisibilityInAChatgptAnswer**
> Object ChatgptMeasureABrandSVisibilityInAChatgptAnswer (string prompt, string brand, string domain = null, string aliases = null, string competitors = null, string country = null, string webSearch = null)

Measure a brand's visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

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
    public class ChatgptMeasureABrandSVisibilityInAChatgptAnswerExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);
            var prompt = "prompt_example";  // string | The prompt to ask ChatGPT.
            var brand = "brand_example";  // string | Brand name to look for in the answer.
            var domain = "domain_example";  // string | Brand domain, for citation matching. (optional) 
            var aliases = "aliases_example";  // string | Comma-separated alternative names. (optional) 
            var competitors = "competitors_example";  // string | Comma-separated competitor names. (optional) 
            var country = "country_example";  // string | ISO-3166 alpha-2 egress country. (optional) 
            var webSearch = "\"force\"";  // string | auto | force | off (optional)  (default to "force")

            try
            {
                // Measure a brand's visibility in a ChatGPT answer
                Object result = apiInstance.ChatgptMeasureABrandSVisibilityInAChatgptAnswer(prompt, brand, domain, aliases, competitors, country, webSearch);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptMeasureABrandSVisibilityInAChatgptAnswer: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptMeasureABrandSVisibilityInAChatgptAnswerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a ChatGPT answer
    ApiResponse<Object> response = apiInstance.ChatgptMeasureABrandSVisibilityInAChatgptAnswerWithHttpInfo(prompt, brand, domain, aliases, competitors, country, webSearch);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptMeasureABrandSVisibilityInAChatgptAnswerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **prompt** | **string** | The prompt to ask ChatGPT. |  |
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

<a id="chatgptmeasureabrandsvisibilityinachatgptanswerpost"></a>
# **ChatgptMeasureABrandSVisibilityInAChatgptAnswerPost**
> Object ChatgptMeasureABrandSVisibilityInAChatgptAnswerPost ()

Measure a brand's visibility in a ChatGPT answer (POST)

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
    public class ChatgptMeasureABrandSVisibilityInAChatgptAnswerPostExample
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
            var apiInstance = new ChatGPTApi(httpClient, config, httpClientHandler);

            try
            {
                // Measure a brand's visibility in a ChatGPT answer (POST)
                Object result = apiInstance.ChatgptMeasureABrandSVisibilityInAChatgptAnswerPost();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ChatGPTApi.ChatgptMeasureABrandSVisibilityInAChatgptAnswerPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChatgptMeasureABrandSVisibilityInAChatgptAnswerPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Measure a brand's visibility in a ChatGPT answer (POST)
    ApiResponse<Object> response = apiInstance.ChatgptMeasureABrandSVisibilityInAChatgptAnswerPostWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ChatGPTApi.ChatgptMeasureABrandSVisibilityInAChatgptAnswerPostWithHttpInfo: " + e.Message);
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

