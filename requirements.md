# CRM Requirements for Maryland Accessible Telecommunications
**Date:** 12/13/2024

---

## Core User Stories

### MAT User Submitting an Application for the First Time
**Title:** First-Time Application Submission by MAT User

**As a** MAT User,  
**I want to** submit an application for assistance through an online form,  
**so that** I can request the necessary equipment and services to meet my needs.

#### Acceptance Criteria:

- **Access Application Form:**
  - The MAT User can access the application form via the Web app.
  - The form is accessible on various devices (laptop, smartphone, tablet).

- **Complete Application Steps:**
  - The application process is broken down into clear, manageable steps (e.g., Personal Information, Equipment Needs, Disability Certification Form, Documentation Upload).
  - The user can navigate between steps without losing entered information.

- **Save Progress:**
  - Users can save their progress and return to complete the application later.
  - Partial applications are saved as "incomplete" and can be resumed.

- **Input Validation:**
  - The form provides real-time validation feedback (e.g., required fields, proper formatting).
  - **Verification of Submitted Documents:**
    - Applicants must submit:
      1. A document identifying them as a resident of Maryland.
      2. Proof of income, which must be less than 400% of the poverty limit in the state of Maryland based on the family size of the applicant.
      3. A disability certification form on file signed by a doctor, nurse practitioner, social worker, or other qualified personnel.
    - If the documentation is insufficient, the system notifies the applicant to submit updated documentation.

- **Submit Application:**
  - Upon completing all required fields, the user can submit the application.
  - A confirmation message is displayed, and a confirmation email is sent to the user's email address.

- **Error Handling:**
  - If submission fails (e.g., due to network issues), the user is notified and prompted to retry.

- **Analytics Tracking:**
  - The system tracks at which step users typically abandon the application to identify and address pain points.

- **Post-Submission Status:**
  - After submission, the application status is updated to "Awaiting Documentation Confirmation" or the relevant next step.

#### User Flow:

1. **Registration/Login:**
   - If not already registered, the MAT User creates an account or logs in.
2. **Access Application:**
   - Navigates to the "Submit Application" section.
3. **Fill Out Application:**
   - Completes each section, providing necessary information and uploading required documents.
4. **Review & Submit:**
   - Reviews the entered information and submits the application.
5. **Confirmation:**
   - Receives a confirmation message and email indicating successful submission.
6. **Post-Submission:**
   - Application status is set to "Awaiting Documentation Confirmation," triggering appropriate workflows and notifications.

---

### Admin User Monitoring and Managing Applications
**Title:** Admin Monitoring and Managing Constituent Applications

**As an** Admin User,  
**I want to** monitor and manage applications submitted by constituents through detailed dashboards,  
**so that** I can oversee the application process, take necessary actions, and ensure efficient service delivery.

#### Required Dashboards and Functionality:

- **Admin Dashboard:**
  - Comprehensive overview of "Active Constituents" with various application statuses:
    - Constituents with completed applications (including total number).
    - Constituents with incomplete applications.
    - Analytics on where constituents abandon the application.
    - Submitted applications awaiting documentation confirmation.
    - Constituents awaiting evaluation.
    - Constituents assigned to an evaluator.
    - Constituents awaiting equipment.
    - Constituents awaiting installation or training.
    - Constituents with open, scheduled, or canceled CF (Communication Facilitator) requests.

- **Constituents Dashboard:**
  - Lists constituents alphabetically by last name.
  - Search functionality to find specific constituents.
  - Sortable fields: Date of last contact, date of last equipment order, date of last evaluation.
  - Clickable rows revealing detailed equipment order and appointment history.
  - Displays contact information, alternate contact person details, equipment order history, and evaluation history.

- **Applications Dashboard:**
  - Lists applications by date and status, with open applications at the top.
  - Sortable by the number of days the application has been open.
  - Displays application status, dates for various stages (received, approved, sent back, determination).
  - Lists all due reminders with details on the number of reminders sent, required documents, and constituent contact information.
  - Provides options to print letters, envelopes, and postage for mailed reminders.

- **Appointments Dashboard:**
  - Lists appointments by request date, grouped by appointment type (evaluations, installation, training, troubleshooting) and date.
  - Details on how each appointment will be conducted (virtually or in-person).

- **Manage Applications:**
  - **Application Documentation Review:**
    - Ability to reject submitted documentation if insufficient and request additional information or documentation from constituents.
    - Update application status accordingly.
  - **Remind to Complete Applications:**
    - Send reminders to constituents to complete their applications.
    - Track the number of reminders sent and manage mailing processes.

- **Admin Account Management:**
  - **Create/Delete Admin Accounts:**
    - MAT staff can create new admin accounts or delete existing ones.
  - **Assign Roles:**
    - MAT staff can assign or modify roles for admin accounts (e.g., evaluator, communication facilitator).

- **Equipment Ordering Management:**
  - **Bid Forms:**
    - Generate weekly batches of equipment bid forms with device types, quantities, delivery details.
    - Send bid forms to relevant vendors.
    - Review returned bids and select the lowest bid for forwarding to the Finance Department.
  - **Manage Vendor Selection:**
    - Send Requests for Bids and track responses.

- **Vendor Notifications:**
  - Notify vendors to upload tracking information, delivery confirmations, and serial numbers.
  - Receive notifications when equipment is shipped to designated addresses.

- **Serial Number Management:**
  - Provide methods for vendors or MAT staff to upload device serial numbers to constituent accounts.

- **Notifications and Alerts:**
  - Receive real-time notifications for critical events (e.g., new applications, bid responses, equipment shipments).

#### User Flow:

1. **Login:**
   - Admin logs into the MAT Admin portal using secure credentials.
2. **Access Dashboard:**
   - Navigates to the main dashboard displaying an overview of active constituents and application statuses.
3. **Monitor Applications:**
   - Reviews the list of constituents and their current application statuses across various dashboards.
4. **Manage Applications:**
   - Clicks on a constituent to view detailed application information.
   - Sends back applications for additional information or sends reminders to complete applications as needed.
5. **Manage Admin Accounts:**
   - Creates new admin accounts or deletes existing ones.
   - Assigns roles to admin users to define their access levels and responsibilities.
6. **Handle Equipment Ordering:**
   - Generates and sends bid forms to vendors.
   - Reviews returned bids, selects the lowest bid, and forwards it to the Finance Department.
7. **Track Deliveries:**
   - Receives notifications when equipment is shipped.
   - Ensures equipment serial numbers are uploaded to constituent accounts for inventory tracking.
8. **Generate Reports and Analytics:**
   - Utilizes dashboard analytics to identify bottlenecks in the application process.
   - Makes data-driven decisions to improve constituent experience and operational efficiency.

---

### Evaluator User Managing Assigned Evaluations
**Title:** Evaluator Managing Assigned Client Evaluations

**As an** Evaluator User,  
**I want to** receive and manage client assignments for evaluations through a dedicated dashboard,  
**so that** I can efficiently assess clients and update their application statuses.

#### Acceptance Criteria:

- **Assignment Notifications:**
  - Receives email and/or in-app notifications when assigned a new constituent for evaluation.

- **Evaluator Dashboard:**
  - Accesses a dashboard listing all assigned constituents awaiting evaluation.
  - Can view constituent details, including contact information, application details, and attached documentation.

- **Assessment Form Completion:**
  - Completes the Assessment Form online via laptop, smartphone, or tablet during client meetings.
  - Ensures the form is user-friendly and accessible across devices.

- **Scheduling Evaluations:**
  - Schedules evaluation appointments, selecting between virtual or in-person evaluations.
  - Sends appointment details to constituents.

- **GPS Check-In for In-Person Evaluations:**
  - For in-person evaluations, can check in at the location using GPS through the Evaluator's account.
  - Confirms completion of the evaluation after meeting the constituent.

- **Updating Application Status:**
  - Updates the constituent’s application status based on evaluation outcomes (e.g., moving to awaiting equipment).

- **Historical Tracking:**
  - Accesses the history of evaluations conducted, including dates, scores, and evaluator comments.

- **Integration with Appointments and Equipment Ordering:**
  - Links evaluations with subsequent processes like equipment ordering and appointment scheduling.

- **Performance Metrics:**
  - Views metrics related to evaluation performance, such as average evaluation time and client satisfaction scores.

#### User Flow:

1. **Login:**
   - Evaluator logs into the MAT Evaluator portal using secure credentials.
2. **Receive Assignment:**
   - Receives a notification about a new constituent assigned for evaluation.
3. **Access Dashboard:**
   - Navigates to the Evaluator Dashboard to view all assigned evaluations.
4. **Review Constituent Details:**
   - Clicks on a constituent to view detailed application information and required documentation.
5. **Schedule Evaluation:**
   - Schedules an appointment with the constituent, selecting the preferred method (virtual or in-person).
   - Sends appointment details to the constituent and updates the Applications Dashboard.
6. **Conduct Evaluation:**
   - Meets with the constituent at the scheduled time and location.
   - For in-person evaluations, checks in via GPS at the location.
   - Completes the Assessment Form using an internet-enabled device.
7. **Update Status:**
   - Submits the completed assessment, updating the application status to the next phase (e.g., awaiting equipment).
8. **Track Progress:**
   - Monitors the application’s progression through subsequent stages using the dashboard analytics.
9. **Historical Records:**
   - Accesses past evaluations to review performance and constituent interactions.

---

### MAT Staff Managing Equipment Ordering and Vendor Interactions
**Title:** MAT Staff Managing Equipment Ordering and Vendor Bids

**As a** MAT Staff Member,  
**I want to** manage equipment ordering by generating bid forms, interacting with vendors, and tracking deliveries,  
**so that** I can ensure constituents receive the necessary equipment efficiently and cost-effectively.

#### Acceptance Criteria:

- **Generate Bid Forms:**
  - Automatically generate weekly batches of equipment bid forms detailing device types, quantities, delivery addresses, and constituent information.

- **Vendor Management:**
  - Maintain a list of vendors and the equipment each vendor supplies.
  - Send bid forms to relevant vendors based on the device types they carry.

- **Review and Select Bids:**
  - Receive and review returned bids from vendors.
  - Select the lowest bid and forward it to the Finance Department along with vendor details.

- **Request for Bids:**
  - After evaluation approval, send Request for Bids to selected vendors (minimum of three, unless a sole source).

- **Track Vendor Responses:**
  - Monitor vendors’ responses, ensuring timely uploads of tracking information, delivery confirmations, and serial numbers.

- **Notification System:**
  - Receive notifications when vendors ship equipment to designated addresses.
  - Ensure equipment serial numbers are uploaded to constituent accounts for inventory tracking.

- **Link Deliveries to Accounts:**
  - Link awarded vendor information, constituent details, and delivery tracking to the respective accounts.

- **Serial Number Management:**
  - Provide interfaces for vendors or MAT staff to upload device serial numbers.

- **Interaction with Finance Department:**
  - Forward selected bids and vendor information to the Finance Department for payment processing.

#### User Flow:

1. **Login:**
   - MAT Staff logs into the MAT Admin portal using secure credentials.
2. **Generate Bid Forms:**
   - The system automatically generates bid forms based on the weekly equipment needs.
3. **Send Bid Forms to Vendors:**
   - Selects appropriate vendors based on the device types they carry.
   - Sends out bid forms to the selected vendors.
4. **Review Returned Bids:**
   - Receives bids from vendors through the system.
   - Reviews each bid for compliance and cost-effectiveness.
5. **Select and Forward Bids:**
   - Chooses the lowest bid and forwards the selection to the Finance Department along with vendor details.
6. **Manage Request for Bids:**
   - Sends Request for Bids to the selected vendors, ensuring at least three vendors are contacted unless a sole source is justified.
7. **Track Deliveries:**
   - Monitors notifications from vendors regarding shipment and delivery statuses.
   - Ensures that tracking information and serial numbers are uploaded to the system.
8. **Update Constituent Accounts:**
   - Links the delivered equipment to the respective constituent’s account, ensuring accurate inventory tracking.
9. **Coordinate with Finance:**
   - Works closely with the Finance Department to process payments for selected bids.

---

### MAT Staff Scheduling and Managing Appointments
**Title:** MAT Staff Scheduling and Managing Installation and Training Appointments

**As a** MAT Staff Member,  
**I want to** schedule and manage equipment installation and training appointments for constituents,  
**so that** constituents receive timely support and training on their equipment.

#### Acceptance Criteria:

- **Schedule Appointments:**
  - Allow constituents to schedule installation and training appointments through their accounts if needed.

- **Appointment Types:**
  - Handle various appointment types: installation, training, troubleshooting.
  - Specify whether appointments will be conducted virtually or in-person.

- **Assign Evaluators/Trainers:**
  - Assign available evaluators or trainers based on constituent needs and trainer expertise.

- **GPS Check-In for In-Person Appointments:**
  - For in-person appointments, allow evaluators/trainers to check in via GPS at the location.
  - Confirm completion of the appointment upon check-out.

- **Map and List View:**
  - Provide MAT staff with a map and list view of upcoming and recent installations and training appointments.

- **Appointment Tracking:**
  - Track the status of each appointment (scheduled, in-progress, completed, rescheduled, canceled).

- **Notifications and Reminders:**
  - Automatically send reminders to constituents and evaluators/trainers seven days prior to the appointment.
  - Generate rescheduling letters if constituents do not attend the appointment.

- **Historical Records:**
  - Maintain a history of all appointments, including dates, types, outcomes, and any follow-up actions required.

#### User Flow:

1. **Login:**
   - MAT Staff logs into the MAT Admin portal using secure credentials.
2. **Access Appointments Dashboard:**
   - Navigates to the Appointments Dashboard to view and manage all appointments.
3. **Schedule Appointment:**
   - Schedules an installation or training appointment for a constituent, selecting the appropriate type and method (virtual or in-person).
4. **Assign Evaluator/Trainer:**
   - Assigns an available evaluator or trainer to the appointment based on constituent needs and trainer qualifications.
5. **Notify Parties:**
   - Sends appointment details to the constituent and the assigned evaluator/trainer.
6. **Monitor Appointment:**
   - Tracks the appointment status and receives real-time updates as evaluators/trainers check in via GPS and complete the appointment.
7. **Handle Reminders and Rescheduling:**
   - Automatically sends reminders to both parties seven days before the appointment.
   - Generates rescheduling letters if the constituent fails to attend.
8. **Review Appointment History:**
   - Accesses historical data on past appointments to assess performance and identify any recurring issues.

---

### Trainers Managing Equipment Retraining Requests
**Title:** Trainers Managing Equipment Retraining Requests

**As a** Trainer User,  
**I want to** manage retraining requests from constituents and conduct effective training sessions,  
**so that** constituents are proficient in using their equipment.

#### Acceptance Criteria:

- **Submit Retraining Requests:**
  - Allow constituents to submit requests for retraining on their equipment through their accounts.

- **Notification of Requests:**
  - MAT staff receive notifications of retraining requests.

- **Assign Trainers:**
  - MAT staff assign available trainers to retraining requests based on constituency type and equipment expertise.

- **Trainer Notifications:**
  - Trainers receive notifications of new retraining assignments, including location, date, and time.

- **Constituent Notifications:**
  - Constituents are notified when a trainer is assigned, including the trainer's contact information (name, email, phone numbers).

- **Scheduling Retraining Sessions:**
  - Trainers schedule retraining sessions, specifying whether they will be conducted virtually or in-person.

- **Reminders and Follow-Ups:**
  - Automatically send reminders to both trainers and constituents seven days prior to the retraining appointment.

- **Rescheduling and No-Show Handling:**
  - Automatically generate letters to constituents to reschedule if they do not attend the retraining session.

- **Training Completion:**
  - Trainers mark retraining sessions as completed, updating the constituent’s status accordingly.

- **Historical Tracking:**
  - Maintain records of all retraining sessions, including dates, trainer feedback, and constituent proficiency assessments.

#### User Flow:

1. **Login:**
   - Trainer logs into the MAT Trainer portal using secure credentials.
2. **Receive Assignment:**
   - Receives a notification about a new retraining request assignment.
3. **Access Retraining Details:**
   - Views constituent details and retraining requirements.
4. **Schedule Retraining:**
   - Schedules a retraining session, selecting the method (virtual or in-person).
   - Sends appointment details to the constituent.
5. **Conduct Retraining:**
   - Meets with the constituent at the scheduled time and location.
   - Completes the training session using the provided materials and equipment.
6. **Update Status:**
   - Marks the retraining session as completed in the system.
7. **Handle No-Shows:**
   - If the constituent does not attend, the system generates a rescheduling letter.
8. **Review Training History:**
   - Accesses past retraining sessions to review constituent progress and trainer feedback.

---

### Equipment Ordering and Tracking
**Title:** MAT Staff Manages Equipment Ordering and Tracks Deliveries Efficiently

**As a** MAT Staff Member,  
**I want to** manage equipment ordering by generating bid forms, interacting with vendors, and tracking deliveries in real-time,  
**so that** I can ensure constituents receive the necessary equipment efficiently and cost-effectively.

#### Acceptance Criteria:

- **Generate Bid Forms:**
  - Automatically generate weekly batches of equipment bid forms detailing device types, quantities, delivery addresses, and constituent information.

- **Vendor Management:**
  - Maintain a list of vendors and the equipment each vendor supplies.
  - Send bid forms to relevant vendors based on the device types they carry.

- **Review and Select Bids:**
  - Receive and review returned bids from vendors.
  - Select the lowest bid and forward it to the Finance Department along with vendor details.

- **Request for Bids:**
  - After evaluation approval, send Request for Bids to selected vendors (minimum of three, unless a sole source).

- **Real-Time Equipment Tracking:**
  - Integrate with shipping carriers' APIs to fetch real-time tracking data for equipment shipments.
  - Provide a dedicated tracking dashboard displaying current shipment statuses, estimated delivery times, and any delays.

- **Automated Inventory Updates:**
  - Automatically update inventory records upon receiving serial numbers and delivery confirmations.

- **Vendor Notifications:**
  - Notify vendors to upload tracking information, delivery confirmations, and serial numbers.
  - Receive notifications when equipment is shipped to designated addresses.

- **Serial Number Management:**
  - Provide interfaces for vendors or MAT staff to upload device serial numbers to constituent accounts.

- **Link Deliveries to Accounts:**
  - Link awarded vendor information, constituent details, and delivery tracking to the respective accounts.

- **Interaction with Finance Department:**
  - Forward selected bids and vendor information to the Finance Department for payment processing.

#### User Flow:

1. **Login:**
   - MAT Staff logs into the MAT Admin portal using secure credentials.
2. **Generate Bid Forms:**
   - The system automatically generates bid forms based on the weekly equipment needs.
3. **Send Bid Forms to Vendors:**
   - Selects appropriate vendors based on the device types they carry.
   - Sends out bid forms to the selected vendors.
4. **Review Returned Bids:**
   - Receives bids from vendors through the system.
   - Reviews each bid for compliance and cost-effectiveness.
5. **Select and Forward Bids:**
   - Chooses the lowest bid and forwards the selection to the Finance Department along with vendor details.
6. **Manage Request for Bids:**
   - Sends Request for Bids to the selected vendors, ensuring at least three vendors are contacted unless a sole source is justified.
7. **Track Deliveries:**
   - Monitors the Tracking Dashboard for real-time updates on equipment shipments.
   - Ensures that tracking information and serial numbers are uploaded to the system.
8. **Update Constituent Accounts:**
   - Links the delivered equipment to the respective constituent’s account, ensuring accurate inventory tracking.
9. **Coordinate with Finance:**
   - Works closely with the Finance Department to process payments for selected bids.

---

### Status Tracking
**Title:** MAT User Tracks Application and Appointment Status in Real-Time

**As a** MAT User,  
**I want to** track the real-time status of my application and appointments,  
**so that** I stay informed about the progress and next steps without needing to contact MAT staff.

#### Acceptance Criteria:

- **Status Dashboard:**
  - Provide a personalized dashboard where users can view the current status of their application, equipment orders, evaluations, and appointments.

- **Progress Indicators:**
  - Use visual indicators (e.g., progress bars, status badges) to represent the current stage of each process.

- **Detailed Status Updates:**
  - Offer detailed explanations of each status stage, including any pending actions or required documents.

- **Historical Records:**
  - Allow users to view a history of all status changes and interactions related to their application and appointments.

- **Notifications Integration:**
  - Sync status updates with the notification system to alert users of changes in real-time.

- **Interactive Elements:**
  - Enable users to click on status indicators to receive more detailed information or take relevant actions (e.g., upload missing documents, reschedule appointments).

- **Mobile and Web Accessibility:**
  - Ensure that status tracking is accessible both through the mobile app and the web portal seamlessly.

#### User Flow:

1. **Access Status Dashboard:**
   - MAT User logs into their account and navigates to the Status Dashboard.
2. **View Current Status:**
   - Sees real-time updates on the application process, equipment orders, evaluations, and scheduled appointments.
3. **Understand Next Steps:**
   - Reads detailed explanations of each status stage and any required actions.
4. **Review History:**
   - Accesses historical records to review past interactions and status changes.
5. **Take Action if Needed:**
   - Clicks on specific status indicators to upload documents, reschedule appointments, or perform other relevant actions.

---

### Vendor Managing Equipment and Bid Submissions
**Title:** Vendor Managing Equipment Listings and Bid Submissions

**As a** Vendor User,  
**I want to** manage my equipment listings and submit bids for MAT’s equipment orders,  
**so that** I can participate in the procurement process and supply the necessary devices.

#### Acceptance Criteria:

- **Vendor Profile Management:**
  - Vendors can create and manage their profiles, including business details, contact information, and equipment listings.

- **Manage Equipment Listings:**
  - Add, update, or remove equipment types that the vendor supplies.
  - Specify device types, quantities, and pricing details.

- **Receive Bid Forms:**
  - Receive bid forms from MAT staff based on weekly equipment ordering needs.

- **Submit Bids:**
  - Submit bids for received bid forms through the vendor portal.
  - Ensure bids are submitted before the specified deadline.

- **View Bid Status:**
  - Track the status of submitted bids (e.g., submitted, under review, selected).

- **Upload Tracking Information:**
  - Upon being awarded a bid, upload tracking information and delivery confirmations.

- **Upload Serial Numbers:**
  - Provide serial numbers of delivered equipment for inventory tracking purposes.

- **Notifications:**
  - Receive notifications about bid awards, shipment confirmations, and any additional requirements.

- **Historical Bid Data:**
  - Access a history of bids submitted, awarded, and pending.

#### User Flow:

1. **Login:**
   - Vendor logs into the Vendor portal using secure credentials.
2. **Manage Profile:**
   - Updates business information and manages equipment listings.
3. **Receive Bid Forms:**
   - Receives bid forms sent by MAT staff based on equipment ordering needs.
4. **Submit Bid:**
   - Reviews the bid form details and submits a competitive bid before the deadline.
5. **Track Bid Status:**
   - Monitors the status of submitted bids through the portal.
6. **Handle Awarded Bids:**
   - Upon selection, receives notification and uploads tracking information and delivery confirmations.
7. **Inventory Management:**
   - Uploads serial numbers of delivered equipment for MAT’s inventory tracking.
8. **Review Bid History:**
   - Accesses past bid submissions and outcomes to inform future bids.

---

### Mobile Accessibility
**Title:** MAT User Engages with the MAT Mobile Application for Enhanced Accessibility

**As a** MAT User,  
**I want to** access application features, receive notifications, and manage my account conveniently from my smartphone,  
**so that** I can interact with the system on-the-go.

#### Acceptance Criteria:

- **Web App Universality:**
  - MAT Rails web app should work across all major platforms (iOS, Android) and be accessible through its website address.

- **Feature Parity:**
  - The Rails Web app includes essential features such as application submission, status tracking, appointment scheduling, and real-time notifications.

- **User-Friendly Interface:**
  - The Web app has an intuitive and responsive design optimized for mobile devices.

- **Secure Login Mechanisms:**
  - Implement secure login mechanisms, including biometric authentication (e.g., fingerprint, facial recognition) where supported.

- **Seamless Syncing:**
  - Ensure data consistency between the mobile app and the web portal, with real-time syncing of information.

---

### MAT Staff Managing System-Generated Notifications and Reminders
**Title:** MAT Staff Managing System-Generated Notifications and Reminders

**As a** MAT Staff Member,  
**I want to** manage system-generated notifications and reminders for various application and appointment stages,  
**so that** constituents and staff receive timely prompts to complete necessary actions.

#### Acceptance Criteria:

- **Configure Notification Settings:**
  - Define rules and templates for different types of notifications (e.g., application reminders, appointment reminders).

- **Automated Reminders:**
  - Automatically send reminders to constituents to complete applications or attend appointments.
  - Automatically send reminders to trainers and evaluators seven days prior to appointments.

- **Rescheduling Notifications:**
  - Automatically generate and send rescheduling letters if constituents do not attend appointments.

- **Notification Tracking:**
  - Track the number of reminders sent to each constituent.

- **Customization:**
  - Customize notification content based on constituent needs and roles.

- **Multi-Channel Notifications:**
  - Send notifications via multiple channels (email, SMS, in-app).

- **Manage Notification Logs:**
  - Access logs of all sent notifications for auditing and reporting purposes.

- **Handle Notification Failures:**
  - Detect and manage failed notification deliveries, prompting retries or alternative communication methods.

#### User Flow:

1. **Login:**
   - MAT Staff logs into the MAT Admin portal using secure credentials.
2. **Access Notification Settings:**
   - Navigates to the Notifications Management section.
3. **Configure Notifications:**
   - Defines rules, templates, and channels for various notifications and reminders.
4. **Monitor Notifications:**
   - Views logs of sent notifications, including successes and failures.
5. **Handle Failures:**
   - Manages failed notifications by initiating retries or alternative communication methods.
6. **Review and Optimize:**
   - Analyzes notification effectiveness and adjusts settings to improve engagement and response rates.

---

### MAT Staff Creating and Managing Administrator Accounts
**Title:** MAT Staff Creating and Managing Administrator Accounts

**As a** MAT Staff Member,  
**I want to** create, delete, and assign roles to administrator accounts,  
**so that** I can ensure that only authorized personnel have access to administrative functionalities.

#### Acceptance Criteria:

- **Create Admin Accounts:**
  - Add new administrator accounts with required details (email, name, role).

- **Delete Admin Accounts:**
  - Remove administrator accounts as needed, ensuring data integrity and security.

- **Assign Roles:**
  - Assign specific roles to admin accounts (e.g., Super Admin, Evaluator, Communication Facilitator).
  - Modify roles of existing admin accounts as necessary.

- **Role-Based Access Control:**
  - Ensure that each role has appropriate access permissions within the application.

- **Secure Account Management:**
  - Implement secure password policies and authentication mechanisms for admin accounts.

- **Audit Trails:**
  - Maintain logs of account creation, deletion, and role assignments for security auditing.

- **Account Recovery:**
  - Provide mechanisms for password resets and account recovery in case of lost credentials.

#### User Flow:

1. **Login:**
   - MAT Staff logs into the MAT Admin portal using secure credentials.
2. **Access Admin Account Management:**
   - Navigates to the Admin Accounts section.
3. **Create New Admin:**
   - Fills out the necessary information to create a new admin account.
4. **Assign Role:**
   - Assigns a specific role to the new admin based on their responsibilities.
5. **Delete Admin:**
   - Selects and deletes an existing admin account, ensuring that all associated data is handled appropriately.
6. **Modify Roles:**
   - Changes the roles of existing admin accounts as organizational needs evolve.
7. **Review Audit Logs:**
   - Accesses audit logs to review changes made to admin accounts for security compliance.

---

## Value-Added Features

### Streamlining Application Processes
**Title:** MAT User Completes Application Efficiently with Guided Assistance and Auto-Save

**As a** MAT User,  
**I want to** complete my application smoothly with guided assistance and have my progress automatically saved,  
**so that** I can submit my application without frustration or data loss.

#### Acceptance Criteria:

- **Guided Assistance:**
  - Application forms include tooltips and inline help for complex fields.
  - Progress indicators display completed sections and upcoming steps.

- **Auto-Save Functionality:**
  - Application data is automatically saved at regular intervals without requiring manual action.
  - Users receive notifications confirming that their progress has been saved.

- **Error Prevention:**
  - Prevent data loss in cases of unexpected interruptions, such as browser crashes or connectivity issues.

- **User-Friendly Navigation:**
  - Users can easily navigate between different sections of the application without losing entered information.

- **Completion and Submission:**
  - Users receive a confirmation message and email upon successful submission of the application.

#### User Flow:

1. **Start Application:**
   - MAT User logs in and begins filling out the application form.
2. **Receive Guidance:**
   - Tooltips and help texts assist in completing each section.
3. **Progress Tracking:**
   - Progress indicators show completed steps and remaining sections.
4. **Auto-Save Activation:**
   - Application data is periodically saved automatically.
5. **Complete and Submit:**
   - MAT User completes all sections and submits the application confidently, knowing their data is secure.

---

### Automating Notifications and Reminders
**Title:** MAT User Receives Personalized and Timely Notifications

**As a** MAT User,  
**I want to** receive personalized notifications and reminders based on my preferences,  
**so that** I stay informed about my application status and upcoming appointments in a way that suits me best.

#### Acceptance Criteria:

- **Notification Preferences:**
  - Users can select preferred notification channels (email, SMS, in-app).

- **Personalized Messaging:**
  - Notifications address users by name and include relevant details about their application or appointments.

- **Intelligent Scheduling:**
  - Notifications are sent at optimal times based on user behavior and time zones.

- **Notification History:**
  - Users can view a history of all notifications received within their account dashboard.

- **Opt-Out Options:**
  - Users can opt out of specific types of notifications if desired.

#### User Flow:

1. **Set Preferences:**
   - MAT User selects preferred notification channels and formats in their account settings.
2. **Receive Notifications:**
   - Receives timely and personalized notifications about application updates and appointment reminders.
3. **Manage Notifications:**
   - Reviews notification history and adjusts preferences as needed within their account settings.

---

### Advanced Reporting
**Title:** MAT Staff Utilizes Advanced Reporting and Analytics for Data-Driven Decisions

**As a** MAT Staff Member,  
**I want to** access advanced reports and analytics on application processes and operational metrics,  
**so that** I can make informed, data-driven decisions to improve efficiency and constituent satisfaction.

#### Acceptance Criteria:

- **Automated Reports:**
  - Schedule and generate reports on key metrics such as application completion rates, average processing times, and constituent satisfaction scores.

- **Interactive Analytics:**
  - Access interactive data visualizations that allow staff to explore trends, identify bottlenecks, and monitor performance indicators.

- **Custom Report Generation:**
  - Create custom reports based on specific criteria and export them in various formats (PDF, Excel).

- **Real-Time Data:**
  - Ensure that reports and analytics reflect real-time data for accurate and timely insights.

- **Data Privacy Compliance:**
  - Ensure that all reporting and analytics adhere to data privacy and security regulations.

- **Dashboard Integration:**
  - Integrate advanced reporting tools within the existing admin dashboards for seamless access.

#### User Flow:
[Link to User Flow](https://github.com/wasafiri/tam-vulcan-requirements/tree/main)

1. **Access Reporting Tools:**
   - MAT Staff navigates to the Reporting and Analytics section within the Admin portal.
2. **Generate Reports:**
   - Selects predefined reports or creates custom reports based on desired metrics.
3. **Analyze Data:**
   - Reviews interactive charts and graphs to identify trends and areas for improvement.
4. **Export and Share:**
   - Exports reports for presentation to stakeholders or for record-keeping purposes.
5. **Implement Improvements:**
   - Uses insights from reports to implement process improvements and enhance constituent satisfaction.

---

### Enhancing Communication and Feedback
**Title:** MAT User Accesses Real-Time Chat Support During Application

**As a** MAT User,  
**I want to** access real-time chat support while completing my application,  
**so that** I can receive immediate assistance and resolve any issues promptly.

#### Acceptance Criteria:

- **Live Chat Availability:**
  - A live chat button is prominently displayed on the application portal.
  - Utilize a gem or AI capability to turn FAQs into a mini chat AI.

#### User Flow:

1. **Encounter Issue:**
   - MAT User faces a question or technical issue while filling out the application.
2. **Initiate Chat:**
   - Clicks the live chat button to start a conversation with a support agent.
3. **Receive Assistance:**
   - Interacts with the support agent to resolve the issue or receive guidance.
4. **Continue Application:**
   - Applies the received assistance to complete the application successfully.

---

## Analysis of User Stories

After reviewing the provided user stories, the following observations regarding conflicts and dangling parts have been identified:

### 1. **Duplicate or Overlapping User Stories**

- **Equipment Ordering and Tracking vs. MAT Staff Managing Equipment Ordering and Vendor Interactions:**
  - Both sections cover equipment ordering processes, including bid form generation, vendor management, bid review, and interaction with the Finance Department.
  - **Recommendation:** Consider consolidating these two user stories into a single, comprehensive section to avoid redundancy and ensure clarity.

### 2. **Dangling Parts**

- **Advanced Reporting User Flow:**
  - The User Flow section contains a URL: `https://github.com/wasafiri/tam-vulcan-requirements/tree/main`
  - **Issue:** The link is incomplete and does not provide a descriptive path for the user flow.
  - **Recommendation:** Provide a detailed user flow diagram or description within the document. If the link is essential, ensure it points directly to the relevant content or remove it to maintain document integrity.

### 3. **Technical Details in User Stories**

- **Enhancing Communication and Feedback - Live Chat Availability:**
  - The acceptance criteria mention using a "gem or some sort of AI capability to turn FAQs into a mini chat AI."
  - **Issue:** User stories should focus on the **what** and **why**, not the **how**. Including specific technical implementations can limit flexibility in design and development.
  - **Recommendation:** Reframe the acceptance criteria to focus on the functionality (e.g., "Provide automated responses for common FAQs to assist users during the chat interaction") without specifying the technical approach.

### 4. **Consistency in User Roles**

- **MAT Staff vs. Admin User:**
  - Different sections refer to "MAT Staff" and "Admin User," which might cause confusion regarding their distinct roles and permissions.
  - **Recommendation:** Clearly define the roles and responsibilities of each user type at the beginning of the document to ensure consistent terminology throughout.

### 5. **Missing Acceptance Criteria**

- **Mobile Accessibility - MAT Staff Notifications Management:**
  - The "Mobile Accessibility" section primarily focuses on MAT Users but also includes acceptance criteria for MAT Staff managing notifications.
  - **Issue:** Mixing user roles within a single user story can lead to unclear requirements.
  - **Recommendation:** Separate user stories based on distinct user roles (e.g., one for MAT Users accessing the mobile app and another for MAT Staff managing notifications) to maintain clarity and focus.

### 6. **Incomplete User Flows**

- **Some User Flows Lack Detail:**
  - While most user flows are detailed, ensuring each step is actionable and complete, some sections like "Advanced Reporting" rely on external links without providing sufficient in-document detail.
  - **Recommendation:** Ensure all user flows are fully described within the document to provide a clear roadmap for development and testing.

### 7. **Role-Based Access Control Details**

- **MAT Staff Creating and Managing Administrator Accounts:**
  - The acceptance criteria mention "Role-Based Access Control" but do not detail the specific permissions associated with each role.
  - **Issue:** Lack of detailed permissions can lead to security vulnerabilities or role confusion.
  - **Recommendation:** Define specific permissions and access levels for each role to ensure secure and appropriate access within the application.
