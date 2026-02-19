# PublicListing

Public company financial data. Only present for public companies.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stock_symbol** | **str** | Stock ticker symbol | [optional] 
**ipo_date** | **str** | IPO date in ISO format | [optional] 
**isin** | **str** | International Securities Identification Number | [optional] 
**figi** | **str** | Financial Instrument Global Identifier | [optional] 
**cusip** | **str** | CUSIP identifier | [optional] 
**lei** | **str** | Legal Entity Identifier | [optional] 
**cik** | **str** | SEC Central Index Key | [optional] 
**sic_code** | **str** | SEC Standard Industrial Classification code | [optional] 
**revenue_usd** | **int** | Annual revenue in USD | [optional] 
**revenue_captured_at** | **str** | Date when revenue data was captured (ISO format) | [optional] 
**ebitda_usd** | **int** | EBITDA in USD | [optional] 
**ebitda_captured_at** | **str** | Date when EBITDA data was captured (ISO format) | [optional] 

## Example

```python
from ninjapear.models.public_listing import PublicListing

# TODO update the JSON string below
json = "{}"
# create an instance of PublicListing from a JSON string
public_listing_instance = PublicListing.from_json(json)
# print the JSON string representation of the object
print(PublicListing.to_json())

# convert the object into a dict
public_listing_dict = public_listing_instance.to_dict()
# create an instance of PublicListing from a dict
public_listing_from_dict = PublicListing.from_dict(public_listing_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


