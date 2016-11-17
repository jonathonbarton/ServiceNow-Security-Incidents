# ServiceNow-Security-Incidents
In ServiceNow, hide Security-related fields on the Incident Form.

The business requirement was:
* Add 4 fields to the INC form to track security vulnerabilities.
* Only allow IT Security to determine which INC are Security Vulnerabilities.
* However, once ITSec has determined that the INC is a vulnerability, the INC may be assigned to other teams, and THEY should be able to update the 4 fields.
* Other groups should not be able to unset the Security Vulnerability checkbox.

SOLUTION:
* Create a new form section that contains the 4 user-defined fields (3 strings, 1 date)
* UI Policy to hide the Security Vulnerability checkbox unless the INC is assigned to the ITSec team.
* Client Script to hide the new form section (tab) unless the checkbox is checked. 
