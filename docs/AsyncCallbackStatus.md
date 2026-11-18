# ScrapeBadger.Model.AsyncCallbackStatus
Webhook delivery state of a call submitted with a callback URL.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RequestId** | **string** |  | 
**State** | **string** | &#x60;pending&#x60;: the call is still running. &#x60;delivering&#x60;: an attempt is under way or the next retry is due at &#x60;next_attempt_at&#x60;. &#x60;delivered&#x60;: the endpoint answered 2xx. &#x60;failed&#x60;: every attempt failed, a final status (not 408/429/5xx) came back, or a gateway restart interrupted the delivery (&#x60;last_error&#x60; \&quot;interrupted (gateway restart)\&quot;). | 
**Attempts** | **int** |  | 
**LastStatus** | **int?** |  | [optional] 
**LastError** | **string** |  | [optional] 
**NextAttemptAt** | **int?** |  | [optional] 
**DeliveredAt** | **int?** |  | [optional] 
**CallbackHost** | **string** | Host of the callback URL only (never its path or query). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

