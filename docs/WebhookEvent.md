# ScrapeBadger.Model.WebhookEvent
The `request.completed` webhook. Signed: `X-ScrapeBadger-Signature` is `sha256=` + hex HMAC-SHA256 of the raw body with the account's webhook secret (`GET /v1/account/webhook-secret`). Deliveries can repeat: deduplicate on `request_id`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Event** | **string** |  | 
**RequestId** | **string** |  | 
**BatchId** | **string** |  | 
**Status** | **int** | The call&#39;s own HTTP status. | 
**Headers** | **Dictionary&lt;string, string&gt;** | The call&#39;s kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). | 
**ResultUrl** | **string** |  | 
**ResultExpiresAt** | **int** | Unix time. | 
**BodySize** | **int?** |  | 
**Body** | **Object** |  | 
**BodyOmitted** | **bool** | Present (true) when the body was over 1 MB: fetch &#x60;result_url&#x60;. | [optional] 
**Attempt** | **int?** |  | 
**SentAt** | **int** | Unix time of this attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

