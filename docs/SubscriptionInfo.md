# ScrapeBadger.Model.SubscriptionInfo
Active subscription details (null when PAYG-only).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PlanCode** | **string** |  | 
**PlanTitle** | **string** |  | 
**BillingCadence** | **string** |  | 
**Status** | **string** |  | 
**CurrentPeriodStart** | **DateTime?** |  | [optional] 
**CurrentPeriodEnd** | **DateTime?** |  | [optional] 
**CancelAtPeriodEnd** | **bool** |  | [optional] [default to false]
**CancelEffectiveAt** | **DateTime?** |  | [optional] 
**MonthlyCredits** | **int** |  | [optional] [default to 0]
**PendingPlanCode** | **string** |  | [optional] 
**PendingPlanTitle** | **string** |  | [optional] 
**PendingChangeEffectiveAt** | **DateTime?** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

