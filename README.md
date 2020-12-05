
# Apple Search Ads Attribution API for React Native

## Requirements
- iAd Framework

## Getting started
`$ yarn add @crowdnautics/react-native-apple-search-ads-attribution`

### Additional Required Manual installation
#### iOS

1. In XCode, [follow the instructions](https://searchads.apple.com/v/advanced/help/pdf/attribution-api.pdf) to add the iAd framework
2. Add the line `pod 'RNAppleAdsAttribution', :path => '../node_modules/@crowdnautics/react-native-apple-search-ads-attribution/RNAppleAdsAttribution.podspec'` to your Podfile
3. `cd ios && pod install && cd ..`
4. Run your project

## Usage
```javascript
import AppleAdsAttribution from '@crowdnautics/react-native-apple-search-ads-attribution'; 

let attributionData = AppleAdsAttribution.getAttributionData();
```

## Documentation

#### getAttributionData()
Gets install attribution data from the Apple Search Ads Attribution API.

##### Examples
```javascript
AppleAdsAttribution.getAttributionData().then(attributionData => {
  console.log(attributionData);

  // {
  //   “Version3.1”: {
  //   “iad-attribution”: true,
  //   “iad-org-name”: “Light Right”,
  //   “iad-campaign-id”: 15292426,
  //   “iad-campaign-name”: “Light Bright Launch”,
  //   “iad-purchase-date”: “2016-10-14T17:18:07Z”,
  //   “iad-conversion-date”: “2016-10-14T17:18:07Z”,
  //   “iad-conversion-type”: “Download”,
  //   “iad-click-date”: “2016-10-14T17:17:00Z”,
  //   “iad-adgroup-id”: 15307675,
  //   “iad-adgroup-name”: “LightRight Launch Group”,
  //   “iad-keyword”: “light right”,
  //   “iad-keyword-matchtype”: “Broad”
  //   }
});
```

##### Notes
> If you receive an empty object, wait a few seconds and try again

> Test values (mirroring the example above) will be sent when using a iOS simulator

