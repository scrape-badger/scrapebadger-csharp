# ScrapeBadger.Model.VintedImageSearchRequest
Search by exactly one public image URL or base64-encoded image.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ImageUrl** | **string** |  | [optional] 
**ImageBase64** | **string** |  | [optional] 
**Market** | **string** | Vinted market code; uk aliases gb | [optional] [default to "fr"]
**Page** | **int** |  | [optional] [default to 1]
**PerPage** | **int** |  | [optional] [default to 20]
**PriceFrom** | **decimal?** |  | [optional] 
**PriceTo** | **decimal?** |  | [optional] 
**BrandIds** | **string** |  | [optional] 
**CatalogIds** | **string** |  | [optional] 
**ColorIds** | **string** |  | [optional] 
**SizeIds** | **string** |  | [optional] 
**MaterialIds** | **string** |  | [optional] 
**StatusIds** | **string** |  | [optional] 
**Time** | **int?** |  | [optional] 
**SearchSessionId** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

