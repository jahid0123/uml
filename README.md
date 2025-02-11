Question: 1
Advertisement Campaign Management

Adwell is small adveritising agency. The following passage describes how Adwell runs advertising campaigns.

Adwell deploys two types of staff in an advertising campaign. The technical staff are responsible for the design and implementation of the customer’s requirements. The administrative staff are responsible for the management controll of the campaign. They manage all exchanges between the technical staff and the customer through the administrative system. Staff are called employees. Adwell keeps a record of all of the employee’s names and start date. Each employees has an employee number. For technical staff a note is made of their area of skill and their availability. For administrative staff is made of their qualification.
When a customer commissions an advertising campaign, Adwell’s administrative staff records the campaign details. The customer provides company name, address, fax number and a contact person. The campaign has a title, a set of requirements, a start date, an end date and a budget cost. The campaign is compossed of several advertisements. Each advertisment has a title , a target date, estimated cost and an actual cost. Adwel deals with two types of advertisement. For a newspaper advertisement the newspaper, the placement, date and repeat dates are recorded, the Newspaper company, which owns the newspaper, supplies this placement availability information. For a website advertisement, the website provider, the start date, and the end date are recorded.

A campaign begins life when a customer proposes it. Adwell’s technical staff assess the propossed campaign but if it looks unsatisfactory they advise against it and it becomes a discarded campaign. Usually the technical staff consider a campaign to be satisfactory and it becomes a recommended campaign, A recommended campaign may be subject to revision if the customer wants one or more changes and Adwell’s technical staff aproved these. The campaign becomes a commisioned campaign when the customer commission it. When the first advertisements are produced by the technical staff the campaign becomes and underway campign. Where it is underway the campaign can be stopped if the customer is unhappy about the response to it and it is marked as a stopped campaign. Othewise a campign becomes a completed campaign when the customers makes the final payment.

Produce the following UML diagrams:

a.	Use case diagrams describing the processes that take place in this system and the actors that ............ and take part in the system. Consider how many system you may need and show the system ........... ......... Draw at least two systems with their appropriate actors, use cases and system boundary, Provede full and detailed descriptions for three use cases.

Use Cases for the Campaign Management System (CMS):
Propose Campaign (Customer proposes a campaign to Adwell)
Record Campaign Details (Administrative staff records the campaign information)
Assess Campaign (Technical staff assesses the feasibility of the campaign)
Advise Campaign (Technical staff advises on whether to proceed with the campaign)
Revise Campaign (Technical staff revises the campaign based on customer feedback)
Stop Campaign (Administrative staff stops a campaign if the customer is unhappy)
Complete Campaign (Administrative staff marks the campaign as completed when the customer makes the final payment)


Actors and Use Cases for the Employee Management System (EMS)
Actors:
Administrative Staff: Manages employee records (both technical and administrative staff).
Use Cases:
Manage Employee Records (Administrative staff manages general employee data).
Manage Technical Staff Information (Administrative staff records technical staff skill and availability).
Manage Administrative Staff Information (Administrative staff records qualifications of administrative staff).

b.	A class diagram showing the classes involved in the system, their attributes, methods. relationships and relationship multiplicity. Show at least one example of each one of the following concepts inheritance, aggregation and composition.

B. Class Diagram
Here is a class diagram representing the core entities, their attributes, methods, relationships, and multiplicities in the system.

Classes and Relationships
Campaign

Attributes:
campaignTitle (String)
startDate (Date)
endDate (Date)
budget (Double)
status (String)
Methods:
proposeCampaign()
recordDetails()
assessCampaign()
markComplete()
Advertisement (Superclass for Newspaper and Website Ads)

Attributes:
adTitle (String)
targetDate (Date)
estimatedCost (Double)
actualCost (Double)
Methods:
createAd()
setCosts()
NewspaperAdvertisement (Subclass of Advertisement)

Attributes:
newspaperName (String)
placement (String)
repeatDates (Date[])
Methods:
setRepeatDates()
WebsiteAdvertisement (Subclass of Advertisement)

Attributes:
websiteProvider (String)
startDate (Date)
endDate (Date)
Methods:
setWebsiteDetails()
Employee

Attributes:
employeeName (String)
startDate (Date)
employeeNumber (String)
Methods:
updateEmployeeInfo()
TechnicalStaff (Subclass of Employee)

Attributes:
areaOfSkill (String)
availability (String)
Methods:
updateSkill()
updateAvailability()
AdministrativeStaff (Subclass of Employee)

Attributes:
qualification (String)
Methods:
updateQualification()
Relationships:
Aggregation:
A Campaign can have multiple Advertisements (1..* relationship).
Composition:
A Technical Staff is a specialized Employee and cannot exist without an Employee (composition between Employee and TechnicalStaff).
Inheritance:
TechnicalStaff and AdministrativeStaff inherit from Employee (inheritance relationship).


+---------------------+    +--------------------------+
|      Campaign       |<>--|      Advertisement       |
+---------------------+    +--------------------------+
| campaignTitle       |    | adTitle                  |
| startDate           |    | targetDate               |
| endDate             |    | estimatedCost            |
| budget              |    | actualCost               |
| status              |    +--------------------------+
+---------------------+    |                          |
| proposeCampaign()   |    +---------------------------+  
| recordDetails()     |    | WebsiteAdvertisement      |
| assessCampaign()    |    +---------------------------+
| markComplete()      |    | websiteProvider           |
+---------------------+    | startDate                 |
                           | endDate                   |
                           +---------------------------+  
                           |                          |
                           | NewspaperAdvertisement    |
                           +---------------------------+
                           | newspaperName             |
                           | placement                 |
                           | repeatDates               |
                           +---------------------------+

     +--------------------------+
     |        Employee           |
     +--------------------------+
     | employeeName             |
     | startDate                |
     | employeeNumber           |
     +--------------------------+
     | updateEmployeeInfo()     |
     +--------------------------+
            ^
            |
+-----------+-----------+  
|                       |
+-------------------+  +------------------------+
| TechnicalStaff    |  | AdministrativeStaff    |
+-------------------+  +------------------------+
| areaOfSkill       |  | qualification           |
| availability      |  +------------------------+
+-------------------+
| updateSkill()     |
| updateAvailability()|
+-------------------+



c.	An Object Interaction Diagram (OID) or Message sequence Diagram which shows one .......... sequence of events for one of the identified use cases. You do not need  to draw OID’s for all the identified use cases. one is sufficient for this questions.


d.	A state transition diagram for one appropriate class from the diagram.


 
Question: 2
World Traveller

You have been asked to analyses and design a system for World Traveller. You have been given the following requirements from the staff of world Traveller. World Traveller is a travel agency, which arranges a variety of travel arrangements. All customers are registered with a sales consultant who records their requirements. The sales consultant has to refer to many different flight timetables, hotel locations and holiday agencies. The sales consultant tries to match the customer requirements as closely as possible. If the specific requirement is not available, then the sales consultant advises the customer on a variety of alternatives to meet their choice and makes bookings on their behalf. The sales consultant also asks the customer if they would like world traveller to organize the holiday insurance and car hire at the same time. Once an itinerary schedule is completed, it is given to the customer in a form of a printout. Once the itinerary is accepted, the customer is billed. Complete payment must be received from the customertoconfirm the booking. If the customer would like to pay later, then a non-refundable deposit must be paid to provisionally book the holiday. Full payment must be received at least one week before the date of travel. If the customer would like to pay by credit card a 1.5% commission is added to the total bill. Once the customer has paid the full invoice they are provided with a receipt.

You are required to produce models to represent only the description provided above. This requirement specification is partial and incomplete description of the problem and you are asked to model it in a way that allows for further classes to be added when required. For example World Traveller only provide package holidays at present and the company may expand to provide other forms of holidays such as cruises repeat business trips, trips to multiple destinations, specialized holidays, and other types of travel, Which may be developed in the future. Another example may be that their billing and collection of payment may change. The model should be designed so it can be easily adapted to meet any changes.

Produce the following UML diagrams:


a.	Use case diagrams describing the processes that take place in this system and the actors that stimulate and take part in the system.  Consider how many systems you may need show the system boundaries. Draw at least two systems with their appropriate actors. Use cases and system boundary. Provide descriptions for all the use cases.

A. Use Case Diagrams for World Traveller System
To properly model the World Traveller system, we can break it into two main subsystems:

Customer Management System (CMS)
Booking and Payment System (BPS)
System 1: Customer Management System (CMS)
This subsystem handles all interactions related to customer registration, consultation, and the collection of their requirements for booking holidays.

Actors:
Customer: Initiates the travel request and interacts with the consultant.
Sales Consultant: Manages customer requirements, makes recommendations, and records their holiday preferences.
Use Cases for CMS:
Register Customer: The sales consultant registers the customer in the system.
Capture Customer Requirements: The sales consultant records the customer's holiday preferences, such as destinations, accommodations, and additional services (e.g., car hire, insurance).
Provide Alternatives: The sales consultant suggests alternative travel options when the customer’s first choice is unavailable.
Finalize Itinerary: Once the customer has chosen the holiday options, the sales consultant creates an itinerary for the customer.
System 2: Booking and Payment System (BPS)
This subsystem handles the booking process, payment options, and the eventual confirmation of the booking.

Actors:
Sales Consultant: Manages the booking, inputs customer payment information, and issues receipts.
Customer: Pays for the booking (either via credit card, deposit, or full payment).
System: Handles the calculation of payment, commissions, and invoice generation.
Use Cases for BPS:
Generate Itinerary Printout: After the itinerary is finalized, a printout of the itinerary is given to the customer.
Process Payment: The customer makes a payment. It could be full or a deposit (with a possibility of credit card payment).
Add Commission for Credit Card Payment: If the customer pays by credit card, a 1.5% commission is added to the total amount.
Confirm Booking: Once full payment is received, the booking is confirmed and a receipt is provided to the customer.
Record Deposit Payment: If a deposit is paid, the booking is provisionally confirmed, and the deposit amount is recorded.
Issue Receipt: The system generates a receipt for the customer once the full payment is made.



Descriptions of Use Cases:
Register Customer:

Actor: Sales Consultant
Description: A sales consultant registers a new customer in the system by entering their name, contact details, and other relevant information.
Capture Customer Requirements:

Actor: Sales Consultant
Description: The consultant collects the customer’s preferences regarding destinations, accommodations, flight requirements, and additional services like insurance or car hire.
Provide Alternatives:

Actor: Sales Consultant
Description: If a customer’s preferred holiday option is unavailable, the consultant offers alternative choices that are similar but meet the customer’s preferences.
Finalize Itinerary:

Actor: Sales Consultant
Description: The sales consultant compiles the customer’s choices into a detailed itinerary, which is then presented to the customer for approval.
Generate Itinerary Printout:

Actor: System
Description: Once the itinerary is finalized, the system generates a printable version of the itinerary that the customer can take home.
Process Payment:

Actor: Customer, Sales Consultant
Description: The customer makes a payment for the holiday, either as a deposit or full payment. This is recorded in the system.
Add Commission for Credit Card Payment:

Actor: System
Description: If the customer chooses to pay by credit card, the system adds a 1.5% commission fee to the total bill amount.
Confirm Booking:

Actor: Sales Consultant, System
Description: Once full payment is made, the booking is confirmed, and a receipt is generated for the customer.
Record Deposit Payment:

Actor: System
Description: If the customer pays a deposit, the system records the deposit amount and marks the booking as provisional.
Issue Receipt:

Actor: System
Description: Once full payment is received, the system generates and issues a receipt for the customer.






b.	A class diagram showing the classes involved in the system, their attributes, methods, relationships and relationship multiplicity. Show at least one example of each one of the following concepts inheritance, aggregation and composition.

B. Class Diagram for World Traveller System
Here’s the class diagram for the system, showing classes involved in the process, their attributes, methods, and relationships.

Classes and Relationships
Customer

Attributes:
customerName (String)
contactInfo (String)
customerID (String)
Methods:
updateContactInfo()
Sales Consultant

Attributes:
consultantName (String)
consultantID (String)
Methods:
registerCustomer()
recordCustomerRequirements()
finalizeItinerary()
HolidayPackage

Attributes:
packageName (String)
destination (String)
accommodation (String)
price (Double)
Methods:
checkAvailability()
suggestAlternatives()
Itinerary

Attributes:
itineraryID (String)
customer (Customer)
package (HolidayPackage)
totalPrice (Double)
paymentStatus (String)
Methods:
generatePrintout()
addPayment()
Payment

Attributes:
paymentID (String)
amount (Double)
paymentType (String) (Full/Deposit)
paymentStatus (String)
Methods:
processPayment()
addCommission()
Receipt

Attributes:
receiptID (String)
issueDate (Date)
totalAmount (Double)
Methods:
generateReceipt()
Relationships:
Aggregation:
A Customer can have many Itineraries (1..* relationship).
Composition:
A Payment is part of an Itinerary (if the itinerary is cancelled, the payment is deleted).
Inheritance:
Sales Consultant is a specialized type of Employee (inherits from Employee).





+-----------------------+    +----------------------+
|      Customer         |    |    Sales Consultant  |
+-----------------------+    +----------------------+
| customerName          |    | consultantName       |
| contactInfo           |    | consultantID         |
| customerID            |    +----------------------+
+-----------------------+    | registerCustomer()   |
| updateContactInfo()    |    | recordCustomerReq()  |
+-----------------------+    | finalizeItinerary()   |
        ^                   +----------------------+
        |                             |
+-----------------------+    +----------------------+
|     HolidayPackage    |    |       Itinerary      |
+-----------------------+    +----------------------+
| packageName           |    | itineraryID          |
| destination           |    | customer (Customer)  |
| accommodation         |    | package (HolidayPackage)|
| price                 |    | totalPrice           |
+-----------------------+    | paymentStatus        |
| checkAvailability()   |    +----------------------+
| suggestAlternatives()  |    | generatePrintout()   |
+-----------------------+    | addPayment()          |
                            +----------------------+
                                   ^
                                   |
                            +----------------------+
                            |       Payment        |
                            +----------------------+
                            | paymentID            |
                            | amount               |
                            | paymentType          |
                            | paymentStatus        |
                            +----------------------+
                            | processPayment()     |
                            | addCommission()      |
                            +----------------------+
                                   ^
                                   |
                            +----------------------+
                            |        Receipt       |
                            +----------------------+
                            | receiptID            |
                            | issueDate            |
                            | totalAmount          |
                            +----------------------+
                            | generateReceipt()    |
                            +----------------------+



Key Concepts:
Inheritance: The Sales Consultant class inherits from Employee (assumed superclass for all employees at World Traveller).

Aggregation: A Customer can have multiple Itineraries, meaning an itinerary can be associated with many customers over time.

Composition: A Payment is a part of an Itinerary. If the itinerary is canceled, the associated payment details will be removed as well.



c.	An Object Interaction Diagram (OID) in the form of a Message sequence Diagram which shows one particular sequence of events for one of the identified use cases. You do not need  to draw OID’s for all the identified use cases, one is sufficient for this questions.


d.	A state transition diagram for one appropriate class from the diagram.


 
Question: 3
Hospital Management

The following passage describes what is recorded when patient is admitted to hospital for medical care :

A community doctor refers the patient to the hospital. The hospital checks the patient’s name, address, date of birth and patient number in its patient file. Each hospital admission is known as an admission episode, it begins with a reason for admission and a planned admission date being recorded when a community doctor refers the patient. The patient is sent an admission card and this card is copied to the community doctor. Each admission episode ends when the patient is discharged the reason for discharge and the discharge date are recorded on the admission episode file. The community doctor is sent discharge notes prepared by the hospital doctor. The patient receives discharge advice. A hospital doctor supervises each admission episode and a hospital doctor supervises many admission episodes. The hospital doctor reports any treatment that is to be undertaken by the patient and this is recorded for the episode.

When the hospital doctor makes a diagnosis, the description of the diagnosis and the diagnosis code is written on the patient file with the date, over time a patient can have many diagnoses recorded. Each admission episode entails the possibility of treatment for the diagnosis. The treatment can be composed of surgery, medication or both. For surgery the date of the surgical operation, the surgery code and a description is recorded. For medication the following are recorded, drug name and its code, the dose, start date, frequency and notes.

An admission episode is created when a community doctor refers the patient; this is called a planned admission. If the community doctor reports that the patient’s circumstances have changes (e.g the patient recovers) then the admission can be cancelled and this becomes a cancelled admission; the cancellation date and reason are recorded. Upon reading the patient details, the hospital doctor offers a planned admission date to the patient. If the hospital doctor reports the need to delay a planned episode it becomes a deferred admission and the patient is advised of the delay as is the community doctor, the length of delay is recorded. A delayed admission can be cancelled. When a patient enters hospital the admission is regarded as being activated and the admission date recorded. If no diagnosis is made or if the diagnosis is not treatable then the patient is discharged from hospital; the admission episode is completed and called a discharged admission. If the patient has treatable diagnoses then the admission is regarded as treatable and the admission episode is marked accordingly. While different treatments are carried out the admission continues to be called treatable. When the treatment cycle is completed the patient is discharged, the discharge date and reason for discharge are written on the episode. The discharge is the final state of admission episode.

There are two types of doctor involved in the care of a patient. Both types of doctor have a doctor number, a medical qualification, and a name. The hospital doctor supervises each admission episode and is responsible for discharging the patient. For the hospital doctor we record the ward/clinic and the specialty the doctor is responsible for. The community doctor refers the patient in the first place. For the community doctor we record the practice address, postcode, telephone number and fax number. A hospital doctor can never be a community doctor as well.

