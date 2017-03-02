---
title: Functional scope
category: Functional
order: 1
---


Functional context

1. As a koppeltaal customer, I receive a request for domain from a koppeltaal consumer. In this request for domain, the koppeltaal consumer indicates which koppeltaal registered applications they would like to exchange which koppeltaal messages with. I review the request for domain, and where needed, I coordinate with the koppeltaal consumer to clarify any issues before submitting the request for domain to the koppeltaal service provider.

2. As a koppeltaal service provider, I receive a request for domain from a koppeltaal customer. I review if the customer has a signed cooperation agreement filed with the koppeltaal contract manager. I then check (how, where) if the koppeltaal consumer on behalf of whom the request is filed is a client of at least one koppeltaal customer. I also check if the koppeltaal customer has a koppeltaal registered application (how, where?). If all checks pass, I review the application for completeness and I make a request (how, where) for the koppeltaal infrastructure operator to create the domain for this customer. If any of these checks fail, I coordinate with the koppeltaal customer and the koppeltaal contract manager/network promoter to see if the situation can be easily resolved. If not, I give the task back to the koppeltaal contract manager.

3. As a koppeltaal infrastructure operator, I receive a request for domain from the koppeltaal service provider. As a koppeltaal infrastructure operator, I setup the domain for the koppeltaal consumer. In the request for domain, I can see which koppeltaal registered applications want to exchange which koppeltaal messages with whom. I allow these applications to exchange data in this domain and I supply the koppeltaal service provider with the credentials the koppeltaal customer can use to manage their domain themselves.

4. As a koppeltaal customer, I receive a message that the request for domain was approved and I receive the credentials to access the domain so that I can further configure my application to exchange data with other koppeltaal registered applications for this domain.

5. After I have configured my application and I have verified that there is at least one other application configured for this domain, I can perform a functional test of the exchange of koppeltaal messages between the applications. For this functional test, I have prepared at least three testroles in my production environment: a patient, a caregiver and a related person.

6. As a caregiver, I open my the patient management function of my application. I select a patient, and I assign a koppeltaal registered application to this patient. If covered by my functional integration with koppeltaal, I also assign subactivities in the application for the patient to perform. I also use any other functionality offered by my application to assist the patient.

7. As a patient, I login to my patient portal. I can see that my caregiver has assigned an activity for me to perform. I can start the activity from my patient portal. If I start the activity, it opens seamlessly and I can start working with the activity right away.

8. As a patient, I have worked with the activity for a while, I have either completed the activity or not, and I decide to stop. I close the activity application and I return to my patient portal. I can see a report of what I have done in the activity (i.e. completed with result x, aborted activity, completed with result y). I can resume the activity if I want to.

9. As a caregiver, I open my patient management function, and I can review any status changes for the activities I have assigned. (i.e started, aborted, paused, completed) and any results (with result x, y or z) of the activity status. If I want to, I can click on an individual patient's assigned activity and the activity opens seamlessly to show me details of the patient's work in the assigned activity.

10. As a caregiver and/or as a patient (depending o the functional coverage of my patient and/or caregiver portal), I am able to invite related persons and assign the an activity as well. Depending on the functional coverage the related person can perform part or all of the aforementioned actions that the caregiver and the patient can perform (apart form playing the game themselves).

11. As a patient, caregiver, and/or related person, I can abort working with any of the applications at any time, and recover the last stable functional state of the applications reliably.