# Release Note { #tb-cs-release-note }

## 3.0.0

A new independent release of the updated TB Case Surveillance Tracker package with new content. This release is based on the [WHO Consolidated guidance on tuberculosis data generation and use](https://www.who.int/publications/i/item/9789240075290) from 2024.

This version is not compatible with previous versions of the TB Case Surveillance Tracker packages and can be imported in an instance with an existing TB Case Surveillance tracker.

### Linkage with TB HMIS package

TB Case Surveillance tracker is closely linked with the newest TB HMIS package. It contains program indicators and aggregate data exchanges that allow automatic aggregation of case-based data and its import into the aggregate data sets. More information can be found in the design and installation guides.

## 2.1.0

A new version of the TB Case Surveillance Tracker package (2.1.0) has been released with new content, configuration fixes and improvements.

### Linkage with TB Household Contacts Investigation Tracker

TB Case Surveillance is closely linked with the TB Household Contacts Investigation program that tracks the household contacts of bacteriologically confirmed new episodes of pulmonary TB. The **Notification and Diagnosis** stage in TB Case Surveillance has a section that becomes available for data entry once such a case has been identified. The users are prompted to enter the number of people (excluding the index case) living in the same household. The user can then enroll these contacts in the [TB Household Investigation tracker](#tb-hh-design) using the relationship widget. The configuration of the relationship type is described in the [installation guide](#tb-hh-installation) of the TB Household Investigation tracker.

The Indicator "TB-HH - Cases diagnosed with a new episode of bacteriologically confirmed PTB" has been configured to provide denominator data for the Household Contacts module in the TB HMIS package.

### Linkage with TB HMIS Package

TB HMIS aggregate module has been significantly changed in accordance with the latest WHO strategic information guidelines for tuberculosis programmes (2023). The program indicators that aggregated data for the TB HMIS package have been removed from the module. The new set of indicators is in planning and will be released in 2024.

### Fixes and Improvements

Program rule and program indicator expressions and filters have been reviewed and aligned with the latest design principles and syntax rules.

## 2.0.0

A new version of the WHO-approved TB Case Surveillance Tracker package (2.0.0) has been released with new content, configuration fixes and improvements.

### Enrollment Stage

In version 2.0.0 the diagnosis was moved from the “Enrollment” to the “Diagnosis and Notification” stage for better support of the laboratory vs clinical workflows. The diagnosis and notification of a confirmed case can therefore happen once the diagnostic test results are available and the clinician can confirm the case together with the baseline information, the risk factors, and the HIV status.
Once a case is diagnosed/confirmed/notified, the user is prompted to enter the TB registration number in the “Enrollment” stage.

### Denotification of a negative presumptive case

In version 1.0.1, denotification was possible in the “Outcome” stage and supported two scenarios:

   1. Denotification of a duplicate case
   2. Denotification of a case notified/confirmed as a result of human error

In version 2.0.0 that supports enrollment of presumptive cases, denotification of a negative presumptive case can happen directly in the "Diagnosis and Notification" stage. Such cases will be excluded from the analysis (except for the lab data).

### Laboratory Results Stage

Version 1.0.1 contained only one repeatable laboratory stage in which all the tests were entered and displayed.

In version 2.0.0, laboratory stage was renamed into “Diagnostic Laboratory Results” stage. Additional sample related variables were added. A new “Monitoring Laboratory Results” stage has been added. Both stages are repeatable. With this design, it is easier to distinguish between the tests that were performed for diagnostic purposes and those performed for monitoring purposes among the confirmed cases.

### Working Lists

Version 2.0.0 contains only 2 working lists in the tracker dashboard:
“All current enrollments” and “Enrollment completion pending”

For custom working lists that can filter enrollments by specific data coming from a specific program stage, it is recommended to configure relevant SQL views or use line lists.

### Notifications (system, SMS, etc)

Version 2.0.0 contains four notification templates that allow users to send messages to clients and other program users. These include notification, denotification and poor sample quality notifications.

### Fixes and Improvements

For further information on the differences between the two versions of the TB-CS tracker, implementers and users can refer to the [diff file](resources/tb_cs-1.0.1-vs-2.0.0.xlsx).
