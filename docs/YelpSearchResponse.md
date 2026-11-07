# ScrapeBadger.Model.YelpSearchResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Market** | **string** |  | 
**Query** | **string** |  | 
**Location** | **string** |  | 
**LocationResolved** | [**YelpResolvedLocation**](YelpResolvedLocation.md) |  | 
**DidYouMean** | **string** |  | [optional] 
**QueryMatched** | **bool** | False when Yelp could not place the query; results are then Yelp&#39;s broader ranking for the location, as Yelp shows them. | 
**TotalResults** | **int** | Yelp&#39;s reported total; at most 110 are browsable. | 
**Page** | **int** |  | 
**PageSize** | **int** |  | 
**TotalPages** | **int** |  | 
**HasNextPage** | **bool** |  | 
**NextPage** | **int?** |  | [optional] 
**Results** | [**List&lt;YelpBusiness&gt;**](YelpBusiness.md) |  | 
**Ads** | [**List&lt;YelpBusiness&gt;**](YelpBusiness.md) |  | 
**Filters** | [**Dictionary&lt;string, YelpFilterGroup&gt;**](YelpFilterGroup.md) |  | 
**RelatedSearches** | [**List&lt;YelpLink&gt;**](YelpLink.md) |  | 
**SourceUrl** | **string** |  | 
**FetchedAt** | **string** |  | 
**FetchedUtc** | **decimal** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

