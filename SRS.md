
Original document: [TT6L_G4_SRS_v1.6.7.docx](https://github.com/user-attachments/files/20814517/TT6L_G4_SRS_v1.6.7.docx)

Change #1 (18th June 25): [TT6L_G4_SRS_v1.6.7_Change1.docx](https://github.com/user-attachments/files/20815833/TT6L_G4_SRS_v1.6.7_Change1.docx)

Change #2 (19th June 25): [TT6L_G4_SRS_v1.6.7_Change2.docx](https://github.com/user-attachments/files/20817992/TT6L_G4_SRS_v1.6.7_Change2.docx)

Change #3 (20th June 25): [TT6L_G4_SRS_v1.6.7_Change3.docx](https://github.com/user-attachments/files/20840200/TT6L_G4_SRS_v1.6.7_Change3.docx)

___

![image](https://github.com/user-attachments/assets/c4704299-cd00-47c6-b8de-ebe5682442c5)


CSE6224 Software Requirements Engineering

Campus Wellness Portal with

Medical System and Fitness Center

Integration Project -- Part 1

SRS Document

Tutorial Section: TT6L

Group 4

| **Group member**                | **Student ID** |
|---------------------------------|----------------|
| Nicholas Thong Meng Shui        | 241UC2415Y     |
| Muhammad Anas bin Khairul Azman | 241UC2401Z     |
| Fikrul Amsyar Azmin             | 241UC24167     |

Table 1: Use Case ID Table

# **Table of Contents** {#table-of-contents .TOC-Heading .unnumbered}

[Changelog Table:](#changelog-table)

[1. Introduction](#introduction)

[1.1 Purpose](#purpose)

[1.2 Scope](#scope)

[1.3 Product Overview](#product-overview)

[1.3.1 Product Perspective](#product-perspective)

[1.3.2 Product functions](#product-functions)

[1.3.3 User Characteristics](#user-characteristics)

[1.3.4 Product Limitations](#product-limitations)

[2.0 References](#references)

[3.0 Requirements](#requirements)

[3.1 Functional Requirement](#functional-requirement)

[Context diagram](#context-diagram)

[Use Case Diagram](#use-case-diagram)

[Use Case ID table](#use-case-id-table)

[3.1.1Login](#login)

[3.1.2Book Fitness Class](#book-fitness-class)

[3.1.3Cancel Fitness Class](#cancel-fitness-class)

[3.1.4Schedule Health Centre Appointment](#schedule-health-centre-appointment)

[3.1.5 Cancel Health Centre Appointment](#cancel-health-centre-appointment)

[3.1.6 Track Wellness Goals](#track-wellness-goals)

[3.1.7 View System Notifications](#view-system-notifications)

[3.1.8 View Personalized Health Tips](#view-personalized-health-tips)

[3.1.9 Manage Health Centre Appointments](#manage-health-centre-appointments)

[3.1.10 Manage Fitness Class Booking](#manage-fitness-class-booking)

[3.1.11Manage User Access Control](#manage-user-access-control)

[3.1.12 View system logs](#view-system-logs)

[3.2 Performance Requirements](#performance-requirements)

[3.3 Usability Requirements](#usability-requirements)

[3.4 Interface Requirements](#interface-requirements)

[3.4.1 System Interfaces](#system-interfaces-1)

[3.4.2 User Interface](#user-interface)

[3.4.3 Hardware Interfaces](#hardware-interfaces)

[3.5 Logical Database Requirements](#logical-database-requirements)

[3.6 Design Constraints](#design-constraints)

[3.7 Software System Attributes](#software-system-attributes)

[3.7.1 Security](#security)

[3.8 Supporting Information](#supporting-information)

[4.0 Verification](#_Toc1770675368)

[4.1 Verification Approach](#verification-approach)

[4.2 Verification Criteria](#verification-criteria)

[4.2.1 Unit testing verification criteria](#unit-testing-verification-criteria)

[4.2.2 Integration testing verification criteria](#integration-testing-verification-criteria)

[4.2.3 Functional testing verification criteria](#functional-testing-verification-criteria)

[4.2.4 User acceptance testing (UAT) verification criteria](#user-acceptance-testing-uat-verification-criteria)

[4.2.5 Performance Verification Criteria](#performance-verification-criteria)

[4.2.6 Usability Verification Criteria](#usability-verification-criteria)

[5.0 Appendices](#appendices)

[5.1 Assumptions and Dependencies](#assumptions-and-dependencies)

[5.2 Acronyms and Abbreviations](#acronyms-and-abbreviations)

# Changelog Table: 

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Version</th>
<th>Author</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>v1.0</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Created this document</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.1</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Added information and content to 1.3.1 Product
Perspective</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.2</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Added information and content to 1.3.3 User
Characteristics</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.3</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added content to 1.3.2 Product Functions</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.4</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Added Use Case Diagram to 3.1 Functions</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.5</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Removed EHR System from 1.3.1</p></li>
<li><p>Updated 1.3.2 Campus Recreation Facility Integration</p></li>
<li><p>Created and added content to table 3-1 in 3.1 functions</p></li>
<li><p>Added table labels to tables 1-1 and 3-1</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.5.1</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added Product Limitations in 1.3.4</p></li>
<li><p>Added pretext for 3.1 Performance Requirements</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.5.2</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added performance requirement and use case table for
3.1.5</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.5.3</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added functional requirement and use case table for 3.1.6, 3.1.7,
3.1.9</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.5.4</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added sequence diagrams for 3.1.5, 3.1.6, 3.1.7, 3.1.9</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.5.5</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Fixed numbering for functional requirements</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V.1.5.6</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Added Functional Requirements and use case table for 3.1.8,
3.1.10, 3.1.11</p></li>
<li><p>Added Sequence Diagram for 3.1.8</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.5.7</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added cover page.</p></li>
<li><p>Added proper Table of Contents.</p></li>
<li><p>Added pre-text for upcoming chapters.</p></li>
<li><p>Added 3.2 Performance Requirements</p></li>
<li><p>Added 3.7 Security Requirements</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.6</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added 3.4 Interface Requirements</p></li>
<li><p>Login interface and appointment interface</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.6.1</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Updated figure 1.0 Use case diagram in 3.1 Functional
Requirements</p></li>
<li><p>Updated table 3-1 Use case ID in 3.1 Functional
Requirements</p></li>
<li><p>Updated use case table for 3.1.10, 3.1.11</p></li>
<li><p>Added Sequence Diagrams for 3.1.10, 3.1.11</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.6.2</td>
<td>Fikrul Amsyar Azmin</td>
<td><ul>
<li><p>Added functional requirements, use case table, and sequence
diagram for 3.1.1, 3.1.2, 3.1.3, 3.1.4</p></li>
<li><p>Added Project Purpose and Project Scope</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.6.3</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Added functional requirements tables for 3.1.11</p></li>
<li><p>Updated figure 1.0 Use case diagram in 3.1 Functional
Requirements</p></li>
<li><p>Updated functional requirements and removed sequence diagram for
3.1.9</p></li>
<li><p>Updated figure 1.0 Use case diagram in 3.1 Functional
Requirements</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.6.4</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Updated the sequence diagrams for 3.1.6, 3.1.7 and
3.1.8.</p></li>
<li><p>Fixed numbering issues for use cases 6, 7, 8.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V.1.6.5</td>
<td>Fikrul Amsyar Azmin</td>
<td><ul>
<li><p>Updated Project Scope</p></li>
<li><p>Update sequence diagrams for 3.1.1, 3.1.2, 3.1.3, 3.1.4</p></li>
<li><p>Added Usability Requirements</p></li>
<li><p>Added Design Constraints</p></li>
<li><p>Added functional requirements, use case table, sequence diagram
for 3.1.11</p></li>
</ul></td>
</tr>
<tr class="even">
<td>V1.6.6</td>
<td>Nicholas Thong Meng Shui</td>
<td><ul>
<li><p>Updated sequence diagrams for 3.1.8, 3.1.10, 3.1.12</p></li>
<li><p>Updated 3.4.2, use case table and 3.5</p></li>
</ul></td>
</tr>
<tr class="odd">
<td>V1.6.7</td>
<td>Muhammad Anas bin Khairul Azman</td>
<td><ul>
<li><p>Added 4.1 Verification Approach and 4.2 Verification
Criteria</p></li>
<li><p>Completed 4.1 and 4.2</p></li>
<li><p>Added labels and captions for every figure and table.</p></li>
<li><p>Added 3.8 Supporting Information.</p></li>
<li><p>Added 5.1 Assumptions and Dependencies and 5.2 Acronyms and
Abbreviations</p></li>
</ul></td>
</tr>
</tbody>
</table>

# Introduction

## Purpose

This project involves developing a wellness platform that integrates
with the university health centre's appointment system and campus
recreation facility management software. The system will enable students
to manage their holistic wellness by scheduling health centre
appointments, booking fitness classes, tracking personal wellness goals,
and receiving tailored health resources. 

## Scope

The system shall: 

ii. Schedule and cancel health centre appointments

iii. Book for a fitness class

iv. Tracks health goals

v.  Receive tailored health resources

vi. View personalized health tips

vii. Manage health centre appointments and fitness class booking

viii. Allow admins to manage user access control

ix. Allow admins to view system logs

The system is set to operate only for university students.

## 1.3 Product Overview {#product-overview}

### 1.3.1 Product Perspective {#product-perspective}

The Wellness Platform is a system that integrates the university health
centre's appointment system and campus recreation facility management
software. Its primary role is to support student wellness through
personalized health resources and wellness goals, integration with
university medical appointment records, and interaction with
recreational facilities.

As such, this system communicates and interoperates with several other
components of the university\'s infrastructure. These include the
university authentication system, recreation portal, and health portal.
The system utilizes these interfaces to authenticate users, retrieve
health data, enable health appointment scheduling, enable fitness class
scheduling, and provide wellness recommendations.

#### System Interfaces {#system-interfaces .unnumbered}

- **Authentication System**: The system relies on the university\'s
  login infrastructure to authenticate student users securely.

- **Recreation Portal**: Interfaces with the university's recreation
  facility management software to enable fitness class booking and data
  sharing.

- **Health Portal**: Interfaces with the university's health centre's
  appointment system to allow students to schedule health appointments.

#### User Interfaces {#user-interface}

1)  Wellness Platform shall include intuitive designs customised by
    their roles:

| User Role    | Interface Description                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Student      | Dashboard for setting, tracking and updating wellness goals, navigation bar to switch between managing fitness classes bookings screen, managing health centre appointments screen and a notifications panel. |
| System Admin | Buttons to access admin console and system logs.                                                                                                                                                              |

2)  Wellness Platform shall make use of light platinum (RGB Hex code:
    \#E1E2E4) colour for its overall background.

3)  Wellness Platform shall always have black (RGB Hex code: \#000000)
    font for non-navigation bar items unless specified otherwise.

4)  Wellness Platform shall always have a blue (RGB Hex code:
    \#000EBF)  
    navigation bar present at the top of the page.

5)  Wellness Platform shall always have white (RGB Hex code: \#FFFFFF)
    font for navigation bar items.

6)  Wellness Platform shall always have white (RGB Hex code: \#FFFFFF)
    for any frames within a page such as student notification frame,
    student wellness goal tracking frame, student manage fitness class
    booking and manage health centre appointment frame.

7)  Wellness Platform shall always have blue (RGB Hex code: \#000EBF)  
    for any buttons present on the platform unless specified otherwise.

#### Hardware Interfaces {#hardware-interfaces}

The system supports standard student devices such as personal computers
and mobile phones. No specialized hardware is required.

#### Software Interfaces {#software-interface}

| **Name**                           | **Mnemonic**     | **Specification Number** | **Version** | **Reference**                                                                                                          |
|------------------------------------|------------------|--------------------------|-------------|------------------------------------------------------------------------------------------------------------------------|
| University Health Portal           | UNIV_HEALTH_PORT | N/A                      | Current     | [University Health Patient Portal](https://www.universityhealth.com/patient-visitor-resources/patients/patient-portal) |
| University Recreation Portal       | UNIV_REC_PORTAL  | N/A                      | Current     | [Columbia University Recreation Portal](https://perec.columbia.edu/content/member-portal-resources)                    |
| OAuth 2.0 Authentication Framework | OAUTH2           | RFC 6749                 | Latest      | [OAuth 2.0 Specification](https://tools.ietf.org/html/rfc6749)                                                         |
| JSON Web Token Standard            | JWT              | RFC 7519                 | Latest      | [JWT Specification](https://tools.ietf.org/html/rfc7519)                                                               |
| RESTful API Interface              | REST_API         | OpenAPI 3.0              | Latest      | [OpenAPI Specification](https://swagger.io/specification/)                                                             |

Interfaces:

- University Health Portal

  - **Purpose**: To allow students to manage medical appointments and
    view personal health records.

  - **Interface Definition**: Web-based interface; provides scheduling,
    messaging, and medical record access. Integration through RESTful
    API.

  - **Reference**: University Health Patient Portal

- University Recreation Portal

  - **Purpose**: To enable scheduling and tracking of fitness classes
    and recreational activities.

  - **Interface Definition**: Booking and facility access information
    exchanged over REST API. Includes user authentication via SSO.

  - **Reference**: Columbia University Recreation Portal

- OAuth 2.0 Authentication Framework

  - **Purpose**: To authenticate students securely across university
    systems.

  - **Interface Definition**: Standard OAuth 2.0 protocol to handle
    login tokens and authorization. Interfaces with the university's
    identity provider.

  - **Reference**: OAuth 2.0 Specification

- JSON Web Token (JWT)

  - **Purpose**: To transmit session data securely between frontend and
    backend systems.

  - **Interface Definition**: Encodes claim-based tokens using standard
    JWT format (RFC 7519), embedded in HTTP headers.

  - **Reference**: JWT Specification

- RESTful API Interface

  - **Purpose**: To facilitate integration between the wellness platform
    and external systems such as the university's health portal and
    recreation systems.

  - **Interface Definition**: Uses HTTP(S) with standard methods (GET,
    POST, PUT, DELETE). Data formatted as JSON. Described using OpenAPI
    Specification.

  - **Reference**: OpenAPI Specification

#### Communication Interfaces {#communication-interfaces .unnumbered}

- HTTPS protocol is used for secure communication with internal
  university systems.

- Authentication via OAuth 2.0 and JWT for cross-system data sharing.

#### Memory Constraints {#memory-constraints .unnumbered}

The system is lightweight and web-based, requiring minimal local memory.
All user data is stored and processed in cloud/university-hosted
servers.

#### Operations {#operations .unnumbered}

The Wellness Platform is intended to function under both user-driven and
automated operations. The following operational requirements are
identified:

1\) Modes of Operation

- **User-Initiated Mode**: Students interact with the web application
  to:

  - Set and view wellness goals.

  - Book or cancel health centre or fitness appointments.

  - View personalized health resources.

  - View system notifications.

- **Admin Mode**: Authorized staff access logs or assign admins roles to
  others through secure dashboards.

2\) Periods of Interactive and Unattended Operations

- Interactive Operations:

  - Occur during active user sessions.

  - Includes booking appointments, viewing data, or modifying goals.

- Unattended Operations:

  - Background data syncing with Health Portal and Recreation Facility
    systems.

  - Periodic refresh of user statistics (e.g., wellness goals,
    appointment reminders).

  - Runs on a scheduled basis (e.g., nightly or hourly intervals).

3\) Data Processing Support Functions

- **Data Aggregation**: Collects fitness and medical data from multiple
  systems and consolidates it in the student dashboard.

- **Data Validation**: Ensures data accuracy and compliance with privacy
  regulations (e.g., HIPAA).

- **Error Logging**: Logs failures during API communication or user
  actions for diagnostics.

- **Monitoring**: System health checks and logging for server uptime and
  performance metrics.

#### Site Adaptation Requirements {#site-adaptation-requirements}

The system requires configuration of university-specific endpoints
(e.g., Recreation API URLs, fitness class schedule formats) during
deployment. It also requires institution-specific policy parameters
(e.g., data retention limits, HIPAA compliance flags).

#### Interfaces with Services {#interfaces-with-services}

Integrates with:

- University SaaS-based portals (e.g., health appointment scheduling)

- Cloud storage services (if enabled)

### 1.3.2 Product functions {#product-functions}

Campus Recreation Facility Integration

- Search and filter fitness classes by their type, date and location.

- Book fitness classes.

- Notification for open slots in fitness classes.

University Health Portal Integration

- Track personal wellness goals.

- Set personal wellness goals (steps, workout, sleep).

- Update existing wellness goals.

- Receive tailored health resources based on user preferences.

- Schedule appointments with the health centre.

- Cancel scheduled appointments.

### 1.3.3 User Characteristics {#user-characteristics}

Table 1-1 User Characteristics

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>User group</strong></th>
<th><strong>Description</strong></th>
<th><strong>Minimum Ability/Knowledge</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Students</td>
<td>Students currently enrolled in the university</td>
<td><ul>
<li><p>Possess basic computer skills.</p></li>
</ul></td>
</tr>
<tr class="even">
<td>System Admin</td>
<td>Administrators assigned by the university for this platform</td>
<td><ul>
<li><p>Possess basic computer skills</p></li>
<li><p>Possess basic grasp of system commands</p></li>
<li><p>Possess knowledge on web development.</p></li>
</ul></td>
</tr>
</tbody>
</table>

### 1.3.4 Product Limitations {#product-limitations .unnumbered}

#### 1.3.4.1 General Limitations {#general-limitations .unnumbered}

> The main limitations of our product comes from the fact that it is
> only accessible via web browser for ease of access for students.
> Furthermore, the use of this wellness portal is only accessible for
> students within the university and is not available for staff members
> (excluding system admins) of the university or students outside of the
> university.
>
> Student functions such as managing fitness classes and health centre
> appointments also depend on integration with the University Recreation
> Portal and University Health Portal. As such, any disruptions from
> either systems will also disrupt the Wellness Platform's
> functionality.
>
> The Wellness Platform is a web-based platform thus an internet
> connection is required to access it. Weak internet connections may
> also lead to buffering or slow loading of website elements.

# 2.0 References {#references .unnumbered}

HIPAA Document - [HIPAA for Dummies - 2025
Update](https://www.hipaaguide.net/hipaa-for-dummies/)

[University Health Patient
Portal](https://www.universityhealth.com/patient-visitor-resources/patients/patient-portal)

[Columbia University
Recreation](https://perec.columbia.edu/content/member-portal-resources)

[OAuth 2.0 Specification](https://tools.ietf.org/html/rfc6749)

[JWT Specification](https://tools.ietf.org/html/rfc7519)

[OpenAPI Specification](https://swagger.io/specification/)

# 3.0 Requirements {#requirements .unnumbered}

## 3.1 Functional Requirement {#functional-requirement .unnumbered}

### Context diagram {#context-diagram}

![A diagram of a campus wellness portal AI-generated content may be
incorrect.](media/image2.jpg){width="4.722222222222222in"
height="3.0555555555555554in"}

Figure 1: Context Diagram for Campus Wellness Portal

### Use Case Diagram {#use-case-diagram }

![A diagram of a company AI-generated content may be
incorrect.](media/image3.png){width="6.268055555555556in"
height="4.871527777777778in"}

Figure 2: Use Case Diagram for Campus Wellness Portal

### Use Case ID table {#use-case-id-table .unnumbered}

Below are the use cases mapped to their relevant requirements from the
Task 4/Kano Model.docx.

<table>
<colgroup>
<col style="width: 11%" />
<col style="width: 15%" />
<col style="width: 17%" />
<col style="width: 19%" />
<col style="width: 35%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th><strong>Actor(s)</strong></th>
<th><strong>Use Case (Function)</strong></th>
<th><p><strong>Relevant Requirement</strong></p>
<p><strong>ID(s)</strong></p></th>
<th><strong>Brief Description</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>UC_001</strong></td>
<td>Student</td>
<td>Login</td>
<td>REQID_01</td>
<td>Allows the student to log into the system using their
credentials.</td>
</tr>
<tr class="even">
<td><strong>UC_002</strong></td>
<td>Student</td>
<td>Book Fitness Class</td>
<td>REQID_04</td>
<td>Enables the student to select and book a fitness class from the
available options.</td>
</tr>
<tr class="odd">
<td><strong>UC_003</strong></td>
<td>Student</td>
<td>Cancel Fitness Class</td>
<td>REQID_05</td>
<td>Allows the student to cancel a previously booked fitness class.</td>
</tr>
<tr class="even">
<td><strong>UC_004</strong></td>
<td>Student</td>
<td>Schedule Health Centre Appointment</td>
<td>REQID_02</td>
<td>Allows the student to choose a time slot and book an appointment
with the health centre.</td>
</tr>
<tr class="odd">
<td><strong>UC_005</strong></td>
<td>Student</td>
<td>Cancel Health Centre Appointment</td>
<td>REQID_03</td>
<td>Enables the student to cancel a scheduled health centre
appointment.</td>
</tr>
<tr class="even">
<td><strong>UC_006</strong></td>
<td>Student</td>
<td>Track Wellness Goals</td>
<td>REQID_06</td>
<td>Allows the student to set, monitor, and update personal wellness
goals.</td>
</tr>
<tr class="odd">
<td><strong>UC_007</strong></td>
<td>Student</td>
<td>View System Notification</td>
<td>REQID_10, REQID_11</td>
<td>Enables the student to view any and all notifications from the
system.</td>
</tr>
<tr class="even">
<td><strong>UC_008</strong></td>
<td>Student</td>
<td>View Personalised Health Tips</td>
<td>REQID_12</td>
<td>Provides the student with curated health and wellness tips.</td>
</tr>
<tr class="odd">
<td><strong>UC_009</strong></td>
<td>Student</td>
<td>Manage Health Centre Appointments</td>
<td>REQID_08</td>
<td>Receives and updates student health appointment bookings and
cancellations.</td>
</tr>
<tr class="even">
<td><strong>UC_010</strong></td>
<td>Student</td>
<td>Manage Fitness Class Booking</td>
<td>REQID_09</td>
<td>Updates the fitness class schedule and availability based on
bookings or cancellations.</td>
</tr>
<tr class="odd">
<td><strong>UC_011</strong></td>
<td>Wellness System Admin</td>
<td>Manage User Access Control</td>
<td>-</td>
<td>Allows the admin to create, modify, and delete user accounts and
assign or revoke roles/permissions.</td>
</tr>
<tr class="even">
<td><strong>UC_012</strong></td>
<td>Wellness System Admin</td>
<td>View System Logs</td>
<td>-</td>
<td>Enables the admin to retrieve, review and export system logs for
monitoring and auditing purposes.</td>
</tr>
</tbody>
</table>

### 3.1.1 Login {#login .unnumbered}

Functional Requirement for Login

| **Requirement ID** | REQ_101                                      |
|--------------------|----------------------------------------------|
| **Description**    | System shall be able to validate user login. |
| **Author**         | Fikrul Amsyar Azmin                          |

| **Requirement ID** | REQ_102                                            |
|--------------------|----------------------------------------------------|
| **Description**    | System shall be able to process user registration. |
| **Author**         | Fikrul Amsyar Azmin                                |

| **Requirement ID** | REQ_103                                                                                                   |
|--------------------|-----------------------------------------------------------------------------------------------------------|
| **Description**    | System shall display an appropriate message when an error occurred where login credentials are incorrect. |
| **Author**         | Fikrul Amsyar                                                                                             |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_001</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F001 Login</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to login to their own account</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks on “Login” button on the wellness platform
portal</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User is in the wellness platform portal</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks on “Login” button on the wellness platform portal.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays the login page to the user.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User inputs login credentials (studentID, studentPassword) and
clicks the “Login” button.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays the wellness platform portal with the user account
logged in if the login credentials is valid.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow - Invalid Login Credentials</strong></td>
<td>1</td>
<td>System displays an appropriate error message to the user.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – Cancel Login</strong></td>
<td>1</td>
<td>User clicks on “Cancel Login” button on the login page.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays the wellness platform portal without the user
account logged in.</td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li><p>Login credentials must be within 25 characters.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Fikrul Amsyar Azmin</td>
</tr>
</tbody>
</table>

![](media/image4.png){width="6.260416666666667in" height="2.78125in"}

Figure 3: Sequence Diagram for Login

### 3.1.2 Book Fitness Class {#book-fitness-class .unnumbered}

| **Requirement ID** | REQ_201                                                          |
|--------------------|------------------------------------------------------------------|
| **Description**    | System shall allow users to book a class if spots are available. |
| **Author**         | Fikrul Amsyar Azmin                                              |

| **Requirement ID** | REQ_202                                                                         |
|--------------------|---------------------------------------------------------------------------------|
| **Description**    | System shall decrease the number of available spots after a successful booking. |
| **Author**         | Fikrul Amsyar Azmin                                                             |

| **Requirement ID** | REQ_203                                                                   |
|--------------------|---------------------------------------------------------------------------|
| **Description**    | System shall display a confirmation message when a booking is successful. |
| **Author**         | Fikrul Amsyar Azmin                                                       |

| **Requirement ID** | REQ_204                                                    |
|--------------------|------------------------------------------------------------|
| **Description**    | System shall display a table of available fitness classes. |
| **Author**         | Fikrul Amsyar Azmin                                        |

| **Requirement ID** | REQ_205                                                               |
|--------------------|-----------------------------------------------------------------------|
| **Description**    | System shall prompt the user if they want to book the selected class. |
| **Author**         | Fikrul Amsyar Azmin                                                   |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_002</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F002 Book Fitness Class</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to book for a fitness class.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks on “Book Fitness Class” button on the
wellness platform portal.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User account is logged in; User is in the wellness
platform portal</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks “Book Fitness Class” button on the wellness platform
portal.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a table of available fitness classes with “Book”
button on each row, and a “Go back” button at the top left near the
table.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks a “Book” button on the fitness classes table.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays a dialog box to the user if they want to book a
class.</td>
</tr>
<tr class="odd">
<td></td>
<td>5</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>6</td>
<td>System displays a confirmation message that a booking is
successful.</td>
</tr>
<tr class="odd">
<td></td>
<td>7</td>
<td>Back to Main Flow Step 2</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” in the dialog
box</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>Back to Main Flow Step 2</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “Go back” in the table of
available fitness classes</strong></td>
<td>1</td>
<td>User clicks “Go back” button in the table of available fitness
classes page.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>System displays the wellness platform portal.</td>
</tr>
<tr class="even">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Author</strong></td>
<td colspan="2">Fikrul Amsyar Azmin</td>
</tr>
</tbody>
</table>

![](media/image5.png){width="6.260416666666667in"
height="2.1979166666666665in"}

Figure 4: Sequence Diagram for Fitness Class Booking

### 3.1.3 Cancel Fitness Class {#cancel-fitness-class .unnumbered}

| **Requirement ID** | REQ_301                                                                      |
|--------------------|------------------------------------------------------------------------------|
| **Description**    | System shall allow users to cancel the selected class that the users booked. |
| **Author**         | Fikrul Amsyar Azmin                                                          |

| **Requirement ID** | REQ_302                                                                   |
|--------------------|---------------------------------------------------------------------------|
| **Description**    | System shall increase the number of available spots after a cancellation. |
| **Author**         | Fikrul Amsyar Azmin                                                       |

| **Requirement ID** | REQ_303                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------|
| **Description**    | System shall display a confirmation message after a successful booked class cancellation. |
| **Author**         | Fikrul Amsyar Azmin                                                                       |

| **Requirement ID** | REQ_304                                                                        |
|--------------------|--------------------------------------------------------------------------------|
| **Description**    | System shall prompt the user if they want to cancel the selected booked class. |
| **Author**         | Fikrul Amsyar Azmin                                                            |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_003</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F003 Cancel Fitness Class</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to cancel a booked fitness class.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks “Cancel” button on the manage fitness class
screen.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User is in the manage fitness class booking screen</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks “Cancel” button on the fitness class table.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a dialog box to the user if they want to cancel the
selected class.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays a confirmation message that the selected booked
class is cancelled.</td>
</tr>
<tr class="odd">
<td></td>
<td>5</td>
<td>System displays the manage fitness class booking screen.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” in the dialog
box</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>System displays the manage fitness class booking screen.</td>
</tr>
<tr class="even">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Author</strong></td>
<td colspan="2">Fikrul Amsyar Azmin</td>
</tr>
</tbody>
</table>

![](media/image6.png){width="6.1464468503937in"
height="2.5772134733158354in"}

Figure 5: Sequence Diagram for Cancelling Fitness Class

### 3.1.4 Schedule Health Centre Appointment {#schedule-health-centre-appointment .unnumbered}

| **Requirement ID** | REQ_401                                                          |
|--------------------|------------------------------------------------------------------|
| **Description**    | System shall allow users to schedule health centre appointments. |
| **Author**         | Fikrul Amsyar Azmin                                              |

| **Requirement ID** | REQ_402                                                               |
|--------------------|-----------------------------------------------------------------------|
| **Description**    | System shall display a table of available health centre appointments. |
| **Author**         | Fikrul Amsyar Azmin                                                   |

| **Requirement ID** | REQ_403                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------|
| **Description**    | System shall display a confirmation message after a successful schedule health centre appointment. |
| **Author**         | Fikrul Amsyar Azmin                                                                                |

| **Requirement ID** | REQ_404                                                                                    |
|--------------------|--------------------------------------------------------------------------------------------|
| **Description**    | System shall prompt the user if they want to make an appointment on the selected schedule. |
| **Author**         | Fikrul Amsyar Azmin                                                                        |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_004</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F004 Schedule Health Centre Appointments</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to schedule health centre
appointments.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks “Schedule Health Centre Appointments” button
on the wellness platform portal.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User account is logged in; User is in the wellness
platform portal</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks “Schedule Health Centre Appointments” button on the
wellness platform portal.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a table of available health centre appointments with
“Schedule appointment” button on each row, and a “Go back” button at the
top left near the table.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks a “Schedule appointment” button on the table of
available health centre appointments.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays a dialog box to the user if they want to make an
appointment on the selected schedule.</td>
</tr>
<tr class="odd">
<td></td>
<td>5</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>6</td>
<td>System displays a confirmation message that the appointment schedule
is successful.</td>
</tr>
<tr class="odd">
<td></td>
<td>7</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” in the dialog
box</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “Go back” in the table of
available health centre appointments</strong></td>
<td>1</td>
<td>User clicks “Go back” button in the table of available health centre
appointments.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>System displays the wellness platform portal.</td>
</tr>
<tr class="even">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Author</strong></td>
<td colspan="2">Fikrul Amsyar Azmin</td>
</tr>
</tbody>
</table>

![](media/image7.png){width="6.260416666666667in"
height="2.2083333333333335in"}

Figure 6: Sequence Diagram for Scheduling Health Centre Appointment

### 3.1.5 Cancel Health Centre Appointment {#cancel-health-centre-appointment .unnumbered}

Functional Requirement for Cancel Health Centre Appointment

| **Requirement ID** | REQ_501                                                            |
|--------------------|--------------------------------------------------------------------|
| **Description**    | System shall allow the user to cancel a health centre appointment. |
| **Author**         | Muhammad Anas                                                      |

| **Requirement ID** | REQ_502                                                                                  |
|--------------------|------------------------------------------------------------------------------------------|
| **Description**    | System shall prompt the user to confirm if they want to cancel the selected appointment. |
| **Author**         | Muhammad Anas                                                                            |

| **Requirement ID** | REQ_503                                                                                       |
|--------------------|-----------------------------------------------------------------------------------------------|
| **Description**    | System shall display a confirmation message that the selected appointment has been cancelled. |
| **Author**         | Muhammad Anas                                                                                 |

| **Requirement ID** | REQ_504                                                                         |
|--------------------|---------------------------------------------------------------------------------|
| **Description**    | System shall update user's appointments to reflect cancellation of appointment. |
| **Author**         | Muhammad Anas                                                                   |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_005</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F005 Cancel Health Centre Appointments</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to cancel their scheduled health centre
appointments.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks on “Cancel Appointment” button on a given
appointment.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User is in the manage health centre appointment
screen</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks on manage health centre appointment screen.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>User clicks on “Cancel Appointment” for a given appointment.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>System displays dialog box to confirm if the user wants to cancel
said appointment.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>User clicks on “Yes” in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>5</td>
<td>System updates user’s appointment table to reflect the cancelled
appointment.</td>
</tr>
<tr class="even">
<td></td>
<td>6</td>
<td>System displays confirmation message that the appointment has been
cancelled.</td>
</tr>
<tr class="odd">
<td></td>
<td>8</td>
<td>System displays the health centre appointment screen with the
cancelled appointment now updated.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” in the dialog
box</strong></td>
<td>1</td>
<td>User clicks on “No” in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>System displays the health centre appointment screen.</td>
</tr>
<tr class="even">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li><p>User must already have an existing scheduled
appointment.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Author</strong></td>
<td colspan="2">Muhammad Anas</td>
</tr>
</tbody>
</table>

![A diagram of a flowchart AI-generated content may be
incorrect.](media/image8.jpg){width="6.268055555555556in"
height="2.3201388888888888in"}

Figure 7: Sequence Diagram for Cancelling Health Centre Appointment

### 3.1.6 Track Wellness Goals {#track-wellness-goals .unnumbered}

Functional Requirement for Tracking Wellness Goals

| **Requirement ID** | REQ_601                                                                              |
|--------------------|--------------------------------------------------------------------------------------|
| **Description**    | System shall display the user's wellness goals over the past month in the dashboard. |
| **Author**         | Muhammad Anas                                                                        |

| **Requirement ID** | REQ_602                                                |
|--------------------|--------------------------------------------------------|
| **Description**    | System shall allow the user to set new wellness goals. |
| **Author**         | Muhammad Anas                                          |

| **Requirement ID** | REQ_603                                                     |
|--------------------|-------------------------------------------------------------|
| **Description**    | System shall allow the user to update their wellness goals. |
| **Author**         | Muhammad Anas                                               |

Use Case Table

| **Use Case ID**                                        | UC_006                                                                   |                                                                               |
|--------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| **Feature**                                            | F006 Track Personal Wellness Goals                                       |                                                                               |
| **Purpose**                                            | To allow users to monitor, set and update their personal wellness goals. |                                                                               |
| **Actor**                                              | Student                                                                  |                                                                               |
| **Trigger**                                            | User clicks on "Wellness Goals" button on the platform portal.           |                                                                               |
| **Precondition**                                       | User is in the wellness platform portal.                                 |                                                                               |
| **Scenario Name**                                      | **Step**                                                                 | **Action**                                                                    |
| **Main Flow -- Monitoring wellness goals**             | 1                                                                        | User clicks on "Wellness Goals" button on the platform portal.                |
|                                                        | 2                                                                        | System displays wellness goals dashboard to the user.                         |
| **Alternate Flow -- Setting new wellness goals**       | 3                                                                        | User clicks on "Set new wellness goal" button.                                |
|                                                        | 4                                                                        | System prompts the user to input their wellness goal.                         |
|                                                        | 5                                                                        | System updates the user's wellness goal database.                             |
|                                                        | 6                                                                        | System displays confirmation message that the wellness goal has been added.   |
|                                                        | 7                                                                        | System displays the updated wellness goal dashboard.                          |
| **Alternate Flow -- Updating existing wellness goals** | 1                                                                        | User clicks on "Update" button on a given wellness goal.                      |
|                                                        | 2                                                                        | System prompts the user to update the values for the wellness goal.           |
|                                                        | 3                                                                        | System updates the user's wellness goal database.                             |
|                                                        | 4                                                                        | System displays confirmation message that the wellness goal has been updated. |
|                                                        | 6                                                                        | System displays the updated wellness goal dashboard                           |
| **Rules**                                              | \-                                                                       |                                                                               |
| **Author**                                             | Muhammad Anas                                                            |                                                                               |

![A diagram of a diagram AI-generated content may be
incorrect.](media/image9.jpg){width="6.268055555555556in"
height="1.9in"}

Figure 8: Sequence Diagram for Tracking Wellness Goals

### 3.1.7 View System Notifications {#view-system-notifications .unnumbered}

Functional Requirement for Viewing Notifications

| Requirement ID | REQ_701                                                                                   |
|----------------|-------------------------------------------------------------------------------------------|
| Description    | System shall allow the user to view any fitness class and/or health centre notifications. |
| Author         | Muhammad Anas                                                                             |

| Requirement ID | REQ_702                                                                                |
|----------------|----------------------------------------------------------------------------------------|
| Description    | System shall display the fitness class and/or health centre notifications to the user. |
| Author         | Muhammad Anas                                                                          |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC_007</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F007 View System Notifications</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow users to view their fitness class and health
centre appointment notifications.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks on “Notifications” button on the platform
portal.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User is in the wellness platform portal.</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks on “Notifications” button on the platform portal.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays the fitness class and/or health centre notifications
to the user.</td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li><p>Users must be signed up/have booked a fitness class.</p></li>
<li><p>Without it, notifications will be empty.</p></li>
<li><p>Or – user must have an appointment booked.</p></li>
<li><p>Without it, no notifications from the health centre will be
sent.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Muhammad Anas</td>
</tr>
</tbody>
</table>

![A diagram of a health care system AI-generated content may be
incorrect.](media/image10.jpg){width="6.268055555555556in"
height="2.545138888888889in"}

Figure 9: Sequence Diagram for Viewing System Notifications

### 3.1.8 View Personalized Health Tips {#view-personalized-health-tips .unnumbered}

Functional Requirements for View Personalized Health Tips

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr class="header">
<th>Requirement ID</th>
<th>REQ_801</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Description</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>System shall retrieve health tips tailored to the student’s profile
and goals.</th>
</tr>
</thead>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td>Author</td>
<td>Nicholas Thong Meng Shui</td>
</tr>
</tbody>
</table>

| Requirement ID | REQ_802                                                                |
|----------------|------------------------------------------------------------------------|
| Description    | System shall display retrieved health tips in the student's dashboard. |
| Author         | Nicholas Thong Meng Shui                                               |

| Requirement ID | REQ_803                                                                      |
|----------------|------------------------------------------------------------------------------|
| Description    | System shall allow the student to request more details on any displayed tip. |
| Author         | Nicholas Thong Meng Shui                                                     |

Use Case Table

<table>
<colgroup>
<col style="width: 49%" />
<col style="width: 9%" />
<col style="width: 40%" />
<col style="width: 0%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="3">UC_008</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>F008 View Personalized Health Tips</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="3">Provide curated health and wellness tips based on
student profile.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="3">Student</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="3">Student selects “View Health Tips” on Student
Dashboard.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="3">Student is logged in and on Student Dashboard page; tips
database is accessible.</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
<td></td>
</tr>
<tr class="odd">
<td rowspan="5"><strong>Main Flow – User viewing health
tips</strong></td>
<td>1</td>
<td><table>
<colgroup>
<col style="width: 2%" />
<col style="width: 97%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Student clicks “Health Tips” menu.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>2</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>System retrieves tailored tips (REQ_801).</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="odd">
<td>3</td>
<td><table>
<colgroup>
<col style="width: 3%" />
<col style="width: 96%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>System displays tips list (REQ_802).</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>4</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Student selects a tip for more details.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="odd">
<td>5</td>
<td>System shows full tip details (REQ_803).</td>
<td></td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – No Tips Available</strong></td>
<td>2a</td>
<td>If no tips match profile, System displays “No personalized tips
available.”</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="3">Tips must be relevant to current wellness goals.</td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Nicholas Thong Meng Shui</td>
<td></td>
</tr>
</tbody>
</table>

![](media/image11.png){width="6.260416666666667in"
height="4.208333333333333in"}

Figure 10: Sequence Diagram for Viewing Personal Health Tips

### 3.1.9 Manage Health Centre Appointments {#manage-health-centre-appointments .unnumbered}

Functional Requirement for Manage Health Centre Appointments

| Requirement ID | REQ_901                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------|
| Description    | System shall allow the user the view their health centre appointments (scheduled and cancelled). |
| Author         | Muhammad Anas                                                                                    |

| Requirement ID | REQ_902                                                                 |
|----------------|-------------------------------------------------------------------------|
| Description    | System shall allow the user to schedule new health centre appointments. |
| Author         | Muhammad Anas                                                           |

| Requirement ID | REQ_903                                                                        |
|----------------|--------------------------------------------------------------------------------|
| Description    | System shall allow the user to cancel their booked health centre appointments. |
| Author         | Muhammad Anas                                                                  |

Use Case Table

| **Use Case ID**                                     | UC_009                                                                                                           |                                                                                         |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Feature**                                         | F009 Manage Health Centre Appointments                                                                           |                                                                                         |
| **Purpose**                                         | To receive and update a user's scheduled and cancelled health centre appointments.                               |                                                                                         |
| **Actor**                                           | University Health Portal                                                                                         |                                                                                         |
| **Trigger**                                         | User clicks on "Schedule Appointment" or "Cancel Appointment" button on the "Health Centre Appointments" screen. |                                                                                         |
| **Precondition**                                    | User is in the Health Centre Appointments screen.                                                                |                                                                                         |
| **Scenario Name**                                   | **Step**                                                                                                         | **Action**                                                                              |
| **Main Flow -- User scheduled an appointment**      | 1                                                                                                                | User clicks on "Health Centre Appointments" button on the Wellness dashboard. (REQ_901) |
|                                                     | 2                                                                                                                | User clicks on "Schedule Appointment" button -- invoke UC_004                           |
| **Alternate Flow -- User cancelled an appointment** | 1                                                                                                                | User clicks on "Health Centre Appointments" button on the Wellness dashboard.           |
|                                                     | 2                                                                                                                | User clicks on "Cancel Appointment" button on desired appointment -- invoke UC_005      |
| **Rules**                                           | \-                                                                                                               |                                                                                         |
| **Author**                                          | Muhammad Anas                                                                                                    |                                                                                         |

![A diagram of a process AI-generated content may be
incorrect.](media/image12.jpg){width="5.666666666666667in"
height="2.0972222222222223in"}

Figure 11: Sequence Diagram for Scheduling Health Centre Appointment

### 3.1.10 Manage Fitness Class Booking {#manage-fitness-class-booking .unnumbered}

Functional Requirements for Manage Fitness Class Booking

| Requirement ID | REQ_1001                                                             |
|----------------|----------------------------------------------------------------------|
| Description    | System shall display a list of the student's current class bookings. |
| Author         | Nicholas Thong Meng Shui                                             |

| Requirement ID | REQ_1002                                                                            |
|----------------|-------------------------------------------------------------------------------------|
| Description    | System shall allow branching to either the Book or Cancel use case based on action. |
| Author         | Nicholas Thong Meng Shui                                                            |

| Requirement ID | REQ_1003                                                                       |
|----------------|--------------------------------------------------------------------------------|
| Description    | Upon completion of the child use case, system shall refresh the bookings list. |
| Author         | Nicholas Thong Meng Shui                                                       |

| Requirement ID | REQ_1004                                                                   |
|----------------|----------------------------------------------------------------------------|
| Description    | If the Book or Cancel use case produces an error, system shall display it. |
| Author         | Nicholas Thong Meng Shui                                                   |

Use Case Table

<table>
<colgroup>
<col style="width: 49%" />
<col style="width: 9%" />
<col style="width: 40%" />
<col style="width: 0%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="3">UC_010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>F010 Manage Fitness Class Booking</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="3">Allows students to view, book and cancel fitness-class
reservations from one page.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Student</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Student navigates to the “Fitness Class Bookings” screen.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="3">Student is logged in; “Fitness Class Bookings” screen is
displayed.</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
<td></td>
</tr>
<tr class="odd">
<td rowspan="6"><strong>Main Flow – Student view, book or cancel fitness
class</strong></td>
<td>1</td>
<td><table>
<colgroup>
<col style="width: 2%" />
<col style="width: 97%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>System displays a table of the student’s current class
reservations.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>2</td>
<td>Student views scheduled fitness classes</td>
<td></td>
</tr>
<tr class="odd">
<td>3</td>
<td><table>
<colgroup>
<col style="width: 3%" />
<col style="width: 96%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Student clicks either “Book Class” or “Cancel Class.”</th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>3.1</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>If “Book Class”: invoke <strong>UC002 Book Fitness
Class</strong></th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="odd">
<td>3.2</td>
<td>If “Cancel Class”: invoke <strong>UC003 Cancel Fitness
Class</strong></td>
<td></td>
</tr>
<tr class="even">
<td>4</td>
<td>System refreshes and re-displays the updated reservations
table.</td>
<td></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Alternate Flow – Table error</strong></td>
<td>1a</td>
<td>Recreation Portal API returns error during table request.</td>
<td></td>
</tr>
<tr class="even">
<td>1b</td>
<td>System logs and displays error</td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="3">Booking requests must include valid student and class
identifiers.</td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Nicholas Thong Meng Shui</td>
<td></td>
</tr>
</tbody>
</table>

![](media/image13.png){width="5.9375in" height="6.260416666666667in"}

Figure 12: Sequence Diagram for Managing Fitness Classes

### 3.1.11 Manage User Access Control {#manage-user-access-control .unnumbered}

Functional Requirement for Manage User Access Control

| **Requirement ID** | REQ_1101                                                  |
|--------------------|-----------------------------------------------------------|
| **Description**    | System shall allow an admin to create a new user account. |
| **Author**         | Fikrul Amsyar Azmin                                       |

| **Requirement ID** | REQ_1102                                                            |
|--------------------|---------------------------------------------------------------------|
| **Description**    | System shall allow an admin to view and edit existing user details. |
| **Author**         | Fikrul Amsyar Azmin                                                 |

| **Requirement ID** | REQ_1103                                                            |
|--------------------|---------------------------------------------------------------------|
| **Description**    | System shall allow an admin to delete or deactivate a user account. |
| **Author**         | Fikrul Amsyar Azmin                                                 |

| **Requirement ID** | REQ_1104                                                           |
|--------------------|--------------------------------------------------------------------|
| **Description**    | System shall allow an admin to assign one or more roles to a user. |
| **Author**         | Fikrul Amsyar Azmin                                                |

| **Requirement ID** | REQ_1105                                                              |
|--------------------|-----------------------------------------------------------------------|
| **Description**    | System shall allow an admin to assign or revoke specific permissions. |
| **Author**         | Fikrul Amsyar Azmin                                                   |

| **Requirement ID** | REQ_1106                                                          |
|--------------------|-------------------------------------------------------------------|
| **Description**    | System shall display a table of all users, including their roles. |
| **Author**         | Fikrul Amsyar Azmin                                               |

| **Requirement ID** | REQ_1107                                                                 |
|--------------------|--------------------------------------------------------------------------|
| **Description**    | System shall prompt for confirmation to the admin before making changes. |
| **Author**         | Fikrul Amsyar Azmin                                                      |

Use Case Table

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 8%" />
<col style="width: 41%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="2">UC011</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="2">F011 Manage User Access Control</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="2">To allow the admin to create, modify, and delete user
accounts and assign or revoke roles/permissions.</td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="2">Wellness System Admin</td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="2">User clicks on “Manage User Accounts” button on the
wellness system admin screen.</td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="2">User account is logged in; User is in the wellness
system admin screen.</td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
</tr>
<tr class="odd">
<td><strong>Main Flow</strong></td>
<td>1</td>
<td>User clicks “Manage User Accounts” button on the wellness system
admin screen.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a table of user accounts with “Edit” and “Delete”
button on each row. A “Create Account” button at the bottom of the
table. A “Go back” button at top left corner of the screen.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks “Go back” button on the manage user accounts
screen.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays wellness system admin screen.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – Edit Account</strong></td>
<td>1</td>
<td>User clicks an “Edit” button in the table .</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays user account edit screen with a “Save” and “Cancel”
button at the bottom of the screen.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User edits the user account details, roles, and permissions, and
clicks “Save” button.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>System displays a dialog box to the user if they want to save the
changes.</td>
</tr>
<tr class="odd">
<td></td>
<td>5</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>6</td>
<td>System displays a confirmation message that the user account data is
updated.</td>
</tr>
<tr class="odd">
<td></td>
<td>7</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” in the save changes dialog
box</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>Back to Alternate Flow – Edit Account Step 2.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “Cancel” button in the user
account edit screen</strong></td>
<td>1</td>
<td>System displays a dialog box to the user if they want to go back to
previous screen without savng.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>3</td>
<td>Back to Main Flow Step 2 without the changes saved.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – User clicks “No” button in the go back
without saving dialog box</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>Back to Alternate Flow – Edit Account Step 2.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – Delete User Account</strong></td>
<td>1</td>
<td>User clicks a “Delete” button in the user accounts table.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a dialog box to the user if they want to delete the
selected account.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>5</td>
<td>System displays a confirmation message that the selected user
account is deleted.</td>
</tr>
<tr class="odd">
<td></td>
<td>6</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – User clicks “No” button in the account
deletion dialog box.</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>Back to Main Flow Step 2 without the selected user account removed
from the table.</td>
</tr>
<tr class="even">
<td><strong>Alternate Flow – Create User Account</strong></td>
<td>1</td>
<td>User clicks “Create Account” button on the manage user account
screen.</td>
</tr>
<tr class="odd">
<td></td>
<td>2</td>
<td>System displays create user account screen with “Create” and
“Cancel” button at the bottom of the screen.</td>
</tr>
<tr class="even">
<td></td>
<td>3</td>
<td>User inputs the user account details, roles, and permissions, and
clicks “Create” button.</td>
</tr>
<tr class="odd">
<td></td>
<td>4</td>
<td>System displays a dialog box to the user if they want to create the
account.</td>
</tr>
<tr class="even">
<td></td>
<td>5</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="odd">
<td></td>
<td>6</td>
<td>System displays a confirmation message that a user account has been
created.</td>
</tr>
<tr class="even">
<td></td>
<td>7</td>
<td>Back to Main Flow Step 2.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – User clicks “No” button in the account
creation dialog box.</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>Back to Alternate Flow – Create User Account Step 2.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – User clicks “Cancel” button in the account
creation screen.</strong></td>
<td>1</td>
<td>User clicks “Cancel” button in the account creation screen.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>System displays a dialog box to the user if they want to cancel the
account creation.</td>
</tr>
<tr class="odd">
<td></td>
<td>3</td>
<td>User clicks “Yes” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>4</td>
<td>Back to Main Flow Step 2 without the user account added in the
table.</td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – User clicks “No” button in the cancel
account creation screen.</strong></td>
<td>1</td>
<td>User clicks “No” button in the dialog box.</td>
</tr>
<tr class="even">
<td></td>
<td>2</td>
<td>Back to Alternate Flow – Create User Account Step 2.</td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="2"><ul>
<li></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Fikrul Amsyar Azmin</td>
</tr>
</tbody>
</table>

![](media/image14.png){width="6.260416666666667in"
height="3.6979166666666665in"}

Figure 13: Sequence Diagram for Managing Use Access

### 3.1.12 View system logs {#view-system-logs .unnumbered}

Functional requirements for view system logs

| Requirement ID | REQ_1201                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------|
| Description    | System shall allow administrators to filter logs by date range, severity level, and source module. |
| Author         | Nicholas Thong Meng Shui                                                                           |

| Requirement ID | REQ_1202                                                                                    |
|----------------|---------------------------------------------------------------------------------------------|
| Description    | System shall display a paginated list of log entries matching the selected filter criteria. |
| Author         | Nicholas Thong Meng Shui                                                                    |

| Requirement ID | REQ_1203                                                                                           |
|----------------|----------------------------------------------------------------------------------------------------|
| Description    | System shall show full details (timestamp, actor, action, message, stack trace) for any log entry. |
| Author         | Nicholas Thong Meng Shui                                                                           |

| Requirement ID | REQ_1204                                                                                |
|----------------|-----------------------------------------------------------------------------------------|
| Description    | System shall allow administrators to export filtered log entries in CSV or JSON format. |
| Author         | Nicholas Thong Meng Shui                                                                |

| Requirement ID | REQ_1205                                                                                              |
|----------------|-------------------------------------------------------------------------------------------------------|
| Description    | System shall restrict access to the View Logs feature to users with the "Wellness System Admin" role. |
| Author         | Nicholas Thong Meng Shui                                                                              |

| Requirement ID | REQ_1206                                                                                        |
|----------------|-------------------------------------------------------------------------------------------------|
| Description    | System shall log each "view" or "export" action performed by administrators for audit purposes. |
| Author         | Nicholas Thong Meng Shui                                                                        |

Use Case Table

<table>
<colgroup>
<col style="width: 49%" />
<col style="width: 9%" />
<col style="width: 40%" />
<col style="width: 0%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Use Case ID</strong></th>
<th colspan="3">UC_012</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Feature</strong></td>
<td colspan="3">F012 View System Logs</td>
</tr>
<tr class="even">
<td><strong>Purpose</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Provide administrators with on-demand access to system logs for
monitoring and troubleshooting.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><strong>Actor</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Wellness System Admin</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><strong>Trigger</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Admin selects “View System Logs” in the admin page.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><strong>Precondition</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Admin is authenticated and has “Wellness System Admin” role.; Log
database is reachable.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="even">
<td><strong>Scenario Name</strong></td>
<td><strong>Step</strong></td>
<td><strong>Action</strong></td>
<td></td>
</tr>
<tr class="odd">
<td rowspan="6"><strong>Main Flow – User scheduled an
appointment</strong></td>
<td>1</td>
<td><table>
<colgroup>
<col style="width: 2%" />
<col style="width: 97%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Admin navigates to the System Logs page.</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>2</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>System displays filter controls (date range, severity, source).
(<em>REQ-1201)</em></th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="odd">
<td>3</td>
<td><table>
<colgroup>
<col style="width: 3%" />
<col style="width: 96%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Admin enters filter criteria and clicks “Search.”</th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="even">
<td>4</td>
<td><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
</tbody>
</table>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>System retrieves matching log entries, paginates them, and displays
a summary list. (<em>REQ-1202)</em></th>
</tr>
</thead>
<tbody>
</tbody>
</table></th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
<td></td>
</tr>
<tr class="odd">
<td>5</td>
<td>Admin clicks on a specific log entry.</td>
<td></td>
</tr>
<tr class="even">
<td>6</td>
<td>System shows full details of that entry (timestamp, actor, action,
message, stack trace). (<em>REQ-1203)</em></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Alternate Flow – No Matching Logs</strong></td>
<td>4a</td>
<td>If no log entries match the filter, System displays “No records
found” and offers to clear filters.</td>
<td></td>
</tr>
<tr class="even">
<td rowspan="3"><strong>Alternate Flow – Export Logs</strong></td>
<td>7a</td>
<td>Integration Service receives data with unexpected format from one
portal.</td>
<td></td>
</tr>
<tr class="odd">
<td>7b</td>
<td>System generates the export file and makes it available for
download. (<em>REQ-1204)</em></td>
<td></td>
</tr>
<tr class="even">
<td>7c</td>
<td>System records the “view” and/or “export” action in an audit log.
(<em>REQ-1206)</em></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>Rules</strong></td>
<td colspan="3"><p>- Only one export operation can run at a time per
admin session.</p>
<p>- Log entries must be retained for at least 90 days.</p></td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="2">Nicholas Thong Meng Shui</td>
<td></td>
</tr>
</tbody>
</table>

Sequence diagram for viewing system
logs:![](media/image15.png){width="6.260416666666667in" height="6.25in"}

Figure 14: Sequence Diagram for Viewing System Logs

## 3.2 Performance Requirements {#performance-requirements .unnumbered}

The performance for the Campus Wellness Portal are as follows:

| **Requirement ID** | **Description**                                                                      | **Priority** | **Author**    |
|--------------------|--------------------------------------------------------------------------------------|--------------|---------------|
| REQ_P001           | The average response time of Wellness Portal functions shall be less than 2 seconds. | High         | Muhammad Anas |

## 3.3 Usability Requirements {#usability-requirements .unnumbered}

| **Requirement ID** | **Description**                                                                                          | **Priority** | **Author**          |
|--------------------|----------------------------------------------------------------------------------------------------------|--------------|---------------------|
| REQ_UR001          | System shall be intuitive enough for first-time users to perform basic tasks without extensive training. | High         | Fikrul Amsyar Azmin |

| **Requirement ID** | **Description**                                                       | **Priority** | **Author**          |
|--------------------|-----------------------------------------------------------------------|--------------|---------------------|
| REQ_UR002          | Consistent design patterns and navigation shall be used across pages. | High         | Fikrul Amsyar Azmin |

| **Requirement ID** | **Description**                                                                                     | **Priority** | **Author**          |
|--------------------|-----------------------------------------------------------------------------------------------------|--------------|---------------------|
| REQ_UR003          | System shall prevent user errors through input validation, tooltips, and disabling invalid options. | High         | Fikrul Amsyar Azmin |

## 3.4 Interface Requirements {#interface-requirements .unnumbered}

This section covers the external interface requirements of the Campus
Wellness Portal, separated by the features of the system.

### 3.4.1 System Interfaces {#system-interfaces-1 .unnumbered}

#### 3.4.1.1 University Health Portal Interface {#university-health-portal-interface .unnumbered}

| **Requirement ID** | REQ_SI101                                                                                                                          | **Version** | 1.0 |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------|-------------|-----|
| **Item**           | Health Portal Interface                                                                                                            |             |     |
| **Description**    | The campus wellness portal interacts with the university's health portal to manage appointments with the university health centre. |             |     |
| **Purpose**        | Allows the management of user's health centre appointment from the wellness portal.                                                |             |     |
| **Author**         | Muhammad Anas                                                                                                                      |             |     |

#### 3.4.1.2 University Recreation Portal Interface {#university-recreation-portal-interface .unnumbered}

| **Requirement ID** | REQ_SI102                                                                                                      | **Version** | 1.0 |
|--------------------|----------------------------------------------------------------------------------------------------------------|-------------|-----|
| **Item**           | Recreation Portal Interface                                                                                    |             |     |
| **Description**    | The campus wellness portal interacts with the university's recreation portal to manage fitness class bookings. |             |     |
| **Purpose**        | Allows the management of user's fitness class bookings from the wellness portal.                               |             |     |
| **Author**         | Muhammad Anas                                                                                                  |             |     |

### 3.4.2 User Interface {#user-interface .unnumbered}

#### 3.4.2.1 Login Interface {#login-interface .unnumbered}

| **Requirement ID** | REQ_UI101                                   | **Version**     | 1.0            |
|--------------------|---------------------------------------------|-----------------|----------------|
| **Item**           | Student ID (input)                          |                 |                |
| **Description**    | Input student ID on the portal login        |                 |                |
| **Purpose**        | To allow the student to log into the portal |                 |                |
| **Format**         | String/Text                                 | **Valid Range** | Not applicable |
| **Related I/O**    | None                                        |                 |                |
| **Author**         | Muhammad Anas                               |                 |                |

| **Requirement ID** | REQ_UI102                                   | **Version**     | 1.0            |
|--------------------|---------------------------------------------|-----------------|----------------|
| **Item**           | Student password (input)                    |                 |                |
| **Description**    | Input student password on the portal login  |                 |                |
| **Purpose**        | To allow the student to log into the portal |                 |                |
| **Format**         | String/Text                                 | **Valid Range** | Not applicable |
| **Related I/O**    | None                                        |                 |                |
| **Author**         | Muhammad Anas                               |                 |                |

| **Requirement ID** | REQ_UI103                                                                      | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | 'Login Button' button (input)                                                  |                 |                |
| **Description**    | Sends Student ID and Student password information to the authentication system |                 |                |
| **Purpose**        | To allow the student to log into the portal                                    |                 |                |
| **Format**         | Button                                                                         | **Valid Range** | Not applicable |
| **Related I/O**    | None                                                                           |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                       |                 |                |

#### 3.4.2.2 Navigation Bar Interface {#navigation-bar-interface .unnumbered}

The navigation bar will provide easy access to students and admins to
navigate to certain pages.

Navigation bar items:

| **Requirement ID** | REQ_UI201                                                     | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------------|-----------------|----------------|
| **Item**           | 'Dashboard' button (input)                                    |                 |                |
| **Description**    | Button to navigate to the Student Dashboard screen            |                 |                |
| **Purpose**        | To allow the student to see and interact with their dashboard |                 |                |
| **Format**         | Button                                                        | **Valid Range** | Not applicable |
| **Related I/O**    | None                                                          |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                      |                 |                |

| **Requirement ID** | REQ_UI202                                                      | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------|-----------------|----------------|
| **Item**           | 'Fitness Class Bookings' button (input)                        |                 |                |
| **Description**    | Button to navigate to the Manage Fitness Class Bookings screen |                 |                |
| **Purpose**        | To allow the student to manage their fitness classes           |                 |                |
| **Format**         | Button                                                         | **Valid Range** | Not applicable |
| **Related I/O**    | Output: "Fitness Class Bookings" screen                        |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                       |                 |                |

| **Requirement ID** | REQ_UI203                                                          | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------------|-----------------|----------------|
| **Item**           | 'Health Centre Appointments' button (input)                        |                 |                |
| **Description**    | Button to navigate to the Manage Health Centre Appointments screen |                 |                |
| **Purpose**        | To allow the student to manage their health centre appointments    |                 |                |
| **Format**         | Button                                                             | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Manage Health Care Appointments table                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                           |                 |                |

| **Requirement ID** | REQ_UI204                                                      | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------|-----------------|----------------|
| **Item**           | 'Notifications' button (Input)                                 |                 |                |
| **Description**    | Button to view notifications from the system                   |                 |                |
| **Purpose**        | To allow the student to view all notifications from the system |                 |                |
| **Format**         | Button                                                         | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Notifications Panel                                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                       |                 |                |

#### 3.4.2.3 Student Dashboard Interface {#student-dashboard-interface .unnumbered}

The Student Dashboard interface will use a responsive layout with a
fixed top navigation bar.

Student Dashboard Items:

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 26%" />
<col style="width: 26%" />
<col style="width: 26%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Requirement ID</strong></th>
<th>REQ_UI301</th>
<th><strong>Version</strong></th>
<th>1.0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Item</strong></td>
<td colspan="3">“Wellness Goals” button (Input)</td>
</tr>
<tr class="even">
<td><strong>Description</strong></td>
<td colspan="3"><table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>Button to open the Wellness Goals dashboard</th>
</tr>
</thead>
<tbody>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><strong>Purpose</strong></td>
<td colspan="3">To allow the student to view their wellness-goals
page</td>
</tr>
<tr class="even">
<td><strong>Format</strong></td>
<td>Button</td>
<td><strong>Valid Range</strong></td>
<td>Not applicable</td>
</tr>
<tr class="odd">
<td><strong>Related I/O</strong></td>
<td colspan="3">Output: Wellness Goals dashboard</td>
</tr>
<tr class="even">
<td><strong>Author</strong></td>
<td colspan="3">Nicholas Thong Meng Shui</td>
</tr>
</tbody>
</table>

| **Requirement ID** | REQ_UI302                                       | **Version**     | 1.0            |
|--------------------|-------------------------------------------------|-----------------|----------------|
| **Item**           | "Set new wellness goal" button (Input)          |                 |                |
| **Description**    | Button to initiate creation of a new goal       |                 |                |
| **Purpose**        | To allow the student to add a new wellness goal |                 |                |
| **Format**         | Button                                          | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Input wellness goal prompt              |                 |                |
| **Author**         | Nicholas Thong Meng Shui                        |                 |                |

| **Requirement ID** | REQ_UI303                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | "Update" button (Input)                                  |                 |                |
| **Description**    | Button to edit an existing wellness goal                 |                 |                |
| **Purpose**        | To allow the student to modify an existing goal's values |                 |                |
| **Format**         | Button                                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Update-goal prompt dialog (Input)                |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

| **Requirement ID** | REQ_UI304                                           | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------|-----------------|----------------|
| **Item**           | Wellness Goals dashboard (Output)                   |                 |                |
| **Description**    | Screen showing the student's current wellness goals |                 |                |
| **Purpose**        | To present all tracked goals and their status       |                 |                |
| **Format**         | Screen/UI                                           | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Wellness Goals" button                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                            |                 |                |

| **Requirement ID** | REQ_UI305                                             | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------|-----------------|----------------|
| **Item**           | Wellness goal prompt dialog (Input)                   |                 |                |
| **Description**    | Dialog prompting student to enter a new wellness goal |                 |                |
| **Purpose**        | To collect details for a new goal                     |                 |                |
| **Format**         | Modal dialog                                          | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Set new wellness goal" button                 |                 |                |
| **Author**         | Nicholas Thong Meng Shui                              |                 |                |

| **Requirement ID** | REQ_UI306                                               | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------|-----------------|----------------|
| **Item**           | Update-goal prompt dialog (Input)                       |                 |                |
| **Description**    | Dialog prompting student to modify existing goal values |                 |                |
| **Purpose**        | To collect updated information for an existing goal     |                 |                |
| **Format**         | Modal dialog                                            | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Update" button                                  |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                |                 |                |

| **Requirement ID** | REQ_UI307                                                   | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------|-----------------|----------------|
| **Item**           | Updated Wellness Goals dashboard                            |                 |                |
| **Description**    | Screen showing the refreshed list of wellness goals         |                 |                |
| **Purpose**        | To inform the student that their goal update has been saved |                 |                |
| **Format**         | Toast/banner                                                | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Update" button                                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                    |                 |                |

| **Requirement ID** | REQ_UI308                                                          | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "View Health Tips" Button (Input)                                  |                 |                |
| **Description**    | Button on the Student Dashboard to access personalized tips        |                 |                |
| **Purpose**        | To allow the student to retrieve tailored health and wellness tips |                 |                |
| **Format**         | Button                                                             | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Health Tips list                                           |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                           |                 |                |

| **Requirement ID** | REQ_UI309                                                       | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------------|-----------------|----------------|
| **Item**           | Health Tips list (Output)                                       |                 |                |
| **Description**    | Scrollable list displaying brief summaries of curated tips      |                 |                |
| **Purpose**        | To present all personalized tips matching the student's profile |                 |                |
| **Format**         | List with selectable items                                      | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "View Health Tips" menu item                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                        |                 |                |

| **Requirement ID** | REQ_UI310                                                                  | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Tip Details panel (Output)                                                 |                 |                |
| **Description**    | Panel or modal showing full details of a selected tip                      |                 |                |
| **Purpose**        | To allow the student to read and understand a specific health tip in-depth |                 |                |
| **Format**         | Panel / Modal dialog                                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Health Tips list (when a tip is selected)                           |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                   |                 |                |

| **Requirement ID** | REQ_UI311                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | "No Tips Available" message (Output))                    |                 |                |
| **Description**    | Inline message stating "No personalized tips available." |                 |                |
| **Purpose**        | To inform the student when no tips match their profile   |                 |                |
| **Format**         | Inline text / Banner                                     | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "View Health Tips" button (when list is empty)    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

#### 3.4.2.4 Notification Interface {#notification-interface .unnumbered}

| **Requirement ID** | REQ_UI401                                                                                | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Notifications Panel (Output)                                                             |                 |                |
| **Description**    | Panel displaying system notifications, including fitness-class and health-centre updates |                 |                |
| **Purpose**        | To present the student with all current notifications in a consolidated view             |                 |                |
| **Format**         | Panel / Sidebar UI                                                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Notifications" button                                                            |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                 |                 |                |

#### 3.4.2.5 Managing Health Care Appointments Interface {#managing-health-care-appointments-interface .unnumbered}

The Managing Health Care Appointments interface will use a responsive
layout with a fixed top navigation bar.

Managing Health Care Appointments items:

| **Requirement ID** | REQ_UI501                                                                                                      | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Manage Health Care Appointments table (Output)                                                                 |                 |                |
| **Description**    | Table listing current appointments with both "Schedule appointment" and "Cancel Appointment" actions available |                 |                |
| **Purpose**        | To present existing bookings and allow scheduling/cancellation without leaving the page                        |                 |                |
| **Format**         | Table with action buttons                                                                                      | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Health Centre Appointments" button                                                                     |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                                       |                 |                |

| **Requirement ID** | REQ_UI502                                                                 | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Schedule Health Centre Appointments" button (Input)                      |                 |                |
| **Description**    | Button to open the available-appointments view                            |                 |                |
| **Purpose**        | To allow the student to view and choose from upcoming health centre slots |                 |                |
| **Format**         | Button                                                                    | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Available Appointments table                                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                  |                 |                |

| **Requirement ID** | REQ_UI503                                                                                   | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Available Appointments table (Output)                                                       |                 |                |
| **Description**    | Tabular list of upcoming health centre timeslots, each with a "Schedule appointment" button |                 |                |
| **Purpose**        | To display all slots the student can book                                                   |                 |                |
| **Format**         | Table with action buttons                                                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Schedule Health Centre Appointments" button                                         |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                    |                 |                |

| **Requirement ID** | REQ_UI504                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | "Schedule appointment" button (Input)                    |                 |                |
| **Description**    | Button on each row to initiate booking of that timeslot  |                 |                |
| **Purpose**        | To let the student confirm which appointment to schedule |                 |                |
| **Format**         | Button (per row)                                         | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Schedule Confirmation dialog                     |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

| **Requirement ID** | REQ_UI505                                               | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------|-----------------|----------------|
| **Item**           | Schedule Confirmation dialog (Output)                   |                 |                |
| **Description**    | Modal asking "Do you want to confirm this appointment?" |                 |                |
| **Purpose**        | To get explicit user confirmation before booking        |                 |                |
| **Format**         | Modal dialog with "Yes"/"No" buttons)                   | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Schedule appointment" button                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                |                 |                |

| **Requirement ID** | REQ_UI506                                                       | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------------|-----------------|----------------|
| **Item**           | Booking Confirmation message (Output)                           |                 |                |
| **Description**    | Inline toast/banner saying "Appointment scheduled successfully" |                 |                |
| **Purpose**        | To inform the student the booking went through                  |                 |                |
| **Format**         | Toast/banner notification                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Schedule Confirmation dialog                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                        |                 |                |

| **Requirement ID** | REQ_UI507                                                      | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Cancel Appointment" button (Input)                            |                 |                |
| **Description**    | Button displayed next to each appointment on the Manage screen |                 |                |
| **Purpose**        | To allow the student to initiate cancellation of a booked slot |                 |                |
| **Format**         | Button (per row)                                               | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Cancel Confirmation dialog                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                       |                 |                |

| **Requirement ID** | REQ_UI508                                                        | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Cancel Confirmation dialog (Output)                              |                 |                |
| **Description**    | Modal asking "Are you sure you want to cancel this appointment?" |                 |                |
| **Purpose**        | To verify the student's intent before removing the booking       |                 |                |
| **Format**         | Modal dialog with "Yes"/"No" buttons                             | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Cancel Appointment" button                               |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                         |                 |                |

| **Requirement ID** | REQ_UI509                                                       | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------------|-----------------|----------------|
| **Item**           | Cancellation Confirmation message (Output)                      |                 |                |
| **Description**    | Inline toast/banner saying "Appointment cancelled successfully" |                 |                |
| **Purpose**        | To inform the student the cancellation was processed            |                 |                |
| **Format**         | Toast/banner notification                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Cancel Confirmation dialog                               |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                        |                 |                |

#### 3.4.2.6 Managing Fitness Class Bookings interface {#managing-fitness-class-bookings-interface .unnumbered}

| **Requirement ID** | REQ_UI601                                                                     | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Fitness Class Bookings" screen (Output)                                      |                 |                |
| **Description**    | Screen showing current class reservations in a table with Book/Cancel actions |                 |                |
| **Purpose**        | To provide a unified view for viewing, booking, and cancelling classes        |                 |                |
| **Format**         | Screen/UI with action buttons                                                 | **Valid Range** | Not applicable |
| **Related I/O**    | Input: 'Fitness Class Bookings' button                                        |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                      |                 |                |

| **Requirement ID** | REQ_UI602                                                                  | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Refresh Bookings action (Input)                                            |                 |                |
| **Description**    | Implicit or visible control to reload the bookings list after an operation |                 |                |
| **Purpose**        | To update the display with the latest reservation state                    |                 |                |
| **Format**         | Automatic Refresh                                                          | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Updated Bookings table                                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                   |                 |                |

| **Requirement ID** | REQ_UI603                                                             | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Error display area (Output)                                           |                 |                |
| **Description**    | Inline message area for showing API errors when loading or refreshing |                 |                |
| **Purpose**        | To inform the student when bookings cannot be retrieved or updated    |                 |                |
| **Format**         | Inline text / Banner                                                  | **Valid Range** | Not applicable |
| **Related I/O**    | Input: system error responses                                         |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                              |                 |                |

| **Requirement ID** | REQ_UI604                                                          | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Book Fitness Class" button (Input)                                |                 |                |
| **Description**    | Button on the wellness portal to initiate booking flow             |                 |                |
| **Purpose**        | To allow the student to view available classes and start a booking |                 |                |
| **Format**         | Button                                                             | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Available Classes table                                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                           |                 |                |

| **Requirement ID** | REQ_UI605                                                                     | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Available Classes table (Output)                                              |                 |                |
| **Description**    | Table listing classes with a "Book" button on each row and a "Go back" button |                 |                |
| **Purpose**        | To display all classes the student can book                                   |                 |                |
| **Format**         | Table with action buttons                                                     | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Book Fitness Class" button                                            |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                      |                 |                |

| **Requirement ID** | REQ_UI606                                                 | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------|-----------------|----------------|
| **Item**           | "Book" button (Input)                                     |                 |                |
| **Description**    | Button on each class row to select that class for booking |                 |                |
| **Purpose**        | To let the student choose which class to reserve          |                 |                |
| **Format**         | Button (per row)                                          | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Booking Confirmation dialog                       |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                  |                 |                |

| **Requirement ID** | REQ_UI607                                                  | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------|-----------------|----------------|
| **Item**           | Booking Confirmation dialog (Output)                       |                 |                |
| **Description**    | Modal asking "Do you want to book this class?"             |                 |                |
| **Purpose**        | To confirm the student's intent before placing the booking |                 |                |
| **Format**         | Modal dialog with "Yes"/"No" buttons                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Book" button                                       |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                   |                 |                |

| **Requirement ID** | REQ_UI608                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | Booking Success message (Output)                         |                 |                |
| **Description**    | Inline toast/banner reading "Booking successful"         |                 |                |
| **Purpose**        | To inform the student that their class has been reserved |                 |                |
| **Format**         | Toast/banner notification                                | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Booking Confirmation dialog                       |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

| **Requirement ID** | REQ_UI609                                             | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------|-----------------|----------------|
| **Item**           | "Cancel" button (Input)                               |                 |                |
| **Description**    | Button next to each booked class on the Manage screen |                 |                |
| **Purpose**        | To allow the student to start a cancellation          |                 |                |
| **Format**         | Button (per row)                                      | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Cancellation Confirmation dialog              |                 |                |
| **Author**         | Nicholas Thong Meng Shui                              |                 |                |

| **Requirement ID** | REQ_UI610                                                      | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------|-----------------|----------------|
| **Item**           | Cancellation Confirmation dialog (Output)                      |                 |                |
| **Description**    | Modal asking "Are you sure you want to cancel this booking?"   |                 |                |
| **Purpose**        | To verify the student's intent before removing the reservation |                 |                |
| **Format**         | Modal dialog with "Yes"/"No" buttons                           | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Cancel" button                                         |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                       |                 |                |

| **Requirement ID** | REQ_UI611                                                    | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------|-----------------|----------------|
| **Item**           | Cancellation Success message (Output)                        |                 |                |
| **Description**    | Inline toast/banner reading "Booking cancelled successfully" |                 |                |
| **Purpose**        | To inform the student that the cancellation was processed    |                 |                |
| **Format**         | Toast/banner notification                                    | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Cancellation Confirmation dialog                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                     |                 |                |

#### 3.4.2.7 System Admin Interface {#system-admin-interface .unnumbered}

| **Requirement ID** | REQ_UI701                                                               | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Manage User Accounts" button (Input)                                   |                 |                |
| **Description**    | Button on the admin console to open the user‐accounts management screen |                 |                |
| **Purpose**        | To allow the admin to view, edit, delete, or create user accounts       |                 |                |
| **Format**         | Button                                                                  | **Valid Range** | Not applicable |
| **Related I/O**    | Output: User Accounts table                                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                |                 |                |

| **Requirement ID** | REQ_UI702                                                                                                               | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | User Accounts table (Output)                                                                                            |                 |                |
| **Description**    | Table listing existing user accounts with "Edit", "Delete" buttons per row, plus "Create Account" and "Go back" buttons |                 |                |
| **Purpose**        | To present all user records and available actions in one view                                                           |                 |                |
| **Format**         | Table with action buttons                                                                                               | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Manage User Accounts" button                                                                                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                                                |                 |                |

| **Requirement ID** | REQ_UI703                                                        | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Edit" button (Input)                                            |                 |                |
| **Description**    | Button on each user‐row to open the edit‐account screen          |                 |                |
| **Purpose**        | To allow the admin to modify a specific user's details and roles |                 |                |
| **Format**         | Button (per row)                                                 | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Edit Account screen                                      |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                         |                 |                |

| **Requirement ID** | REQ_UI704                                                                                   | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Edit Account screen (Output)                                                                |                 |                |
| **Description**    | Form displaying user fields, roles/permissions checkboxes, with "Save" and "Cancel" buttons |                 |                |
| **Purpose**        | To allow the admin to update account details and manage permissions                         |                 |                |
| **Format**         | Screen/Form with buttons                                                                    | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Edit" button                                                                        |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                    |                 |                |

| **Requirement ID** | REQ_UI705                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | "Save" button (Input)                                    |                 |                |
| **Description**    | Button on the Edit Account screen to submit changes      |                 |                |
| **Purpose**        | To finalize and persist modifications to the user record |                 |                |
| **Format**         | Button                                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Save Confirmation dialog                         |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

| **Requirement ID** | REQ_UI706                                                   | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------|-----------------|----------------|
| **Item**           | Save Confirmation dialog (Output)                           |                 |                |
| **Description**    | Modal asking "Do you want to save changes to this account?" |                 |                |
| **Purpose**        | To confirm the admin's intent before updating               |                 |                |
| **Format**         | Modal with "Yes"/"No" buttons                               | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Save" button                                        |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                    |                 |                |

| **Requirement ID** | REQ_UI707                                                  | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Cancel" button (Input)                                    |                 |                |
| **Description**    | Button on the Edit Account screen to abandon edits         |                 |                |
| **Purpose**        | To allow the admin to exit without saving changes          |                 |                |
| **Format**         | Button                                                     | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Cancel‐Without‐Save dialog                         |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                   |                 |                |
| **Requirement ID** | REQ_UI708                                                  | **Version**     | 1.0            |
| **Item**           | Cancel‐Without‐Save dialog (Output)                        |                 |                |
| **Description**    | Modal asking "Discard changes and return to account list?" |                 |                |
| **Purpose**        | To verify the admin's choice before losing edits           |                 |                |
| **Format**         | Modal with "Yes"/"No" buttons                              | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Cancel" button                                     |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                   |                 |                |

| **Requirement ID** | REQ_UI709                                           | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------|-----------------|----------------|
| **Item**           | "Delete" button (Input)                             |                 |                |
| **Description**    | Button on each user‐row to initiate account removal |                 |                |
| **Purpose**        | To allow the admin to remove a user record          |                 |                |
| **Format**         | Button (per row)                                    | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Delete Confirmation dialog                  |                 |                |
| **Author**         | Nicholas Thong Meng Shui                            |                 |                |

| **Requirement ID** | REQ_UI710                                                 | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------|-----------------|----------------|
| **Item**           | Delete Confirmation dialog (Output)                       |                 |                |
| **Description**    | Modal asking "Are you sure you want to delete this user?" |                 |                |
| **Purpose**        | To confirm the admin's intent before deleting             |                 |                |
| **Format**         | Modal with "Yes"/"No" buttons                             | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Delete" button                                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                  |                 |                |

| **Requirement ID** | REQ_UI711                                                       | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------------------|-----------------|----------------|
| **Item**           | Deletion Success message (Output)                               |                 |                |
| **Description**    | Inline toast/banner reading "User account deleted successfully" |                 |                |
| **Purpose**        | To inform the admin that the removal was processed              |                 |                |
| **Format**         | Toast/banner notification                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Delete Confirmation dialog                               |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                        |                 |                |

| **Requirement ID** | REQ_UI712                                                                     | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Create Account" button (Input)                                               |                 |                |
| **Description**    | Button at bottom of the User Accounts table to open the account‐creation form |                 |                |
| **Purpose**        | To allow the admin to add a new user record                                   |                 |                |
| **Format**         | Button                                                                        | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Create Account screen                                                 |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                      |                 |                |

| **Requirement ID** | REQ_UI713                                                                                  | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Create Account screen (Output)                                                             |                 |                |
| **Description**    | Form to enter new user details, roles, and permissions, with "Create" and "Cancel" buttons |                 |                |
| **Purpose**        | To collect and submit new account information                                              |                 |                |
| **Format**         | Screen/Form with buttons                                                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Create Account" button                                                             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                                   |                 |                |

| **Requirement ID** | REQ_UI714                                                   | **Version**     | 1.0            |
|--------------------|-------------------------------------------------------------|-----------------|----------------|
| **Item**           | "Create" button (Input)                                     |                 |                |
| **Description**    | Button on the Create Account screen to finalize new account |                 |                |
| **Purpose**        | To submit and persist the new user record                   |                 |                |
| **Format**         | Button                                                      | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Create Confirmation dialog                          |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                    |                 |                |

| **Requirement ID** | REQ_UI715                                            | **Version**     | 1.0            |
|--------------------|------------------------------------------------------|-----------------|----------------|
| **Item**           | Create Confirmation dialog (Output)                  |                 |                |
| **Description**    | Modal asking "Confirm creation of new user account?" |                 |                |
| **Purpose**        | To verify the admin's intent before adding           |                 |                |
| **Format**         | Modal with "Yes"/"No" buttons                        | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Create" button                               |                 |                |
| **Author**         | Nicholas Thong Meng Shui                             |                 |                |

| **Requirement ID** | REQ_UI716                                | **Version**     | 1.0            |
|--------------------|------------------------------------------|-----------------|----------------|
| **Item**           | "Cancel" button (Input) on Create screen |                 |                |
| **Description**    | Button to abandon new‐account form       |                 |                |
| **Purpose**        | To exit account creation without saving  |                 |                |
| **Format**         | Button                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Cancel‐Create dialog             |                 |                |
| **Author**         | Nicholas Thong Meng Shui                 |                 |                |

| **Requirement ID** | REQ_UI717                                              | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------|-----------------|----------------|
| **Item**           | Cancel‐Create dialog (Output)                          |                 |                |
| **Description**    | Modal asking "Discard new account and return to list?" |                 |                |
| **Purpose**        | To confirm before losing entered data                  |                 |                |
| **Format**         | Modal with "Yes"/"No" buttons                          | **Valid Range** | Not applicable |
| **Related I/O**    | Input: Cancel button on Create screen                  |                 |                |
| **Author**         | Nicholas Thong Meng Shui                               |                 |                |

| **Requirement ID** | REQ_UI718                                               | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------|-----------------|----------------|
| **Item**           | "View System Logs" menu item (Input)                    |                 |                |
| **Description**    | Menu item or button on the admin page to open logs view |                 |                |
| **Purpose**        | To allow the admin to access log‐viewing functionality  |                 |                |
| **Format**         | Menu item / Button                                      | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Filter controls                                 |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                |                 |                |

| **Requirement ID** | REQ_UI719                                                  | **Version**     | 1.0            |
|--------------------|------------------------------------------------------------|-----------------|----------------|
| **Item**           | Filter controls panel (Output)                             |                 |                |
| **Description**    | UI elements for date range, severity, and source filtering |                 |                |
| **Purpose**        | To enable precise log queries by the admin                 |                 |                |
| **Format**         | Panel with date‐pickers, dropdowns, checkboxes             | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "View System Logs" menu item                        |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                   |                 |                |

| **Requirement ID** | REQ_UI720                                    | **Version**     | 1.0            |
|--------------------|----------------------------------------------|-----------------|----------------|
| **Item**           | "Search" button (Input)                      |                 |                |
| **Description**    | Button to submit the filter criteria         |                 |                |
| **Purpose**        | To trigger retrieval of matching log entries |                 |                |
| **Format**         | Button                                       | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Log Entries table                    |                 |                |
| **Author**         | Nicholas Thong Meng Shui                     |                 |                |

| **Requirement ID** | REQ_UI721                                                                       | **Version**     | 1.0            |
|--------------------|---------------------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Log Entries table (Output)                                                      |                 |                |
| **Description**    | Paginated table showing timestamp, actor, action, severity, and message summary |                 |                |
| **Purpose**        | To display the filtered log results to the admin                                |                 |                |
| **Format**         | Table with pagination controls                                                  | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Search" button                                                          |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                                        |                 |                |

| **Requirement ID** | REQ_UI722                                                            | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------------------|-----------------|----------------|
| **Item**           | Log Details panel (Output)                                           |                 |                |
| **Description**    | Panel or modal showing full log entry details, including stack trace |                 |                |
| **Purpose**        | To allow the admin to drill down into a specific log event           |                 |                |
| **Format**         | Panel / Modal dialog                                                 | **Valid Range** | Not applicable |
| **Related I/O**    | Input: row selection in Log Entries table                            |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                             |                 |                |

| **Requirement ID** | REQ_UI723                                                | **Version**     | 1.0            |
|--------------------|----------------------------------------------------------|-----------------|----------------|
| **Item**           | "Export" button (Input)                                  |                 |                |
| **Description**    | Button to export current filtered logs to CSV or JSON    |                 |                |
| **Purpose**        | To allow the admin to download logs for offline analysis |                 |                |
| **Format**         | Button                                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Output: Export file link                                 |                 |                |
| **Author**         | Nicholas Thong Meng Shui                                 |                 |                |

| **Requirement ID** | REQ_UI724                                           | **Version**     | 1.0            |
|--------------------|-----------------------------------------------------|-----------------|----------------|
| **Item**           | Export file link (Output)                           |                 |                |
| **Description**    | Download link to the generated CSV or JSON log file |                 |                |
| **Purpose**        | To provide the admin with the exported data         |                 |                |
| **Format**         | Hyperlink / Button                                  | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Export" button                              |                 |                |
| **Author**         | Nicholas Thong Meng Shui                            |                 |                |

| **Requirement ID** | REQ_UI725                                              | **Version**     | 1.0            |
|--------------------|--------------------------------------------------------|-----------------|----------------|
| **Item**           | "No records found" message (Output)                    |                 |                |
| **Description**    | Inline text shown when no logs match the filter        |                 |                |
| **Purpose**        | To inform the admin that the query returned no results |                 |                |
| **Format**         | Inline text / Banner                                   | **Valid Range** | Not applicable |
| **Related I/O**    | Input: "Search" button                                 |                 |                |
| **Author**         | Nicholas Thong Meng Shui                               |                 |                |

### 3.4.3 Hardware Interfaces {#hardware-interfaces-1 .unnumbered}

The system should support the following hardware-related considerations:

#### 3.4.3.1 Client Devices: {#client-devices .unnumbered}

- Personal computers (PC) both laptops and desktops (Windows, macOS and
  Linux)

- Mobile devices (iOS and Android)

#### 3.4.3.2 Server Infrastructure: {#server-infrastructure .unnumbered}

- Campus Wellness Portal shall be deployed on university hosted servers.

- Supports standard networking, monitoring and backup operations.

## 3.5 Logical Database Requirements {#logical-database-requirements .unnumbered}

Below is the ERD
diagram:![](/media/imageb.png){width="5.9013801399825025in"
height="7.795009842519685in"}

*Figure 15: ERD diagram*

Below is the data dictionary:

| **Entity**                | **Field Name**         | **Data Type**                                                 | **Description**                                      |
|---------------------------|------------------------|---------------------------------------------------------------|------------------------------------------------------|
| **UserAccount**           | UserID                 | INT (PK)                                                      | Unique identifier for the user                       |
|                           | Username               | VARCHAR                                                       | User\'s login name                                   |
|                           | PasswordHash           | VARCHAR                                                       | Hashed password                                      |
|                           | Email                  | VARCHAR                                                       | User\'s email address                                |
|                           | FirstName              | VARCHAR                                                       | User\'s first name                                   |
|                           | LastName               | VARCHAR                                                       | User\'s last name                                    |
|                           | Role                   | ENUM(\'Student\', \'Admin\', \'Practitioner\')                | Role of the user                                     |
|                           | DateRegistered         | TIMESTAMP                                                     | Account creation timestamp                           |
|                           | Permissions            | TEXT/JSON (Optional)                                          | Custom permissions or overrides                      |
| **FitnessClass**          | ClassID                | INT (PK)                                                      | Unique class identifier                              |
|                           | ClassName              | VARCHAR                                                       | Name of the class                                    |
|                           | Description            | TEXT                                                          | Description of the class                             |
|                           | InstructorName         | VARCHAR                                                       | Name of the instructor                               |
|                           | ScheduleDateTime       | TIMESTAMP                                                     | Scheduled date and time                              |
|                           | DurationMinutes        | INT                                                           | Duration in minutes                                  |
|                           | Capacity               | INT                                                           | Maximum number of participants                       |
|                           | Location               | VARCHAR                                                       | Class location                                       |
|                           | DifficultyLevel        | VARCHAR                                                       | Difficulty level (e.g., Beginner, Intermediate)      |
| **FitnessClassBooking**   | BookingID              | INT (PK)                                                      | Unique booking identifier                            |
|                           | UserID                 | INT (FK → UserAccount.UserID)                                 | Student who made the booking                         |
|                           | ClassID                | INT (FK → FitnessClass.ClassID)                               | Booked class                                         |
|                           | BookingTimestamp       | TIMESTAMP                                                     | Booking creation time                                |
|                           | Status                 | ENUM(\'Booked\', \'Cancelled\', \'Attended\')                 | Booking status                                       |
| **HealthAppointment**     | AppointmentID          | INT (PK)                                                      | Unique appointment ID                                |
|                           | StudentID              | INT (FK → UserAccount.UserID)                                 | Student who booked the appointment                   |
|                           | PractitionerID         | INT (FK → UserAccount.UserID, Nullable)                       | Practitioner assigned (nullable)                     |
|                           | PractitionerName       | VARCHAR                                                       | Name of external practitioner (optional)             |
|                           | ServiceType            | VARCHAR                                                       | Type of service (e.g., Consultation, Check-up)       |
|                           | AppointmentDateTime    | TIMESTAMP                                                     | Appointment date and time                            |
|                           | DurationMinutes        | INT                                                           | Appointment duration in minutes                      |
|                           | Location               | VARCHAR                                                       | Appointment location                                 |
|                           | Status                 | ENUM(\'Scheduled\', \'Cancelled\', \'Completed\', \'NoShow\') | Status of the appointment                            |
|                           | Notes                  | TEXT (Nullable)                                               | Additional comments or notes                         |
| **WellnessGoal**          | GoalID                 | INT (PK)                                                      | Unique goal ID                                       |
|                           | UserID                 | INT (FK → UserAccount.UserID)                                 | Owner of the goal                                    |
|                           | GoalType               | VARCHAR                                                       | Type of goal (e.g., Weight, Steps)                   |
|                           | Description            | TEXT (Nullable)                                               | Goal description                                     |
|                           | TargetValue            | DECIMAL or VARCHAR                                            | Target value to achieve                              |
|                           | CurrentValue           | DECIMAL or VARCHAR (Nullable)                                 | Progress made                                        |
|                           | Unit                   | VARCHAR                                                       | Unit of measurement                                  |
|                           | StartDate              | DATE                                                          | When the goal begins                                 |
|                           | TargetDate             | DATE                                                          | Deadline to achieve the goal                         |
|                           | Status                 | ENUM(\'Active\', \'Achieved\', \'Abandoned\')                 | Goal status                                          |
|                           | DateCreated            | TIMESTAMP                                                     | Goal creation date                                   |
|                           | LastUpdated            | TIMESTAMP                                                     | Last modified date                                   |
| **HealthTip**             | TipID                  | INT (PK)                                                      | Unique tip ID                                        |
|                           | Title                  | VARCHAR                                                       | Title of the tip                                     |
|                           | Content                | TEXT                                                          | Description or guidance                              |
|                           | Category               | VARCHAR (Nullable)                                            | Category (e.g., Nutrition, Exercise)                 |
|                           | DatePublished          | TIMESTAMP                                                     | Date the tip was published                           |
|                           | Author                 | VARCHAR (Nullable)                                            | Source or author of the tip                          |
|                           | TargetAudienceCriteria | TEXT/JSON (Nullable)                                          | Optional filters for personalization                 |
| **Notification**          | NotificationID         | INT (PK)                                                      | Unique notification ID                               |
|                           | UserID                 | INT (FK → UserAccount.UserID)                                 | Notification recipient                               |
|                           | Title                  | VARCHAR                                                       | Notification title                                   |
|                           | Message                | TEXT                                                          | Content of the message                               |
|                           | TimestampCreated       | TIMESTAMP                                                     | Time the notification was created                    |
|                           | ReadStatus             | BOOLEAN                                                       | Whether the notification is read                     |
|                           | NotificationType       | VARCHAR (Nullable)                                            | Type of notification                                 |
|                           | RelatedEntityID        | INT (Nullable)                                                | Related entity (e.g., Class ID)                      |
|                           | RelatedEntityType      | VARCHAR (Nullable)                                            | Type of the related entity                           |
| **SystemLog**             | LogID                  | INT (PK)                                                      | Unique log ID                                        |
|                           | Timestamp              | TIMESTAMP                                                     | Log timestamp                                        |
|                           | EventType              | VARCHAR                                                       | Type of event (e.g., Login, Update)                  |
|                           | Description            | TEXT                                                          | Event description                                    |
|                           | UserID                 | INT (FK → UserAccount.UserID, Nullable)                       | User who triggered the event                         |
|                           | IPAddress              | VARCHAR (Nullable)                                            | Source IP address                                    |
| **LogExport**             | ExportID               | INT (PK)                                                      | Unique export identifier                             |
|                           | RequestedByAdminID     | INT (FK → UserAccount.UserID)                                 | Admin who requested the export                       |
|                           | TimestampRequested     | TIMESTAMP                                                     | Export request time                                  |
|                           | ExportCriteria         | TEXT/JSON (Nullable)                                          | Filter criteria used                                 |
|                           | FileLink               | VARCHAR (Nullable)                                            | Path to exported file                                |
|                           | Status                 | ENUM(\'Pending\', \'Processing\', \'Completed\', \'Failed\')  | Status of export                                     |
| **WellnessGoalHealthTip** | GoalID                 | INT (FK → WellnessGoal.GoalID)                                | Related goal                                         |
|                           | TipID                  | INT (FK → HealthTip.TipID)                                    | Related health tip                                   |
|                           | RelevanceScore         | DECIMAL                                                       | How relevant the tip is to the goal                  |
|                           | AssignedDate           | TIMESTAMP                                                     | When the tip was linked to the goal                  |
|                           | IsAutoRecommended      | BOOLEAN                                                       | Whether the tip was auto-assigned or manually chosen |

## Design Constraints

| **Requirement ID** | **Description**                                                    | **Priority** | **Author**          |
|--------------------|--------------------------------------------------------------------|--------------|---------------------|
| REQ_DC001          | System shall be compatible with latest versions of major browsers. | High         | Fikrul Amsyar Azmin |

| **Requirement ID** | **Description**                                                                                                                    | **Priority** | **Author**          |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------|--------------|---------------------|
| REQ_DC002          | The interface design shall comply with university's branding guidelines. (fonts, color palette, logo placement, and illustrations) | High         | Fikrul Amsyar Azmin |

| **Requirement ID** | **Description**                                                                     | **Priority** | **Author**          |
|--------------------|-------------------------------------------------------------------------------------|--------------|---------------------|
| REQ_DC003          | The system shall be responsive and usable on desktops, laptops, and mobile devices. | High         | Fikrul Amsyar Azmin |

## 3.7 Software System Attributes {#software-system-attributes .unnumbered}

This section specifies the attributes that are expected from the
Wellness Portal and its implementations.

### 3.7.1 Security {#security .unnumbered}

The security requirements for the Wellness Portal are as follows:

| **Requirement ID** | **Description**                                                         | **Priority** | **Author**    |
|--------------------|-------------------------------------------------------------------------|--------------|---------------|
| REQ_Q001           | The Wellness Portal may only be accessed by students of the university. | High         | Muhammad Anas |

## Supporting Information

### 3.8.1 Sample Input/Output Formats {#sample-inputoutput-formats .unnumbered}

For exporting system log files, data can be exported in either JSON or
CSV format.

### 3.8.2 Problems to Be Solved by the Software

- Organize the university's many health-related facilities into a
  universal software (Wellness Portal).

### 3.8.3 Validation Session  {#validation-session .unnumbered}

| **Session ID**  | **Date and Time**             | **Technique**  | **Section Reviewed**                   | **Participant**  | **No. of Defect**  |
|-----------------|-------------------------------|----------------|----------------------------------------|------------------|--------------------|
| VS_01           | 18^th^ June 2025; 4pm - 7pm   | Inspection     | 1.3, 3.1, 3.2, 3.3, 3.4, 3.5, 3.8      | Tham Yong Shian  | 5                  |
| VS_02           | 19^th^ June 2025; 5pm-7pm     | Inspection     | 3.1, 3.2, 3.3, 3.4, 4.1, 4.2, 5.1, 5.2 | Tham Yong Shian  | 6                  |
| VS_03           | 20^th^ June 2025; 6pm -- 10pm | Inspection     | 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 3.7, 3.8 | Tham Yong Shian  | 3                  |

### 3.8.4 Defect Summary

A. Content Defect 

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 16%" />
<col style="width: 17%" />
<col style="width: 26%" />
<col style="width: 14%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Req ID</strong> </th>
<th><strong>Validation and Defect Description</strong> </th>
<th><strong>Detected By</strong> </th>
<th><strong>Comment/Suggested Fix</strong> </th>
<th><strong>Session ID</strong> </th>
<th><strong>Severity (1–5)</strong> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CD_01</td>
<td>Missing / insufficient software system attributes </td>
<td>Tham Yong Shian </td>
<td>Define and add software system attributes. </td>
<td><p>VS_01 </p>
<p> </p></td>
<td>5 </td>
</tr>
<tr class="even">
<td>CD_02</td>
<td>Cells not merged although same entity</td>
<td>Tham Yong Shian</td>
<td>Merge cells that have the same entity together to improve
clarity.</td>
<td>VS_02</td>
<td>1</td>
</tr>
<tr class="odd">
<td>CD_03</td>
<td>Inconsistent plural / singular form terms</td>
<td>Tham Yong Shian</td>
<td>Ensure every word used follows the correct noun form. (e.g. removes
or remove)</td>
<td>VS_02</td>
<td>1</td>
</tr>
<tr class="even">
<td>CD_04</td>
<td>Missing document</td>
<td>Tham Yong Shian</td>
<td>Task 4/Kano Model.docx is mentioned but isn’t shown in the SRS
document itself.</td>
<td>VS_02</td>
<td>4</td>
</tr>
<tr class="odd">
<td>CD_05</td>
<td>Incorrect Use Case Actor (UC_009)</td>
<td>Tham Yong Shian</td>
<td>UC_009 is done by the system and not the students.</td>
<td>VS_03</td>
<td>5</td>
</tr>
<tr class="even">
<td>CD_06</td>
<td>Incorrect Use Case Actor (UC_010)</td>
<td>Tham Yong Shian</td>
<td>UC_010 is done by the system and not the students.</td>
<td>VS_03</td>
<td>5</td>
</tr>
</tbody>
</table>

B. Documentation Defect

| **Req ID**  | **Validation and Defect Description**      | **Detected By**  | **Comment/Suggested Fix**                                          | **Session ID**  | **Severity (1--5)**  |
|-------------|--------------------------------------------|------------------|--------------------------------------------------------------------|-----------------|----------------------|
| DD_01       | Inconsistent font choice                   | Tham Yong Shian  | Fix all font to be Aptos.                                          | VS_01           | 1                    |
| DD_02       | Blank page                                 | Tham Yong Shian  | Remove blank page. (page 17)                                       | VS_01           | 1                    |
| DD_03       | Author section not in tables               | Tham Yong Shian  | Either add/remove respective authors from table.                   | VS_01           | 2                    |
| DD_04       | Inconsistent terminology used for students | Tham Yong Shian  | Students, end-users, and users are used to refer to student actor. | VS_02           | 3                    |
| DD_05       | Duplicate acronym                          | Tham Yong Shian  | JWT is mentioned twice.                                            | VS_02           | 1                    |

C. Agreement Defect

| **Req ID**  | **Validation and Defect Description**                         | **Detected By**  | **Comment/Suggested Fix**                                                                                             | **Session ID**  | **Severity (1--5)**  |
|-------------|---------------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|-----------------|----------------------|
| AD_01       | Password hashing algorithm unexplained                        | Tham Yong Shian  | Explain what algorithm is used to hash passwords.                                                                     |  VS_01          |  4                   |
| AD_02       | Data recovery and/or backup is mentioned but not implemented. | Tham Yong Shian  | Incorporate Recovery Point Objective RPO or Recovery Time Objective RTO principle in case of data breach and/or leak. | VS_02           | 5                    |
| AD_03       | HIPAA compliance is mentioned but not implemented.            | Tham Yong Shian  | Explain how the student's health privacy is protected.                                                                | VS_03           | 5                    |


### 3.8.5 Conflict Analysis

<table>
<colgroup>
<col style="width: 14%" />
<col style="width: 21%" />
<col style="width: 27%" />
<col style="width: 19%" />
<col style="width: 15%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Conflict ID</strong></th>
<th><strong>Conflict Description</strong></th>
<th><strong>Conflict Analysis</strong></th>
<th><strong>Stakeholders Involved</strong></th>
<th><strong>Session ID</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CF_01</td>
<td>Dispute in actors (UC_009)</td>
<td>Data conflict – UC_009 states that the student is the actor,
however, the description is the responsibility of the University Health
Portal. This misrepresents the party who initiates the action which may
lead to mismatched interface designs.</td>
<td>Developer, student</td>
<td>VS_03</td>
</tr>
<tr class="even">
<td>CF_02</td>
<td>Dispute in actors (UC_010)</td>
<td>Data conflict – UC_010 states that the student is the actor,
however, the description is the responsibility of the University
Recreation Portal. This misrepresents the party who initiates the action
which may lead to mismatched interface designs.</td>
<td>Developer, student</td>
<td>VS_03</td>
</tr>
<tr class="odd">
<td>CF_03</td>
<td>Admin vs Security concerns</td>
<td><p>Interest conflict – Admin can create, modify, and delete user accounts and assign or revoke role, without
any justification, as well as access logs without conforming to the
HIPAA.</p></td>
<td>System Admin, Security Team</td>
<td>VS_03</td>
</tr>
</tbody>
</table>

### 3.8.6 Conflict Analysis and Resolution

<table>
<colgroup>
<col style="width: 13%" />
<col style="width: 29%" />
<col style="width: 13%" />
<col style="width: 22%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Conflict ID</strong></th>
<th><strong>Conflict Resolution Strategy</strong></th>
<th><strong>Resolved (y/n)</strong></th>
<th><strong>Outcome (if resolved)</strong></th>
<th><strong>Justification</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CF_01</td>
<td>Identify and communicate with the developers and system admins on a
collective consensus on the actor role of student and University Health
Portal.</td>
<td>y</td>
<td><p>Identification reached on the action to be initiated by the
student. The University Health Portal then receives and updates student health appointment, bookings and cancellations only after the initiation<</td>
<td>Ensures correct system design and avoids misassigned
responsibilities.</td>
</tr>
<tr class="even">
<td>CF_02</td>
<td>Identify and communicate with the developers and system admins on a
collective consensus on the actor role of student and University
Recreation Portal.</td>
<td>y</td>
<td><p>Identification reached on the action to be initiated by the
student. The University Recreation Portal then updates the fitness
class schedule and availability based on bookings or cancellations only after the initiation</p></td>
<td>Ensures correct system design and avoids misassigned
responsibilities.</td>
</tr>
<tr class="odd">
<td>CF_03</td>
<td>Hold a meeting and discussion with system admin as well as
University IT team with an additional scrum master to understand the
functions and limitations of a system admin, adhering to the HIPAA.</td>
<td>y</td>
<td>More secure role control and accountability added if any privacy
issues are detected.</td>
<td>Conformity with security laws and data privacy laws, while also
preventing insider threats and breaches.</td>
</tr>
</tbody>
</table>

### 3.8.7 Change Log

### 3.8.8 Requirements Traceability Matrix

### 3.8.9 Role in Requirements Validation, Negotiation and Management

### 3.8.10 Version Control and Configuration Summary

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Repository Branch</th>
<th>project-part-2</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Key Files</td>
<td><p>SRS.md</p>
<p>TT6L_G1_SRS.docx</p>
<p>Changelog.md</p></td>
</tr>
<tr class="even">
<td>Commits</td>
<td>Tham Yong Shian</td>
</tr>
<tr class="odd">
<td>Pull</td>
<td>Tham Yong Shian</td>
</tr>
<tr class="even">
<td>Changelog</td>
<td>Tham Yong Shian</td>
</tr>
</tbody>
</table>

###


# 4.0 Verification

This section describes the approach and criteria that will be used to
verify that the Campus Wellness Portal system meets its functional and
non-functional requirements. This is done to ensure that the
stakeholder's expectations are met, and that the system performs in
accordance to the specification.

## 4.1 Verification Approach

Verification of the Campus Wellness Portal will be conducted using
various software testing techniques throughout the development cycle.
The table below lists out the verification method, responsible parties,
timeline and location for the techniques.

| **Verification Technique**        | **Description**                                                           | **Responsible Party(s)**    | **Timeline** | **Location**                      |
|-----------------------------------|---------------------------------------------------------------------------|-----------------------------|--------------|-----------------------------------|
| **Unit Testing**                  | Tests that individual modules function as intended.                       | Developer                   | Week 3-6     | Developer environment             |
| **Integration Testing**           | Tests that integration/interaction between modules functions as intended. | Developer, QA Tester        | Week 7-9     | Staging/test environment          |
| **Functional Testing**            | Tests that the functions (F001-F011) meet requirements.                   | QA Team, Project Supervisor | Week 9-10    | University Test Lab               |
| **System Testing**                | Assess the entire system behaviour alongside performance and security.    | QA Team                     | Week 10-11   | Controlled Lab/Test Server        |
| **User Acceptance Testing (UAT)** | Tests with real users to confirm that it meets real-world needs.          | End-user, QA Team           | Week 11-12   | Campus Lab or Virtual Environment |

## 4.2 Verification Criteria {#verification-criteria .unnumbered}

### 4.2.1 Unit testing verification criteria

| **Module**                         | **Test Case**                                                                    | **Expected Output**                                                                        |
|------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Login                              | Users login to their own accounts.                                               | Returns the campus wellness dashboard upon successful login.                               |
| Book Fitness Class                 | Book fitness classes.                                                            | Return successful booking message to the user.                                             |
| Cancel Fitness Class               | Cancel previously booked fitness classes.                                        | Return successful booking cancellation to the user.                                        |
| Schedule Health Centre Appointment | Schedule new health centre appointment.                                          | Updates user appointments database and returns successful appointment booking to the user. |
| Cancel Health Centre Appointment   | Cancel previously scheduled health centre appointments.                          | Removes selected appointment from user's scheduled appointments table in database.         |
| Track Wellness Goals               | Track user wellness goals.                                                       | Return updated wellness goals in student dashboard to the user.                            |
| View System Notifications          | View pending notifications.                                                      | Returns notifications regarding health centre/fitness class bookings to the user.          |
| View Personalized Health           | View personalized health tips.                                                   | Returns personalized health tips to the user.                                              |
| Manage Health Centre Appointments  | View user's health centre appointments.                                          | Returns the health centre appointment dashboard to the user.                               |
| Manage Fitness Class Booking       | View booked fitness class booking.                                               | Returns the fitness class dashboard to the user.                                           |
| Manage User Access Control         | Create, modify, and delete user accounts and assign or revoke roles/permissions. | Return the users access dashboard to the user.                                             |
| View System Logs                   | View system logs                                                                 | Return the system logs.                                                                    |

### 4.2.2 Integration testing verification criteria

| **Integrated Modules**                                                                                   | **Test Case**                                                                                                               | **Expected Outcome**                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Book Fitness Class + Cancel Fitness Class + Manage Fitness Class Bookings                                | Users view the fitness class bookings and can book new fitness class sessions and cancel previously booked classes.         | Fitness class dashboard displays correctly and success message pops up for successful booking and cancellation of fitness class.                         |
| Schedule Health Centre Appointment + Cancel Health Centre Appointment + Manage Health Centre Appointment | User views their scheduled health centre appointments and can schedule a new appointment or cancel a scheduled appointment. | Health centre appointment dashboard displays correctly and success message pops up for successful booking and cancellation of health centre appointment. |

### 4.2.3 Functional testing verification criteria

| **Function Code** | **Feature**                        | **Test Case**                                                            | **Expected Outcome**                              |
|-------------------|------------------------------------|--------------------------------------------------------------------------|---------------------------------------------------|
| F001              | Login                              | Login with valid credentials.                                            | Redirected to campus wellness portal dashboard    |
| F002              | Book Fitness Class                 | Book a fitness class.                                                    | Fitness class successfully booked                 |
| F003              | Cancel Fitness Class               | Cancel a booked fitness class.                                           | Fitness class successfully cancelled              |
| F004              | Schedule Health Centre Appointment | Schedule a new health centre appointment.                                | Health centre appointment successfully scheduled. |
| F005              | Cancel Health Centre Appointment   | Cancel a scheduled health centre appointment.                            | Health centre appointment successfully cancelled  |
| F006              | Track Personal Wellness Goals      | View personal wellness goals.                                            | Redirect to personal wellness goals dashboard     |
| F007              | View System Notifications          | View system notifications (fitness class and health centre appointments) | Redirect to notifications dashboard.              |
| F008              | View Personalized Health Tips      | View personalized health tips                                            | Redirect to personalized health tips dashboard.   |
| F009              | Manage Health Centre Appointments  | View scheduled health centre appointments.                               | Redirect to health centre appointments dashboard. |
| F010              | Manage Fitness Class Bookings      | View fitness class bookings.                                             | Redirect to fitness class bookings dashboard.     |
| F011              | Manage User Access Control         | Manage users access to the system.                                       | Redirect to user access dashboard.                |
| F012              | View System Logs                   | View past system logs.                                                   | Shows the past system logs.                       |

### 4.2.4 User acceptance testing (UAT) verification criteria

| User Role | UAT Scenario                                                                                                                                                                                              | Acceptance Criteria                                           |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Student   | Login, book fitness class, cancel fitness class, manage fitness class bookings, manage health centre appointments, schedule health centre appointment, cancel health centre appointment, view health tips | All actions complete without errors and are easy to navigate. |
| Admin     | Manage user access control, view system logs                                                                                                                                                              | User access can be changed and system logs can be viewed.     |

### 4.2.5 Performance Verification Criteria

| Requirement ID | Description                                                                          | Verification Criteria                                                  | Priority |
|----------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------|
| REQ_P001       | The average response time of Wellness Portal functions shall be less than 2 seconds. | Wellness Portal functions must load and complete within \<= 2 seconds. | High     |

### 4.2.6 Usability Verification Criteria

| Requirement ID | Description                                                                                              | Verification Criteria                                                                                                                        | Priority |
|----------------|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------|
| REQ_UR001      | System shall be intuitive enough for first-time users to perform basic tasks without extensive training. | Users are able to navigate the system and interact with it and use its functions without much instructions                                   | High     |
| REQ_UR002      | Consistent design patterns and navigation shall be used across pages.                                    | Design language of the system UI must be uniform and consistent across the whole system.                                                     | Medium   |
| REQ_UR003      | System shall prevent user errors through input validation, tooltips, and disabling invalid options.      | Tooltips show up on buttons where applicable, input validation is done for input boxes and invalid options are disabled for selection boxes. | High     |

[]{#_Toc1816687531 .anchor}

# 5.0 Appendices

## 5.1 Assumptions and Dependencies

### 5.1.1 University Authentication System

Type: OAuth 2.0 Single Sign-on (SSO)

Role: Secure login and access control

Dependency: The Wellness Portal depends on this framework to validate
user login and assign permissions. Any downtime in the SSO will affect
all user access.

Type: JSON Web Token Standard (JWT)

Role: Verify user identities

Dependency: The Wellness Portal depends on this system to differentiate
between normal users and system administrators. It works in conjunction
with OAuth 2.0 for handling user authentication.

### 5.1.2 Fitness Class Booking

Type: REST API integration

Role: Book fitness classes and cancel booked fitness classes.

Dependency: The Wellness Portal depends on this system to handle fitness
class availability.

### 5.1.3 Health Centre Appointment Booking

Type: REST API integration

Role: Schedule health centre appointments and cancel health centre
appointments.

Dependency: The Wellness Portal depends on this system to handle health
centre appointment availability.

### 5.1.4 Browser Standards

Type: Client-side software

Role: Interface in which users will access the Wellness Portal

Dependency: The Wellness Portal will assume compliance with ECMAScript
and HTML5 standards. Use of unsupported browsers may cause UI/UX issues.

### 5.1.5 Stakeholder Availability

Type: Organizational

Role: Provide input, feedback and UAT participation

Dependency: Lack of participation from students and staff may put
requirements validation and UAT at risk.

## 5.2 Acronyms and Abbreviations

| **Acronym/Abbreviation** | **Meaning**                                         |
|--------------------------|-----------------------------------------------------|
| **JWT**                  | JSON Web Token                                      |
| **RGB**                  | Red, Green, Blue (values for colour)                |
| **JSON**                 | JavaScript Object Notation                          |
| **HTTP**                 | Hyper Text Transfer Protocol                        |
| **UAT**                  | User Acceptance Testing                             |
| **HIPAA**                | Health Insurance Portability and Accountability Act |
| **SaaS**                 | Software as a Service                               |
| **JWT**                  | JSON Web Token                                      |
| **CSV**                  | Comma Separated Value (A file type)                 |
| **UI**                   | User Interface                                      |
