# ScrapeBadger.Model.ExtractRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Url** | **string** | The page to fetch. | 
**WaitFor** | **string** |  | [optional] 
**Country** | **string** |  | [optional] 
**ProxyTier** | **string** | Proxy pool: simple, premium or ultra. | [optional] [default to ProxyTierEnum.Simple]
**ExtractRules** | [**Dictionary&lt;string, ExtractRequestExtractRulesValue&gt;**](ExtractRequestExtractRulesValue.md) |  | [optional] 
**AiExtractRules** | **Dictionary&lt;string, string&gt;** |  | [optional] 
**AiQuery** | **string** |  | [optional] 
**RenderJs** | **bool** | Render the page in a browser first. | [optional] [default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

