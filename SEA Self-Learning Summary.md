**Self-Learning Summary**

**Software Engineering and Architecture**

---

**1\. Introduction**

Software Engineering involves the systematic application of engineering principles to the development, testing, deployment, and maintenance of software systems. Modern software development requires effective management of requirements, collaboration between teams, continuous feedback, and reliable software delivery.

As part of this self-learning activity, I studied the concepts of **Agile, DevOps, project management tools such as Jira and Asana, user stories and acceptance criteria, advanced requirement elicitation techniques, Requirement Traceability Matrix (RTM), and IBM DOORS**.

These topics are closely connected with the Software Development Life Cycle (SDLC). Requirements are first identified and analyzed, converted into manageable user stories, developed and tested using suitable methodologies, and finally delivered and maintained using modern development and operational practices.

---

**2\. Agile vs DevOps**

**2.1 Agile**

Agile is an iterative and incremental approach to software development that focuses on flexibility, collaboration, continuous customer feedback, and frequent delivery of working software.

In traditional development, requirements are often defined at the beginning and the complete product is developed through a sequence of phases. Agile, on the other hand, divides development into smaller iterations. Each iteration produces a working part of the system.

**Key Principles of Agile**

* Customer collaboration  
* Continuous feedback  
* Iterative development  
* Frequent delivery of working software  
* Adaptability to changing requirements  
* Team collaboration  
* Continuous improvement

One of the most commonly used Agile frameworks is **Scrum**, where work is organized into short development cycles called **Sprints**.

**Example**

Consider the development of an online shopping application. Instead of developing the entire application at once, the team can develop it incrementally:

1. User registration and login  
2. Product search  
3. Shopping cart  
4. Online payment  
5. Order tracking

After each iteration, the team can obtain feedback and make improvements in subsequent iterations.

---

**2.2 DevOps**

DevOps is an approach that combines **software development and IT operations** to improve collaboration, automation, reliability, and speed of software delivery.

DevOps aims to reduce the gap between development and operations teams. Instead of treating development, testing, deployment, and operations as completely separate activities, DevOps promotes continuous collaboration throughout the software lifecycle.

A typical DevOps lifecycle can be represented as:

**Plan → Code → Build → Test → Release → Deploy → Operate → Monitor**

**Important DevOps Practices**

* Continuous Integration (CI)  
* Continuous Delivery/Deployment (CD)  
* Automated testing  
* Infrastructure automation  
* Continuous monitoring  
* Collaboration between development and operations  
* Continuous feedback

Automation is an important part of DevOps because it allows repetitive activities such as building, testing, and deployment to be performed quickly and consistently.

---

**2.3 Agile and DevOps Comparison**

| Aspect | Agile | DevOps |
| :---: | :---: | :---: |
| Primary Focus | Software development | Software delivery and operations |
| Main Goal | Deliver customer value incrementally | Deliver software quickly and reliably |
| Teams | Developers, testers, product owners | Development, Operations, QA and other teams |
| Development | Iterative | Continuous |
| Testing | Frequent | Continuous and highly automated |
| Deployment | Usually after development iterations | Frequent or continuous |
| Automation | Helpful | Very important |
| Feedback | Mainly customer feedback | Customer and operational feedback |
| Common Practices | Sprints, backlog, user stories | CI/CD, automation, monitoring |

**Relationship Between Agile and DevOps**

Agile and DevOps are not competing approaches. They complement each other.

**Agile focuses mainly on how software is planned and developed, while DevOps extends the process toward continuous integration, deployment, operation, and monitoring.**

Therefore:

**Agile helps teams build software iteratively, while DevOps helps teams deliver and operate that software continuously.**

---

**3\. Case Study: Jira and Asana in Real Projects**

**3.1 Jira**

**Jira** is a project and work-management tool developed by Atlassian. It is widely used by software-development teams to plan, track, and manage work.

Jira is particularly useful for Agile and Scrum-based software projects. Teams can create and manage:

* Epics  
* User stories  
* Tasks  
* Sub-tasks  
* Bugs  
* Sprints

A typical software development workflow in Jira can be:

**Backlog → To Do → In Progress → Testing → Done**

**Example**

Suppose a team is developing a **Food Delivery Application**.

An Epic may be:

**Food Ordering System**

This Epic can contain user stories such as:

* As a customer, I want to search for restaurants.  
* As a customer, I want to add food items to my cart.  
* As a customer, I want to place an order.  
* As a customer, I want to make an online payment.

Each user story can then be divided into development and testing tasks.

Jira therefore provides a structured way of connecting requirements with actual development work.

---

**3.2 Asana**

**Asana** is a project and work-management platform used to organize tasks, projects, deadlines, responsibilities, and collaboration among team members.

Asana provides different ways of viewing project information, such as:

* List view  
* Board view  
* Calendar  
* Timeline  
* Dashboard

**Example**

For the development of a mobile application, an Asana project could contain:

| Task | Responsible Team | Status |
| :---: | :---: | :---: |
| Design Login Screen | UI Team | Completed |
| Develop Login API | Backend Team | In Progress |
| Set up Database | Database Team | Completed |
| Perform Testing | QA Team | Pending |
| Prepare Documentation | Documentation Team | Pending |

Asana is useful for both technical and non-technical teams and can be used for projects involving multiple departments.

---

**3.3 Jira vs Asana**

| Feature | Jira | Asana |
| :---: | :---: | :---: |
| Primary Use | Software development and work tracking | General project and work management |
| Agile Support | Strong | Available |
| Issue Tracking | Excellent | Available but less developer-focused |
| Sprint Management | Strong | Less specialized |
| User Stories | Strong | Supported |
| Task Management | Strong | Strong |
| Team Collaboration | Strong | Strong |
| Interface | More technical | More general and visual |
| Suitable For | Software-development teams | Cross-functional teams |

**Case Study Conclusion**

Jira and Asana both help teams organize and monitor project work, but they have different strengths. **Jira is particularly suitable for software-development projects involving Agile workflows, user stories, issues, and sprints. Asana is more general-purpose and is useful for managing projects and collaboration across technical and non-technical teams.**

---

**4\. Writing Effective User Stories and Acceptance Criteria**

**4.1 User Stories**

A **User Story** is a short description of a requirement written from the perspective of the person who will use the system.

A commonly used format is:

**As a \[type of user\], I want \[function\], so that \[benefit\].**

**Example**

**As a customer, I want to reset my password so that I can regain access to my account if I forget it.**  
A good user story should be:

* Clear  
* Concise  
* Valuable to the user  
* Testable  
* Small enough to implement  
* Understandable by the development team

The **INVEST** principles are commonly used to evaluate user stories:

| Letter | Meaning |
| ----- | ----- |
| I | Independent |
| N | Negotiable |
| V | Valuable |
| E | Estimable |
| S | Small |
| T | Testable |

---

**4.2 Acceptance Criteria**

Acceptance criteria define the conditions that must be satisfied for a user story to be considered complete.

For the password-reset user story, suitable acceptance criteria could be:

1. The user can select **Forgot Password**.  
2. The user can enter a registered email address.  
3. The system sends a password-reset link.  
4. The reset link is valid only for a specified period.  
5. The user can create a new password according to the password rules.  
6. The user can log in using the new password.

Acceptance criteria help developers understand exactly what needs to be implemented and help testers determine whether the requirement has been successfully fulfilled.

---

**4.3 Given–When–Then Format**

Acceptance criteria can also be expressed using the **Given–When–Then** format.

**Given:** The user has a registered account.

**When:** The user selects "Forgot Password" and enters the registered email address.

**Then:** The system should send a password-reset link to the user's email.

This format makes requirements easier to understand and convert into test cases.

---

**5\. Advanced Requirement Elicitation Techniques**

Requirement elicitation is the process of identifying, understanding, and documenting the requirements of stakeholders.

Requirements cannot always be obtained simply by asking users what they want. Users may forget important details or may not be aware of all the requirements of a system. Therefore, advanced elicitation techniques are useful for discovering both explicit and hidden requirements.

---

**5.1 Interviews**

Interviews involve directly communicating with stakeholders to understand their needs, problems, expectations, and existing processes.

They can be:

* Structured  
* Semi-structured  
* Unstructured

**Advantages**

* Provides detailed information.  
* Allows follow-up questions.  
* Helps understand stakeholder expectations.

**Limitation**

Interviews can be time-consuming and the information may be influenced by personal opinions.

---

**5.2 Ethnography**

**Ethnography** involves studying users in their actual working environment.

Instead of only asking users how they perform a task, the analyst observes them while they perform their normal activities.

**Example**

For a hospital management system, an analyst could observe:

**Receptionist → Doctor → Nurse → Laboratory → Pharmacy**

This may reveal actual workflows, shortcuts, or problems that users may not mention during interviews.

**Advantage**

It helps discover hidden and undocumented requirements.

---

**5.3 Observation**

Observation involves watching users perform their regular tasks.

It can help identify:

* Repetitive activities  
* Unnecessary steps  
* Workarounds  
* Errors  
* Actual user behavior

Observation is useful when users find it difficult to explain their complete workflow.

---

**5.4 Workshops**

Requirement workshops bring multiple stakeholders together to discuss and define requirements.

Participants may include:

**Customer \+ Business Analyst \+ Developer \+ Tester \+ Project Manager**

Workshops allow different perspectives to be considered at the same time and can help resolve disagreements early.

---

**5.5 Prototyping**

Prototyping involves creating an early representation of the proposed system.

Examples include:

* Wireframes  
* Mock-ups  
* Interactive prototypes

Stakeholders can examine the prototype and provide feedback before the actual system is developed.

This can help identify misunderstandings at an early stage.

---

**5.6 Focus Groups**

A focus group involves a selected group of users discussing their experiences, expectations, and requirements.

It is particularly useful when a system has a large and diverse group of users.

**Comparison of Elicitation Techniques**

| Technique | Main Purpose | Key Benefit |
| :---: | :---: | :---: |
| Interviews | Obtain detailed stakeholder information | Direct communication |
| Observation | Understand actual behavior | Identifies real workflows |
| Ethnography | Understand users in their environment | Reveals hidden requirements |
| Workshops | Gather multiple stakeholders | Different viewpoints |
| Prototyping | Validate proposed solution | Early feedback |
| Focus Groups | Understand user opinions | Multiple users at once |

Using a combination of techniques generally provides a more complete understanding of system requirements.

---

**6\. Requirement Traceability Matrix (RTM)**

**6.1 Definition**

A **Requirement Traceability Matrix (RTM)** is a document used to establish relationships between requirements and related project artifacts such as design elements, development tasks, and test cases.

The basic relationship can be represented as:

**Requirement → Design → Development → Testing → Verification**

The main purpose of RTM is to ensure that every requirement is properly implemented and tested.

---

**6.2 Example of RTM**

Consider an online shopping application:

| Requirement ID | Requirement | Development Task | Test Case | Status |
| ----- | ----- | ----- | ----- | ----- |
| REQ-01 | User registration | DEV-01 | TC-01 | Complete |
| REQ-02 | User login | DEV-02 | TC-02 | Complete |
| REQ-03 | Product search | DEV-03 | TC-03 | Complete |
| REQ-04 | Add product to cart | DEV-04 | TC-04 | In Progress |
| REQ-05 | Online payment | DEV-05 | TC-05 | Pending |

The table allows the team to determine whether a particular requirement has corresponding development work and testing activities.

---

**6.3 Types of Traceability**

**Forward Traceability**

Forward traceability follows a requirement through the development process:

**Requirement → Design → Code → Test**

It ensures that all requirements are implemented.

**Backward Traceability**

Backward traceability follows development or testing artifacts back to their original requirements:

**Test → Implementation → Requirement**

It helps ensure that development work can be justified by an approved requirement.

**Bidirectional Traceability**

Bidirectional traceability combines both directions:

**Requirement ↔ Design ↔ Development ↔ Testing**

It provides better visibility across the software development lifecycle.

---

**6.4 Benefits of RTM**

* Ensures complete requirement coverage.  
* Helps identify missing requirements.  
* Helps testers create relevant test cases.  
* Supports impact analysis when requirements change.  
* Improves project documentation.  
* Provides evidence that requirements have been implemented and tested.

---

**7\. Requirement Management Tool – IBM DOORS**

**7.1 Introduction**

**IBM Engineering Requirements Management DOORS**, including **DOORS Next**, is a requirements-management solution used to capture, organize, analyze, trace, and manage requirements throughout the development lifecycle.

It is especially useful for large and complex projects where requirements must be formally documented and traced across different stages of development.

---

**7.2 Major Features**

**Requirement Creation and Organization**

Requirements can be created and organized using structures such as folders, modules, attributes, and views.

**Requirement Traceability**

Requirements can be linked to related requirements, design elements, development work, and testing artifacts.

**Change Management**

When a requirement changes, its connected elements can be examined to understand the potential impact of the change.

**Collaboration and Review**

Stakeholders can review requirements, provide feedback, and participate in approval processes.

**Version and Baseline Management**

Different versions of requirements can be maintained, allowing teams to track changes over time and preserve approved versions.

---

**7.3 Example**

Consider an automotive software project with the following requirement:

**REQ-101: The braking system shall respond to a detected obstacle within the specified response time.**  
This requirement can be linked to:

**Requirement → System Design → Software Implementation → Test Case → Test Result**

If the requirement changes, the traceability links can help engineers identify which design elements, implementation tasks, and test cases may also require modification.

This demonstrates why formal requirement management becomes important in complex and safety-critical projects.

---

**8\. Integration of the Concepts**

The topics studied in this activity are not isolated. They form a connected process within modern software development.

A simplified process can be represented as:

**Stakeholder Needs**  
 ↓  
 **Requirement Elicitation**  
 ↓  
 **Requirement Analysis**  
 ↓  
 **User Stories**  
 ↓  
 **Acceptance Criteria**  
 ↓  
 **Requirement Management / RTM**  
 ↓  
 **Agile Development**  
 ↓  
 **Testing**  
 ↓  
 **DevOps Practices**  
 ↓  
 **Deployment**  
 ↓  
 **Monitoring**  
 ↓  
 **Customer Feedback**  
 ↓  
 **Next Iteration**

For example, a customer's requirement can first be discovered through interviews or observation. The requirement can then be written as a user story with acceptance criteria. It can be tracked using a requirement-management approach or RTM and converted into development tasks in Jira.

The development team can implement the feature using an Agile process. After testing, DevOps practices such as automated testing and continuous deployment can help deliver the software. Monitoring and customer feedback can then provide information for future improvements.

Thus, these concepts collectively support a structured and continuous software development process.

**9\. References**

1. Amazon Web Services (AWS) – *What is DevOps?*  
2. Atlassian – *Jira and Agile Project Management Resources*  
3. Asana – *Project and Work Management Resources*  
4. IBM – *Engineering Requirements Management / DOORS Next*  
5. Software Engineering and Architecture classroom learning materials.

 

