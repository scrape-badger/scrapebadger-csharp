# ScrapeBadger.Api.LinkedInApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**LinkedinGetACompanySJobPostings**](LinkedInApi.md#linkedingetacompanysjobpostings) | **GET** /v1/linkedin/companies/{company_id}/jobs | Get a company&#39;s job postings |
| [**LinkedinGetACourse**](LinkedInApi.md#linkedingetacourse) | **GET** /v1/linkedin/learning/{course_slug} | Get a course |
| [**LinkedinGetAPublicArticle**](LinkedInApi.md#linkedingetapublicarticle) | **GET** /v1/linkedin/articles/{article_slug} | Get a public article |
| [**LinkedinGetAPublicPost**](LinkedInApi.md#linkedingetapublicpost) | **GET** /v1/linkedin/posts/{post_slug} | Get a public post |
| [**LinkedinGetCompany**](LinkedInApi.md#linkedingetcompany) | **GET** /v1/linkedin/companies/{universal_name} | Get company |
| [**LinkedinGetJobDetail**](LinkedInApi.md#linkedingetjobdetail) | **GET** /v1/linkedin/jobs/{job_id} | Get job detail |
| [**LinkedinGetPublicProfile**](LinkedInApi.md#linkedingetpublicprofile) | **GET** /v1/linkedin/profiles/{public_id} | Get public profile |
| [**LinkedinGetSchool**](LinkedInApi.md#linkedingetschool) | **GET** /v1/linkedin/schools/{universal_name} | Get school |
| [**LinkedinLinkedinScraperHealthCheck**](LinkedInApi.md#linkedinlinkedinscraperhealthcheck) | **GET** /v1/linkedin/health | LinkedIn scraper health check |
| [**LinkedinLinkedinScraperHealthCheckHead**](LinkedInApi.md#linkedinlinkedinscraperhealthcheckhead) | **HEAD** /v1/linkedin/health | LinkedIn scraper health check |
| [**LinkedinSearchLinkedinJobs**](LinkedInApi.md#linkedinsearchlinkedinjobs) | **GET** /v1/linkedin/jobs/search | Search LinkedIn jobs |
| [**LinkedinSuggestLocationGeoIds**](LinkedInApi.md#linkedinsuggestlocationgeoids) | **GET** /v1/linkedin/geo/suggest | Suggest location geo ids |

<a id="linkedingetacompanysjobpostings"></a>
# **LinkedinGetACompanySJobPostings**
> Object LinkedinGetACompanySJobPostings (string companyId, int? start = null, string country = null)

Get a company's job postings

Public job postings for a company (numeric company id from the company endpoint).

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
    public class LinkedinGetACompanySJobPostingsExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var companyId = "companyId_example";  // string | 
            var start = 0;  // int? | Pagination offset (0, 25, 50, ...) (optional)  (default to 0)
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get a company's job postings
                Object result = apiInstance.LinkedinGetACompanySJobPostings(companyId, start, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetACompanySJobPostings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetACompanySJobPostingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a company's job postings
    ApiResponse<Object> response = apiInstance.LinkedinGetACompanySJobPostingsWithHttpInfo(companyId, start, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetACompanySJobPostingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **companyId** | **string** |  |  |
| **start** | **int?** | Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetacourse"></a>
# **LinkedinGetACourse**
> Object LinkedinGetACourse (string courseSlug, string country = null)

Get a course

A public LinkedIn Learning course — provider, workload, instructors, rating.

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
    public class LinkedinGetACourseExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var courseSlug = "courseSlug_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get a course
                Object result = apiInstance.LinkedinGetACourse(courseSlug, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetACourse: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetACourseWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a course
    ApiResponse<Object> response = apiInstance.LinkedinGetACourseWithHttpInfo(courseSlug, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetACourseWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **courseSlug** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetapublicarticle"></a>
# **LinkedinGetAPublicArticle**
> Object LinkedinGetAPublicArticle (string articleSlug, string country = null)

Get a public article

A public Pulse article — title, body, author, reactions (JSON-LD).

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
    public class LinkedinGetAPublicArticleExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var articleSlug = "articleSlug_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get a public article
                Object result = apiInstance.LinkedinGetAPublicArticle(articleSlug, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetAPublicArticle: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetAPublicArticleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a public article
    ApiResponse<Object> response = apiInstance.LinkedinGetAPublicArticleWithHttpInfo(articleSlug, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetAPublicArticleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **articleSlug** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetapublicpost"></a>
# **LinkedinGetAPublicPost**
> Object LinkedinGetAPublicPost (string postSlug, string country = null)

Get a public post

A public activity share — text, author, reactions, comments (JSON-LD).

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
    public class LinkedinGetAPublicPostExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var postSlug = "postSlug_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get a public post
                Object result = apiInstance.LinkedinGetAPublicPost(postSlug, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetAPublicPost: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetAPublicPostWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get a public post
    ApiResponse<Object> response = apiInstance.LinkedinGetAPublicPostWithHttpInfo(postSlug, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetAPublicPostWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **postSlug** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetcompany"></a>
# **LinkedinGetCompany**
> Object LinkedinGetCompany (string universalName, string country = null)

Get company

Public company page — industry, size, HQ, followers, specialties (JSON-LD + SSR).

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
    public class LinkedinGetCompanyExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var universalName = "universalName_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get company
                Object result = apiInstance.LinkedinGetCompany(universalName, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetCompany: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetCompanyWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get company
    ApiResponse<Object> response = apiInstance.LinkedinGetCompanyWithHttpInfo(universalName, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetCompanyWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **universalName** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetjobdetail"></a>
# **LinkedinGetJobDetail**
> Object LinkedinGetJobDetail (string jobId, string country = null)

Get job detail

Full detail for one job posting (guest API, no login).

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
    public class LinkedinGetJobDetailExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var jobId = "jobId_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get job detail
                Object result = apiInstance.LinkedinGetJobDetail(jobId, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetJobDetail: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetJobDetailWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get job detail
    ApiResponse<Object> response = apiInstance.LinkedinGetJobDetailWithHttpInfo(jobId, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetJobDetailWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **jobId** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetpublicprofile"></a>
# **LinkedinGetPublicProfile**
> Object LinkedinGetPublicProfile (string publicId, string country = null)

Get public profile

Public profile by vanity id (the ``/in/{public_id}`` slug) — name, headline, location, about, experience, education (public JSON-LD + SSR subset).

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
    public class LinkedinGetPublicProfileExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var publicId = "publicId_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get public profile
                Object result = apiInstance.LinkedinGetPublicProfile(publicId, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetPublicProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetPublicProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get public profile
    ApiResponse<Object> response = apiInstance.LinkedinGetPublicProfileWithHttpInfo(publicId, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetPublicProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **publicId** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedingetschool"></a>
# **LinkedinGetSchool**
> Object LinkedinGetSchool (string universalName, string country = null)

Get school

Public school page — name, description, website, follower/alumni counts.

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
    public class LinkedinGetSchoolExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var universalName = "universalName_example";  // string | 
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Get school
                Object result = apiInstance.LinkedinGetSchool(universalName, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinGetSchool: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinGetSchoolWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get school
    ApiResponse<Object> response = apiInstance.LinkedinGetSchoolWithHttpInfo(universalName, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinGetSchoolWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **universalName** | **string** |  |  |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedinlinkedinscraperhealthcheck"></a>
# **LinkedinLinkedinScraperHealthCheck**
> Object LinkedinLinkedinScraperHealthCheck ()

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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
    public class LinkedinLinkedinScraperHealthCheckExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);

            try
            {
                // LinkedIn scraper health check
                Object result = apiInstance.LinkedinLinkedinScraperHealthCheck();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinLinkedinScraperHealthCheck: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinLinkedinScraperHealthCheckWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // LinkedIn scraper health check
    ApiResponse<Object> response = apiInstance.LinkedinLinkedinScraperHealthCheckWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinLinkedinScraperHealthCheckWithHttpInfo: " + e.Message);
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

<a id="linkedinlinkedinscraperhealthcheckhead"></a>
# **LinkedinLinkedinScraperHealthCheckHead**
> Object LinkedinLinkedinScraperHealthCheckHead ()

LinkedIn scraper health check

Check health of the LinkedIn scraper service (accepts HEAD).

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
    public class LinkedinLinkedinScraperHealthCheckHeadExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);

            try
            {
                // LinkedIn scraper health check
                Object result = apiInstance.LinkedinLinkedinScraperHealthCheckHead();
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinLinkedinScraperHealthCheckHead: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinLinkedinScraperHealthCheckHeadWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // LinkedIn scraper health check
    ApiResponse<Object> response = apiInstance.LinkedinLinkedinScraperHealthCheckHeadWithHttpInfo();
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinLinkedinScraperHealthCheckHeadWithHttpInfo: " + e.Message);
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

<a id="linkedinsearchlinkedinjobs"></a>
# **LinkedinSearchLinkedinJobs**
> Object LinkedinSearchLinkedinJobs (string keywords = null, string location = null, string geoId = null, string companyId = null, string datePosted = null, string experience = null, string jobType = null, string workplace = null, string sort = null, int? start = null, string country = null)

Search LinkedIn jobs

Search public LinkedIn job postings (guest API, no login).

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
    public class LinkedinSearchLinkedinJobsExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var keywords = "keywords_example";  // string | Job title / keywords (optional) 
            var location = "location_example";  // string | Location text, e.g. 'New York' (optional) 
            var geoId = "geoId_example";  // string | LinkedIn numeric geo id (overrides location) (optional) 
            var companyId = "companyId_example";  // string | Restrict to a company (numeric id) (optional) 
            var datePosted = "datePosted_example";  // string | past_24h | past_week | past_month | any (optional) 
            var experience = "experience_example";  // string | internship|entry|associate|mid_senior|director|executive (comma-separated) (optional) 
            var jobType = "jobType_example";  // string | full_time|part_time|contract|temporary|internship|volunteer|other (optional) 
            var workplace = "workplace_example";  // string | onsite|remote|hybrid (comma-separated) (optional) 
            var sort = "sort_example";  // string | relevant | recent (optional) 
            var start = 0;  // int? | Pagination offset (0, 25, 50, ...) (optional)  (default to 0)
            var country = "\"us\"";  // string | Residential proxy country (optional)  (default to "us")

            try
            {
                // Search LinkedIn jobs
                Object result = apiInstance.LinkedinSearchLinkedinJobs(keywords, location, geoId, companyId, datePosted, experience, jobType, workplace, sort, start, country);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinSearchLinkedinJobs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinSearchLinkedinJobsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search LinkedIn jobs
    ApiResponse<Object> response = apiInstance.LinkedinSearchLinkedinJobsWithHttpInfo(keywords, location, geoId, companyId, datePosted, experience, jobType, workplace, sort, start, country);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinSearchLinkedinJobsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **keywords** | **string** | Job title / keywords | [optional]  |
| **location** | **string** | Location text, e.g. &#39;New York&#39; | [optional]  |
| **geoId** | **string** | LinkedIn numeric geo id (overrides location) | [optional]  |
| **companyId** | **string** | Restrict to a company (numeric id) | [optional]  |
| **datePosted** | **string** | past_24h | past_week | past_month | any | [optional]  |
| **experience** | **string** | internship|entry|associate|mid_senior|director|executive (comma-separated) | [optional]  |
| **jobType** | **string** | full_time|part_time|contract|temporary|internship|volunteer|other | [optional]  |
| **workplace** | **string** | onsite|remote|hybrid (comma-separated) | [optional]  |
| **sort** | **string** | relevant | recent | [optional]  |
| **start** | **int?** | Pagination offset (0, 25, 50, ...) | [optional] [default to 0] |
| **country** | **string** | Residential proxy country | [optional] [default to &quot;us&quot;] |

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

<a id="linkedinsuggestlocationgeoids"></a>
# **LinkedinSuggestLocationGeoIds**
> Object LinkedinSuggestLocationGeoIds (string query, string type = null)

Suggest location geo ids

Resolve a name to LinkedIn ids (job-search ``geo_id`` / ``company_id`` helper).

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
    public class LinkedinSuggestLocationGeoIdsExample
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
            var apiInstance = new LinkedInApi(httpClient, config, httpClientHandler);
            var query = "query_example";  // string | Location text, e.g. 'London'
            var type = "\"geo\"";  // string | geo | company (optional)  (default to "geo")

            try
            {
                // Suggest location geo ids
                Object result = apiInstance.LinkedinSuggestLocationGeoIds(query, type);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LinkedInApi.LinkedinSuggestLocationGeoIds: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LinkedinSuggestLocationGeoIdsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Suggest location geo ids
    ApiResponse<Object> response = apiInstance.LinkedinSuggestLocationGeoIdsWithHttpInfo(query, type);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LinkedInApi.LinkedinSuggestLocationGeoIdsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **query** | **string** | Location text, e.g. &#39;London&#39; |  |
| **type** | **string** | geo | company | [optional] [default to &quot;geo&quot;] |

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

