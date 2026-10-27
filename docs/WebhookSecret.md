# ScrapeBadger.Model.WebhookSecret
Signs every X-Callback-URL / batch webhook of this account (SCR-470).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Secret** | **string** |  | 
**SignatureHeader** | **string** |  | [optional] [default to "X-ScrapeBadger-Signature"]
**Algorithm** | **string** |  | [optional] [default to "sha256=<hex HMAC-SHA256 of the raw request body>"]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

