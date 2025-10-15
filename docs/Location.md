# Location

An identification or estimation of a geographic location of an object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**continent** | [**LocationContinent**](LocationContinent.md) |  | [default to undefined]
**country** | **string** | The highest administrative division, also known as a nation. The value is a two-letter country code, as defined in ISO 3166. For example, US for United States, BR for Brazil and DE for Germany. | [default to undefined]
**region** | [**Region**](Region.md) |  | [default to undefined]
**city** | **string** | The name of the incorporated city or town political entity. For example, \&quot;Sao Paulo\&quot;. | [default to undefined]
**district** | **string** | An administrative division smaller than a city and larger than a neighborhood. For example, the district of Manhattan in New York. | [default to undefined]
**timezone** | **string** | The time-zone ID as defined in IANA Time Zone Database. For example, \&quot;America/New_York\&quot;. | [default to undefined]
**coordinates** | [**GeoPoint**](GeoPoint.md) |  | [default to undefined]
**currency** | [**Currency**](Currency.md) |  | [optional] [default to undefined]
**phoneCode** | **string** | The international dialing code for this location. For example, \&#39;+1\&#39; or \&#39;+55\&#39;. | [optional] [default to undefined]
**population** | **string** | The approximate number of people living within the borders of the represented location. | [optional] [default to undefined]
**postalCode** | **string** | The general postal code for the location, such as a starting range, but it may also represent another relevant code for the area. For example, \&#39;12345-678\&#39;. | [optional] [default to undefined]
**languages** | **Array&lt;string&gt;** | A list of locales following the ISO 639-1 and ISO 3166-1 standards, representing the languages spoken in the location, ordered from the most spoken to the least spoken. For example, \&#39;pt-br\&#39; or \&#39;en-us\&#39;. | [optional] [default to undefined]
**tags** | **Array&lt;string&gt;** | A list of tags addressing different aspects of a location. For example, \&#39;beach\&#39; or \&#39;ocean\&#39;. | [optional] [default to undefined]
**source** | [**LocationSource**](LocationSource.md) |  | [default to undefined]

## Example

```typescript
import { Location } from '@croct/export';

const instance: Location = {
    continent,
    country,
    region,
    city,
    district,
    timezone,
    coordinates,
    currency,
    phoneCode,
    population,
    postalCode,
    languages,
    tags,
    source,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
