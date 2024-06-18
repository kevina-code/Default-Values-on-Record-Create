This is a robust solution of defaulting values in record creation screens. It serves as an alternative to using:
```/lightning/o/ObjectName/new?defaultFieldValues``` 
but with greater customizability like validating on quick action button click. 

Implementation steps:

1. Deploy the package to your org
   
3. Create your action button:
   
Action Type: Lightning Web Component
Lightning Web Component: navToNewRecCreateModalWithDefaults
Label: desired label for button
Naming convention: NameOfObjectGettingCreated_XXXXX_Create_Object
Example: Opportunity_XXXXX_Create_Opp

4. reate a Default_Values_Field_Mapping__mdt record for each field you want to map to the object getting created when the action button is clicked. See screenshot for an example field mapping.
