# Breadcrumbs

You set the breadcrumbs by using the chrome service:
```
  chrome.setBreadcrumbs([
    {
      text: i18n.translate('visualize.listing.breadcrumb', {
        defaultMessage: 'Visualize',
      }),
      href: `/`,
    },
    {
      text: i18n.translate('wizard.nav.breadcrumb.create', {
        defaultMessage: 'Create',
      }),
    },
  ]);
```
If no href is supplied on a breadcrumb object, the text appears as flat text.  If an href is supplied, the crumb is a link to the href.
