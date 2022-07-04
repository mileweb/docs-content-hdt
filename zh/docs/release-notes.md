# Release Notes

## Jun 23, 2022
### API updates
1. Added query parameter 'scope' for GET /report/flow and GET /report/requests.
2. Updated APIs of service quota to meet the requirements of trial customers.
3. Added a scheduler to check trial deadline and traffic usage of trial customers, and send out notifications.
4. Added a scheduler to disable transport service when a trial deadline or traffic limit has been reached.
5. Reorganized the acceleration regions of existing transports.
6. Made API query parameters case-insensitive for easy use.

### Portal updates
1. Added a notification module for pushing news about service updates and marketing promotions.
2. Added reminders for trial date and traffic usage when trial customers log in in the portal.
3. Reorganized the acceleration regions.
4. Display query filters when downloading the billing reports.
5. In Reports page, set 'All' as the default value for access domain selection and limited the number of access domains and transports that can be selected.
6. Adjusted the buttons in the transport query page.
7. Updated message information text when viewing or managing transports.
8. Improved session timeout control.
 
## Dec 6, 2021
### API updates
1. Supported modifying acceleration regions of exiting transports.
2. Supported managing transport shield by specifying regions.
3. Added APIs to get service quotas, billing data, and resource summary.

### Portal updates
1. Supported selection of acceleration regions.
2. Supported managing fixed shields.
3. Added validations for access domain, including ICP Beian check and cross check with target domain.
4. Improved download performance by using local storage for fonts.

## May 27, 2021
### API updates
1. Supported selection of acceleration region for HTTP and HTTPS applications.
2. Added PoP management APIs.

### Portal updates
1. Improved page displays.
2. Added validation of access domain and ICP Beian license when managing a transport.
3. Fixed the display issue for logout confirmation.
4. Updated PoPs data.

## March 9, 2021
### API updates
1. Added Virtual Private Line (VPL) attributes.
2. Supported range-report in report APIs.

### Portal updates
1. Supported IPv6 applications.
2. Paid customers of VPL can view VPL usage dashboards and reports.
3. Supported reports query of deleted transports.
4. Added input validation and tool tips in transport page.
5. Updated PoPs (point of presence) data.

## December 18, 2020
### API updates
1. Added transport management APIs.
2. Added reports query APIs.

### Portal updates
1. Supported transport management.
2. Added reports query page.
3. Added Global Presence page.
4. Enabled Central Authentication Service for Single Sign On.
5. Supported customer impersonation for resellers.
