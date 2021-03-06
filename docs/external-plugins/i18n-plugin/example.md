# Example
  
1. Setup environment. Please refer to [Environment Setup](./setup.md).
2. Config localization in i18n-plugin. Add the following example `zh-CN.json` file in `translations` directory. In `.i18nrc.json`, add the path `"translations": ["translations/zh-CN.json"]`. 


```json
{
    "formats": {
        "number": {
            "currency": {
                "style": "currency"
            },
            "percent": {
                "style": "percent"
            }
        },
        "date": {
            "short": {
                "month": "numeric",
                "day": "numeric",
                "year": "2-digit"
            },
            "medium": {
                "month": "short",
                "day": "numeric",
                "year": "numeric"
            },
            "long": {
                "month": "long",
                "day": "numeric",
                "year": "numeric"
            },
            "full": {
                "weekday": "long",
                "month": "long",
                "day": "numeric",
                "year": "numeric"
            }
        },
        "time": {
            "short": {
                "hour": "numeric",
                "minute": "numeric"
            },
            "medium": {
                "hour": "numeric",
                "minute": "numeric",
                "second": "numeric"
            },
            "long": {
                "hour": "numeric",
                "minute": "numeric",
                "second": "numeric",
                "timeZoneName": "short"
            },
            "full": {
                "hour": "numeric",
                "minute": "numeric",
                "second": "numeric",
                "timeZoneName": "short"
            }
        },
        "relative": {
            "years": {
                "units": "year"
            },
            "months": {
                "units": "month"
            },
            "days": {
                "units": "day"
            },
            "hours": {
                "units": "hour"
            },
            "minutes": {
                "units": "minute"
            },
            "seconds": {
                "units": "second"
            }
        }
    },
    "messages": {
        "console.devToolsDescription": "?????? cURL ????????? JSON ??????????????????????????????????????????",
        "console.devToolsTitle": "??? OpenSearch API ????????????",
        "core.ui.welcomeMessage": "???????????? OpenSearch",
        "dashboard.featureCatalogue.dashboardSubtitle": "??????????????????????????????",
        "discover.discoverSubtitle": "????????????????????????????????????",
        "home.addData.sectionTitle": "??????????????????",
        "home.breadcrumbs.homeTitle": "??????",
        "home.header.title": "????????????",
        "home.manageData.sectionTitle": "??????????????????",
        "home.tutorialDirectory.featureCatalogueDescription": "??????????????????????????????????????????",
        "home.tutorialDirectory.featureCatalogueTitle": "????????????",
        "opensearchDashboardsOverview.opensearchDashboards.solution.subtitle": "??????????????????",
        "opensearch-dashboards-react.osdOverviewPageHeader.addDataButtonLabel": "????????????",
        "opensearch-dashboards-react.osdOverviewPageHeader.devToolsButtonLabel": "????????????",
        "opensearch-dashboards-react.osdOverviewPageHeader.stackManagementButtonLabel": "??????",
        "opensearch-dashboards-react.pageFooter.appDirectoryButtonLabel": "??????????????????",
        "opensearch-dashboards-react.pageFooter.changeHomeRouteLink": "???????????????????????????"
    }
}
```
3. Config localization in OpenSearch Dashboards. Add `i18n.locale: "zh-CN"` in `opensearch_dashboards.yml` file.
4. Run OpenSearch and OpenSearch Dashboards. Verify the login and home pages are correctly translated.