Question: 1
Advertisement Campaign Management

Adwell is small adveritising agency. The following passage describes how Adwell runs advertising campaigns.

Adwell deploys two types of staff in an advertising campaign. The technical staff are responsible for the design and implementation of the customer’s requirements. The administrative staff are responsible for the management controll of the campaign. They manage all exchanges between the technical staff and the customer through the administrative system. Staff are called employees. Adwell keeps a record of all of the employee’s names and start date. Each employees has an employee number. For technical staff a note is made of their area of skill and their availability. For administrative staff is made of their qualification.
When a customer commissions an advertising campaign, Adwell’s administrative staff records the campaign details. The customer provides company name, address, fax number and a contact person. The campaign has a title, a set of requirements, a start date, an end date and a budget cost. The campaign is compossed of several advertisements. Each advertisment has a title , a target date, estimated cost and an actual cost. Adwel deals with two types of advertisement. For a newspaper advertisement the newspaper, the placement, date and repeat dates are recorded, the Newspaper company, which owns the newspaper, supplies this placement availability information. For a website advertisement, the website provider, the start date, and the end date are recorded.

A campaign begins life when a customer proposes it. Adwell’s technical staff assess the propossed campaign but if it looks unsatisfactory they advise against it and it becomes a discarded campaign. Usually the technical staff consider a campaign to be satisfactory and it becomes a recommended campaign, A recommended campaign may be subject to revision if the customer wants one or more changes and Adwell’s technical staff aproved these. The campaign becomes a commisioned campaign when the customer commission it. When the first advertisements are produced by the technical staff the campaign becomes and underway campign. Where it is underway the campaign can be stopped if the customer is unhappy about the response to it and it is marked as a stopped campaign. Othewise a campign becomes a completed campaign when the customers makes the final payment.

Produce the following UML diagrams:

a.	Use case diagrams describing the processes that take place in this system and the actors that ............ and take part in the system. Consider how many system you may need and show the system ........... ......... Draw at least two systems with their appropriate actors, use cases and system boundary, Provede full and detailed descriptions for three use cases.

b.	A class diagram showing the classes involved in the system, their attributes, methods. relationships and relationship multiplicity. Show at least one example of each one of the following concepts inheritance, aggregation and composition.


c.	An Object Interaction Diagram (OID) or Message sequence Diagram which shows one .......... sequence of events for one of the identified use cases. You do not need  to draw OID’s for all the identified use cases. one is sufficient for this questions.


d.	A state transition diagram for one appropriate class from the diagram.


 
Question: 2
World Traveller

You have been asked to analyses and design a system for World Traveller. You have been given the following requirements from the staff of world Traveller. World Traveller is a travel agency, which arranges a variety of travel arrangements. All customers are registered with a sales consultant who records their requirements. The sales consultant has to refer to many different flight timetables, hotel locations and holiday agencies. The sales consultant tries to match the customer requirements as closely as possible. If the specific requirement is not available, then the sales consultant advises the customer on a variety of alternatives to meet their choice and makes bookings on their behalf. The sales consultant also asks the customer if they would like world traveller to organize the holiday insurance and car hire at the same time. Once an itinerary schedule is completed, it is given to the customer in a form of a printout. Once the itinerary is accepted, the customer is billed. Complete payment must be received from the customertoconfirm the booking. If the customer would like to pay later, then a non-refundable deposit must be paid to provisionally book the holiday. Full payment must be received at least one week before the date of travel. If the customer would like to pay by credit card a 1.5% commission is added to the total bill. Once the customer has paid the full invoice they are provided with a receipt.

You are required to produce models to represent only the description provided above. This requirement specification is partial and incomplete description of the problem and you are asked to model it in a way that allows for further classes to be added when required. For example World Traveller only provide package holidays at present and the company may expand to provide other forms of holidays such as cruises repeat business trips, trips to multiple destinations, specialized holidays, and other types of travel, Which may be developed in the future. Another example may be that their billing and collection of payment may change. The model should be designed so it can be easily adapted to meet any changes.

Produce the following UML diagrams:


a.	Use case diagrams describing the processes that take place in this system and the actors that stimulate and take part in the system.  Consider how many systems you may need show the system boundaries. Draw at least two systems with their appropriate actors. Use cases and system boundary. Provide descriptions for all the use cases.


b.	A class diagram showing the classes involved in the system, their attributes, methods, relationships and relationship multiplicity. Show at least one example of each one of the following concepts inheritance, aggregation and composition.


c.	An Object Interaction Diagram (OID) in the form of a Message sequence Diagram which shows one particular sequence of events for one of the identified use cases. You do not need  to draw OID’s for all the identified use cases, one is sufficient for this questions.


d.	A state transition diagram for one appropriate class from the diagram.


 
Question: 3
Hospital Management

The following passage describes what is recorded when patient is admitted to hospital for medical care :

A community doctor refers the patient to the hospital. The hospital checks the patient’s name, address, date of birth and patient number in its patient file. Each hospital admission is known as an admission episode, it begins with a reason for admission and a planned admission date being recorded when a community doctor refers the patient. The patient is sent an admission card and this card is copied to the community doctor. Each admission episode ends when the patient is discharged the reason for discharge and the discharge date are recorded on the admission episode file. The community doctor is sent discharge notes prepared by the hospital doctor. The patient receives discharge advice. A hospital doctor supervises each admission episode and a hospital doctor supervises many admission episodes. The hospital doctor reports any treatment that is to be undertaken by the patient and this is recorded for the episode.

When the hospital doctor makes a diagnosis, the description of the diagnosis and the diagnosis code is written on the patient file with the date, over time a patient can have many diagnoses recorded. Each admission episode entails the possibility of treatment for the diagnosis. The treatment can be composed of surgery, medication or both. For surgery the date of the surgical operation, the surgery code and a description is recorded. For medication the following are recorded, drug name and its code, the dose, start date, frequency and notes.

An admission episode is created when a community doctor refers the patient; this is called a planned admission. If the community doctor reports that the patient’s circumstances have changes (e.g the patient recovers) then the admission can be cancelled and this becomes a cancelled admission; the cancellation date and reason are recorded. Upon reading the patient details, the hospital doctor offers a planned admission date to the patient. If the hospital doctor reports the need to delay a planned episode it becomes a deferred admission and the patient is advised of the delay as is the community doctor, the length of delay is recorded. A delayed admission can be cancelled. When a patient enters hospital the admission is regarded as being activated and the admission date recorded. If no diagnosis is made or if the diagnosis is not treatable then the patient is discharged from hospital; the admission episode is completed and called a discharged admission. If the patient has treatable diagnoses then the admission is regarded as treatable and the admission episode is marked accordingly. While different treatments are carried out the admission continues to be called treatable. When the treatment cycle is completed the patient is discharged, the discharge date and reason for discharge are written on the episode. The discharge is the final state of admission episode.

There are two types of doctor involved in the care of a patient. Both types of doctor have a doctor number, a medical qualification, and a name. The hospital doctor supervises each admission episode and is responsible for discharging the patient. For the hospital doctor we record the ward/clinic and the specialty the doctor is responsible for. The community doctor refers the patient in the first place. For the community doctor we record the practice address, postcode, telephone number and fax number. A hospital doctor can never be a community doctor as well.

