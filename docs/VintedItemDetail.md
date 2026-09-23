# ScrapeBadger.Model.VintedItemDetail
A single listing with the fields only the detail endpoint carries.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int** |  | 
**Title** | **string** |  | 
**Price** | [**VintedPrice**](VintedPrice.md) |  | 
**BrandTitle** | **string** |  | [optional] 
**DisplayTitle** | **string** |  | [optional] 
**DisplaySubtitle** | **string** |  | [optional] 
**SizeTitle** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Url** | **string** |  | 
**Path** | **string** |  | [optional] 
**IsVisible** | **bool** |  | [optional] [default to true]
**Promoted** | **bool** |  | [optional] [default to false]
**FavouriteCount** | **int** |  | [optional] [default to 0]
**ViewCount** | **int** |  | [optional] [default to 0]
**ServiceFee** | **string** |  | [optional] 
**TotalItemPrice** | **string** |  | [optional] 
**ContentSource** | **string** |  | [optional] 
**SellerCountryCode** | **string** |  | [optional] 
**SimilarityScore** | **decimal?** |  | [optional] 
**User** | [**VintedUserSummary**](VintedUserSummary.md) |  | [optional] 
**Photo** | [**VintedPhoto**](VintedPhoto.md) |  | [optional] 
**Photos** | [**List&lt;VintedPhoto&gt;**](VintedPhoto.md) |  | [optional] 
**Description** | **string** |  | [optional] 
**CatalogId** | **int?** |  | [optional] 
**Color1** | **string** |  | [optional] 
**Color2** | **string** |  | [optional] 
**PackageSizeId** | **int?** |  | [optional] 
**IsFavourite** | **bool** |  | [optional] [default to false]
**CanBuy** | **bool** |  | [optional] [default to true]
**CanBundle** | **bool** |  | [optional] [default to false]
**CanReserve** | **bool** |  | [optional] [default to false]
**InstantBuy** | **bool** |  | [optional] [default to false]
**IsHidden** | **bool** |  | [optional] [default to false]
**IsReserved** | **bool** |  | [optional] [default to false]
**IsClosed** | **bool** |  | [optional] [default to false]
**Seller** | [**VintedSellerSummary**](VintedSellerSummary.md) |  | [optional] 
**SizeId** | **int?** |  | [optional] 
**StatusId** | **int?** |  | [optional] 
**BrandId** | **int?** |  | [optional] 
**Category** | **List&lt;string&gt;** |  | [optional] 
**UploadDate** | **string** |  | [optional] 
**UploadedAt** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

