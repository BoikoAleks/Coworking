

## **TEST STRATEGY**
---

# **1\. Introduction**

## **1.1 Purpose**

This document outlines the high-level test strategy for the Coworking management system project, defining the preliminary test scope, high-level test activities, organization, and test management. This test strategy is a tool that will provide the starting point for detailed test planning.

## **1.2 Revision History**

| Version | Date | Changed by | Summary |
| ----- | ----- | ----- | ----- |
|   |   |   | \<xxx section removed/ added/ updated according to yyy reason\> |
|   |   |   |   |
|   |   |   |   |

 

## **1.3 Reviews/Approvals/Commitment**

## **1.4 Definitions**

| Abbreviation / term | Definition |
| ----- | ----- |
|   |   |
|   |   |
|   |   |

 

## **1.5 Referenced documents**

| Document name | File location |
| ----- | ----- |
|   |   |
|   |   |
|   |   |

# 

# **2\. Scope and Limitations**

## **2.1 Scope**

Testing activities for the Coworking Management System will focus on validating both functional and non-functional requirements as described in the SRS. The following areas are within scope:

### **Business Processes**

- User registration and authentication (admin, client).  
- Workspace and meeting room booking process (including real-time availability).  
- Service/resource management (Wi-Fi, printers, coffee machines).  
- User management (role-based access, account creation/edit/deletion).  
- Report generation and export (PDF/Excel).

### **Technology Components**

The testing will also cover the technological backbone of the platform to ensure stability, security, and seamless integration:

*Frontend Components*

- Web interface usability and navigation.  
- Interactive map for workspace occupancy.  
- Compatibility across supported browsers (Chrome, Firefox, Safari, Opera).  
- Responsive design for mobile devices.

*Technology Components:*

- *Integration with third-party calendars (Google Calendar, Outlook).*  
- *Real-time data synchronization.*  
- *Security mechanisms (encryption, authentication, OAuth).*  
- *Performance and load handling (response time ≤ 2 seconds, scalability).*

### **In Scope:**

The following types of testing will be conducted:

*Functional Testing:*

- User registration and authentication (admin, client).  
- Workspace and meeting room booking flow (availability, scheduling, email confirmations).  
- Viewing occupancy and services (real-time interactive map).  
- User management (roles, permissions, CRUD operations).  
- Report generation and export (PDF, Excel).

*Usability Testing:*

- UI/UX validation for intuitive navigation.  
- User workflows for booking and resource management.  
- Responsiveness for mobile and tablet devices.  
- Compatibility Testing  
- Cross-browser support: Chrome, Firefox, Safari, Opera.  
- Cross-device checks (desktop, mobile, tablet).

*Security Testing:*

- Authentication & authorization (role-based access control).  
- Data encryption and secure storage validation.  
- OAuth login flows.  
- Basic vulnerability scanning (SQL injection, XSS, CSRF).  
- Performance & Load Testing  
- Response time ≤ 2 seconds under expected load.  
- Scalability validation (adding new workspaces, handling multiple concurrent users).

*Integration Testing:*

- Synchronization with Google Calendar and Outlook.  
- Correct handling of booking conflicts.  
- Availability & Reliability Testing  
- Service uptime validation (≥ 99%).  
- Failover/recovery scenarios within system boundaries.

## **2.2 Limitations and exclusions**

Testing will not cover the following areas:

- Third-party services: Google Calendar/Outlook reliability (only integration correctness will be verified, but not external service stability).  
- Infrastructure setup: Cloud hosting, network performance outside the application’s scope.  
- Non-project devices/browsers: Only Chrome, Firefox, Safari, Opera will be tested. Edge, IE, and other browsers are excluded.  
- Localization/Internationalization: Only primary project language(s) will be tested; multi-language support is out of scope unless explicitly added.  
- Hardware testing: Physical printers, Wi-Fi routers, and coffee machines will not be tested (only system-side integration/management).  
- Load extremes beyond expected capacity: Stress testing up to contractual user limits will be performed, but catastrophic load testing (e.g., millions of concurrent users) is excluded.

# **3\. Testing Approach**

The tests will follow a structured approach to ensure the thorough evaluation of the website’s functionality, usability, and security. The general sequence of testing will include:

*Functional Testing:*

Focused on ensuring that the core features, such as user authentication, order processing, and payment methods, work as expected. Automated tests will be created for these scenarios using Selenium/Selenide and RestAssured.

*Usability Testing:*

Ensuring ease of use for customers interacting with the website. This will be done manually to ensure user flows are intuitive, supported by automated UI testing for critical interactions.

*Compatibility Testing:*

Automated tests will be run across different browsers and devices using Selenium to ensure the UI behaves correctly on major browsers (Chrome, Firefox, Safari, Edge).

*Security Testing:*

Testing for vulnerabilities such as SQL injection, XSS, and session management, using security tools in conjunction with the test automation framework to identify and address weaknesses.

*API Testing:*

Using RestAssured, the backend APIs will be tested for their functionality, ensuring that product browsing, wishlist management, and order processing work as expected.

*Regression Testing:*

Every time new features or updates are added, regression tests will be executed to ensure that existing functionality remains unaffected.

*Reporting:*

All test results will be captured using Allure Reports to provide insights into the testing process and ensure transparency. The test results will be shared with stakeholders for review.

# **4 Testing Organization**

This section outlines the structure and governance of the testing process to ensure that testing is efficient, organized, and meets the project’s quality goals. The testing process will be governed by a dedicated team of testers and stakeholders, ensuring collaboration and transparency at all stages of the development lifecycle.

## **4.1 Entry Criteria**

The following conditions are preferred before any testing can begin:

§  Business owner signs off business requirement documentation

§  Test artifacts are up to date and prioritized according to a risk-based analysis

§  Test environment must be ready and accessible

§  Technical resources have been allocated and are available for support

§  Development is complete, and no new major features or changes are planned during the testing phase.

§  Test data (e.g., user accounts, product listings) is prepared and available for testing.

§  The project stakeholders have approved the testing phase to begin.

## **4.2 Exit Criteria**

These are the minimum acceptable conditions before promoting the SBR solution to a live production environment:

§  There are no outstanding high-priority issues

§  All Test Cases with a high and medium priority have been successfully executed

§  Test coverage of 80% has been completed

§  The business owners and product managers have reviewed the test results and approved the product for release.

§  All necessary test documentation, including test logs, reports, and defect reports, are completed and shared with stakeholders.

## **4.3 Test Case Management**

Effective test case management is crucial to ensure that all testing efforts are structured, traceable, and aligned with project requirements. This section outlines the process for creating, managing, and executing test cases throughout the testing lifecycle.

*Test Case Design*

Test cases will be designed based on the following criteria:

 

§  Test Coverage: Ensure all functional, non-functional, and business requirements are covered, including user authentication, product browsing, order processing, payment methods, and security.

§  Clear and Concise: Each test case will have clear steps, expected results, and detailed preconditions to ensure reproducibility.

§  Reusability: Common test scenarios will be written in a reusable manner to support automated testing where applicable (using Selenium/Selenide for UI automation and RestAssured for API testing).

*Test Case Repository*

All test cases will be stored in a centralized repository within Jira for easy access, collaboration, and traceability. The repository will include the following:

§  Test Case Documentation: Test cases will be documented using a standard format within Jira, including test case ID, description, prerequisites, test steps, expected results, and test data.

§  Automation Scripts: Automated test scripts for core functionality will be stored in Git and linked to the corresponding test cases in Jira for traceability and version control.

## **4.4 Defect Management**

Defect management is a critical part of the testing process, ensuring that any issues identified during testing are properly tracked, reported, and addressed. This section outlines the process for managing defects throughout the testing lifecycle.

### **Defect Reporting**

Defect Logging: Defects will be logged in Jira by the testing team as soon as they are identified. Each defect will include detailed information, such as:

1\.    Defect ID: A unique identifier for the defect.

2\.    Description: A clear description of the defect, including steps to reproduce.

3\.    Severity: The impact level of the defect (Critical, Major, Minor).

4\.    Priority: The urgency for fixing the defect (Immediate, High, Medium, Low).

5\.    Environment: Information about the environment where the defect was found (e.g., browser, OS, device).

6\.    Attachments: Screenshots, logs, or any other supporting documentation to aid in the investigation of the defect.

7\.    Test Case Link: The specific test case(s) or scenario(s) under which the defect was found.

## **4.5 Severity Definitions**

**Severity:** The degree of impact that a defect has on the development or operation of a component or system.

| Severity | Definition |
| ----- | ----- |
| Critical | The defect that results in the termination of the complete system or one or more components of the system and causes extensive data corruption. The failed function is unusable, and there is no acceptable alternative method to achieve the required results. |
| Major | The defect that results in the termination of the complete system or one or more components of the system and causes extensive data corruption. The failed function is unusable, but an acceptable alternative method exists to achieve the required results. |
| Minor | The defect that does not result in the termination and does not damage the usability of the system, and the desired results can be easily obtained by working around. |

 

## **4.6 Priority Definitions**

**Priority:** The level of (business) importance assigned to an item, e.g., defect.

At a high level, priority is determined by considering the following:

§  Businesses need for fixing the defect

§  Severity/Impact

§  Probability/Visibility

§  Available Resources (Developers to fix and Testers to verify the fixes)

§  Available Time (Time for fixing, verifying the fixes, and performing regression tests after the verification of the fixes)

| Priority | Definition |
| ----- | ----- |
| Immediate | Must be fixed immediately (work started in 1 hour) because of:  \- Data Loss or Corruption \- Numerous customer complaints about the issue \- Blocks further development or\\and testing, no workaround |
| High | Must be fixed within the current iteration because of: \- a critical area of the system affected \- major feature (High priority Test Cases) broken or unavailable \- Numerous or\\and major UI issues \- interrupts business workflow with workarounds (for all end users) |
| Medium | Must be fixed within the current iteration because of: \- not a critical area of the system \- minor feature (Medium priority Test Cases) broken or unavailable \- Numerous or\\and minor UI issues \- interrupts business workflow with workarounds for some end users (not for all) |
| Low | Must be fixed within the next iteration because of: \- trivial, cosmetic \- may affect business workflow |

 **4.7 Tools**

This section outlines the tools that will be used during the testing process to support various stages of testing, from automation to reporting and continuous integration.

*Selenium/Selenide:*

Purpose: Used for automating web browsers, enabling UI testing and interaction with the application.

Usage: Selenium will be employed for functional and regression testing of the website, including verifying elements, workflows, and user interactions. Selenide, built on top of Selenium, will be used for its enhanced API, making browser interaction simpler and more effective.

*TestNG:*

Purpose: A testing framework for Java that provides support for test configuration, parallel execution, and generating reports.

Usage: TestNG will be used to organize and execute test cases for both UI (via Selenium/Selenide) and API testing (via RestAssured), along with managing test dependencies and grouping tests effectively.

*Gradle:*

Purpose: A build automation tool that will be used to compile, run, and manage testing scripts.

Usage: Gradle will be configured to automate the execution of test cases, manage dependencies (e.g., Selenium, RestAssured), and facilitate continuous integration within the testing pipeline.

*RestAssured:*

Purpose: A Java-based library for testing RESTful APIs, providing a domain-specific language (DSL) for writing API tests.

Usage: RestAssured will be used for API testing to verify interactions between the website and its backend services, ensuring that endpoints for order processing, user registration, and product listings work as expected.

*GitLab CI:*

Purpose: A continuous integration (CI) tool used to automate the testing pipeline.

Usage: GitLab CI will be used for continuous integration, automating the running of tests after each code commit or merge. It will ensure that test cases are executed consistently and that any regressions are caught early in the development cycle.

*Podman:*

Purpose: A container management tool used to create and manage containers.

Usage: Podman will be used to create isolated testing environments, ensuring consistency in the testing setup across different environments (e.g., development, staging, and production).

*Allure Reports*

Purpose: A flexible, lightweight test reporting tool that integrates with various testing frameworks.

Usage: Allure reports will be used to generate detailed, user-friendly test reports, providing insights into test execution, pass/fail statuses, and overall test coverage. It will be integrated with TestNG for reporting after test execution.

*Lombok:*

Purpose: A Java library that reduces boilerplate code by automatically generating common methods such as getters, setters, and constructors.

Usage: Lombok will be used to simplify the test code, making it more concise and easier to maintain by eliminating repetitive code for models and test helpers.

# **5 Roles and Responsibilities**

| Role | Responsibility / Accountability |
| ----- | ----- |
| QA Test Automation Engineer |   |

 

# **6\. Schedule**

| Test Activity / Milestone | Start Date | End Date |
| ----- | ----- | ----- |
| Review UML diagrams (UML diagrams) | \<mm/dd/yyyy\> | \<mm/dd/yyyy\> |
| Review SRS (Documentation) |   |   |
| Create Test Strategy (Test Documentation) |  |  |
| Create Test Plan (Test Documentation) |  |  |
| Create Test Scenarios / Checklists (Test Documentation) |  |  |

