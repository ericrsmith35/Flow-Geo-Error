# Flow-Geo-Error
Test code to reproduce a datatable error with LWC, Flow and GeoLocation Fields

This includes a simple datatable LWC to display records from the standard Contact object. 
There is also a test Flow that displays a datatable of Contact records with record selection enabled.  

# Instructions
Install the 'dtGeoError' LWC and the 'Test Geo Error' Flow into an Org
Add a custom field to Contact called 'geo'.  There is no need to populate any data for this field in any records.

Connect the Flow Start element to one of the three Get Records elements and run the Flow.
Select some records and goto the Next screen to display just the selected records using the same datatable component.

Only the Get All Contacts - Choose Fields will work.

## Get All Contacts - Choose Fields ##
Choose fields and let Salesforce do the rest
- Id
- Name
- Phone
- Title
- geo__Latitude__s
- geo__Longitude__s

## Choose Fields - FAIL ##
Choose fields and let Salesforce do the rest
- Id
- Name
- Phone
- Title
- geo__Latitude__s
- geo__Longitude__s
- geo__c

## Auto Fields - FAIL ##
Automatically store all fields


