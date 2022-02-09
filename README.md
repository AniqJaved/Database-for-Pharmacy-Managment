# Database-for-Pharmacy-Managment
This repositry involves creation of database for the pharmacy. It involves various use cases.
## Project Description
### Entities:
The entities in our pharmacy management system are:
1. Doctor
2. Patient
3. Pharmacy
4. Pharmacist
5. Drug
6. Drug manufacturer

Doctor:

Doctor has three attributes. Dr_ID is primary attribute and doctor name and specialization are other attributes.

Patient:

Patient has five attributes. Patient_Id is primary attribute and Name, sex, are regular attributes. Contact is a multi-Valued attribute because may have two or more contact number and address is composite attribute which have city and house no.

Pharmacy:

Pharmacy has four attributes. Phar_Id is primary attribute and Name and contact no. are other attributes. Address is composite attribute which have city and house no.

Pharmacist:

Pharmacist has two attributes. Pharmacist_Id is primary attribute and Name is other attributes. 

Drug:

Drug has three attributes. Trade_No is primary attribute and Name and QR code are other attributes. 

Drug manufacturer:

Drug manufacturer has three attributes. Manufacture_Id is primary attribute and Name is other attributes. Address is composite attribute which have city and house no. 
###  Relationships:

Consult:

It is binary relationship between Patient and Doctor. Zero or many patients can consult to one or many doctor.

Prescribe:

It is ternary relationship between Patient, Drug and Doctor. So, it become associative entity. It has attribute date. One Doctor will give one or many Drugs to one Patient.

Manufacture:

It is binary relationship between Drug Manufacturer and Drug. Zero or many drug manufacturer will make one or many Drugs but drug will be made be mandatory one or many manufacturer.

Sell:

It is binary relationship between Pharmacy and Drug. One or many drug will be sold at one or many pharmacies. Sell has its attribute price.

Contract:

It is binary relationship between Pharmacy and Drug manufacturer. One or many drug manufacturer will make a contract with one or many pharmacies. Contract has its start_date and end_date of contract as attribute.

Work:

It is binary relationship between Pharmacy and Pharmacist. One or many pharmacists will work at one pharmacy. Work has its shift_start and shift_end as attribute.
## Files description
1. The file Creation of tables is for creating the tables where the data for the pharmacy managment system will be stored.
2. The file Raw_entries is used to add the raw values in the table.
3. The file trigger_1 (save all deleted drug into deleted_drugs table) is used to show the event driven entries of table which invloves insertion, update or deletion of the entries.
4. The file trigger_2 (No drug can be sold at price greater than 1000) is used to show the event driven entries of table which invloves insertion, update or deletion of the entries.
5. The below files include the sample queries which are run to check the functionality of the database system.
  1. sample_query_1 states the following problem: Show all drugs that are not prescribed yet.
  2. sample_query_2 states the following problem: Give the name of Doctors who are Gynecology specialist.
  3. sample_query_3 states the following problem: Give the name of pharmacist and pharmacy contact no of pharmacy whose phar_id is PH_101.
 
6. The below files include the sample view
  1. sample_view_1 states the following problem: Create view named as Prescribed_Drug containing Prescribed_Date, Drug_Name, Manufacturer_Name
  2. sample_view_2 states the following problem: Create view named as Drug_price that contains the drug trade no, name and price at which it is sold.
