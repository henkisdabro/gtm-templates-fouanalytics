# gtm-templates-fouanalytics

Google Tag Manager (Web) tag template for loading the FouAnalytics JS library. It's simply a template "wrapper" to offer a safe(r) way to load the javascript library as opposed to using the Custom HTML tag when deploying FouAnalytics. This is not an official template. Feedback is welcome.

Thanks to Dr. Augustine Fou for building a great product. Read more about the service here and consider supporting his work.

[What is FouAnalytics? How does FouAnalytics work?](https://www.linkedin.com/pulse/what-fouanalytics-how-does-work-dr-augustine-fou-oglve/)

## Installation

### From the Community Template Gallery
1. In your GTM container, go to **Templates** > **Tag Templates**
2. Click **Search Gallery** and search for "FouAnalytics"
3. Select the template and click **Add to workspace**

### Manual Import
1. Download the `template.tpl` file from this repository
2. In your GTM container, go to **Templates** > **Tag Templates**
3. Click **New** > **Import** (three dots menu)
4. Select the downloaded `template.tpl` file

## Configuration

1. **FouAnalytics Script URL**: Copy the on-site URL from your FouAnalytics settings. The URL should:
   - Start with `https://`
   - Use the `api.fouanalytics.com` hostname
   - End with `init-[your-unique-id].js`

2. **Log debug messages to console**: Enable this checkbox to see loading status messages in the browser console (useful for troubleshooting).

## Important Considerations

### Firing Order
For optimal ad fraud detection, configure this tag to fire **before** your advertising tags (Google Ads, DV360, prebid.js, etc.). This ensures FouAnalytics can analyze traffic before ad requests are made.

**Recommended trigger**: Use a trigger that fires early in the page lifecycle, such as "Consent Initialization" or "Page View" with high priority.

### Consent Management
This template does not include built-in consent management. If you operate in regions requiring user consent (GDPR, CCPA, etc.), ensure you:

1. Configure appropriate consent triggers in GTM
2. Only fire this tag after obtaining required consent for analytics/measurement
3. Consider using GTM's Consent Mode if applicable

The responsibility for consent compliance lies with the template user, not the template itself.

## Changelog

- **v1**: Initial release

## License

See [LICENSE](LICENSE) file.

## Credits

Template created by [Henrik Söderlund](https://www.henriksoderlund.com/).

FouAnalytics is a product of Dr. Augustine Fou. Learn more at the link above.
