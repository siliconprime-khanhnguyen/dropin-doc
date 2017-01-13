# Next release notes

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


## Deploy notes
- Run the script `db-script/pr279-DAUTO-1061-update-stream-dealerInfo.js` before/after deployment
- Run the script `db-script/DAUTO1086-addIsMainStream.js` before/after deployment
- Set unique index for config.key in DB
