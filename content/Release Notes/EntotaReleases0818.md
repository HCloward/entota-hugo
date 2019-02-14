---
id: EntotaReleases0818
sidebar_label:  August 2018
title:  August 2018
---

# August 2018

## August 30, 2018

### Enhancement

You can view a dashboard with Entota™ centric metrics and information. You must have permissions to the Director persona in Admin to access the dashboard. Refer to Entota™ Dashboard for more information.

### Bug Fix

[IGC-1495] — Fixed an issue where when a user navigated away from an asset page without making changes, the user was prompted to save.

## August 24, 2018

### Enhancement

[IGC-1351] — Removed redundant feature flag gates that inhibited persona-based dashboard from displaying for all tenants.

### Bug Fix

[IGC-1474] — Removed an extra horizontal scroll bar that appeared under the asset header on Detail pages.

## August 20, 2018

### Enhancement

[IGC-1464] — Changed the title of the side panel that appears when the + button is pressed to relate an asset on a Detail page from “Add [Asset]” to “Relate [Asset]” for clarity.

### Bug Fixes

* [IGC-1408] — Fixed an issue where when a link was added to supporting documentation for an asset, the Save and Cancel buttons were not active.
* [IGC-1441] — Fixed an issue where pop-up windows displayed in inconsistent positions.
* [IGC-1463] —Fixed an issue where lines appeared under the Quick Add on Detail pages.
* [IGC-1482] — Fixed an issue where the last field on the Add Field tab of the Data Set page did not allow the user to select it.
* [IGC-1485] — Fixed an issue where new users permissions were assigned an unnecessary filter field.
* [IGC-1484] — Fixed an issue that caused new users to have missing permissions by adding new Data Catalog and Strategy security role templates.

## August 10, 2018

### Bug Fix

[IGC-1486] — Reverted the updates made by Entota™‌-1408 since the solution created additional issues. We are exploring other approaches to fix the initial issue.

## August 9, 2018

### Bug Fixes

* [IGC-1479] – Fixed an issue where a field did not display in a data set after it was added to the data set if the field was uploaded to the system with a backslash ("\") in the Location field.
* [IGC-1408] – Fixed an issue where when a link was added to supporting documentation for a term, the Save and Cancel buttons were not active.
* [IGC-1478] – Fixed an issue where the Criticality section displayed in the wrong place on the Policy Detail page when the Criticality value was updated.

## August 8, 2018

### Bug Fix

[IGC-1476] – Fixed an issue where the Deep Guidance icon appeared on manually added term-to-term relationships, but it did not appear on inferred term-to-term relationships. Now, the Deep Guidance icon no longer appears for term-to-term manual relationships and does appear for inferred term-to-term relationships.

## August 7, 2018

### Bug Fixes

* [IGC-344] – Fixed an issue in Process Designer where the change for adding a scenario dependency was not included in the change history.
* [IGC-1422] – Fixed an issue where Rule was only enforcing user level permissions, even though Policy and Rule share the same permission level and Policy enforces up to Admin. Now, both Rule and Policy enforce permissions up to Admin.
* [IGC-1445] – Fixed an issue where when users accessing Entota™ with a Chrome browser received a red error notification within a Decision Point in Process Designer, the notification bounced everywhere when hovered over, requiring users to catch the moving notification icon to display the error.
* [IGC-1007] – Updated the line under the Data Set tabs to be the same color as the one on top so that it is more easily seen.