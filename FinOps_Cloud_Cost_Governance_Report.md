# A FinOps Approach to Cloud Cost Governance (Bridging Engineering and Finance)

**PROJECT REPORT OF CO-OP Project at Industry (Module-2)**

Submitted in partial fulfilment of the requirements for the award of the degree of **Bachelor of Engineering** in **Computer Science and Engineering**.

**Submitted by:**
- Muskan Bandta — 2210991947
- Riya — 2210990734
- Parisha — 2210992023

**Supervised By:** Preeti Saini, Mentor, Chitkara University

Department of Computer Science and Engineering
Chitkara University Institute of Engineering and Technology
Chitkara University, Punjab, India

---

## Declaration

I hereby certify that the work which is being presented in the project report entitled "A FinOps Approach to Cloud Cost Governance (Bridging Engineering and Finance)" in partial fulfilment of requirement for the award of the degree of Bachelor of Engineering (Computer Science and Engineering) submitted in the department of Computer Science and Engineering at Chitkara University Institute of Engineering and Technology, Chitkara University, Punjab, India, is an authentic record of our own work carried out under the supervision of Preeti Saini, Mentor, Zop. The matter presented in this project report has not been submitted in any other university/institute for the award of any degree.

**Place:** Bangalore
**Date:** 6 May 2026

This is to certify that the above statement made by the candidates is correct to the best of my knowledge and belief.

**Preeti Saini**
Mentor, Chitkara University

---

## Acknowledgement

We would like to express our sincere gratitude to all those who have supported and guided us throughout the duration of this CO-OP project. The completion of this work would not have been possible without their valuable contributions.

First, we extend our heartfelt thanks to our industry mentor, Ms. Preeti Saini, at Zop, for her continuous guidance, technical insight, and constructive feedback during every phase of the project. Her practical perspective on cloud cost governance and her willingness to share real-world experience helped us connect academic concepts to industry practice in a meaningful way.

We are also deeply grateful to the Department of Computer Science and Engineering, Chitkara University Institute of Engineering and Technology, for facilitating this CO-OP programme and for the academic foundation that prepared us for this engagement. We thank our faculty coordinators for their guidance on the structure and scope of the project report and for their prompt support whenever we approached them.

We would also like to acknowledge the engineering and finance professionals who participated in our research interviews and shared their honest experiences with FinOps adoption. Their insights formed the empirical core of this study.

Finally, we thank our families and peers for their constant encouragement, patience, and moral support, which made this work possible.

— Muskan Bandta, Riya, Parisha

---

## Contents

- Acknowledgement
- Abstract
- 1 Introduction
- 2 Methodology
- 3 Tools and Technologies
- 4 Implementation
- 5 Major Findings, Outcomes and Results
- 6 Conclusion and Future Scope
- References
- Appendices

## List of Figures and Tables

**Figures**
- Figure 1: Cloud Cost Reduction Achieved After FinOps Implementation
- Figure 2: Hub-and-Spoke FinOps Governance Model

**Tables**
- Table 1: Comparison of Related Literature
- Table 2: Tools and Technologies Used
- Table 3: Evaluation Metrics and Measurement Approach
- Table 4: Financial Performance by Organization

---

## Abstract

The rapid adoption of cloud computing has transformed organizational IT infrastructure, offering unmatched scalability and flexibility. However, this shift has also introduced significant challenges in cost management and resource optimization. Traditional financial management practices often fail to address the dynamic nature of cloud spending, leading to budget overruns and inefficient resource utilization. FinOps emerges as a collaborative framework that bridges the gap between engineering, finance, and business teams, enabling organizations to maximize cloud value while maintaining financial accountability and operational efficiency.

This project explores the implementation of FinOps practices for effective cloud cost governance. The objectives include analyzing the integration of engineering and financial workflows, evaluating cost optimisation strategies, assessing the role of cross-functional collaboration in cloud resource management, and identifying best practices for sustainable cloud financial operations. A mixed-methods approach was employed, combining a literature review of more than forty sources, in-depth case-study analysis of five organizations across technology, financial services, healthcare, retail, and manufacturing sectors, and semi-structured interviews with eighteen practitioners.

The study found that organizations implementing FinOps practices achieved an average cloud cost reduction of 27.4 percent, with mature implementations reaching up to 35 percent within a single year. Cross-functional collaboration improved resource allocation efficiency by 38 to 40 percent on average. Key success factors included executive sponsorship, real-time cost visibility, automated resource tagging, dedicated FinOps champions, and consistent monthly review cycles. The proposed hub-and-spoke governance model, combined with a three-phase Crawl-Walk-Run roadmap, provides a practical framework that organizations can adapt across different maturity levels.

**Keywords:** FinOps, cloud cost governance, cost optimization, cross-functional collaboration, cloud financial management.

---

## 1. Introduction

### 1.1 Background of the Problem

Cloud computing has grown rapidly over the past decade and is now a core part of enterprise IT infrastructure. Organizations can access computing resources on demand without having to invest in physical hardware, which has led to wide adoption across industries. However, this shift has also created serious problems around cost control. According to Flexera (2023), organizations estimate that around 32 percent of their cloud spending goes to waste every year. This is mainly because teams provision more resources than they actually need, forget to delete unused services, or pick expensive pricing options when cheaper alternatives are available.

The traditional way of managing IT costs does not work well in the cloud. In the past, companies would plan their IT budget in advance and spend a fixed amount on hardware. In the cloud, costs change in real time depending on how much is being used. This creates a mismatch between engineering teams who make decisions about cloud usage and finance teams who are responsible for tracking spending. Storment and Fuller (2019) explain that this gap between engineering and finance is one of the main reasons cloud costs spiral out of control.

### 1.2 Motivation

The problem of cloud overspending is getting worse as companies move to multi-cloud environments. HashiCorp (2022) found that 90 percent of organizations prefer using more than one cloud provider, but fewer than 40 percent have put proper cost governance policies in place. Without clear rules and shared accountability, teams end up spending more than planned and have little idea where the money is going. For large companies, this can mean wasting hundreds of millions of dollars every year.

FinOps, short for Financial Operations, has developed as a way to address this problem. The goal of FinOps is to get engineering, finance, and business teams to work together on cloud spending decisions. Rather than leaving cost management to one team, FinOps distributes responsibility across the organization so that everyone who uses cloud resources also takes ownership of the costs they create (FinOps Foundation, 2023).

### 1.3 Research Gap

Even though FinOps is gaining popularity in the industry, there is not much academic research that looks at it as a complete governance framework. Most technical guidance comes from cloud vendors like AWS, Microsoft, and Google, and focuses only on how to reduce costs within their own platforms. These guides are helpful for technical teams but they do not address how organizations need to change their culture and structure to make FinOps work. There is also very little empirical research that measures what actually happens when organizations adopt FinOps over time. This study aims to fill that gap.

### 1.4 Objectives

This project focuses on four main objectives:

1. To analyze how engineering and financial workflows can be integrated through FinOps governance.
2. To evaluate cloud cost optimization strategies used by organizations that have adopted FinOps.
3. To assess how cross-functional collaboration between engineering and finance affects cloud resource management.
4. To identify best practices for sustainable cloud financial operations that can work across different types of organizations.

### 1.5 Report Organization

Section 2 explains the research methodology used in this project. Section 3 describes the tools and technologies adopted. Section 4 presents the proposed governance model and its implementation roadmap. Section 5 discusses the major findings and results from the case study organizations. Section 6 provides the conclusion along with directions for future research.

---

## 2. Methodology

This study uses a mixed-methods research design that combines literature review, case studies, and interviews. This approach was chosen because cloud cost governance is both a technical and an organizational problem. Quantitative data captures the financial impact, while qualitative data explains the human and structural factors that drive those outcomes.

### 2.1 Literature Review and Comparison

Sources include academic papers, industry reports, and vendor documentation published between 2011 and 2023. The review covered IEEE Xplore, Springer, Google Scholar, and FinOps practitioner databases. Search terms included FinOps, cloud cost governance, cloud financial management, cross-functional collaboration, and cloud cost optimization. A total of 40 sources were included in the final review.

**Table 1: Comparison of Related Literature**

| Author(s) & Year | Focus Area | Methods | Key Findings | Limitation |
|---|---|---|---|---|
| Storment & Fuller (2019) | FinOps framework | Practitioner framework & case studies | Defined FinOps; introduced Crawl-Walk-Run maturity model | Limited academic empirical validation |
| FinOps Foundation (2023) | FinOps maturity & adoption | Annual survey with 5,000+ practitioners | Only 20% at Run maturity; cost management remains top challenge | Self-reported data; may over-represent FinOps-aware respondents |
| Flexera (2023) | Cloud cost waste | Industry survey with 750 decision-makers | 32% cloud spend wasted; cost management top challenge four years running | Does not examine governance or collaboration frameworks |
| AWS (2022); Microsoft (2023); Google Cloud (2022) | Vendor cost optimization frameworks | Prescriptive vendor guidelines | Right-sizing, reserved pricing, autoscaling reduce cloud costs | Platform-specific; ignore organizational and cultural factors |
| HashiCorp (2022) | Cloud governance strategy | Industry survey with 3,000 professionals | Governance policies linked to lower cost overruns; <40% have full frameworks | No longitudinal data on governance maturity outcomes |

### 2.2 Research Design and Data Collection

The research design has four components: a systematic literature review of more than forty sources; an in-depth case study analysis of five organizations across technology, retail, healthcare, financial services, and manufacturing sectors; semi-structured interviews with eighteen practitioners including FinOps engineers, cloud architects, CFOs, and DevOps leads; and quantitative metrics analysis covering cloud billing data, utilization rates, cost reduction percentages, and tagging coverage.

Quantitative data was collected from the cloud billing dashboards and cost reports of the five case organizations that agreed to share data confidentially. The main metrics tracked were monthly cloud spend, percentage of resources with proper cost tags, idle resource rates, reserved instance usage, and year-over-year cost changes. Qualitative data came from eighteen semi-structured interviews lasting forty-five to sixty minutes each.

---

## 3. Tools and Technologies

The five case study organizations used a range of tools to manage cloud costs. Table 2 summarizes the tools used and their specific purpose in this study.

**Table 2: Tools and Technologies Used**

| Tool / Technology | Category | Usage in Study |
|---|---|---|
| AWS Cost Explorer | Cost Visibility | Real-time cost monitoring and usage reports for AWS resources. |
| Azure Cost Management | Cost Visibility | Budgeting, cost analysis, and anomaly detection for Azure services. |
| Google Cloud Billing | Cost Visibility | Usage-based billing dashboards and export to BigQuery for analysis. |
| Terraform | Tagging & Governance | Infrastructure-as-code with mandatory tagging policies enforced at provisioning. |
| CloudHealth by VMware | Optimization | Multi-cloud cost management, rightsizing recommendations, and showback reporting. |
| Apptio Cloudability | Optimization | Financial management platform for cloud cost allocation and chargeback. |
| NVivo | Qualitative Analysis | Coding and thematic analysis of eighteen stakeholder interview transcripts. |
| Cloud-Native Policy Tools | Governance | AWS SCPs, Azure Policy, and GCP Organization Policies for governance enforcement. |

These tools were chosen because they cover the full FinOps lifecycle: cost visibility (knowing what is being spent), governance (enforcing rules), optimization (reducing waste), and analysis (understanding patterns). The diversity of tools also reflects the multi-cloud nature of the case organizations, which made tool integration and a single source of truth a recurring challenge.

---

## 4. Implementation

This section presents the FinOps governance model proposed and tested in this project. The model is designed to address three gaps found in the literature: lack of organizational structure, absence of cross-functional collaboration tools, and no clear implementation roadmap for different maturity levels.

### 4.1 Hub-and-Spoke Governance Structure

The model uses a hub-and-spoke architecture. The central hub is a Cloud Financial Operations Center of Excellence that includes members from finance, engineering, and senior leadership. This team is responsible for setting governance policies, maintaining shared cost dashboards, defining tagging standards, and publishing regular cost performance reports. Each engineering team then has a FinOps champion who is part of their team but also connected to the central hub. These champions are responsible for applying governance standards in their day-to-day work and participating in monthly cost review meetings. Figure 2 illustrates this governance structure.

*Figure 2: Hub-and-Spoke FinOps Governance Model — Senior Leadership, Finance Team, and Engineering Team connect to the Cloud Financial Ops Center (Central Hub), which connects out to FinOps Champion A (Tech), FinOps Champion B (Retail), and FinOps Champion C (Healthcare).*

The three core principles of the model are: (i) all teams must have real-time visibility of their cloud costs; (ii) financial accountability is shared across engineering and finance; and (iii) optimization is a continuous process, not a one-time project.

### 4.2 Three-Phase Implementation Roadmap

The model is implemented in three phases based on the Crawl-Walk-Run framework from the FinOps Foundation (2023).

- **Phase 1 (Crawl, Months 1–3):** Set up basic cost visibility. Deploy cost monitoring across all cloud accounts, enforce mandatory resource tagging, create a central dashboard, and train both engineering and finance staff on FinOps basics. Target: full visibility across accounts and over 80 percent tagging coverage.
- **Phase 2 (Walk, Months 4–8):** Start optimizing actively. Review and act on rightsizing recommendations, begin purchasing reserved instances, hold joint monthly cost reviews with engineering and finance, and publish showback reports to product teams. Target: 15 to 20 percent cost reduction from Phase 1 baseline.
- **Phase 3 (Run, Month 9 and beyond):** Automate and scale governance. Set up automated cost anomaly alerts, integrate budget guardrails into deployment pipelines, track unit economics tied to business outcomes, and embed FinOps into the annual planning process. Target: 25 to 35 percent total cost reduction and over 90 percent tagging compliance.

### 4.3 Evaluation Metrics

Five key metrics were used to measure FinOps performance.

**Table 3: Evaluation Metrics and Measurement Approach**

| Metric | Definition | Measurement Approach |
|---|---|---|
| Cloud Cost Reduction (%) | Percentage reduction in total cloud spend versus prior year baseline (pre-FinOps). | Primary financial KPI; validated against billing dashboard exports. |
| Resource Utilization Improvement (%) | Change in CPU and memory utilization rates after rightsizing and optimization. | Measured via cloud monitoring tools; baseline vs. post-optimization. |
| Resource Tagging Coverage (%) | Percentage of cloud resources with mandatory cost-allocation tags applied. | Governance indicator; threshold of 80% set for Phase 1 target. |
| Budget Forecast Accuracy (%) | Accuracy of monthly cloud cost predictions versus actual spend. | Tracks FinOps impact on financial planning quality over time. |
| Collaboration Index | Composite score derived from interview responses on cross-team alignment. | Qualitative metric; coded using NVivo thematic analysis framework. |

### 4.4 Collaboration Mechanisms

Four specific mechanisms are built into the model to improve engineering and finance collaboration. First, shared real-time dashboards give both teams access to the same cost data at the same time, removing the information gap. Second, monthly joint cost review meetings create a regular forum where both teams discuss spending together and agree on priorities. Third, FinOps champions within engineering teams act as translators, helping engineers understand the financial impact of their technical decisions. Fourth, short training sessions are run to help finance staff understand basic cloud concepts and help engineers understand how their decisions affect the budget.

---

## 5. Major Findings, Outcomes and Results

This section presents the findings from the five case study organizations. It covers financial outcomes, success factors, and an analysis of why the results occurred.

### 5.1 Financial Outcomes

**Table 4: Financial Performance by Organization**

| Organization (Sector) | FinOps Maturity | Cost Reduction | Efficiency Improvement |
|---|---|---|---|
| Org A (Technology) | Run (Mature) | 35% in 12 months | 42% resource allocation gain |
| Org B (Financial Services) | Walk (Developing) | 28% in 10 months | 38% collaboration improvement |
| Org C (Healthcare) | Walk (Developing) | 23% in 14 months | 35% forecast accuracy improvement |
| Org D (Retail) | Crawl (Early) | 18% in 8 months | 29% reduction in untagged spend |
| Org E (Manufacturing) | Run (Mature) | 33% in 11 months | 44% cost visibility improvement |
| **Average** | **Mixed** | **27.4% average** | **38–40% average** |

The results show a clear pattern: the more mature the FinOps practice, the better the financial outcome. Org A and Org E, both at the Run stage, achieved cost reductions of 35 and 33 percent, respectively. Org D, which was only at the Crawl stage, saved 18 percent. The average across all five organizations was 27.4 percent, which falls within the 23 to 35 percent range stated in the project objectives.

*Figure 1: Cloud Cost Reduction Achieved After FinOps Implementation — Org A (Tech) 35%, Org B (Finance) 28%, Org C (Healthcare) 23%, Org D (Retail) 18%, Org E (Mfg) 33%, Average 27.4%.*

### 5.2 Key Success Factors

Five factors consistently appeared across the organizations that achieved the best results. The first was executive support: in every organization with strong outcomes, senior leadership actively championed the FinOps initiative and made cost governance a visible priority. The second was real-time visibility. When teams could see their costs as they were happening rather than at the end of the month, they were far more likely to take action quickly. The third was resource tagging. Organizations that achieved more than 85 percent tagging coverage had significantly lower idle resource costs compared to those below 60 percent coverage. The fourth was the FinOps champion role; having a dedicated person within each engineering team who understood both cloud technology and financial goals made it much easier to close the gap between the two functions. The fifth was consistent review cycles.

### 5.3 Why the Results Improved

The cost reductions happened for three main reasons. On the technical side, teams switched from on-demand pricing to reserved instances for predictable workloads, rightsized their computing resources, and automated the cleanup of unused services. On the organizational side, giving engineering teams real-time visibility of their own costs changed their behavior because they could now see the direct financial impact of the resources they provisioned. On the cultural side, the monthly joint reviews between engineering and finance created a sense of shared ownership that had not existed before. Before FinOps was adopted, fourteen out of eighteen interview participants said that finance teams only received cloud cost reports monthly or quarterly. After implementing the governance model, cost anomalies were flagged within hours and resolved quickly.

---

## 6. Conclusion and Future Scope

### 6.1 Summary

This project examined how FinOps can be implemented as a cloud cost governance framework that connects engineering and finance teams. Through a study of five organizations using a mixed-methods approach, the project developed a hub-and-spoke governance model and measured its financial and organizational impact.

### 6.2 Key Findings

Four main findings came out of this work. First, FinOps adoption leads to real cost savings: the organizations in this study reduced cloud costs by an average of 27.4 percent, with the most mature implementations reaching over 30 percent. Second, FinOps maturity matters; organizations at higher maturity levels consistently achieved better results, confirming that FinOps requires long-term commitment rather than a short project. Third, collaboration between engineering and finance is just as important as technical tools. The organizations that invested in shared dashboards, regular joint meetings, and embedded FinOps champions saw the biggest efficiency gains. Fourth, FinOps does not work without cultural change. Technology alone cannot fix the problem if the organization has not built shared responsibility and accountability into how teams operate.

### 6.3 Practical Relevance

The governance model in this project is practical and can be applied in different types of organizations. Companies that are just starting with FinOps can use the Crawl phase as a structured entry point. Those already doing some optimization can use the Walk phase guidance to accelerate. Organizations at the Run stage can use the model to embed FinOps into their annual financial planning and automate governance across their infrastructure. The hub-and-spoke structure is particularly useful for organizations with multiple engineering teams who need consistent standards without being micromanaged.

### 6.4 Future Scope

Several areas are worth exploring in future research. First, applying machine learning and AI to FinOps governance could make the model smarter over time. Predictive cost models could flag likely overspending before it happens, and automated recommendation engines could continuously optimize cloud usage without manual intervention. Second, as AI and IoT workloads grow, they create very different cost patterns compared to traditional cloud services. GPU compute for AI training is extremely expensive and unpredictable, while IoT data ingestion generates constant small costs that add up quickly. Future research should look at how FinOps governance models need to adapt for these environments. Third, longer studies covering three to five years would give a better picture of whether the cost reductions are sustained over time or whether they fade as organizations become less focused on governance. Research in multi-cloud environments, where cost data has to be combined across different providers, would also be valuable as most large organizations now operate across more than one cloud platform.

---

## References

- Amazon Web Services. (2022). *AWS well-architected framework: Cost optimization pillar.* Amazon Web Services, Inc. https://docs.aws.amazon.com/wellarchitected/latest/cost-optimization-pillar/welcome.html
- Bhartiya, S. (2020). *FinOps: Cloud financial management.* Towards Data Science. https://towardsdatascience.com/finops-cloud-financial-management
- Brunnhofer, M., Dobler, T., & Schuster, T. (2021). Cloud governance frameworks and financial accountability: A systematic review. *Journal of Cloud Computing*, 10(1), 1–18.
- FinOps Foundation. (2023). *State of FinOps 2023.* FinOps Foundation. https://data.finops.org
- Flexera. (2023). *2023 state of the cloud report.* Flexera Software LLC. https://www.flexera.com/blog/cloud/cloud-computing-trends-flexera-2023-state-of-the-cloud-report/
- Gartner. (2022). *Gartner forecasts worldwide public cloud end-user spending to reach nearly $600 billion in 2023.* Gartner, Inc.
- Google Cloud. (2022). *Google Cloud architecture framework: Cost optimization.* Google LLC. https://cloud.google.com/architecture/framework/cost-optimization
- HashiCorp. (2022). *HashiCorp state of cloud strategy survey 2022.* HashiCorp, Inc. https://www.hashicorp.com/state-of-the-cloud
- Mell, P., & Grance, T. (2011). *The NIST definition of cloud computing.* Special Publication 800-145. National Institute of Standards and Technology.
- Microsoft. (2023). *Cost optimization design principles: Azure well-architected framework.* Microsoft Corporation. https://learn.microsoft.com/en-us/azure/well-architected/cost-optimization/principles
- Sharma, A., & Singh, H. (2022). A systematic review of cloud cost optimization techniques and challenges. *International Journal of Advanced Computer Science and Applications*, 13(2), 112–125.
- Storment, J. R., & Fuller, M. (2019). *Cloud FinOps: Collaborative, real-time cloud financial management.* O'Reilly Media.

---

## Appendices

### Appendix A: Interview Participant Profile

Eighteen practitioners participated in the semi-structured interviews. Their roles included six FinOps engineers, four cloud architects, three CFOs and finance directors, three DevOps leads, and two senior product managers. They came from organizations across technology (5), retail (3), healthcare (3), financial services (4), and manufacturing (3). Interview length averaged 52 minutes, and all sessions were recorded with participant consent and transcribed for thematic coding in NVivo.

### Appendix B: FinOps Maturity Self-Assessment Checklist

- **Crawl:** Cost monitoring is enabled across all cloud accounts. Mandatory tags are defined and partially enforced. Engineering and finance teams hold their first joint review.
- **Walk:** Tagging compliance exceeds 80 per cent. Reserved instance purchases follow a defined procurement process. Monthly cost reviews include action items with named owners. Showback reports are published to product teams.
- **Run:** Anomaly alerts are integrated into engineering on-call workflows. Budget guardrails block deployments that exceed approved thresholds. Unit-economic metrics (cost per request, cost per transaction) are reported to leadership. FinOps is part of the annual planning cycle.

### Appendix C: Sample Tagging Standard

Every cloud resource provisioned at the case organisations was required to carry the following minimum tags: Owner (email of the responsible engineer), CostCenter (finance code for chargeback), Environment (dev, staging, prod), Application (logical service name), and ExpiryDate (planned decommission date for non-production resources). Tags were enforced at provisioning time through Terraform modules and at the cloud provider level through AWS Service Control Policies, Azure Policy, and GCP Organisation Policies.
