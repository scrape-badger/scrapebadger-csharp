# ScrapeBadger.Model.AutoScout24Listing
Public data on a search card; nullable fields are absent from some cards.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**CrossReferenceId** | **string** |  | [optional] 
**Position** | **int** |  | 
**Title** | **string** |  | 
**Url** | **string** |  | 
**Images** | **List&lt;string&gt;** |  | [optional] 
**OnlinePurchaseImages** | **List&lt;string&gt;** |  | [optional] 
**Price** | **decimal?** |  | [optional] 
**Currency** | **string** |  | [optional] [default to "EUR"]
**PriceFormatted** | **string** |  | [optional] 
**PriceEvaluation** | **int?** |  | [optional] 
**PriceEvaluationEnabled** | **bool?** |  | [optional] 
**PriceDetails** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**OldPriceFormatted** | **string** |  | [optional] 
**IsSuperDeal** | **bool?** |  | [optional] 
**IsConditionalPrice** | **bool?** |  | [optional] 
**VatLabelRequired** | **bool?** |  | [optional] 
**Make** | **string** |  | [optional] 
**Model** | **string** |  | [optional] 
**ModelId** | **int?** |  | [optional] 
**ModelGroup** | **string** |  | [optional] 
**Variant** | **string** |  | [optional] 
**MotorType** | **string** |  | [optional] 
**VarVersion** | **string** |  | [optional] 
**Subtitle** | **string** |  | [optional] 
**ArticleType** | **string** |  | [optional] 
**OfferType** | **string** |  | [optional] 
**Fuel** | **string** |  | [optional] 
**FuelType** | **string** |  | [optional] 
**Transmission** | **string** |  | [optional] 
**MileageKm** | **int?** |  | [optional] 
**FirstRegistration** | **string** |  | [optional] 
**RegistrationYear** | **int?** |  | [optional] 
**RegistrationMonth** | **int?** |  | [optional] 
**PowerKw** | **decimal?** |  | [optional] 
**PowerHp** | **decimal?** |  | [optional] 
**DisplacementCc** | **int?** |  | [optional] 
**IsDamaged** | **bool?** |  | [optional] 
**AvailableNow** | **bool?** |  | [optional] 
**AvailableAt** | **string** |  | [optional] 
**AvailableUtc** | **decimal?** |  | [optional] 
**AvailabilityInDays** | **int?** |  | [optional] 
**Location** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**Seller** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**Rating** | **decimal?** |  | [optional] 
**RatingCount** | **int?** |  | [optional] 
**RatingsEnabled** | **bool?** |  | [optional] 
**Leasing** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**Seals** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** |  | [optional] 
**OnlinePurchase** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**ElectricVehicleBanner** | **Dictionary&lt;string, Object&gt;** |  | [optional] 
**IsDeliverable** | **bool?** |  | [optional] 
**HasVideo** | **bool?** |  | [optional] 
**Has360Image** | **bool?** |  | [optional] 
**InterestLevel** | **string** |  | [optional] 
**IsTrending** | **bool?** |  | [optional] 
**AdTier** | **string** |  | [optional] 
**ResultType** | **string** |  | [optional] 
**ResultSection** | **string** |  | [optional] 
**SpecialConditions** | **List&lt;Object&gt;** |  | [optional] 
**VehicleDetails** | **List&lt;Dictionary&lt;string, Object&gt;&gt;** |  | [optional] 
**WltpValues** | **List&lt;string&gt;** |  | [optional] 
**Vehicle** | **Dictionary&lt;string, Object&gt;** | Additional native vehicle attributes, including localized labels. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

