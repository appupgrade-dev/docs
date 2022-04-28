## Integrate Using API

If you want to integrate your app with App Upgrade using API. You will need to call just one API.

<img src="https://raw.githubusercontent.com/appupgrade-dev/docs/main/images/api-sequence.png">

### API Contract:

GET: https://appupgrade.dev/api/v1/versions/check

This API is used for checking the app version is marked for upgrade or not.

#### Request Headers
| Header Name   |      Description      |  Example |
|:----------|:-------------|:------|
| x-api-key |  x-api-key for your project | MDNmNmZkNDEtNmNkMi00NzY3LThjOWEtYWYxMGFjZWQ0ZjI2 |

?> You can find the x-api-key in Accounts tab.

#### Response Headers
| Param Name   |      Description      |  Example |
|:----------|:-------------|:------|
| app_name |  You app name | Wallpaper app |
| app_version |  You app name | 1.0.0 |
| platform |  You platform name | android |
| environment |  You environment name | production |

#### Request Example:
```curl
curl --location --request GET 'https://appupgrade.dev/api/v1/versions/check?app_name=Wallpaper app&app_version=1.0.0&platform=android&environment=production' \
--header 'x-api-key: MDNmNmZkNDEtNmNkMi00NzY3LThjOWEtYWYxMGFjZWQ0ZjI2'
```

#### Response Example:
```json
{
    "found": true,
    "forceUpgrade": true,
    "query": {
        "app_name": "Wallpaper app",
        "app_version": "1.0.0",
        "platform": "android",
        "environment": "production"
    }
}
```

The API will respond with the required checks. If `found` is true that
means app is marked for upgrade.

If `forceUpgrade` is true that means
app needs to force the user to update the app. If false than just show
a popup to user for upgrade but it's not mandatory.

?> This call can be made on start of the app or periodically to check for the upgrade is required or not.