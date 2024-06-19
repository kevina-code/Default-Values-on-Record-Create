This is a robust solution of defaulting values in record creation screens. It serves as an alternative to using:
```/lightning/o/ObjectName/new?defaultFieldValues``` 
but with greater customizability like validating on quick action button click. 

Implementation steps:

1. Deploy the package to your org
   
2. Create your action button:
   
**Action Type**: Lightning Web Component

**Lightning Web Component**: navToNewRecCreateModalWithDefaults

**Label**: desired label for button

**Naming convention**: NameOfObjectGettingCreated_XXXXX_Create_Object

Example: Opportunity_XXXXX_Create_Opp

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/212a88ac-dedf-4db7-a507-a2f46268e884)

3. Create a Default_Values_Field_Mapping__mdt record for each field you want to map to the object getting created when the action button is clicked. See screenshot for an example field mapping.

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/53fede59-c9de-43e8-9cbd-754d43799f83)

When your action button is clicked, it will open the record creation model and populate the defaults within the modal:

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/d58d66d0-5f98-4840-b47f-86d3cfc7a726)
