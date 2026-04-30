# Gateway-SMS-Reports

A Salesforce package providing pre-built reports and a dashboard for monitoring SMS usage via the Gateway SMS (encsms) managed package.

<a href="https://github.com/Enclude-Components/Gateway-SMS-Reports/releases/latest">
  <img
    alt="Install Latest Release"
    src="https://img.shields.io/badge/Install%20Latest%20Release-238636?style=for-the-badge&logoColor=white&logo=DocuSign"
  >
</a>

## Metadata

### Reports — `SMSUsageReports`

| Name | Description |
|---|---|
| `SMS Costing 2+ Credits This Year` | Messages consuming more than one credit this year |
| `SMS Delivered Last Month` | Successfully delivered messages last month |
| `SMS Delivered This Month` | Successfully delivered messages this month |
| `SMS Delivered This Year` | Successfully delivered messages this year |
| `SMS Failed This Year` | Failed messages this year |
| `SMS Inbound This Year` | Inbound messages received this year |
| `SMS This Year` | All SMS messages sent this calendar year |

### Dashboard — `SMSUsageDashboard`

| API Name | Description |
|---|---|
| `SMS_Usage_Dashboard` | Overview dashboard with above reports |

## Development

> [!WARNING]
> This section is for developers only.

1. [Set up CumulusCI](https://cumulusci.readthedocs.io/en/latest/tutorial.html)
2. Run `cci flow run dev_org --org dev` to deploy this project.
3. Run `cci org browser dev` to open the org in your browser.

### Release

1. Release a Beta Version
```bash
cci flow run release_unlocked_beta --org dev
```

2. Test Deploy the Beta Version
```bash
cci flow run ci_beta --org beta
```

3. Promote to a Production Version. ***This promotes the latest beta version by default***
```bash
cci flow run release_unlocked_production --org release
```