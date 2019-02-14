---
id: EntotaReleases0718
sidebar_label:  July 2019
title:  July 2019
---

# July 2019

## July 27, 2018

### Enhancement

Guidance has been added so that if a user does not have permission to edit an asset, the panel is no longer blank, but tells the user that permission is required.
Bug Fixes

* [IGC-1437] – Fixed an issue where a user could not edit a sponsor in IE 11.
* [IGC-1436] – Fixed an issue where a rule could not be added to a term in IE 11.
* [IGC-1424] – Fixed an issue where related terms with long names were partially hidden by the guidance panel.
* [IGC-1430] – Fixed the formatting of the user name display in the upper right in IE 11.
* [IGC-1433] – Fixed an issue where it was difficult to remove sponsors with long names on Vision and Mission goals and initiatives because the long name obscured the x to remove it.
* [IGC-1434] – Fixed an issue where the x that displayed on supporting documentation throughout the IGC was formatted incorrectly in IE 11.
* [IGC-1435] – Fixed an issue where a user with a long name who was assigned to an asset could not be edited or removed in IE 11.
* [IGC-1439] – Fixed an issue where the presence of a long policy name prevented the user from entering data in other policy fields.
* [IGC-1440] – Fixed an issue where clicking Cancel when editing supporting documentation on an asset did not cancel the changes.

## July 23, 2018

### Enhancements

* Guidance has been updated for assets.
* The Critical Data Element toggle switch has been reduced in height on the Term detail page.
* The spacing and padding in the Comments sections of the asset detail pages has been updated.

Bug Fixes

* [IGC-1418] – Fixed an issue that prevented the My Profile page from displaying in IE 11.
* [IGC-1426] – Fixed an issue where users adding a new policy were able to click the Save button without setting the required Policy Type field, resulting in an error.

## July 20, 2018

### Bug Fixes

* [IGC-1417] – Fixed an issue that prevented the Privacy Policy modal from displaying.
* [IGC-1431] – Fixed an issue that prevented the New Goal and New Initiative icons from displaying on their respective asset detail pages.
* [IGC-1407] – Fixed an issue where the page that displayed after users updated their profile was not the page that they were working in, but the previous page in their navigation.

## July 17, 2018

### Bug Fixes

* [IGC-1421] – Fixed an issue where policy definitions were not always appearing as expected in search results.
* [IGC-1423] – Fixed an issue that prevented the user from assigning a user to an asset when adding an asset via the Quick Add modal.

## July 16, 2018

### Enhancements

* The appearance of fonts, styles, and icons has been updated throughout Entota™:
    * On the header area of the detail pages for assets
    * On the list to select relationships between terms
    * For text input fields on asset detail pages
* The Term detail page layout has been updated.
* The appearance of the Guidance panel has been updated to improve readability.
* Guidance for Vision has been updated.
* The Critical Data Element has been updated from a check box to a toggle switch on the Terms detail page.
* Hover text has been added to the navigation icons: Deep Guidance, Navigation and Notifications.

## July 12, 2018

### Enhancement

Guidance for adding system fields has been added.

### Bug Fixes

[IGC-1413] – Fixed the display of the edit icon next to the program name on the landing page. For users who do not have custom permissions to edit the program, the icon no longer displays.

## July 10, 2018

### Enhancements

* Security options have been updated for Entota™. You can now set permissions for user access to Data Catalog and Strategy components.
* User and Approver permissions have been added to all assets.
* For Data Catalog, Users and Approvers are granted read-only permission only.
* User permission allows a user read-only access to a component. This type of user can add comments, share a URL and view change history for an asset, but cannot sponsor an asset or otherwise edit it.
* If a user has User permission for a component, that asset does not display in the Quick Add list because the user cannot add the asset. Additionally, guidance related to adding or editing assets does not display for a user with User permission.
* If a user has Approver permission, the user can sponsor an asset in the Strategy, Policy, and Glossary components.
Refer to Add a User to Entota™ for more information.

> IMPORTANT: With this security update, all users are granted “User” level, read-only access by default. *This means that existing users no longer have the ability to edit Strategy(Visions, Missions, Goals and Initiatives), Data Sets, and Systems.* To restore these permissions, the platform administrator must update these users' custom permissions for the Strategy and Data Catalog components.

Refer to Edit a User Account for more information.

## July 5, 2018

### Enhancements

* The Status field has been added to the Goal and Initiative detail pages.
* A font family has been added to the UI to allow for more font weights.

### Bug Fixes

* [IGC-999] – Fixed an issue where, on a company goal’s detail page, the Status for related program goals was not being updated in the Contains Program Goals section when the status was updated on the program goal’s detail page.
* [IGC-778] – Fixed an issue where it was possible to add a large amount of text to the Term field, which caused an error, by limiting the amount of text allowed in the Term field.
* [IGC-1388] – Fixed an issue where, when working in the Admin section, clicking the Jump To options resulted in an error.
* [IGC-1338] – Updated the watermark in the link field when adding a URL to a Policy definition to indicate that the http:// or https:// is required.