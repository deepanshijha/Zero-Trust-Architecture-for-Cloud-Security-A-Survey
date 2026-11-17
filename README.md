# Zero-Trust-Architecture-for-Cloud-Security-A-Survey
 
IILM UNIVERSITY, GURUGRAM
School of Computer Science and Engineering

SURVEY PAPER
A review of published work, prepared and submitted in research paper format

Zero Trust Architecture for Cloud Security: A Survey
An Overview of Security Principles, Implementation Approaches, Challenges, and the Future of Zero Trust in Cloud Environments.
COURSE DETAILS
Field	Detail
Course Title	Foundation of Cybersecurity 
Course Code	CSE25303 
Programme and Semester	B. Tech (CSE), Semester 3RD 
Batch and Session	Batch 2025-29, Session 2026-27
Works reviewed	[ 25 ] papers, tools or systems, published between [ 2020] and [ 2026]
Sources searched	IEEE Xplore, ACM Digital Library, SpringerLink, Google Scholar, arXiv 

SUBMITTED BY
S. No.	Full Name	Enrolment No.	Institute E-mail
1	Deepanshi Jha 	2581309	Deepanshi.jha.ug25@iilm.edu

SUPERVISED BY
Field	Detail
Name	Dr. Abhishek Pandey
Designation and Department	Assistant Professor, School of Computer Science and Engineering
Course Coordinator	Dr. Preetishree Patnaik 

EVIDENCE REPOSITORY (REFERENCE LIBRARY AND LITERATURE MATRIX)
https://github.com/deepanshijha/Zero-Trust-Architecture-for-Cloud-Security-A-Survey















ACKNOWLEDGEMENT

I would like to express my heartfelt gratitude to Dr. Abhishek Pandey, my faculty guide, for his valuable guidance, patience, and encouragement during the preparation of this survey paper. His feedback helped me improve my understanding of Zero Trust Architecture and its relevance to cloud security. I am grateful for the time he devoted to reviewing my work and helping me shape its scope and structure.
I also extend my thanks to the faculty members of the School of Computer Science and Engineering, IILM University, for the knowledge and academic support they have provided. The concepts studied in my coursework helped me approach this topic and develop my understanding of cybersecurity.
I acknowledge the researchers whose papers informed this survey, as well as the standards bodies and organizations that publish guidance on Zero Trust and cloud security. Their work provided the material for my review and helped me identify key concepts, implementation challenges, and areas for further study.
I am thankful to my classmates and friends for their discussions and encouragement. I also deeply appreciate my family’s continued support and motivation throughout my studies and while completing this paper.
Preparing this survey has been a valuable learning experience. I have made every effort to represent the sources accurately, and I accept responsibility for checking the final document, citations, and references before submission.


















Zero Trust Architecture for Cloud Security: A Survey
Deepanshi Jha, B. Tech CSE, Third Semester
School of Computer Science and Engineering, IILM University, Gurugram.


ABSTRACT

Cloud computing provides flexible access to applications and data, but its distributed nature creates security challenges involving identity, access control, and changing network boundaries. Zero Trust Architecture (ZTA) addresses these challenges through the principle of “never trust, always verify,” requiring access decisions to consider users, devices, context, and resource sensitivity. This survey reviews how ZTA is applied to cloud security, focusing on its core components, deployment approaches, benefits, and implementation challenges. It organizes the topic into identity and policy management, device and workload security, network segmentation, continuous monitoring, and automation. The review also compares architectural guidance and research directions, including the use of artificial intelligence to support threat detection and adaptive access decisions. Key challenges include integration with legacy systems, policy complexity, monitoring overhead, privacy concerns, and the difficulty of evaluating security outcomes consistently. The survey identifies research needs in measurable evaluation methods, explainable automation, and practical guidance for hybrid and multi-cloud environments. It concludes that ZTA can strengthen cloud security when implemented as a coordinated, risk-based approach supported by reliable identity, monitoring, and governance practices.

I. INTRODUCTION
A. Background
Cloud computing has changed how organizations store data and deliver digital services. Instead of managing every server and application on their own premises, organizations can use resources hosted by cloud providers. This can make services easier to scale and access, but it also means that users, devices, applications, and data may be spread across different networks and locations. As a result, protecting cloud resources requires more than securing a traditional network perimeter.
Traditional security models often treat activity inside an organization’s network as more trustworthy than activity outside it. This assumption is less reliable in cloud environments, where employees may connect remotely, applications may communicate across cloud services, and resources can change frequently. A compromised account or device can therefore create risks even when a connection appears to come from an approved location.
Zero Trust Architecture (ZTA) is a security approach that responds to this problem by requiring access to be verified for each request. A user or device is not automatically trusted simply because it is inside a network. Access decisions can consider identity, device condition, resource sensitivity, and another available context. Permissions are limited to what is needed, and activity can be monitored so that access may be reviewed when circumstances change.
For cloud security, ZTA brings together several practices: strong identity and access management, multi-factor authentication, policy-based decisions, least-privilege access, segmentation, and ongoing monitoring. These practices can help organizations control access to cloud applications and data. However, implementing them can be challenging. Organizations may need to connect existing systems, manage complex policies, protect user privacy, and avoid creating unnecessary delays or operational overhead.
This survey reviews the foundations and use of ZTA in cloud environments. It organizes the topic around identity and policy management, devices and workloads, network controls, monitoring, and automation. It also compares research and official guidance, summarizes implementation challenges, and identifies areas for further study. The aim is to provide a clear overview of how ZTA can support cloud security and what questions remain for researchers and practitioners.
B. Motivation and review questions
Cloud environments make it harder to rely on a fixed network boundary. Users connect from different locations and devices, while applications and data may be distributed across cloud services. A stolen account, misconfigured permission, or compromised workload can expose resources even when traditional perimeter controls are in place. Zero Trust Architecture (ZTA) offers a way to address these risks by evaluating access requests based on identity, context, and policy, and by limiting permissions to what is necessary.
However, ZTA is a broad set of principles and practices rather than a single product or configuration. Organizations may implement its components differently, and cloud deployments introduce practical concerns such as integration with existing systems, policy complexity, monitoring demands, and privacy. Reviewing the literature can help clarify the main components of cloud-focused ZTA, compare reported approaches, and identify areas where further research is needed.
C. Review Questions
This survey is guided by the following review questions:
•	RQ1: What core components and principles of ZTA are used to protect cloud environments?
•	RQ2: How are identity, access policies, devices, workloads, network segmentation, and monitoring combined in cloud ZTA implementations?
•	RQ3: What benefits and implementation challenges are reported for applying ZTA to cloud security?
•	RQ4: How are automation and artificial intelligence being explored to support ZTA, and what limitations are identified?
•	RQ5: What research gaps and future directions emerge from the reviewed literature?

II. REVIEW METHODOLOGY
A. Sources and search strings
This survey uses academic databases and official sources to identify research and guidance on Zero Trust Architecture (ZTA) in cloud security. Search the following sources and record which ones you actually used:
•	IEEE Xplore
•	ACM Digital Library
•	Scopus or Web of Science, if available
•	Google Scholar
•	Official standards and guidance from NIST and CISA
B. Criteria and selection process
The working inclusion criteria were English-language material from 2020–2026 (with older foundational work for context), direct relevance ZTA or cloud controls, an identifiable standard, paper, or clearly marked preprint, and accessible information on scope or approach. Exclude duplicates, abstracts without adequate method information, unrelated security work, and numerical claims without a traceable test basis. The nine supplied PDFs form a seed corpus, not a completed PRISMA database sample. Search hits, duplicates, screening totals, and exclusions must be filled from the student’s own exported records.



TABLE I. INCLUSION AND EXCLUSION CRITERIA
Include	Exclude from evidence synthesis
Directly addresses ZTA, cloud access, identity, segmentation, or cloud-native enforcement	Uses zero trust only as a label without a relevant mechanism
Identifiable standard, peer-reviewed paper, or clearly labeled preprint/review	Duplicate, promotional summary, or unusable record
Approach or scope can be described from accessible text	Reports numerical improvement without method or test basis
Evidence level and limitation are recorded separately	Outside scope or publication record cannot be verified


III. TAXONOMY OF THE REVIEWED WORK
The reviewed work on Zero Trust Architecture (ZTA) for cloud security can be grouped by the main security function it addresses. These categories may overlap: a single architecture or study can cover several functions.
Category	Focus	Common approaches
Identity and access management	Verifying users and controlling their permissions	Strong authentication, multi-factor authentication, least privilege, role- or attribute-based access
Device and workload security	Assessing the security of endpoints, virtual machines, containers, and services	Device posture checks, workload identity, configuration monitoring, endpoint protection
Policy decision and enforcement	Deciding whether a specific request should be allowed	Context-aware policy evaluation, policy decision points, policy enforcement points
Network segmentation	Limiting communication between users, applications, and resources	Micro-segmentation, software-defined perimeters, service-level access controls
Continuous monitoring and response	Observing activity and adjusting access as conditions change	Logging, security analytics, anomaly detection, session review, incident response
Automation and AI support	Helping analyse signals and manage security decisions	Automated policy actions, machine-learning-based detection, risk scoring

Across these categories, the literature can also be compared by deployment setting (single cloud, hybrid cloud, or multi-cloud), type of contribution (architecture, implementation, evaluation, or guidance), and evaluation method (conceptual analysis, case study, experiment, or performance measurement).

IV. REVIEW OF THE LITERATURE
A. Architecture and governance
A cloud Zero Trust Architecture (ZTA) combines technical controls with rules for deciding who can access which resources, under what conditions, and how those decisions are reviewed. The architecture applies the principle of least privilege and verifies each access request using available information about the user, device, application, and resource. Trust is not assumed solely from a user’s network location.
A useful way to describe the architecture is through three functions:
•	Policy decision: evaluates the request and determines whether access should be allowed.
•	Policy enforcement: applies that decision, such as granting, limiting, or denying a connection.
•	Information sources: provide signals for the decision, such as identity, device status, resource sensitivity, and security alerts.
In cloud deployments, these functions may be implemented across identity services, cloud-native controls, endpoint tools, application gateways, and monitoring systems. The exact arrangement varies by provider and organization. A ZTA should therefore be described as a coordinated architecture, rather than as one product or a single network device.
Governance defines how that architecture is managed. It includes assigning responsibility for access policies, classifying data and resources, setting approval and review processes, retaining audit records, and establishing how exceptions are handled. Organizations also need to consider privacy, regulatory obligations, and the division of security responsibilities between themselves and their cloud providers.
Effective governance keeps technical controls aligned with organizational risk. Policies should be reviewed when users’ roles, device conditions, applications, or resource sensitivity change. Monitoring and audit results can help identify overly broad permissions or policy gaps. At the same time, organizations should assess whether the controls create operational delays or collect more user information than necessary.
In this survey, architecture and governance can be compared by examining each paper’s described components, access-decision process, deployment setting, policy ownership, monitoring approach, and evaluation method. Only report a feature as present when the source explicitly describes it.
B. Identity and adaptive access
Identity is central to Zero Trust Architecture (ZTA) because access decisions begin by establishing which user, device, application, or service is making a request. In cloud environments, identity systems can connect authentication and authorization across cloud platforms and organizational services. Common controls include multi-factor authentication, single sign-on, and least-privilege permissions. These controls help reduce reliance on network location as a sign of trust.
Adaptive access extends this approach by using context when deciding whether to allow a request. Depending on the system and policy, context may include the user’s role, device security status, requested resource, location, time, or relevant security alerts. A policy can allow access, require additional verification, limit the session, or deny the request. The decision should follow documented rules and be reviewed when organizational needs or risks change.
Identity and adaptive access also create implementation challenges. Inconsistent identity records, legacy applications, overly broad permissions, and poor integration between cloud services can weaken policy enforcement. Collecting contextual signals can raise privacy concerns, while frequent challenges or denials can disrupt legitimate work. Organizations therefore need to balance risk reduction with usability and data minimization.
When reviewing a source, record which identities it covers, what context it uses, what actions its policies can take, and how the approach is evaluated. Avoid describing an access model as adaptive if the paper only discusses static authentication or permissions.
C. Cloud-native enforcement and evaluation
Cloud-native enforcement is the part of a Zero Trust Architecture (ZTA) that applies access decisions to cloud resources. A policy may allow, restrict, or deny a request, but it only protects the resource when an enforcement mechanism carries out that decision. Depending on the cloud environment, enforcement can occur at an identity service, application gateway, workload, network layer, or another point close to the protected resource.
Cloud platforms provide controls that organizations can use to enforce access policies. Examples include identity and access management rules, workload permissions, network security policies, application proxies, and service-to-service controls. These mechanisms can help limit access to specific users, applications, or workloads. Their configuration and capabilities vary between providers, however, so a policy created for one platform may not transfer directly to another.
A typical access request passes through several steps. A user or workload requests a resource; the system checks the identity and other available context; a policy decision is made; and an enforcement point applies the result. Context might include the user’s role, device condition, requested resource, or security alerts. Depending on the policy, the system may grant access, require additional verification, provide limited access, or deny the request. If conditions change during a session, the organization may review or revoke access, provided its systems support that process.
Enforcement can be more difficult in hybrid and multi-cloud environments. Organizations may rely on different identity providers, policy languages, monitoring tools, and network controls. This can lead to inconsistent permissions or gaps between the policy decision and the enforcement point. Legacy applications may not support modern authentication or fine-grained access controls, while complex policies can be difficult to maintain. Integrating controls also requires clear responsibility for configuration, updates, and incident response.
Evaluation helps determine what a proposed architecture or implementation demonstrates. The reviewed studies may use conceptual analysis, prototypes, simulations, experiments, or case studies. Each method provides different kinds of evidence. A conceptual paper can explain how components fit together, while a prototype or experiment may test particular functions under specified conditions. A case study may describe deployment experience in an organization, but its results may not apply to every cloud environment.
Studies may report measures such as access-decision time, policy consistency, resource consumption, usability, detection performance, or the rate of false alerts. These measures should be interpreted in context. For example, lower response time may show faster policy processing, but it does not alone prove that unauthorized access is prevented. Similarly, a detection model’s reported accuracy may depend on its dataset and test setup. Comparisons are meaningful only when the environment, assumptions, and measurement methods are clear.
For each reviewed source, record the cloud setting, protected resources, enforcement location, policy process, evaluation method, measures reported, and limitations stated by the authors. Note whether the work covers a single cloud, hybrid cloud, or multiple providers, and whether it addresses users, applications, and workloads. If a paper proposes an architecture but does not test it, describe it as a conceptual or architectural contribution. This keeps the survey’s conclusions aligned with the evidence each source actually provides.
V. COMPARATIVE ANALYSIS AND DISCUSSION
A. Cross-category comparison
The categories in this survey describe related parts of cloud Zero Trust Architecture (ZTA), and many reviewed works may address more than one. Identity and adaptive access establish who or what is requesting access and under which conditions. Architecture and governance define how decisions are organized, who manages policies, and how access is reviewed. Cloud-native enforcement applies those decisions to specific resources, while evaluation examines the evidence for how well the approach works.

Dimension	Architecture and governance	Identity and adaptive access	Cloud-native enforcement and evaluation
Main concern	How ZTA components and responsibilities are organized	How users, devices, and workloads are identified and assessed	How access policies are applied and how their effects are assessed
Typical mechanisms	Policy decision and enforcement functions, security governance, audit and review processes	Authentication, authorization, least privilege, contextual signals, adaptive policies	Cloud IAM, gateways, workload and network controls, prototypes, experiments, case studies
Key question	Are policies and responsibilities clearly defined and coordinated?	Does the access decision reflect identity and relevant context?	Is the decision enforced consistently, and what evidence supports its effectiveness?
Common challenge	Coordinating policies across teams and services	Integrating identity sources while balancing security, usability, and privacy	Maintaining consistent controls across cloud platforms and demonstrating measurable outcomes
Evidence to record	Architecture diagrams, governance processes, policy ownership, audit approach	Identity types, context signals, possible policy actions, access review	Cloud setting, enforcement point, evaluation method, metrics, limitations

How the Categories Work Together
In a cloud ZTA, an access request typically connects all three areas. First, identity and access mechanisms establish the requester and provide available context. This may include a user or workload identity, permissions, and information about the device or resource. Next, the architecture’s policy process evaluates the request according to organizational rules. Governance determines who sets and maintains those rules, how exceptions are approved, and how decisions are audited. Finally, cloud-native enforcement controls apply the outcome to the requested service or resource.
This relationship means that a weakness in one category can reduce the value of the others. Strong authentication alone does not ensure that permissions are appropriately limited. A well-defined policy may not provide protection if it is not consistently enforced across cloud services. Likewise, technically effective enforcement can become difficult to maintain if policy ownership, review responsibilities, and exception handling are unclear.
Differences in Research Emphasis
The reviewed works may emphasize different parts of this overall process. Architecture-focused papers often describe components and their relationships, but may not test them in a deployed cloud environment. Identity-focused research may examine authentication or contextual access decisions, while giving less attention to governance or workload enforcement. Cloud enforcement studies may implement controls or measure system performance, yet provide limited discussion of organizational responsibilities, privacy, or long-term policy maintenance.
These differences matter when interpreting a paper’s contribution. A proposed model can help explain how components might be arranged, but it should not be described as proven effective unless the authors evaluate it. An implementation study can provide evidence about a particular configuration and setting, but its findings may not automatically apply to other providers, organizations, or workloads. Governance recommendations can be useful even without an experiment, though they provide a different kind of evidence from performance measurements.
Comparison of Challenges and Evidence
Common challenges also vary across categories. Governance work may focus on coordination, accountability, auditability, and consistent policy management. Identity and adaptive access work may address fragmented identity records, stale permissions, contextual signal quality, privacy, and user friction. Enforcement work may address platform differences, integration with legacy applications, policy consistency, operational complexity, and performance overhead.
The evidence used to discuss these issues is not always comparable. Conceptual analysis can identify design concerns, but does not demonstrate operational performance. A prototype may show that a mechanism can work under test conditions, while a case study may describe organizational experience in a particular environment. Metrics such as access-decision time, detection accuracy, policy consistency, usability, or resource consumption each measure different outcomes. A lower latency, for example, does not by itself establish that a system provides stronger security.
Implications for the Survey
A cross-category comparison should therefore record both the topic and the evidence type for each source. For every paper, identify which categories it addresses, the cloud environment it considers, the mechanisms it describes, and whether its claims are conceptual, implemented, or experimentally evaluated. Also record limitations stated by the authors, such as a restricted test environment, limited datasets, or lack of deployment evidence.
This comparison can help identify gaps across the literature. If many works describe identity controls but few explain how decisions are enforced consistently across multi-cloud services, that may indicate an area needing further study. If technical evaluations report performance but omit governance or privacy considerations, the survey can note that their findings cover only part of the implementation problem. Such observations should be based on the papers actually included in the review.
Overall, the categories provide a framework for understanding how cloud ZTA research connects policy, identity, enforcement, and evidence. They also help distinguish between what a paper proposes and what it demonstrates. This distinction supports a balanced synthesis and prevents the survey from presenting an architectural idea as an empirically validated result.

B. Trends observed
The field has moved from defining ZTA principles toward multi-cloud and cloud-native applications. The chart below counts only the nine supplied PDFs by file title year; it is not a bibliometric count. It shows a recent concentration of review and conceptual materials alongside one identifiable 2025 research article. This folder cannot represent publication trends across the field.

C. Measures and evidence
Evaluating Zero Trust Architecture (ZTA) in cloud environments requires more than stating that a system follows Zero Trust principles. A study should explain what it evaluates, how it performs the evaluation, and what its results can support. The evidence may come from a conceptual analysis, prototype, simulation, experiment, case study, or production deployment. Each provides a different level and type of evidence, so they should be described separately in the survey.
Evaluation Methods
Conceptual analysis explains an architecture, framework, or set of principles. It can clarify how components are intended to work together, but it does not establish that the design performs effectively in practice.
Prototype evaluation implements some or all of a proposed design. It can show whether the components work under the test conditions, though the prototype may not include the complexity of a full cloud deployment.
Simulation or emulation models a cloud environment or access scenario. This can support controlled comparisons, but results depend on the assumptions and realism of the model.
Experiment or benchmark measures system behaviour under defined conditions. The paper should describe its setup, workload, comparison baseline, and metrics so readers can interpret the results.
Case study or deployment report describes use in a specific organization or environment. It can provide practical insight, but the findings may not generalize to other organizations or cloud providers.

Measure	What it can indicate	What to check in the source
Access-decision latency	Time required to evaluate and enforce an access request	Test conditions, baseline, and whether the measure includes network delay
Policy consistency	Whether similar requests receive decisions aligned with the same policy	How consistency is defined and tested across services or providers
Unauthorized access prevention	Whether prohibited requests are blocked in tested scenarios	Threat scenarios, test coverage, and false acceptance cases
Detection performance	How well a monitoring or analytics method identifies suspicious activity	Dataset, labels, precision, recall, false positives, and test split
Resource overhead	Computing, storage, or network cost introduced by controls	Environment size, workload, and measurement method
Usability and operational effort	Effects on users and administrators	Participants, task design, survey methods, and study limitations
Scalability	How behaviour changes as users, workloads, or requests increase	Scale tested and whether the environment reflects realistic cloud use
These measures capture different outcomes and should not be treated as interchangeable. For example, low access-decision latency says something about speed, but does not by itself show that access is secure. High detection accuracy may be less informative if the data is limited, imbalanced, or unrelated to real cloud activity. Any comparison should consider the study’s environment, assumptions, and definitions.
VI. RESEARCH GAPS AND OPEN CHALLENGES
Zero Trust Architecture (ZTA) is often presented as a way to improve cloud security through verified access, least privilege, and ongoing assessment. Turning these principles into a consistent, manageable, and measurable system remains difficult. The gaps below are topics to examine across the sources included in this survey. Retain and expand only the points that your reviewed papers support.
1. Limited and inconsistent evaluation
Research studies may evaluate different parts of ZTA using different cloud settings, threat scenarios, assumptions, and performance measures. One study may test an authentication method, while another describes a broad architecture without implementing it. Even when studies report results, differences in test environments can make direct comparison difficult. A prototype tested with a small workload may not reflect the behaviour of a large production environment.
This limits the conclusions a survey can draw about which approaches work best. A design may appear promising based on its architecture, but its operational performance, usability, and resistance to attack may remain untested.
Open challenge: Develop evaluation methods that clearly define the cloud environment, threat model, baseline, test workload, and measures used. Researchers should report enough detail for others to understand and, where possible, reproduce the evaluation. Comparisons should distinguish conceptual contributions from tested implementations.
2. Consistent policy enforcement across cloud environments
Organizations often combine public cloud services with private infrastructure and on-premises systems. They may also use multiple cloud providers, each with different identity services, policy languages, logging systems, and enforcement mechanisms. This makes it difficult to express and apply one coherent access policy everywhere.
A policy that is strict in one environment may be incomplete or configured differently in another. This can create inconsistent access decisions, monitoring gaps, or unexpected exceptions. Centralized policy management may help coordination, but it also introduces questions about provider compatibility, failure handling, and where enforcement should occur.
Open challenge: Investigate ways to represent and coordinate access policies across hybrid and multi-cloud environments. Future work should examine how to preserve consistent policy intent while accommodating provider-specific controls, and how to detect gaps or conflicts between policy decisions and actual enforcement.
3. Integration with legacy systems
Many organizations depend on older applications that were built around network boundaries or static permissions. These systems may not support modern authentication, workload identity, contextual access decisions, or detailed audit logging. Replacing them may be expensive or risky, while adding gateways and adapters can introduce additional components to configure and maintain.
Legacy integration also raises a sequencing problem: organizations may need to modernize identity and access controls gradually, while continuing to support existing systems. If transition steps are not planned carefully, temporary exceptions may persist and undermine least-privilege goals.
Open challenge: Develop practical migration strategies for bringing legacy applications into a ZTA. Such strategies should describe how to prioritize systems, manage transitional controls, test compatibility, and retire exceptions safely without disrupting essential services.

4. Reliability and quality of identity and context signals
Adaptive access decisions depend on information about users, devices, workloads, applications, and requested resources. These signals may come from separate services and may differ in accuracy, freshness, and availability. A device’s security status might be outdated, an identity record may not reflect a recent role change, or a workload may be misidentified.
If the system treats uncertain or missing information as trustworthy, it may grant access under unsafe conditions. If it always denies access when a signal is unavailable, it may interrupt legitimate work. Different policies may also interpret the same signal differently.
Open challenge: Study how ZTA systems can validate signals, communicate uncertainty, and make safe decisions when information is incomplete, stale, or conflicting. Research should explain which signals are necessary for a decision and how their reliability is assessed.
5. Balancing security, privacy, and usability
Continuous verification and monitoring can improve visibility into access activity, but they may involve collecting sensitive information about users, devices, locations, and behaviour. Excessive monitoring can create privacy concerns. Frequent authentication challenges or access denials can also frustrate users and disrupt ordinary work.
These concerns can affect adoption. If controls are difficult to use or poorly explained, users may seek workarounds, and administrators may create broad exceptions to reduce operational friction. At the same time, overly permissive access policies can reduce the security benefits of ZTA.
Open challenge: Evaluate access controls using both security and user-cantered measures. Future work can examine whether data minimization, clear policy explanations, risk-based verification, and accessible appeal processes can reduce unnecessary collection and disruption while preserving protection.
6. Policy complexity and lifecycle management
As organizations add cloud services, users, devices, workloads, and exceptions, the number of access rules can grow. Policies may overlap, conflict, or become outdated when employees change roles or applications are retired. Broad permissions may remain in place because removing them appears operationally risky.
Managing policies is therefore an ongoing process, not a one-time configuration task. Organizations need to understand who approves changes, how policy effectiveness is checked, how exceptions expire, and how audit findings lead to corrective action.
Open challenge: Explore methods for detecting redundant, conflicting, overly broad, or unused permissions. Research should also examine how policy changes can be tested before enforcement, how exceptions can be time-limited, and how administrators can understand why a request was allowed or denied.
7. Safe and explainable automation and AI
Automation and artificial intelligence may support threat detection, risk scoring, or policy adjustment. These tools could help process large amounts of security information, but their decisions may be difficult to interpret. False alarms can block legitimate activity, while missed detections can leave suspicious access unnoticed. The quality of results can depend strongly on the training data, labels, and test conditions.
There are also operational questions about how an automated system should respond. An automatic denial may be appropriate in some contexts but disruptive in others. Administrators need to understand what information influenced a decision and how to correct errors.
Open challenge: Evaluate automated and AI-supported ZTA approaches using transparent methods and relevant data. Studies should report the test setup, measures, error cases, and limitations. They should also examine explainability, human review, safe fallback behaviour, and processes for correcting mistaken decisions. Do not claim that AI improves security unless the sources provide evidence for that claim.
8. Operational cost, performance, and scalability
ZTA may introduce additional identity checks, policy evaluations, monitoring, logging, and enforcement steps. These controls can affect access latency, computing resources, network traffic, storage, and administrator workload. The impact may be small in one environment and significant in another, depending on the number of requests, the location of enforcement points, and the complexity of policies.
Performance considerations should not be reduced to speed alone. A system may process requests quickly but produce excessive false alerts or require substantial manual policy maintenance. Conversely, stronger checks may add delay but provide useful risk reduction. The trade-offs need to be measured in the context of the intended use.
Open challenge: Measure security outcomes, performance, resource use, and operational effort together under realistic workloads. Studies should state the scale tested and explain how their results may change in larger or more complex deployments.
9. Governance and shared responsibility
Cloud providers and customers share responsibility for securing cloud services, but the boundary between their duties can vary. Customers may control identities and permissions while providers manage parts of the infrastructure. If responsibilities for policy ownership, monitoring, incident response, and audit evidence are unclear, important tasks may be missed or duplicated.
Governance also determines how policies are approved, documented, reviewed, and changed. A technically strong system can be difficult to sustain if teams lack clear ownership or if decisions are not recorded. Regulatory and organizational requirements may further affect how data is handled and how access is audited.
Open challenge: Examine governance models that clarify responsibilities across customers, providers, and internal teams. Research can investigate how policy changes, exceptions, audit records, and incident decisions should be documented and reviewed over time.
10. Security of the ZTA components themselves
ZTA relies on identity providers, policy services, enforcement points, telemetry, and administrative interfaces. These components become important parts of the security architecture. If a policy service is unavailable or compromised, access decisions may be delayed, weakened, or incorrectly applied. Centralized components can also become attractive targets.
The architecture must account for failure conditions. For example, organizations need to decide whether access should fail closed or remain available in a limited mode when a decision service cannot be reached. The appropriate choice may depend on the sensitivity of the resource and the operational consequences of interruption.
Open challenge: Assess the resilience of ZTA components against compromise, outage, misconfiguration, and communication failure. Studies should explain how systems preserve secure access decisions during failures and how administrators can detect tampering or unexpected policy changes.
11. Cloud workload and service-to-service access
Cloud applications often consist of many services that communicate with one another. These workloads may be short-lived, automatically scaled, or distributed across environments. Managing their identities and permissions can be different from managing human user access. Static credentials or broad service permissions can persist longer than needed.
A cloud ZTA therefore needs to address machine identities as well as people. It must also account for how service relationships change as applications are updated or redeployed.
Open challenge: Investigate scalable approaches for assigning, verifying, and revoking workload identities and permissions. Research should consider short-lived workloads, service-to-service communication, containerized environments, and the effect of automated deployment processes.
12. Measuring security outcomes over time
A single test may show how a system behaves under a particular set of conditions, but ZTA is intended to operate continuously. Policies, users, applications, and threats change over time. A deployment that performs well initially may become less effective if permissions accumulate, monitoring is neglected, or controls are not updated.
It can also be difficult to attribute a reduction in incidents to ZTA alone, because organizations usually use several security controls together. Studies need to distinguish between the presence of a control and evidence that it contributed to a security outcome.
Open challenge: Develop longitudinal evaluation approaches that observe ZTA deployments over time. These could examine policy drift, access changes, incident handling, usability, and operational effort, while clearly describing other controls that may influence the results.
Summary
These gaps show that cloud ZTA research involves connected technical, organizational, and evaluation challenges. More comparable evidence is needed to assess how architectures perform across different cloud settings. Researchers also need to address policy consistency, legacy integration, signal reliability, privacy, usability, governance, resilience, and workload identity.
For this survey, present these points as research gaps only where they are supported by the papers and official guidance you have reviewed. A useful synthesis should identify which sources raise each issue, distinguish author-reported limitations from your own observations, and avoid presenting proposed solutions as proven results.
VII. FUTURE DIRECTIONS
Future research on Zero Trust Architecture (ZTA) for cloud security can build on the gaps identified in the reviewed work. The following directions are areas for investigation, rather than claims that particular solutions have already been proven effective.
1. Comparable evaluation frameworks
Researchers could define common evaluation scenarios, threat assumptions, and measures for cloud ZTA studies. Reports should clearly describe the cloud environment, workload, baseline, controls tested, and limitations. This would make it easier to compare results while recognizing that different organizations have different risks and requirements.
2. Policy coordination across cloud platforms
Further work could examine how organizations can maintain consistent policy intent across hybrid and multi-cloud environments. This includes studying policy translation, conflict detection, auditability, and the handling of provider-specific controls. Research should also consider what happens when policy services or enforcement points are unavailable.
3. Gradual migration for legacy systems
Many organizations cannot replace older applications at once. Future studies could propose and evaluate step-by-step migration approaches, including how to prioritize systems, introduce interim protections, test compatibility, and remove temporary exceptions.
4. More reliable context for adaptive access
Adaptive decisions depend on the accuracy and freshness of identity, device, workload, and risk signals. Research could explore ways to measure signal reliability and handle missing, stale, or conflicting information. It should also explain how systems make decisions when context is uncertain.
5. Privacy-aware and usable controls
Future work could assess how monitoring and contextual access affect privacy and user experience. Studies might examine data minimization, clear explanations for access decisions, and methods for reducing unnecessary verification prompts while preserving appropriate security.
6. Policy lifecycle and administration
Research could investigate tools and processes for finding outdated, conflicting, or overly broad permissions. Other useful topics include testing policy changes before deployment, setting expiry dates for exceptions, and helping administrators understand why a request was permitted or denied.
7. Explainable automation and AI
AI-supported detection and automated policy actions need careful evaluation. Future studies could report how models are trained and tested, what kinds of errors occur, and how administrators can review or correct automated decisions. Researchers should also examine safe fallback behaviour when a model or data source is unavailable.
8. Workload and service identity
Cloud applications rely on services that communicate with one another, and these workloads may be created or removed automatically. Future work could explore how to assign, verify, and revoke workload identities and permissions in dynamic environments, including containers and automated deployment systems.
9. Resilience and long-term operation
ZTA depends on identity services, policy systems, monitoring tools, and enforcement points. Research could test how these components behave during outages, compromise, or configuration errors. Longer-term studies could also examine policy drift, maintenance effort, access changes, and security outcomes over time.
Overall, future studies should describe their assumptions and settings in enough detail for readers to judge how applicable the results are. They should distinguish proposed designs from tested implementations and report both benefits and limitations. In this survey, include only directions that follow from gaps found in the sources you actually reviewed.

VIII. CONCLUSION
This survey reviewed Zero Trust Architecture (ZTA) for cloud security through its architecture and governance, identity and adaptive access, and cloud-native enforcement and evaluation. Across these areas, ZTA is presented as an approach in which access decisions are based on verified identity, policy, and relevant context, with permissions limited to what is needed. In cloud environments, these principles can help organizations manage access to users, applications, workloads, and data across changing and distributed systems.
The reviewed work also highlights practical challenges. Organizations may need to coordinate policies across cloud providers, integrate legacy applications, maintain reliable identity and context information, and balance security with privacy and usability. Evaluation is another concern: studies use different settings and measures, so their results may not be directly comparable. Architectural proposals should therefore be distinguished from approaches that have been implemented and tested.
Future research can strengthen the evidence base through clearer evaluation methods, more consistent policy management across cloud environments, practical migration strategies, and careful study of automation and AI. Researchers should state their assumptions, describe their test settings, report limitations, and avoid presenting expected benefits as measured outcomes.
Overall, ZTA offers a useful framework for thinking about cloud access and security, but its effectiveness depends on how well its policies, identity systems, enforcement controls, and governance processes work together. This survey provides an overview of those elements and the open questions that remain. Its conclusions should be read in light of the sources and search process documented in the final paper.

























REFERENCES
[1] S. Rose, O. Borchert, S. Mitchell, and S. Connelly, “Zero Trust Architecture,” NIST SP 800-207, 2020, doi: 10.6028/NIST.SP.800-207.
[2] R. Chandramouli, “A Zero Trust Architecture Model for Access Control in Cloud-Native Applications in Multi-Location Environments,” NIST SP 800-207A, 2023, doi: 10.6028/NIST.SP.800-207A.
[3] NCCoE, “Implementing a Zero Trust Architecture,” NIST SP 1800-35, 2024.
[4] N. F. Syed et al., “Zero trust architecture (ZTA): A comprehensive survey,” IEEE Access, vol. 10, pp. 57143–57179, 2022, doi: 10.1109/ACCESS.2022.3174679.
[5] S. Sarkar et al., “Security of zero trust networks in cloud computing: A comparative review,” Sustainability, vol. 14, no. 18, Art. 11213, 2022, doi: 10.3390/su141811213.
[6] G. B. Oladimeji, “A critical analysis of foundations, challenges and directions for zero trust security in cloud environments,” arXiv:2411.06139, 2024, doi: 10.48550/arXiv.2411.06139.
[7] “Cloud-based zero trust access control policy: An approach to support work-from-home driven by COVID-19 pandemic,” New Generation Computing, vol. 39, pp. 599–622, 2021, doi: 10.1007/s00354-021-00130-6. [Verify author list.]
[8] S. Xiao et al., “SoK: Context and risk aware access control for zero trust systems,” Security and Communication Networks, 2022, Art. 7026779, doi: 10.1155/2022/7026779.
[9] M. Buck et al., “Performance analysis of zero-trust multi-cloud,” Proc. IEEE CLOUD, 2021, doi: 10.1109/CLOUD53861.2021.00097.
[10] M. Tsai, S. Lee, and S. W. Shieh, “Strategy for implementing of zero trust architecture,” IEEE Trans. Reliability, vol. 73, no. 1, pp. 93–100, 2024, doi: 10.1109/TR.2023.3345665.
[11] R. Chandramouli and Z. B. Tariq, “Implementation of DevSecOps for a microservices-based application with service mesh,” NIST SP 800-204C, 2022, doi: 10.6028/NIST.SP.800-204C.
[12] L. Ferretti, F. Magnanini, M. Andreolini, and M. Colajanni, “Survivable zero trust for cloud computing environments,” Computers & Security, vol. 110, Art. 102419, 2021, doi: 10.1016/j.cose.2021.102419.
[13] S. Tiwari, W. Sarma, and A. Srivastava, “Integrating artificial intelligence with zero trust architecture,” Int. J. Research and Analytical Reviews, vol. 9, no. 2, 2022. [Verify full title and pages.]
[14] S. Lilhore et al., “SmartTrust: A hybrid deep learning framework for real-time threat detection in cloud environments using zero-trust architecture,” Journal of Cloud Computing, vol. 14, Art. 35, 2025, doi: 10.1186/s13677-025-00764-7.
[15] S. Ahmadi, “Zero trust architecture in cloud networks: Application, challenges and future opportunities,” J. Engineering Research and Reports, vol. 26, no. 2, pp. 215–228, 2024, doi: 10.9734/JERR/2024/v26i21083.
[16] K. Mudau, K. Mudumani, and S. M. Zwane, “Zero trust architecture: Frameworks and implementation strategies in modern cybersecurity,” Zenodo, 2025, doi: 10.5281/zenodo.17404160. [Verify version/status.]
[17] S. Bondhala, “Modern defense paradigms: Zero trust architecture, network segmentation, and micro-segmentation,” IJ of Scientific Research in Computer Science, Engineering and IT, vol. 11, no. 2, pp. 2230–2239, 2025, doi: 10.32628/CSEIT25112714.
[18] M. Maqbool et al., “Integrated cyber defense strategies for the modern digital ecosystem,” Journal of Management Science Research Review, vol. 5, no. 1, pp. 28–43, 2026, doi: 10.5281/zenodo.18207381. [Resolve file-year discrepancy.]
[19] C. Ward and B. Beyer, “BeyondCorp: A new approach to enterprise security,” ;login:, vol. 39, no. 6, 2014.
[20] CISA, “Zero Trust Maturity Model,” Version 2.0, 2023.
[21] Google, “BeyondProd: A new approach to cloud-native security,” 2019.
[22] “Towards a zero-trust micro-segmentation network security strategy: An evaluation framework,” Proc. IEEE/IFIP NOMS, 2022, doi: 10.1109/NOMS54207.2022.9789888. [Verify author list.]
[23] P. Dhiman, N. Saini, Y. Gulzar, S. Turaev, A. Kaur, K. U. Nisa, and Y. Hamid, “A review and comparative analysis of relevant approaches of zero trust network model,” Sensors, vol. 24, no. 4, Art. 1328, 2024, doi: 10.3390/s24041328.
[24] E. B. Fernández and A. Brazhuk, “A critical analysis of Zero Trust Architecture (ZTA),” Computer Standards & Interfaces, vol. 89, Art. 103832, 2024, doi: 10.1016/j.csi.2024.103832.
[25] J. Bartakke and R. Kashyap, “The usage of clouds in zero-trust security strategy: An evolving paradigm,” Journal of Information and Organizational Sciences, vol. 48, no. 1, pp. 149–165, 2024, doi: 10.31341/jios.48.1.8.









ANNEXURE: SEARCH LOG, CONTRIBUTION AND DECLARATION
A. Evidence repository
Item	Status
Repository URL	https://github.com/deepanshijha/Zero-Trust-Architecture-for-Cloud-Security-A-Survey

