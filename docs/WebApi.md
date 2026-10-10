# ScrapeBadger.Api.WebApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**WebDetectAntiBotAndCaptchaSystems**](WebApi.md#webdetectantibotandcaptchasystems) | **POST** /v1/web/detect | Detect anti-bot and CAPTCHA systems |
| [**WebExtractStructuredData**](WebApi.md#webextractstructureddata) | **POST** /v1/web/extract | Extract structured data |
| [**WebPollAnAutoUnblockDiscoveryJob**](WebApi.md#webpollanautounblockdiscoveryjob) | **GET** /v1/web/unblock/{job_id} | Poll an auto-unblock discovery job |
| [**WebScrapeAUrl**](WebApi.md#webscrapeaurl) | **POST** /v1/web/scrape | Scrape a URL |
| [**WebTakeAScreenshot**](WebApi.md#webtakeascreenshot) | **POST** /v1/web/screenshot | Take a screenshot |
| [**WebWebScraperHealthCheck**](WebApi.md#webwebscraperhealthcheck) | **GET** /v1/web/health | Web scraper health check |
| [**WebWebScraperHealthCheckHead**](WebApi.md#webwebscraperhealthcheckhead) | **HEAD** /v1/web/health | Web scraper health check |

<a id="webdetectantibotandcaptchasystems"></a>
# **WebDetectAntiBotAndCaptchaSystems**
> Object WebDetectAntiBotAndCaptchaSystems ()

Detect anti-bot and CAPTCHA systems

Detect which anti-bot and CAPTCHA systems are present on a URL.  Uses rnet to fetch the page and identify DataDome, Cloudflare, Akamai, Kasada, Amazon WAF, reCAPTCHA, hCaptcha, GeeTest, and more. Cost: 1 credit.

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
    public class WebDetectAntiBotAndCaptchaSystemsExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);

            try
            {
                // Detect anti-bot and CAPTCHA systems
                Object result = apiInstance.WebDetectAntiBotAndCaptchaSystems();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebDetectAntiBotAndCaptchaSystems: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebDetectAntiBotAndCaptchaSystemsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Detect anti-bot and CAPTCHA systems
    ApiResponse<Object> response = apiInstance.WebDetectAntiBotAndCaptchaSystemsWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebDetectAntiBotAndCaptchaSystemsWithHttpInfo: " + e.Message);
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

<a id="webextractstructureddata"></a>
# **WebExtractStructuredData**
> Object WebExtractStructuredData (ExtractRequest extractRequest)

Extract structured data

Scrape a URL and extract fields with CSS/XPath selectors and/or AI.  ``extract_rules`` maps a field to a selector and returns ``data``; ``ai_extract_rules`` (field -> description) and ``ai_query`` return ``ai_extraction``. Billed as a scrape, plus the AI extraction credits when AI is asked for and succeeds.

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
    public class WebExtractStructuredDataExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);
            var extractRequest = new ExtractRequest(); // ExtractRequest | 

            try
            {
                // Extract structured data
                Object result = apiInstance.WebExtractStructuredData(extractRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebExtractStructuredData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebExtractStructuredDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Extract structured data
    ApiResponse<Object> response = apiInstance.WebExtractStructuredDataWithHttpInfo(extractRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebExtractStructuredDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **extractRequest** | [**ExtractRequest**](ExtractRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="webpollanautounblockdiscoveryjob"></a>
# **WebPollAnAutoUnblockDiscoveryJob**
> Object WebPollAnAutoUnblockDiscoveryJob (string jobId)

Poll an auto-unblock discovery job

Return the status + progress narration for an auto-unblock job.  Polled by the playground loader. ``job_id`` is an unguessable UUID handed out in the ``202 unblocking`` envelope and acts as a capability token, so any authenticated caller holding it can read the job (this is what lets several users share one discovery run's loader).

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
    public class WebPollAnAutoUnblockDiscoveryJobExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);
            var jobId = "jobId_example";  // string | 

            try
            {
                // Poll an auto-unblock discovery job
                Object result = apiInstance.WebPollAnAutoUnblockDiscoveryJob(jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebPollAnAutoUnblockDiscoveryJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebPollAnAutoUnblockDiscoveryJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Poll an auto-unblock discovery job
    ApiResponse<Object> response = apiInstance.WebPollAnAutoUnblockDiscoveryJobWithHttpInfo(jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebPollAnAutoUnblockDiscoveryJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **jobId** | **string** |  |  |

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

<a id="webscrapeaurl"></a>
# **WebScrapeAUrl**
> Object WebScrapeAUrl ()

Scrape a URL

Scrape a URL and return its content.  The Generic Web Scraping API is fully user-driven: callers pick their own request parameters (engine, proxy tier, country, JS rendering, …). A blocked target surfaces the raw 422 ``blocking_page_detected`` so the caller can tune parameters themselves — we do NOT auto-trigger host discovery. Curated per-origin overrides (which the dedicated scraper APIs depend on) still apply.  One exception, added for SB-001083/SCR-64: a plain ``google.com/search`` web-SERP fetch is served by the dedicated Google scraper, whose rotation loop is built for SearchGuard. Same request shape, same response shape, billed at what it actually cost — the caller sees only a better hit rate. ``serp_adapter`` fails closed, so any request carrying a parameter it does not recognise as route-or-cost takes the generic path unchanged, and the user-driven contract above still holds.

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
    public class WebScrapeAUrlExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);

            try
            {
                // Scrape a URL
                Object result = apiInstance.WebScrapeAUrl();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebScrapeAUrl: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebScrapeAUrlWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Scrape a URL
    ApiResponse<Object> response = apiInstance.WebScrapeAUrlWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebScrapeAUrlWithHttpInfo: " + e.Message);
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

<a id="webtakeascreenshot"></a>
# **WebTakeAScreenshot**
> Object WebTakeAScreenshot (ScreenshotRequest screenshotRequest)

Take a screenshot

Render a URL in the browser engine and return a PNG screenshot.  ``screenshot`` is the PNG, base64-encoded. ``width``/``height`` set the viewport; ``full_page`` captures the whole scrollable page. Billed as a browser scrape (plus the proxy tier); a page that loads without a screenshot is a 502 and costs nothing.

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
    public class WebTakeAScreenshotExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);
            var screenshotRequest = new ScreenshotRequest(); // ScreenshotRequest | 

            try
            {
                // Take a screenshot
                Object result = apiInstance.WebTakeAScreenshot(screenshotRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebTakeAScreenshot: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebTakeAScreenshotWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Take a screenshot
    ApiResponse<Object> response = apiInstance.WebTakeAScreenshotWithHttpInfo(screenshotRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebTakeAScreenshotWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **screenshotRequest** | [**ScreenshotRequest**](ScreenshotRequest.md) |  |  |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="webwebscraperhealthcheck"></a>
# **WebWebScraperHealthCheck**
> Object WebWebScraperHealthCheck ()

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class WebWebScraperHealthCheckExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);

            try
            {
                // Web scraper health check
                Object result = apiInstance.WebWebScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebWebScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebWebScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web scraper health check
    ApiResponse<Object> response = apiInstance.WebWebScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebWebScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="webwebscraperhealthcheckhead"></a>
# **WebWebScraperHealthCheckHead**
> Object WebWebScraperHealthCheckHead ()

Web scraper health check

Check health of the web scraper service.  Bypasses the proxy abstraction because web-scraper exposes ``/health`` at the root (no ``/api/v1`` prefix, unlike the other scraper services).  Accepts ``HEAD`` so external uptime checkers (UptimeRobot uses HEAD by default for HTTP monitors) don't get a 405 Method Not Allowed.

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
    public class WebWebScraperHealthCheckHeadExample
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
            var apiInstance = new WebApi(httpClient, config, httpClientHandler);

            try
            {
                // Web scraper health check
                Object result = apiInstance.WebWebScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebApi.WebWebScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the WebWebScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Web scraper health check
    ApiResponse<Object> response = apiInstance.WebWebScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebApi.WebWebScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

