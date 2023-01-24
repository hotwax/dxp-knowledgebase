January 2022

<table>
<tr>
<th>Feature</th>
<th>Planned</th>
<th>Status</th>
</tr>

<tr>
<td>Permissions</td>
<td>2 applications (namely Job Manager and Threshold Management)</td>
<td>Job Manager - Implementation done, rules pending</td>
</tr>

<tr>
<td>Timezone</td>
<td>Fix UTC issue. Add timezone support in all applications</td>
<td>Fix done, moment to luxon migration pending in some apps</td>
</tr>

<tr>
<td>Logger</td>
<td>POC Done. Add in-app logger and implement in 2 applications (namely Job Manager and Threshold Management)</td>
<td>Job Manager, Threshold Management and Import app done</td>
</tr>

<tr>
<td>OMS API</td>
<td>Apply the Product, User, and Stock modules to all apps</td>
<td> Product (Import), User (1 method in OMS API), Stock (PR) Revising the strategy</td>
</tr>


<tr>
<td>Showing app version, build information, and browser compatibility</td>
<td>Implementation and applying to all the apps</td>
<td>App version, & build information published a plugin, done in Import, Job Manager. Dependency of Luxon work in other apps</td>
</tr>

<tr>
<td>Hotwax Theme package</td>
<td>Implementation and application to all the apps</td>
<td>Done for all apps</td>
</tr>


</table>



Releases done:

| Date | Application | Release Version | Highlights |
| --- | --- | --- | --- |
| 20/01/2023 | import | [v2.2.0](https://github.com/hotwax/import/releases/tag/v2.2.0) | Show app version & build information |
| 20/01/2023 | bopis | [v2.2.0](https://github.com/hotwax/bopis/releases/tag/v2.2.0) | Updated UI of Settings page, used hotwax-apps-theme |
| 20/01/2023 | oms-api | [v1.4.0](https://github.com/hotwax/oms-api/releases/tag/v1.4.0) | Method to fetch stock on all facilities for products |
| 20/01/2023 | job manager | [v1.6.0](https://github.com/hotwax/job-manager/releases/tag/v1.6.0) | Bulk scheduling, used hotwax-apps-theme, show app version & build information |
| 20/01/2023 | inventory-count | [v1.3.0](https://github.com/hotwax/inventory-count/releases/tag/v1.3.0) | Updated UI of Settings page, used hotwax-apps-theme |
| 19/01/2023 | job manager | [v1.5.1](https://github.com/hotwax/job-manager/releases/tag/v1.5.1) | |
| 13/01/2023 | threshold-management | [v1.2.0](https://github.com/hotwax/threshold-management/releases/tag/v1.2.0) | |
| 13/01/2023 | receiving | [v2.5.0](https://github.com/hotwax/receiving/releases/tag/v2.5.0) | |
| 13/01/2023 | inventory-count | [v1.2.0](https://github.com/hotwax/inventory-count/releases/tag/v1.2.0) | |
| 13/01/2023 | picking | [v1.3.0](https://github.com/hotwax/picking/releases/tag/v1.3.0) | Upgraded to Ionic 6.2.9 |
| 13/01/2023 | oms-api | [v1.3.0](https://github.com/hotwax/oms-api/releases/tag/v1.3.0) | Stock schema, method to fetch stock for multiple products and defined tranformation rule for stock response |
| 13/01/2023 | preorder | [v1.1.0](https://github.com/hotwax/preorder/releases/tag/v1.1.0) | Upgraded Ionic to 6.2, updated settings page, and brands through API |
| 13/01/2023 | import | [v2.1.0](https://github.com/hotwax/import/releases/tag/v2.1.0) | Used hotwax-apps-theme |
| 12/01/2023 | hotwax-apps-theme | [v1.1.0](https://github.com/hotwax/hotwax-apps-theme/releases/tag/v1.1.0) | |
| 06/01/2023 | job manager | [v1.5.0](https://github.com/hotwax/job-manager/releases/tag/v1.5.0) | Used generic API for webhooks, and change shopify config from menu footer |
| 06/01/2023 | import | [v2.0.0](https://github.com/hotwax/import/releases/tag/v2.0.0) | Used oms-api package for product methods  |
| 06/01/2023 | hotwax-apps-themes | [v1.0.0](https://github.com/hotwax/hotwax-apps-theme/releases/tag/v1.0.0) | |
| 06/01/2023 | oms-api | [v1.2.0](https://github.com/hotwax/oms-api/releases/tag/v1.2.0) | |
| 06/01/2023 | receiving | [v2.4.0](https://github.com/hotwax/receiving/releases/tag/v2.4.0) | Show receiving history upon clicking on shipment item 'received' chip |
| 05/01/2023 | app-version-info | [v1.0.0](https://github.com/hotwax/app-version-info/releases/tag/v1.0.0) | |
| 02/01/2023 | oms-api | [v1.1.0](https://github.com/hotwax/oms-api/releases/tag/v1.1.0/) | Fetch grouped product information |
