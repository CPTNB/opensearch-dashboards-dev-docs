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
        "console.devToolsDescription": "跳过 cURL 并使用 JSON 接口在控制台中处理您的数据。",
        "console.devToolsTitle": "与 OpenSearch API 进行交互",
        "core.ui.welcomeMessage": "正在加载 OpenSearch",
        "dashboard.featureCatalogue.dashboardSubtitle": "在控制板中分析数据。",
        "discover.discoverSubtitle": "搜索和查找数据分析结果。",
        "home.addData.sectionTitle": "获取你的数据",
        "home.breadcrumbs.homeTitle": "主页",
        "home.header.title": "欢迎归来",
        "home.manageData.sectionTitle": "管理你的数据",
        "home.tutorialDirectory.featureCatalogueDescription": "从热门应用和服务中采集数据。",
        "home.tutorialDirectory.featureCatalogueTitle": "添加数据",
        "opensearchDashboardsOverview.opensearchDashboards.solution.subtitle": "可视化和分析",
        "opensearch-dashboards-react.osdOverviewPageHeader.addDataButtonLabel": "添加数据",
        "opensearch-dashboards-react.osdOverviewPageHeader.devToolsButtonLabel": "开发工具",
        "opensearch-dashboards-react.osdOverviewPageHeader.stackManagementButtonLabel": "管理",
        "opensearch-dashboards-react.pageFooter.appDirectoryButtonLabel": "查看应用目录",
        "opensearch-dashboards-react.pageFooter.changeHomeRouteLink": "登录时显示不同页面"
    }
}
```
3. Config localization in OpenSearch Dashboards. Add `i18n.locale: "zh-CN"` in `opensearch_dashboards.yml` file.
4. Run OpenSearch and OpenSearch Dashboards. Verify the login and home pages are correctly translated.