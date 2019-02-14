+++
title = "Migration Dashboard"
weight = 2
+++


The Migration dashboard, available with DSP 7.0.1 and later, provides
visibility into progress and status associated with enterprise Data
Migration efforts by giving you access to the most important migration
project metrics.

Using this dashboard you can:

-   Understand the current status of migration waves
-   Identify any waves that are running behind schedule
-   Ascertain go-live readiness for a wave

Whether you are responsible for one or multiple waves, across a single
instance or multiple instances in the DSP, you can view progress against
milestones to assess risk, determine a need for resource adjustment and
communicate effectively to all project stakeholders.

**NOTE**: The waves that display on the dashboard, along with their
milestones and thresholds, are configured in the DSP. Refer to
[Configure the Migration
Dashboard](https://dsphelp.boaweb.com/702/general/Configure%20the%20Migration%20Dashboard.htm)
for more information.

The Migration dashboard can be used on desktop, iOS 11 or later, and
Android Oreo, using Chrome, IE 11 and Safari browsers.

This topic contains:

-   [Access the Migration Dashboard](#Access)
-   [When should I configure the Wave to send metrics to the
    Dashboard?](#When)
-   [When will Metrics Percentages Increase from 0%?](#When2)
-   [When is data sent to the Dashboard?](#When3)
-   [Project Waves Timeline Chart](#Project)
-   [Milestone Details](#Mileston)
-   [Migration Dashboard Detail Page](#Migratio)

[]{#Access}Access the Migration Dashboard
-----------------------------------------

If you are assigned the Migration persona, the Migration dashboard
displays when you log in to Entota. If you do not have access to the
dashboard, your Entota tenant administrator should be able to help, or
you can send an email to your Customer Success Team.

If you have purchased a subscription for Entota, access it by clicking
the menu link in the upper right of the Migration Dashboard.

When in Entota, click the Entota logo in the upper left to access the
Migration dashboard.

**NOTE**: To access the Migration dashboard as you would an app on your
mobile device, use the Add to Home Screen feature. It launches in full
screen mode, can be switched with other tasks, and supports the
device\'s default orientation.

[]{#When}When should I configure the Wave to send metrics to the Dashboard?
---------------------------------------------------------------------------

Configure a wave within the DSP to send data to the dashboard after the
initial structure of the wave (wave, process areas and objects) has been
defined and the first steps of Target Design have begun. The first
metrics displayed on the Dashboard are Design Complete, thus there is no
requirement to configure the Wave to send metrics data to the dashboard
until after Target Design has started.

[]{#When2}When will Metrics Percentages Increase from 0%?
---------------------------------------------------------

After the wave is configured to send data to the dashboard the metrics
are calculated for all four milestones.

-   Design Complete percentage rises above 0% once targets are assigned
    a design status of Design Finished or Complete in Target Design in
    the DSP.
-   Mappings Complete is calculated across both field and value mapping
    and rises above 0% once a Target Design is synced to Map in the DSP.
-   Rules Complete percentage increases once source and target rules
    that are defined in Target Design and Map have been assigned a
    status of Complete in Map in the DSP.
-   Data Quality is calculated when a user registers a target report for
    each of the Opportunity reports and Error reports in the DSP. The
    calculation compares the record counts in each of these registered
    reports to calculate a quality percentage.

Flexibility is built into the Data Quality metric calculation. In the
DSP, a user can register an Opportunity report and Error report for each
target defined within the wave. In most situations, a single Opportunity
report and Error report is defined using the Target Report syntax
tv...Sel at the top-level target for the object.

For example, for SAP Material, the top-level target is MARA (Material
Basic Data). The Opportunity report counts all materials in the target
table data set and the Error report counts all distinct material IDs
that have an error at any level of the Material target data structure
(errors in MARC, MARD etc). By defining the reports in this way, a
simple calculation can be performed at an object level which is then
rolled up across all objects within the wave. Refer to [Configure the
Migration
Dashboard](https://dsphelp.boaweb.com/702/general/Configure%20the%20Migration%20Dashboard.htm)
for more information.

[]{#When3}When is Data Sent to the Dashboard?
---------------------------------------------

Data is sent to the Migration dashboard when:

-   A wave has been created and added to the Migration dashboard
    following the steps in Configure the Migration Dashboard
-   A wave that has been added to the Migration dashboard has the name,
    description, start date or end date updated in Console in the DSP
-   A wave is deleted in Console
-   A milestone is created by the user in the DSP
-   A milestone is updated by the user in the DSP
-   A user-created milestone is deleted in the DSP

By default, when a wave is configured to be included in the dashboard, a
start and end date milestone are added and the thresholds are set at 0%.

The dashboard does not display data if:

-   The waves have not been configured in the DSP.
-   Waves have been configured but the end dates for all waves have
    passed by one month.
-   There is an issue with the data, connectivity, or other errors. In
    this case, a link to Customer Support displays.

A wave does not display on the dashboard if:

-   The wave has been configured in the DSP, but the current date is
    greater than one month past the wave's end date
-   The wave has been configured in the DSP, but has then been deleted
    from Console in the DSP

A DSP user can also configure metrics data to stop being sent from the
DSP. In this case, the metrics data no longer updates, but does continue
to display in the detail row on the dashboard.

[]{#Project}Project Waves Timeline Chart
----------------------------------------

The Project Waves Timeline Gantt chart displays all waves that:

-   Have been configured to display in the DSP
-   Have an end date that is less than 28 days from the current date

Waves are sorted in the chart by end date in ascending order. The wave
with the next end date displays first.

The time span displayed on the timeline is based on the earliest start
date and the latest end date for all waves.

On a desktop, hover your cursor over a wave to see the day for the start
and end date. On a device, tap the wave once to see the details.

On a desktop, to view the milestone details, click the wave in the
timeline, or scroll down. On a device, tap the wave twice to scroll to
the details for that wave.

[]{#Mileston}Milestone Details
------------------------------

Detail rows are also sorted by wave with end date in ascending order.
The wave with next end date displays first. If multiple waves have the
same end date, they are then sorted by start date in ascending order.

The data is current as of the Last Updated date and time displayed in
the upper right of the dashboard. Metrics data is updated hourly.

For each wave, the start and end date display, followed by metrics data
related to each milestone in a detail row. All waves have a start and
end date milestone by default. Additional milestones can be added in the
DSP.

The following metrics display for each milestone.

-   Design Complete indicates how much of the design work has been
    completed. This percentage is calculated as the total number of
    active fields within active targets where design is complete (the
    design status is Design Complete or Finished) divided by the total
    number of active fields within active targets, regardless of design
    status.
-   Mappings Complete indicates how much of the field mapping and value
    mapping work has been completed. This percentage is calculated as
    the total number of total mappings opportunities for both value and
    field mapping divided by the total number of mappings in Complete
    status.
-   Rules Complete indicates how many of the rules have been completed.
    This percentage is calculated by the total number of source and
    target rules for the active fields with a rule status of Complete
    divided by the total number of source and target rules (also called
    rule opportunities).
-   Quality indicates the data quality of the wave. This percentage is
    calculated using the totals on the Error reports registered to the
    wave and targets (post load reports) divided by the total number of
    records on the Opportunity reports registered to the waves and
    targets (preload reports).

On a desktop, hover your cursor over a metric to view details about the
milestone date, current percentage, milestone goal and thresholds. On a
device, tap the metric to view these details.

The metrics percentage calculations listed above are compared to the
thresholds configured in the DSP in relation to the milestone date. If
the percentage calculation is equal to or greater than the upper
threshold percentage, this milestone is complete and the detail row for
the metric displays green on the dashboard. If the percentage
calculation is between the upper and lower thresholds, the detail row
for the metric displays light blue. If the percentage calculation is
less than or equal to the lower threshold, the detail row for the metric
displays red.

**NOTE**: If a milestone is added for the current date, it does not
display in the dashboard.

[]{#Migratio}Migration Dashboard Detail Page
--------------------------------------------

Users with the Migration persona can view additional details about a
migration project's progress on the Migration Dashboard's Detail page.
The Detail page is also a dashboard, and allows you to understand prior
trends and current progress being made towards the defined milestone
thresholds per wave.

The data is current as of the Last Updated date and time displayed in
the upper right of the Detail page. Data is updated and refreshed on the
Detail page hourly.

All waves have a start and end date milestone by default. Milestones are
added in the DSP.

The Detail page contains these sections.

-   **A Gantt chart displaying a timeline for milestones for the
    selected wave**. As with the Migration Dashboard, milestones are
    sorted in the chart by end date in ascending order. On a desktop,
    hover your cursor over a milestone to see the the start and end
    date. On a device, tap the milestone once to see these details. The
    timespan displayed on the timeline is based on the earliest start
    date and the latest end date for all milestones for the wave.
-   **Current Metric values compared to next Milestone.** Hover over
    each metric to view details about the milestone date, the current
    percentage, and the threshold percentage range. On a desktop, hover
    your cursor over a milestone metric to see the the details. On a
    device, tap the milestone metric once to see the details.
-   **A line chart with history of progress on the current milestone's
    metrics**, using data collected metrics from the Start Date of the
    wave to the current date. The X-axis includes the beginning and end
    dates of collected data for the wave. There is a line for each of
    three of the metrics. The Data Quality metric is not tracked on the
    History line graph. On a desktop, hover your cursor over a date
    point in the line to see the details. On a device, tap the line to
    view these details.
-   **A table with details about each milestone's targeted and actual
    percentage for the metrics.** The actual value is calculated from
    DSP data. The target value ranges are the threshold values set in
    the DSP. A red icon displays next to those at risk values that are
    below the low threshold range for the milestone. A green icon
    displays in the first column to indicate a milestone whose
    percentages have met or exceeded their threshold values and is
    therefor complete.

To return to the Migration Dashboard, click the wave name at the top of
the Detail page.
