Laptop Request Catalog Item – ServiceNow Project

 Problem Statement:

Employees in an organization need a quick and efficient way to request laptops for work.
The existing manual process is slow, error-prone, and lacks dynamic form behavior.

Solution: Build a ServiceNow Service Catalog Item that allows employees to easily request laptops, with dynamic fields, validation, reset functionality, and governance tracking via Update Sets.

 Project Setup
1. ServiceNow Instance

Sign up at ServiceNow Developer Portal

Request a personal developer instance (latest release).

2. Local Update Set

Create an Update Set named Laptop Request.

Ensure all changes are recorded under this Update Set.

3. Service Catalog Item

Create a Catalog Item:

Name: Laptop Request

Catalog: Service Catalog

Category: Hardware

Short Description: Use this item to request a new laptop

 Variables Created

Laptop Model – Single Line Text

Justification – Multi Line Text

Additional Accessories – Checkbox

Accessories Details – Multi Line Text

 Dynamic Behavior

UI Policy: Shows and makes Accessories Details mandatory when Additional Accessories is checked.

 UI Action (Reset Button)

Table: sc_cart

Action Name: Reset Form

Script:

function resetForm() {
    g_form.clearForm(); // Clears all fields in the form
    alert("The form has been reset.");
}

 Update Set Migration

Export the Update Set (Laptop Request) as XML.

Import into another instance via Retrieved Update Sets.

Preview → Commit to apply changes.

 Testing

Navigate to Service Catalog → Hardware.

Open Laptop Request item.

Verify dynamic behavior:

Checking Additional Accessories → shows & requires Accessories Details.

 Conclusion

This project:

Automates laptop request handling.

Replaces manual processes with a streamlined ServiceNow workflow.

Improves accuracy, efficiency, and employee satisfaction.

 Repository Contents
 Update-Set/ → XML file of the project
 README.md → Documentation (this file)

Update-Set/ → XML file of the project

README.md → Documentation (this file)
