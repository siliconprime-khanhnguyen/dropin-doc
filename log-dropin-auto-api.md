# Next release notes
- Support export leads to csv and send to client's CRM
[DAUTO-884](https://dropin.atlassian.net/browse/DAUTO-884)(DAUTO-886, DAUTO-888)
[PR#251](https://github.com/dropininc/dropin-auto-api-v1/pull/251)
- Check app version
[DAUTO-892](https://dropin.atlassian.net/browse/DAUTO-892)(DAUTO-892)
[PR#283](https://github.com/dropininc/dropin-auto-api-v1/pull/253)

## Deploy notes
- Update config in DB
```
db.config.update({
  key: 'appVersions'
}, {
  $set: {
	  key: 'appVersions',
	  value: {
      // Ex: iosDealer: '>=1.2' will match all version from 1.2.0
      newIosDealer: '>=1.0.1', // iOS Dealer enterprise
      iosDealerAppStore: '>=1.0.1', // iOS Dealer app store
      iosDealer: '>=1.0.1' // android dealer
    }
  }
}, {
  upsert: true
});

db.config.update({
  key: 'appLinks'
}, {
  $set: {
	  key: 'appLinks',
	  value: {
      // Ex: newIosDealer: 'https://itunes.apple.com/us/app/dropin-auto/id1144320824?ls=1&mt=8'
      newIosDealer: 'iOS Auto Dealer enterprise link',
      iosDealerAppStore: 'iOS Auto Dealer app store link',
      iosDealer: 'Android Auto Dealer play store link'
    }
  }
}, {
  upsert: true
});
```
