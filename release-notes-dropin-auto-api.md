# 2017-01-20 - Staging
- Update dealerInfo in streams when account is updated
[DAUTO-1061](https://dropin.atlassian.net/browse/DAUTO-1061)
[PR#279](https://github.com/dropininc/dropin-auto-api-v1/pull/279)
- Return org logo when a stream request is missed-offhour
[DAUTO-1075](https://dropin.atlassian.net/browse/DAUTO-1075)
[PR#285](https://github.com/dropininc/dropin-auto-api-v1/pull/285)
- update logic when count & get streams for dashboard APIs
[DAUTO-1062](https://dropin.atlassian.net/browse/DAUTO-1062)
[DAUTO-1086](https://dropin.atlassian.net/browse/DAUTO-1086)
[PR#291](https://github.com/dropininc/dropin-auto-api-v1/pull/291)
- return info of other streams in the same session when get stream
[DAUTO-1106](https://dropin.atlassian.net/browse/DAUTO-1106)
[PR#296](https://github.com/dropininc/dropin-auto-api-v1/pull/296)
- Update dealerInfo in streams when account is updated
[DAUTO-1119](https://dropin.atlassian.net/browse/DAUTO-1119)
[PR#297](https://github.com/dropininc/dropin-auto-api-v1/pull/297)

## Deploy notes
- Run the script `db-script/pr279-DAUTO-1061-update-stream-dealerInfo.js` before/after deployment
- Run the script `db-script/DAUTO1086-addIsMainStream.js` before/after deployment
- Set unique index for config.key in DB

# 2017-01-05 - Staging
- Return more info in API getcalls
[DAUTO-949](https://dropin.atlassian.net/browse/DAUTO-949)
[PR#260](https://github.com/dropininc/dropin-auto-api-v1/pull/260)
- Organization logo
[DAUTO-966](https://dropin.atlassian.net/browse/DAUTO-966)
[PR#263](https://github.com/dropininc/dropin-auto-api-v1/pull/263)

# 2016-12-14 - Staging + Production
- Add New Relic
[DAUTO-938](https://dropin.atlassian.net/browse/DAUTO-938)
[PR#258](https://github.com/dropininc/dropin-auto-api-v1/pull/258)

# 2016-12-12 - Staging + Production
- Set default no-reply email to no-reply@dropininc.com
[DAUTO-930](https://dropin.atlassian.net/browse/DAUTO-930)
[PR#257](https://github.com/dropininc/dropin-auto-api-v1/pull/257)

# 2016-12-05 - Production

# 2016-12-02 - Staging
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

# 2016-11-16
- Cron job to send lead
[DAUTO-714](https://dropin.atlassian.net/browse/DAUTO-714)
[PR#246](https://github.com/dropininc/dropin-auto-api-v1/pull/246)
[PR#247](https://github.com/dropininc/dropin-auto-api-v1/pull/247)
- Apply DST for org's business hour
[DAUTO-757](https://dropin.atlassian.net/browse/DAUTO-757)
[PR#248](https://github.com/dropininc/dropin-auto-api-v1/pull/248)
- Update logic for org's business hour
[DAUTO-842](https://dropin.atlassian.net/browse/DAUTO-842)
[PR#249](https://github.com/dropininc/dropin-auto-api-v1/pull/249)
- Update text & app link in SMS. Also update link in config file for dev, qa, staging, production
[DAUTO-847](https://dropin.atlassian.net/browse/DAUTO-847)
[PR#250](https://github.com/dropininc/dropin-auto-api-v1/pull/250)

## Deploy notes
- Update App link config (currently on dev, qa, staging, production)
