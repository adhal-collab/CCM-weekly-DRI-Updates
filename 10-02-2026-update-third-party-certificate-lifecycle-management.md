# CCM Update - 10/2/2026
## Third-party Certificate Lifecycle Management (CCM) for CDN

---

## Release Timeline Overview

### Beta
- **Status**: Complete
- **Target Date**: 31 Jul 2025

### LA (Limited Availability)
- **Status**: Complete
- **Target Date**: 02 Jan 2026

### GA (General Availability)
- **Status**: At Risk for 30 November 2026
- **Target Date**: 30 Nov 2026

---

## Customer Engagement (At Risk)

### Customer Adoption Report
**Customer Adoption Metrics:**
- Total certificates: **610**
- Certs with end-end workflow exercised: **209** (200 is the exit criteria)

### Dashboard
- Target List of Customers for Cert Lineage
- **Note**: There is no lineage usage as of now
- Product Management is continuing to work on customer on-boarding

---

## Overall Status
**⚠️ At Risk for 30 November 2026**

---

## Key Milestones and Risks

### Certificate Lineage
- **Status**: Released
- **Target Date**: 24 September 2026
- **Completion**: Certificate Lineage was enabled in production for all customers on 24 Sep 2026

**Risks:**
- SRE indicated risk of alerting readiness; updated runbooks for edge case remediation
- **Mitigation**: Risks being addressed with an end date of 6 October 2026

**Execution Timeline:**
- **6 October**: Follow up on deciding when to deprecate v1 API support
- **6 October**: SRE to complete deployment of all major alerting
- **9 October**: Newly identified MVP bugs discovered during qualification to be reported
- **30 October**: P3 and P4 bugs resolution target

**Completed Milestones:**
- Certificate Lineage enabled for all customers
- v1 and v2 API currently live in production

---

### Certificate Referencing
- **Status**: At Risk
- **Original Target**: 4 November 2026
- **Updated Target**: 12 November 2026

**Risks and Schedule Impact:**
- Testnet setup issues and integration challenges with downstream components have impacted SQA qualification
- Any impact to the schedule will be evaluated by next update
- Currently estimated release date for CCM components: **9 Nov 2026**
- Target Ghost release 22.7.1 is still scheduled for 11/12 (delay unrelated to CCM changes)
- **Note**: This schedule change does not impact the overall GA date

**Execution Timeline:**
- **2 November 2026**: CPS Engineering development and qualification completion
- **12 November 2026**: Ghost World deployment
- **14 November 2026**: End to end post production testing

**Completed Milestones:**
- SQA completed verification of deploying cert reference file on ghost sandbox and tower channels
- Delivery SQA completed initial round of functional testing on Ghost sandbox
- Cryptoserver release confirmed to be in October 2026
- Redshirt development complete

---

## Operational Risks

### CPS SRE Risk: Retention Window
- **Risk**: The available retention window may be insufficient
- **Issue**: Pulsar team indicated that Lighthouse DB is not FedRAMP compliant
- **Mitigation**: CPS SRE will pursue scraping Prometheus and populating Lighthouse DB
- **Action**: CTG Compliance ticket raised by SRE to obtain approval for data export
- **Target Date**: 6 October 2026

---

## Product Scope

### Terraform (External Dependency)
- **Status**: On Track
- **Target Date**: 28 Oct 2026
- **Lead**: Lukasz Kowalski
- **Details**: Cert Lineage terraform support for happy paths to be available 30 Sep 2026; complete support to be released by 31 Oct 2026

### Object Move Tool (External Dependency)
- **Status**: Complete
- **Target Date**: 17 Mar 2026
- **Lead**: Sean McIntyre
- **Details**: Ticket StoryIDZ-7842 - Support custom CCM certificates move in Object move tool (Closed)

### Tower (External Dependency)
- **Status**: On Track
- **Target Date**: 30 Sep 2026
- **Lead**: Geir Nerboe
- **Details**: Production channels to be created by October 26

### Ghost (External Dependency)
- **Status**: At Risk
- **Target Date**: 12 Nov 2026
- **Lead**: Jessica Hook / Tyler Dietz
- **Details**:
  - Redshirt development complete
  - Changes to go out with Ghost 22.7.1, world deployed on 02 Nov 2026 → 12 Nov 2026
  - Delay unrelated to CCM
  - Follow up on cryptoserver release - 28 Sep 2026

### Product Design
- **Status**: Complete
- **Target Date**: 12 May 2026
- **Lead**: Ramya Narayana Murthy
- **Details**: PA design signed off

### System Design
- **Status**: Complete
- **Target Date**: 14 Aug 2026
- **Lead**: Ken Iwamoto

### CCM - Incremental Releases
- **Status**: At Risk
- **Lead**: Vaios Papadimitriou
- **Details**:
  - Cert lineage released and activated
  - Plan available for Cert referencing, release target - 02 Nov 2026

### DCM - Incremental Releases
- **Status**: At Risk
- **Lead**: Vaios Papadimitriou
- **Details**: Cert lineage released and activated

### UX Design
- **Status**: Complete
- **Target Date**: 28 Aug 2026
- **Lead**: Monika Pluta

### Documentation
- **Status**: On Track
- **Lead**: Katarzyna Poreba / Jakub Podsiadlo
- **Details**:
  - Cert referencing documentation to be released with PM 26.9
  - Cert lineage PM and API documentation released

### SRE - Incremental Releases
- **Status**: At Risk
- **Lead**: Tingshan Huang / Nathan Murphree
- **Details**:
  - Risk of not having adequate retention window
  - CTG Compliance ticket raised, follow up on 6 Oct 2026

### Property Manager
- **Status**: On Track
- **Target Date**: 27 Oct 2026
- **Lead**: Saurabh Agrawal
- **Details**:
  - Cert Lineage deployed to production and enabled
  - Change for explicit promotion scheduled to go out with PM 26.9 on 27 Oct 2026

### End to End SQA
- **Status**: On Track
- **Lead**: Gaurav Saxena
- **QA Status & Blockers**: Testing faces consecutive blocking issues; initial downstream configuration delays and CPS integration bug for Ghost resolved. Additional blockers being worked out.
- **Schedule Impact**: The 2026-11-02 QA deadline is at risk and expected to shift to 2026-11-09, with confirmed timelines due by 2026-10-07 EOD.

---

**Last Updated**: October 2, 2026
