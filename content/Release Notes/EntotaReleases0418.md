---
id: EntotaReleases0418
sidebar_label:  April 2018
title:  April 2018
---

# April 2018

## April 30, 2018

### Bug Fix

[IGC-351] - Fixed an issue that caused multiple errors when adding tasks to a published scenario by updating the status of that scenario when changes to roles and tasks are made.

## April 26, 2018

### Bug Fixes

* [IGC-1178] – Fixed an issue where the horizontal dividing lines in the left panel on asset detail pages were missing.
* [IGC-1179] – Fixed an issue where suggested terms in all caps were not being truncated in the guidance panel.
* [IGC-1192] – Fixed an issue where a user could enter a Start Date that was later than the End Date for an Initiative.
* [IGC-1231] – Fixed an issue on the Quick Add modal for Policy where an error message was displayed when the modal was first displayed.
* [IGC-1232] – Fixed an issue where there were two horizontal dividing lines for Rule Implication field.
* [IGC-1256] – Fixed an issue where the Critical Data Element check box was being cleared automatically when a term was contested.

## April 24, 2018

### Bug Fixes

* [IGC-1257] – Fixed issues where sponsor's individual endorsements or contests to assets were not displayed in change history and where changes to the Sponsors list was not being reflected in change history.

* [IGC-1261] – Fixed an issue where if a user started the review process and endorsed an asset that had been previously in contested status the change history New column displayed both the current endorser and the user who had previously contested.

## April 18, 2018

### Enhancement

Terms can now be identified as Critical Data Elements. Refer to Set up Terms for more information.

### Bug Fixes

* [IGC-1199] – Fixed an issue where when adding fields to a Data Set the Data Type length was not displayed in the add modal and a label for a classification option was incorrect.
* [IGC-1200] – Fixed an issue where a GUID was being displayed for the assignee instead of the assignee name in the change history for Systems and Data Sets.
* [IGC-1220] – Fixed an issue where change history was not being updated for System and Data Set assets if a contact had been added to the asset.
* [IGC-1223] – The following issues have been fixed in change history:
    * NULL was displayed in change history when adding a Data Set.
    * Endorsements and contests to assets were not displaying in change history for Terms, and Policies.
    * Changes to Connectivity were not displayed correctly when updating a System.
    * Changes to Supporting Documentation were not displayed correctly for all assets.
* [IGC-1225] – Fixed word wrapping in Strategy bar to make the content more readable.
* [IGC-1226] – Fixed an issue where Rule endorsements were not shown in change history.
* [IGC-1227] – Fixed an issue where term relationships from Deep Guidance™ were not displaying with the Discover icon and where the relationship was not being removed after a user deleted the relationship.

## April 11, 2018

### Enhancement

The image in the header now follows the theme from the login page in all components. The Guidance, and Notifications icons are now displayed on all pages in Entota™.

## April 6, 2018

### Bug Fix

IGC-1137 – Fixed an issue where endorsing or contesting an asset that had unsaved changes in other fields (for example, Assigned To) would cause the changes in the other fields to be lost. Also fixed an issue where after clicking Cancel to discard changes to an asset, the Cancel and Save options would be re-displayed even though there were no changes to cancel or save.

## April 2, 2018

### Enhancements

* The Change History modal for Systems now displays information about the fields imported. The following is now recorded in change history:
    * The user who loaded the fields.
    * The date and time stamp of the upload.
    * The number of fields uploaded.
Refer to Set Up a System and View Change History for Assets for more information.

* The Change History modal for Data Sets now displays information about changes to fields in a Data Set. The following is now recorded in change history for Data Sets:
    * Field added to a Data Set
    * Field removed from a Data Set
    * Owner on a field in a Data Set changed
    * Classification for a field in a Data Set changed
Refer to Set up a Data Set and View Change History for Assets for more information.