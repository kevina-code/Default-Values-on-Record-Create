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


Flow use case:

Instead of invoking the record creation screen with prepulated defaults from a Quick Action, we can do so from a flow as well.

**Step 1**: create a new screen flow that invokes the LWC:

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/d6bdb702-1727-412d-9fd0-461f9123ea62)

**Step 2:**: configure the screen flow node that invokes the LWC:

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/a4c128f9-afb6-4689-b415-ee12274c94e6)

**Step 3:**: add the flow to a Lightning Record Page:

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/731b0145-b033-4bf6-91f7-35e7b0e8d217)

**Step 4:**: create Default Value Field Mapping (Custom Metadata Type) records for each field you want to map from parent to object getting created:

![image](https://github.com/kevina-code/Default-Values-on-Record-Create/assets/124932501/c34e172f-aec2-4a6e-82de-7f7463bfffe6)

