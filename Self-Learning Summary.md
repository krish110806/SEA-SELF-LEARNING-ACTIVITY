# Self-Learning Summary — Software Engineering and DevOps Practices

## 1. What is DevOps

According to AWS, DevOps is the combination of cultural philosophies, practices, and tools that increases an organization's ability to deliver applications and services quickly, allowing teams to evolve and improve products faster than through traditional siloed development and infrastructure processes. Development and operations teams stop working as separate units — in many organizations they merge into a single team whose engineers work across the entire application lifecycle instead of owning just one function. When security is folded into that same team, the practice is usually called **DevSecOps**.

AWS identifies the core benefits of DevOps as:

- **Speed** — innovate and respond to market changes faster
- **Rapid Delivery** — ship features and fixes more frequently
- **Reliability** — every update is tested and delivered consistently
- **Scale** — manage infrastructure and processes efficiently as the system grows
- **Improved Collaboration** — shared ownership instead of finger-pointing between teams
- **Security** — compliance and safety checks are automated, not added at the end

These benefits are made possible through practices such as continuous integration, continuous delivery, microservices architecture, infrastructure as code, and continuous monitoring/logging.

## 2. Agile vs DevOps

| Dimension | Agile | DevOps |
|---|---|---|
| **Primary focus** | Iterative software development (sprints, backlog, user stories) | End-to-end delivery pipeline — CI/CD, automation, operations |
| **Goal** | Deliver working software quickly and adapt to changing requirements | Ship frequent, reliable deployments without sacrificing stability |
| **Team** | Developers, Product Owner, Scrum Master | Dev + Ops + QA + Security, working as one shared-ownership unit |
| **Feedback loop** | End of sprint (days to weeks) | Near real-time, via automated tests and monitoring (minutes to hours) |
| **Cadence** | Sprint-based (typically 1–4 weeks) | Continuous — multiple releases per day are possible |
| **Key practices** | Sprint planning, daily stand-ups, retrospectives | CI/CD pipelines, Infrastructure as Code, automated testing, monitoring |
| **Typical tools** | Jira, Trello, Asana, Confluence | Jenkins, GitHub Actions, Docker, Kubernetes, Ansible, Prometheus |

**Relationship:** DevOps does not replace Agile — it operationalizes it. Agile answers *"how do we build the software iteratively?"*, while DevOps answers *"how do we deliver and run it reliably at scale?"* Mature teams typically use Agile ceremonies to manage the backlog and sprints, then layer DevOps practices such as CI/CD and monitoring on top to achieve continuous delivery.

## 3. Case Study: Jira vs Asana in Real Projects

### Jira — a distributed software product team

A mid-size software company with product teams spread across three time zones adopted Jira alongside Confluence to bring transparency to a backlog that had become hard to prioritize. Jira was used to plan the product roadmap and triage incoming requests from the sales and customer-success teams, while Confluence held the requirement documents and onboarding material for new engineers. Once the pilot team saw fewer missed handoffs and clearer sprint reporting, the same setup was rolled out to the rest of the engineering organization — a good illustration of Jira anchoring large-scale, developer-centric coordination.

### Asana — a marketing and operations team

A fast-growing consumer app company standardized on Asana to replace a mix of spreadsheets, email threads, and chat messages that made it nearly impossible to know the real status of any campaign or launch. By introducing reusable project templates and a standard intake process, the team consolidated all planning into Asana, cutting the time spent chasing status updates and freeing up meaningful hours every month for actual work instead of coordination.

### Takeaway

Jira is the stronger fit for software and Agile teams that need sprint boards, burndown charts, and integrations with developer tools such as GitHub and Jenkins. Asana is the stronger fit for cross-functional teams — marketing, design, operations — that value Gantt-style timeline views and a gentler learning curve. Many organizations end up running both and syncing them through connectors such as Zapier or Unito.

## 4. DevOps Lifecycle & Jira Workflow

### DevOps Lifecycle

The DevOps lifecycle is a continuous loop rather than a one-time sequence, letting teams repeatedly develop, deliver, monitor, and improve their software:

**Plan → Code → Build → Test → Release → Deploy → Operate → Monitor**, with feedback constantly flowing back into Plan.

- **Plan** — gather requirements, prioritize the backlog, and organize the upcoming work.
- **Code** — write and version-control the source code.
- **Build** — compile and package the application for testing and deployment.
- **Test** — run automated and manual tests to catch defects early.
- **Release** — approve a tested build for deployment to production.
- **Deploy** — push the approved build into the target environment.
- **Operate** — keep the application running smoothly in production.
- **Monitor** — track performance, logs, and errors, and feed those insights back into the next planning cycle.

### Jira Workflow

A Jira workflow defines the sequence of statuses an issue passes through from creation to closure. A typical workflow for a software team looks like:

**Backlog → To Do → In Progress → In Review → Testing → Done**

- **Backlog** — identified, but not yet picked up for work.
- **To Do** — planned and ready to start.
- **In Progress** — actively being worked on.
- **In Review** — completed work awaiting peer review.
- **Testing** — verified against its acceptance criteria.
- **Done** — completed and accepted by the team.

Workflows can be customized per project, but this basic structure gives everyone visibility into where work stands and helps surface bottlenecks early.

## 5. Writing Effective User Stories & Acceptance Criteria

**Template:** As a [user], I want [goal], so that [benefit].

**Example:** As a returning customer, I want to save items to a wishlist so that I can buy them later without searching again.

### INVEST Principles

Good user stories should be:

- **I**ndependent
- **N**egotiable
- **V**aluable
- **E**stimable
- **S**mall
- **T**estable

### Acceptance Criteria (AC)

Acceptance criteria should be testable, unambiguous, and each should cover exactly one condition.

**Checklist style:**

- AC1: A logged-in customer can add a product to their wishlist.
- AC2: A wishlisted product displays a filled heart icon.
- AC3: The customer can remove a product from the wishlist.
- AC4: A wishlisted product that goes out of stock is flagged automatically.

**Given/When/Then (BDD) style — better for conditional logic:**

```
Given a product is already in my wishlist
When I try to add the same product again
Then the system shows a message instead of creating a duplicate entry
```

## 6. Advanced Requirement Elicitation: Interviews & Ethnography

### Interviews

Structured, semi-structured, or unstructured conversations with stakeholders.

- **Strength:** direct access to stated needs, with room for immediate clarifying questions.
- **Weakness:** relies on what people *say* they do, which can be incomplete, outdated, or biased.

### Ethnography

Observing users inside their actual working environment (shadowing, contextual interviews, field notes).

- **Strength:** surfaces implicit requirements users can't easily put into words — informal workarounds, real step-by-step workflows, or a hidden spreadsheet formula that quietly encodes an important business rule.
- **Weakness:** time-intensive, the observer's presence can change how people behave, and interpreting what was observed is still somewhat subjective.

### Best Practice

Combine both techniques — interview stakeholders first to capture what they believe the process is, then observe them at work to check that belief against what actually happens.

## 7. Requirement Traceability Matrix (RTM)

An RTM links every requirement to its source, its design, its implementation, and its test case, so that nothing is quietly dropped along the way.

### Sample RTM

| Req ID | Requirement | Source | Design Ref | Test Case | Status |
|---|---|---|---|---|---|
| REQ-01 | User can create an account | Customer | User Mgmt Module | TC-01 | Tested |
| REQ-02 | User can log in securely | Customer | Auth Module | TC-02 | Tested |
| REQ-03 | User can browse the product catalog | Customer | Catalog Module | TC-03 | Tested |
| REQ-04 | User can add products to a wishlist | Customer | Wishlist Module | TC-04 | Implemented |
| REQ-05 | User can check out and pay | Business | Checkout Module | TC-05 | Implemented |
| REQ-06 | System emails an order receipt | Business | Notification Module | TC-06 | Planned |

### Steps to Build an RTM

1. Gather requirements from the backlog or SRS document.
2. Assign each requirement a unique ID.
3. Link each requirement to its design specification.
4. Map each requirement to one or more test cases.
5. Track test results after every sprint.
6. Validate that no requirement is left orphaned, without a design or test link.

### Why It Matters

An RTM enables impact analysis (understanding what else breaks if a requirement changes), supports compliance in regulated industries, and catches gaps in test coverage before they reach production.

## 8. Requirement Management Tools (IBM DOORS & Alternatives)

### IBM DOORS

An enterprise-grade tool for capturing and tracing requirements across large projects.

- **Strengths:** hierarchical module structure, bidirectional traceability, built-in coverage reports, formal change and version management, integration with Office tools and PLM systems.
- **Weaknesses:** steep learning curve, dated interface, expensive licensing, and generally overkill for fast-moving Agile teams — it earns its complexity mainly in regulated domains such as aerospace, defense, and medical devices, where standards like ISO 26262 or DO-178C require formal, auditable traceability.

### Alternatives

| Tool | Best For | Trade-off |
|---|---|---|
| Jama Connect | Cloud-based traceability and compliance | Can take effort to configure well |
| Helix ALM | Aerospace and defense projects | Needs deep, careful configuration |
| Siemens Polarion | Organizations already using Siemens/PLM tools | Oriented heavily around PLM workflows |
| Strictdoc | Lightweight, open-source traceability | Limited enterprise-level features |
| Jira + Confluence | Agile software teams | Traceability needs add-on plugins |

For most software teams, a combination like Jira + Confluence (or GitHub Projects + a wiki) provides enough traceability without the overhead of DOORS — DOORS is worth its complexity only when strict regulatory requirements demand it.

## References

- Amazon Web Services (AWS), "What is DevOps?" — https://aws.amazon.com/devops/what-is-devops/
- Atlassian, "Introduction to Jira." — https://www.atlassian.com/software/jira/guides
- Atlassian, "Jira Software Documentation." — https://confluence.atlassian.com/jirasoftware
- Asana, "Get Started with Asana." — https://asana.com/resources/collections/getting-started-with-asana
- Asana, "Quick-start Guide to Asana." — https://help.asana.com/s/article/quick-start-guide-to-asana
- IBM, "Engineering Requirements Management DOORS Next Documentation." — https://www.ibm.com/docs/en/engineering-lifecycle-management-suite/doors-next
