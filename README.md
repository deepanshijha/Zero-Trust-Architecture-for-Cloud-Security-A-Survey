# Zero Trust Architecture for Cloud Security: A Survey

> An overview of security principles, implementation approaches, challenges, and the future of Zero Trust in cloud environments.

This repository is the evidence repository (reference library and literature matrix) for a survey paper submitted at **IILM University, Gurugram**.

## Course Details

| Field | Detail |
|---|---|
| Course Title | Foundation of Cybersecurity |
| Course Code | CSE25303 |
| Programme and Semester | B. Tech (CSE), Semester 3 |
| Batch and Session | Batch 2025-29, Session 2026-27 |
| Works reviewed | 25 papers, tools or systems, published between 2020 and 2026 |
| Sources searched | IEEE Xplore, ACM Digital Library, SpringerLink, Google Scholar, arXiv |

## Authors

| Role | Name |
|---|---|
| Author | Deepanshi Jha, B. Tech CSE, School of Computer Science and Engineering, IILM University |
| Supervisor | Dr. Abhishek Pandey, Assistant Professor, School of Computer Science and Engineering |
| Course Coordinator | Dr. Preetishree Patnaik |

## Abstract

Cloud computing provides flexible access to applications and data, but its distributed nature creates security challenges involving identity, access control, and changing network boundaries. Zero Trust Architecture (ZTA) addresses these challenges through the principle of "never trust, always verify," requiring access decisions to consider users, devices, context, and resource sensitivity.

This survey reviews how ZTA is applied to cloud security, focusing on its core components, deployment approaches, benefits, and implementation challenges. It organizes the topic into identity and policy management, device and workload security, network segmentation, continuous monitoring, and automation. It also compares architectural guidance and research directions, including the use of AI to support threat detection and adaptive access decisions.

Key challenges include legacy integration, policy complexity, monitoring overhead, privacy concerns, and the difficulty of evaluating security outcomes consistently. The survey identifies research needs in measurable evaluation methods, explainable automation, and practical guidance for hybrid and multi-cloud environments. It concludes that ZTA can strengthen cloud security when implemented as a coordinated, risk-based approach supported by reliable identity, monitoring, and governance practices.

## Review Questions

- **RQ1:** What core components and principles of ZTA are used to protect cloud environments?
- **RQ2:** How are identity, access policies, devices, workloads, network segmentation, and monitoring combined in cloud ZTA implementations?
- **RQ3:** What benefits and implementation challenges are reported for applying ZTA to cloud security?
- **RQ4:** How are automation and AI being explored to support ZTA, and what limitations are identified?
- **RQ5:** What research gaps and future directions emerge from the reviewed literature?

## Review Methodology

**Sources:** IEEE Xplore, ACM Digital Library, SpringerLink, Google Scholar, arXiv, plus official standards and guidance from NIST and CISA.

**Selection criteria**

| Include | Exclude from evidence synthesis |
|---|---|
| Directly addresses ZTA, cloud access, identity, segmentation, or cloud-native enforcement | Uses zero trust only as a label without a relevant mechanism |
| Identifiable standard, peer-reviewed paper, or clearly labeled preprint/review | Duplicate, promotional summary, or unusable record |
| Approach or scope can be described from accessible text | Reports numerical improvement without method or test basis |
| Evidence level and limitation are recorded separately | Outside scope or publication record cannot be verified |

Inclusion also required English-language material from 2020-2026 (with older foundational work for context).

## Taxonomy of the Reviewed Work

| Category | Focus | Common approaches |
|---|---|---|
| Identity and access management | Verifying users and controlling their permissions | Strong authentication, MFA, least privilege, role- or attribute-based access |
| Device and workload security | Assessing endpoints, VMs, containers, and services | Device posture checks, workload identity, configuration monitoring, endpoint protection |
| Policy decision and enforcement | Deciding whether a request should be allowed | Context-aware policy evaluation, policy decision points, policy enforcement points |
| Network segmentation | Limiting communication between users, applications, and resources | Micro-segmentation, software-defined perimeters, service-level access controls |
| Continuous monitoring and response | Observing activity and adjusting access as conditions change | Logging, security analytics, anomaly detection, session review, incident response |
| Automation and AI support | Helping analyse signals and manage security decisions | Automated policy actions, ML-based detection, risk scoring |

The literature is also compared by deployment setting (single, hybrid, or multi-cloud), type of contribution (architecture, implementation, evaluation, or guidance), and evaluation method (conceptual analysis, case study, experiment, or performance measurement).

## Summary of the Literature Review

The review is organized into three themes:

1. **Architecture and governance.** A cloud ZTA is described through three functions: *policy decision*, *policy enforcement*, and *information sources*. Governance covers policy ownership, data classification, review and audit processes, exception handling, privacy, and shared responsibility with cloud providers.
2. **Identity and adaptive access.** Identity underpins every access decision. Controls include MFA, single sign-on, and least privilege. Adaptive access adds context (role, device status, location, time, alerts) so a policy can allow, step up verification, limit, or deny.
3. **Cloud-native enforcement and evaluation.** Enforcement applies decisions at identity services, gateways, workloads, or network layers. Evidence types differ (conceptual analysis, prototype, simulation, experiment, case study) and should not be treated as interchangeable.

### Evaluation measures

| Measure | What it can indicate |
|---|---|
| Access-decision latency | Time to evaluate and enforce a request |
| Policy consistency | Whether similar requests get decisions aligned with the same policy |
| Unauthorized access prevention | Whether prohibited requests are blocked in tested scenarios |
| Detection performance | How well analytics identify suspicious activity |
| Resource overhead | Compute, storage, or network cost of controls |
| Usability and operational effort | Effects on users and administrators |
| Scalability | Behaviour as users, workloads, or requests increase |

## Research Gaps and Open Challenges

1. Limited and inconsistent evaluation
2. Consistent policy enforcement across cloud environments
3. Integration with legacy systems
4. Reliability and quality of identity and context signals
5. Balancing security, privacy, and usability
6. Policy complexity and lifecycle management
7. Safe and explainable automation and AI
8. Operational cost, performance, and scalability
9. Governance and shared responsibility
10. Security of the ZTA components themselves
11. Cloud workload and service-to-service access
12. Measuring security outcomes over time

## Future Directions

1. Comparable evaluation frameworks
2. Policy coordination across cloud platforms
3. Gradual migration for legacy systems
4. More reliable context for adaptive access
5. Privacy-aware and usable controls
6. Policy lifecycle and administration
7. Explainable automation and AI
8. Workload and service identity
9. Resilience and long-term operation

## Conclusion

ZTA offers a useful framework for thinking about cloud access and security, but its effectiveness depends on how well its policies, identity systems, enforcement controls, and governance processes work together. Architectural proposals should be distinguished from approaches that have been implemented and tested, and expected benefits should not be presented as measured outcomes.

## References

1. S. Rose, O. Borchert, S. Mitchell, and S. Connelly, "Zero Trust Architecture," NIST SP 800-207, 2020, doi: 10.6028/NIST.SP.800-207.
2. R. Chandramouli, "A Zero Trust Architecture Model for Access Control in Cloud-Native Applications in Multi-Location Environments," NIST SP 800-207A, 2023, doi: 10.6028/NIST.SP.800-207A.
3. NCCoE, "Implementing a Zero Trust Architecture," NIST SP 1800-35, 2024.
4. N. F. Syed et al., "Zero trust architecture (ZTA): A comprehensive survey," *IEEE Access*, vol. 10, pp. 57143-57179, 2022, doi: 10.1109/ACCESS.2022.3174679.
5. S. Sarkar et al., "Security of zero trust networks in cloud computing: A comparative review," *Sustainability*, vol. 14, no. 18, Art. 11213, 2022, doi: 10.3390/su141811213.
6. G. B. Oladimeji, "A critical analysis of foundations, challenges and directions for zero trust security in cloud environments," arXiv:2411.06139, 2024, doi: 10.48550/arXiv.2411.06139.
7. "Cloud-based zero trust access control policy: An approach to support work-from-home driven by COVID-19 pandemic," *New Generation Computing*, vol. 39, pp. 599-622, 2021, doi: 10.1007/s00354-021-00130-6. *(Verify author list.)*
8. S. Xiao et al., "SoK: Context and risk aware access control for zero trust systems," *Security and Communication Networks*, 2022, Art. 7026779, doi: 10.1155/2022/7026779.
9. M. Buck et al., "Performance analysis of zero-trust multi-cloud," *Proc. IEEE CLOUD*, 2021, doi: 10.1109/CLOUD53861.2021.00097.
10. M. Tsai, S. Lee, and S. W. Shieh, "Strategy for implementing of zero trust architecture," *IEEE Trans. Reliability*, vol. 73, no. 1, pp. 93-100, 2024, doi: 10.1109/TR.2023.3345665.
11. R. Chandramouli and Z. B. Tariq, "Implementation of DevSecOps for a microservices-based application with service mesh," NIST SP 800-204C, 2022, doi: 10.6028/NIST.SP.800-204C.
12. L. Ferretti, F. Magnanini, M. Andreolini, and M. Colajanni, "Survivable zero trust for cloud computing environments," *Computers & Security*, vol. 110, Art. 102419, 2021, doi: 10.1016/j.cose.2021.102419.
13. S. Tiwari, W. Sarma, and A. Srivastava, "Integrating artificial intelligence with zero trust architecture," *Int. J. Research and Analytical Reviews*, vol. 9, no. 2, 2022. *(Verify full title and pages.)*
14. S. Lilhore et al., "SmartTrust: A hybrid deep learning framework for real-time threat detection in cloud environments using zero-trust architecture," *Journal of Cloud Computing*, vol. 14, Art. 35, 2025, doi: 10.1186/s13677-025-00764-7.
15. S. Ahmadi, "Zero trust architecture in cloud networks: Application, challenges and future opportunities," *J. Engineering Research and Reports*, vol. 26, no. 2, pp. 215-228, 2024, doi: 10.9734/JERR/2024/v26i21083.
16. K. Mudau, K. Mudumani, and S. M. Zwane, "Zero trust architecture: Frameworks and implementation strategies in modern cybersecurity," Zenodo, 2025, doi: 10.5281/zenodo.17404160. *(Verify version/status.)*
17. S. Bondhala, "Modern defense paradigms: Zero trust architecture, network segmentation, and micro-segmentation," *IJ of Scientific Research in Computer Science, Engineering and IT*, vol. 11, no. 2, pp. 2230-2239, 2025, doi: 10.32628/CSEIT25112714.
18. M. Maqbool et al., "Integrated cyber defense strategies for the modern digital ecosystem," *Journal of Management Science Research Review*, vol. 5, no. 1, pp. 28-43, 2026, doi: 10.5281/zenodo.18207381. *(Resolve file-year discrepancy.)*
19. C. Ward and B. Beyer, "BeyondCorp: A new approach to enterprise security," *;login:*, vol. 39, no. 6, 2014.
20. CISA, "Zero Trust Maturity Model," Version 2.0, 2023.
21. Google, "BeyondProd: A new approach to cloud-native security," 2019.
22. "Towards a zero-trust micro-segmentation network security strategy: An evaluation framework," *Proc. IEEE/IFIP NOMS*, 2022, doi: 10.1109/NOMS54207.2022.9789888. *(Verify author list.)*
23. P. Dhiman, N. Saini, Y. Gulzar, S. Turaev, A. Kaur, K. U. Nisa, and Y. Hamid, "A review and comparative analysis of relevant approaches of zero trust network model," *Sensors*, vol. 24, no. 4, Art. 1328, 2024, doi: 10.3390/s24041328.
24. E. B. Fernandez and A. Brazhuk, "A critical analysis of Zero Trust Architecture (ZTA)," *Computer Standards & Interfaces*, vol. 89, Art. 103832, 2024, doi: 10.1016/j.csi.2024.103832.
25. J. Bartakke and R. Kashyap, "The usage of clouds in zero-trust security strategy: An evolving paradigm," *Journal of Information and Organizational Sciences*, vol. 48, no. 1, pp. 149-165, 2024, doi: 10.31341/jios.48.1.8.

## Repository

https://github.com/deepanshijha/Zero-Trust-Architecture-for-Cloud-Security-A-Survey

---

*Prepared for academic submission at IILM University, Gurugram. Reference entries marked "Verify" should be checked against the original publication records.*
