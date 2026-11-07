# ScrapeBadger.Model.YelpBusiness
A business card as ranked on the search page; nullable fields are absent from some cards.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Position** | **int** | 1-based place in Yelp&#39;s organic order across pages (page 2 starts at 11): Yelp&#39;s own number where it numbers the results; services searches are unnumbered and keep Yelp&#39;s order. For ads, the slot order. | 
**IsAd** | **bool** |  | 
**Id** | **string** | Yelp encrypted business ID. | 
**Alias** | **string** | Business slug used in /biz/&lt;alias&gt;. | 
**Name** | **string** |  | 
**Url** | **string** |  | 
**Rating** | **decimal?** |  | [optional] 
**ReviewCount** | **int?** |  | [optional] 
**Price** | **string** |  | [optional] 
**PriceLevel** | **int?** |  | [optional] 
**Categories** | [**List&lt;YelpCategory&gt;**](YelpCategory.md) |  | [optional] 
**Neighborhoods** | **List&lt;string&gt;** |  | [optional] 
**Address** | **string** |  | [optional] 
**City** | **string** |  | [optional] 
**Phone** | **string** |  | [optional] 
**Timezone** | **string** |  | [optional] 
**OpeningHours** | [**List&lt;YelpHours&gt;**](YelpHours.md) |  | [optional] 
**Snippet** | **string** |  | [optional] 
**SnippetType** | **string** |  | [optional] 
**Highlights** | **List&lt;string&gt;** |  | [optional] 
**Tags** | **List&lt;string&gt;** |  | [optional] 
**Photos** | **List&lt;string&gt;** |  | [optional] 
**AlternateNames** | **List&lt;string&gt;** |  | [optional] 
**IsServiceAreaBusiness** | **bool?** |  | [optional] 
**IsYelpGuaranteed** | **bool?** |  | [optional] 
**HasVerifiedLicense** | **bool?** |  | [optional] 
**AdPlacement** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

