# FundTrace
### Follow the Money. Verify the Impact.

**FundTrace** is a blockchain-based public financial transparency and accountability platform designed to improve how government funds are recorded, tracked, and audited.

The platform aims to provide a tamper-evident record of government financial activities, including budget allocations, fund transfers, public expenditure, and development project financing. By maintaining a shared ledger among authorized institutions and providing a public transparency portal, FundTrace seeks to make government financial information more accessible, traceable, and verifiable.

FundTrace is designed to help answer a fundamental question:

**Where does public money come from, where does it go, and how is it used?**

---

## Table of Contents

- [Problem Statement](#problem-statement)
- [Proposed Solution](#proposed-solution)
- [Objectives](#objectives)
- [Core Features](#core-features)
- [How It Works](#how-it-works)
- [System Architecture](#system-architecture)
- [Blockchain Approach](#blockchain-approach)
- [User Roles](#user-roles)
- [Financial Record Model](#financial-record-model)
- [Security and Transparency](#security-and-transparency)
- [Proposed Technology Stack](#proposed-technology-stack)
- [Development Roadmap](#development-roadmap)
- [Expected Impact](#expected-impact)
- [Limitations and Considerations](#limitations-and-considerations)
- [Project Status](#project-status)
- [Contributing](#contributing)
- [License](#license)

---

## Problem Statement

Governments manage substantial amounts of money collected through taxes, grants, loans, donations, and other public revenue sources. These funds are distributed across ministries, departments, local authorities, public institutions, and development projects.

Despite existing financial management and auditing systems, tracking the movement of funds across multiple institutions can be challenging.

Financial information may be distributed across disconnected systems, making it difficult to establish a complete picture of how money moves through the public sector.

These challenges can contribute to:

- Limited public visibility into government financial transactions.
- Difficulty tracing funds from their original sources to their final destinations.
- Delays in financial reconciliation and auditing.
- Challenges identifying discrepancies between approved budgets and recorded expenditure.
- Limited accessibility of financial information to citizens.
- Difficulties verifying whether recorded expenditure corresponds to actual payments and project activities.

Traditional centralized databases can provide effective financial record-keeping, but their reliability depends on access controls, institutional governance, audit mechanisms, and the integrity of their operators.

FundTrace explores how blockchain technology can strengthen the integrity and traceability of financial records while enabling authorized institutions to share a consistent transaction history.

## Proposed Solution

FundTrace proposes a permissioned blockchain network that maintains a shared, tamper-evident record of government financial activities.

Authorized institutions will be able to submit financial records according to their assigned permissions. Transactions will undergo validation before being committed to the ledger.

The system will associate financial transactions with relevant budgets, institutions, funding sources, and projects, allowing users to follow the movement of funds across the government financial system.

A public transparency portal will present information classified as publicly accessible, enabling citizens and other stakeholders to examine government financial activities without requiring direct access to the underlying administrative systems.

The platform will combine blockchain-backed records with conventional application services, financial data management, document storage, and verification mechanisms.

**The goal is not merely to record government transactions, but to make their financial history traceable and independently auditable.**

---

## Objectives

FundTrace aims to:

1. **Improve financial transparency:** Make publicly disclosable government financial records easier to access and understand.
2. **Enable fund traceability:** Connect financial transactions so users can follow money across institutions and projects.
3. **Strengthen accountability:** Maintain an auditable history of financial activities and their authorizations.
4. **Support financial auditing:** Help auditors examine transaction histories, investigate discrepancies, and reconcile financial records.
5. **Improve public oversight:** Enable citizens to monitor government expenditure and access information about publicly funded projects.
6. **Reduce information fragmentation:** Establish a shared financial record across participating institutions.
7. **Improve verification:** Associate transactions with supporting evidence and confirmations from relevant financial systems.

---

## Core Features

The following features define the proposed platform. Their implementation status will depend on the development stage.

### 1. Government Financial Record Management

Maintain structured records of government financial activities, including:

- Public revenue and funding receipts.
- Approved budgets and budget revisions.
- Budget allocations to ministries and departments.
- Transfers between authorized government institutions.
- Payments to contractors, suppliers, and other recipients.
- Recorded public expenditure.
- Financial adjustments, reversals, and corrections.

Each record will have a unique identifier, a timestamp, a transaction type, and references to relevant financial entities.

### 2. Budget Allocation Tracking

Track how approved budgets are distributed across government institutions and spending categories.

Users with the appropriate permissions will be able to examine:

- Original budget allocations.
- Approved budget revisions.
- Amounts committed to expenditure.
- Recorded transfers and payments.
- Reported expenditure.
- Remaining available budget, where sufficient verified information exists.

The system should distinguish between a budget authorization and money that has actually been transferred or spent.

### 3. Fund Flow Tracking

Allow users to trace financial movements between institutions and destinations.

For example:

```text
Government Revenue
        |
        v
   National Treasury
        |
        v
   Ministry of Health
        |
        v
    District Council
        |
        v
 Hospital Construction
        |
        +------------------+
        |                  |
        v                  v
   Contractor A       Supplier B
```

Each connection represents a recorded financial event rather than an assumption that money physically moved.

Users will be able to inspect the details and verification status of individual transactions.

Where the underlying financial evidence is available, the system can distinguish between recorded allocations, confirmed payments, and independently verified expenditure.

### 4. Public Transparency Dashboard

Provide a public-facing dashboard displaying financial information approved for public disclosure.

Potential dashboard indicators include:

- Total approved government budgets.
- Recorded government revenue.
- Allocations by ministry or department.
- Recorded expenditure by financial period.
- Transfers between public institutions.
- Funding associated with development projects.
- Projects with available financial records.
- Transactions awaiting confirmation or verification.

The dashboard will support searches and filters by institution, project, transaction type, financial year, and other relevant categories.

Financial indicators will clearly identify their reporting periods, data sources, and verification status.

### 5. Project Financial Monitoring

Connect development projects to their associated budgets, funding sources, allocations, transfers, and expenditure records.

Each project may include:

- Project identification number.
- Project name and description.
- Responsible government institution.
- Approved budget.
- Funding sources.
- Recorded financial transactions.
- Contract and procurement references.
- Supporting documents.
- Project milestones and reported progress.
- Audit findings and verification status.

This feature will help users understand the financial history of a project without confusing financial expenditure with physical project completion.

### 6. Audit and Verification Tools

Provide authorized auditors with tools for examining financial records and identifying inconsistencies.

Potential capabilities include:

- Transaction history inspection.
- Verification of ledger records.
- Budget-to-expenditure reconciliation.
- Detection of duplicate transaction references.
- Identification of expenditure exceeding approved allocations.
- Review of supporting financial documents.
- Recording of audit findings.
- Tracking the resolution of identified discrepancies.

Automated alerts will identify records requiring further investigation. An alert will not, by itself, establish fraud or misconduct.

### 7. Role-Based Access Control

Restrict administrative operations according to organizational roles and assigned permissions.

For example, an institution may be permitted to submit transactions associated with its own financial activities without being authorized to approve its own submissions or modify another institution's records.

Sensitive operations may require multiple approvals.

### 8. Transaction Verification

Provide mechanisms for verifying whether a financial record corresponds to an event in the underlying financial system.

Possible verification sources include:

- Treasury and government financial management systems.
- Bank payment confirmations.
- Official payment references.
- Approved invoices and payment vouchers.
- Supporting documents.
- Independent audit records.

The availability of these integrations will depend on the participating institutions and the interfaces they provide.

### 9. Audit Trail and Record Corrections

Maintain a history of submitted, approved, rejected, and corrected financial records.

Committed blockchain records should not be silently overwritten or deleted.

Where an error is identified, the system should record a correction or reversal that references the original transaction and explains the reason for the change.

This preserves the historical context needed for auditing.

---

## How It Works

The proposed transaction lifecycle consists of the following stages.

### Step 1: Register the Financial Activity

An authorized institution submits a financial record through the application.

The record identifies the financial activity, amount, relevant institutions, transaction type, and associated budget or project.

### Step 2: Validate the Submission

The application checks the submission against applicable business rules.

Validation may include:

- Confirming the submitting institution's identity.
- Checking its authorization to perform the operation.
- Verifying required fields.
- Checking transaction references for duplicates.
- Confirming applicable budget limits.
- Validating approval requirements.
- Checking available supporting evidence.

Passing application validation does not automatically prove that the underlying payment occurred.

### Step 3: Obtain Required Approvals

Transactions requiring additional authorization are routed to the appropriate officials.

Depending on the transaction type, approval may involve multiple authorized parties.

The application records the approval history and the identities associated with each approval.

### Step 4: Commit the Transaction

Once the required validation and approval conditions are satisfied, the transaction is submitted to the permissioned blockchain network.

The network validates the transaction according to its configured rules and consensus process.

Successfully committed transactions become part of the ledger's historical record.

### Step 5: Associate Supporting Evidence

The system links the transaction to relevant supporting evidence, such as payment confirmations, invoices, or authorization documents.

Documents containing sensitive information may be stored outside the blockchain.

Where appropriate, cryptographic hashes can be recorded on the ledger to help detect changes to the referenced documents.

A matching hash demonstrates that a document matches the content previously hashed; it does not establish that the document is authentic or factually correct.

### Step 6: Publish Permitted Information

The application makes approved public information available through the transparency portal.

Private information remains restricted according to the applicable access-control and disclosure rules.

### Step 7: Enable Tracking and Auditing

Users can follow related transactions, inspect their verification status, and examine the available supporting evidence.

Auditors can reconcile records against authoritative financial sources and document their findings.

---

## System Architecture

FundTrace is intended to use a layered architecture that separates the user interface, application logic, financial data management, and blockchain network.

```text
                  USERS
                    |
        +-----------+-----------+
        |           |           |
   Government    Auditors     Citizens
        |           |           |
        +-----------+-----------+
                    |
                    v
          WEB APPLICATION
            Next.js / UI
                    |
                    v
              BACKEND API
          Authentication & RBAC
          Financial Business Rules
          Validation & Approvals
          Transaction Management
                    |
          +---------+----------+
          |         |          |
          v         v          v
      PostgreSQL  Blockchain  Document
      Application   Gateway    Storage
        Data          |          |
                      v          |
             PERMISSIONED        |
             BLOCKCHAIN NETWORK  |
                      |          |
          +-----------+---------+|
          |           |          |
          v           v          v
      Government   Independent  Verification
         Nodes       Auditors   & Evidence
```

*This diagram represents a conceptual architecture. The final implementation may change as the team establishes its requirements and technology choices.*

### Architectural Components

**Frontend**

The frontend provides the administrative interface, financial dashboards, project pages, and public transparency portal.

**Backend API**

The backend enforces business rules, handles authentication and authorization, validates submissions, coordinates approvals, and communicates with the blockchain network.

**PostgreSQL Database**

The application database stores searchable metadata, user accounts, organizational information, project details, and other operational records.

It can also maintain indexed representations of ledger events to support efficient searches and dashboard queries.

The database is not the authoritative source for blockchain transaction integrity; ledger records must remain independently verifiable.

**Blockchain Gateway**

The gateway connects the backend to the permissioned blockchain network. It submits transactions, retrieves ledger information, and handles relevant responses.

**Permissioned Blockchain Network**

Authorized organizations operate network nodes according to the agreed governance model.

The network maintains the shared ledger and validates transactions according to its consensus and authorization rules.

**Document Storage**

Supporting documents are stored separately from the blockchain where appropriate. Access controls protect sensitive documents, while cryptographic hashes can support integrity checks.

---

## Blockchain Approach

FundTrace is designed around a **permissioned blockchain**.

Unlike a public blockchain, where participation and transaction visibility may be broadly open, a permissioned network restricts participation according to defined identities, roles, and governance rules.

This approach is suitable for exploring collaboration between government institutions and independent organizations that need to share a trusted financial history while respecting legal and confidentiality requirements.

### Proposed Participants

The network may include:

- Government treasury or finance authorities.
- Participating ministries and departments.
- Authorized public financial institutions.
- Independent audit institutions.
- Approved development partners, where appropriate.

Citizens and other members of the public can access permitted information through the transparency portal without necessarily operating blockchain nodes.

### Candidate Technology: Hyperledger Fabric

[Hyperledger Fabric](https://hyperledger-fabric.readthedocs.io/) is a candidate blockchain framework for the project.

It provides permissioned identities, organizational membership, transaction endorsement policies, and a distributed ledger.

These capabilities could support a network in which multiple organizations participate in validating financial records.

The team should confirm the framework's suitability after evaluating the required deployment complexity, governance model, transaction volume, privacy requirements, and available development resources.

### What Should Be Stored on the Blockchain?

The ledger should contain the information necessary to establish a reliable financial history.

Potential on-chain data includes:

- Unique transaction identifiers.
- Transaction types.
- Financial amounts and currencies.
- Relevant institutional identifiers.
- References to budgets and projects.
- Timestamps and sequence information.
- Authorization or endorsement references.
- References to supporting evidence.
- Cryptographic hashes of selected documents.
- References to correction and reversal transactions.

The final schema must account for privacy, confidentiality, data retention requirements, and the operational cost of storing information on the ledger.

### What Should Remain Off-Chain?

Large documents, sensitive personal information, confidential procurement details, and other information that does not need to be replicated across the network should generally remain in appropriately protected storage.

The ledger can retain references and integrity proofs where suitable.

**Important:** A permissioned blockchain does not automatically guarantee transparency or independence. Its trustworthiness depends on the organizations operating it, the distribution of control, the consensus configuration, and the effectiveness of its governance arrangements.

---

## User Roles

FundTrace will support different user roles according to their responsibilities.

| Role | Responsibilities |
|---|---|
| Government Financial Administrator | Manages authorized financial records and institutional information. |
| Budget Officer | Registers budgets, allocations, and approved revisions. |
| Transaction Approver | Reviews and authorizes transactions within assigned limits. |
| Auditor | Examines records, verifies evidence, and documents audit findings. |
| Development Partner | Monitors relevant funding commitments, disbursements, and project records. |
| Contractor or Supplier | Accesses permitted contract, invoice, and payment information. |
| Public User | Views publicly available financial records and project information. |
| System Administrator | Manages application configuration, accounts, and technical operations. |

Permissions should be assigned according to the principle of least privilege.

Where practical, transaction submission, approval, and independent audit responsibilities should be separated to reduce conflicts of interest.

---

## Financial Record Model

A reliable implementation must distinguish between different financial events.

FundTrace should not treat every recorded amount as money that has already been spent.

### Proposed Financial Event Types

| Event Type | Meaning |
|---|---|
| Revenue Receipt | Money received by a government entity. |
| Budget Approval | Authorization to spend up to a specified amount for an approved purpose. |
| Budget Revision | An approved change to a budget. |
| Fund Allocation | Distribution of budget authority or funding to an institution or purpose. |
| Commitment | A financial obligation, such as an approved contract or purchase order. |
| Transfer | A recorded movement of funds between accounts or institutions. |
| Payment | A payment recorded by the relevant financial system. |
| Expenditure Verification | Confirmation that expenditure meets the defined verification requirements. |
| Reversal | A record reversing the accounting effect of an earlier transaction. |
| Correction | An additional record correcting an identified error. |

The exact definitions and accounting treatment should follow the financial rules adopted by participating institutions.

### Example Transaction

```json
{
  "transactionId": "FT-TXN-2026-0001",
  "transactionType": "PAYMENT",
  "projectId": "FT-PRJ-2026-001",
  "reportingInstitution": "MINISTRY-001",
  "sourceInstitution": "TREASURY-001",
  "destinationInstitution": "SUPPLIER-042",
  "amount": "25000000.00",
  "currency": "MWK",
  "referenceNumber": "PAY-REF-001",
  "recordedAt": "2026-10-17T10:00:00Z",
  "verificationStatus": "PENDING",
  "evidenceReference": "DOC-REF-001",
  "correctionOf": null
}
```

This is an illustrative data structure, not a finalized schema.

The example represents a recorded payment submission with pending verification. It does not establish that a real payment occurred.

A production implementation should use appropriate monetary precision, validate currency and transaction rules, and define authoritative timestamp and identity requirements.

---

## Security and Transparency

Security and transparency must be considered together.

Financial information should be publicly accessible where appropriate, while sensitive information remains protected.

FundTrace will require controls in the following areas.

### Identity and Authentication

- Authenticate users before permitting restricted operations.
- Associate submissions and approvals with verified institutional identities.
- Apply role-based access control.
- Protect administrative accounts with appropriate authentication safeguards.

### Transaction Authorization

- Require authorization for sensitive financial operations.
- Apply transaction-specific approval policies.
- Record the relevant authorization and endorsement history.
- Separate responsibilities where appropriate.

### Data Integrity

- Use blockchain-backed transaction history to make unauthorized retrospective alteration more detectable.
- Use cryptographic hashes to support document integrity checks.
- Preserve corrections and reversals as additional records.
- Maintain verifiable links between related financial events.

### Privacy and Confidentiality

- Classify financial information according to disclosure requirements.
- Restrict confidential records to authorized users.
- Avoid storing unnecessary personal or sensitive information on an immutable ledger.
- Apply appropriate retention, encryption, and access-control policies to off-chain documents.

### Monitoring and Auditing

- Record security-relevant administrative actions.
- Monitor failed authorization attempts and suspicious activity.
- Support independent verification and financial reconciliation.
- Maintain procedures for incident response and key management.

### Limits of Blockchain

Blockchain technology protects the integrity of information after it is recorded under the network's rules. It does not independently prove that the information entered into the system was true.

For example, a fraudulent invoice can still be recorded unless validation and approval mechanisms detect the problem.

Similarly, a transaction recorded on the blockchain does not independently prove that a bank transfer occurred.

FundTrace must therefore combine ledger integrity with reliable source data, independent verification, and effective institutional governance.

---

## Proposed Technology Stack

The following technologies are candidates for the initial implementation. Final selections should be confirmed after a technical feasibility assessment.

| Component | Proposed Technology | Purpose |
|---|---|---|
| Frontend | Next.js | Administrative interfaces and public dashboards. |
| Programming Language | TypeScript | Shared typing across frontend and backend services. |
| Backend | NestJS | API development, validation, authorization, and business logic. |
| Application Database | PostgreSQL | Structured operational data and efficient queries. |
| Blockchain Framework | Hyperledger Fabric | Permissioned distributed ledger. |
| Authentication | OpenID Connect-compatible identity provider | User authentication and identity integration. |
| Document Storage | S3-compatible object storage | Storage of supporting financial documents. |
| API Documentation | OpenAPI / Swagger | API discovery and testing. |
| Containerization | Docker | Reproducible development and deployment environments. |
| Testing | Jest and appropriate integration-testing tools | Unit, integration, and application testing. |

The blockchain framework and supporting infrastructure should be evaluated before implementation begins.

A conventional database with cryptographically verifiable audit records should also be considered as a baseline, so the team can demonstrate which requirements genuinely benefit from a distributed ledger.

---

## Development Roadmap

FundTrace can be developed incrementally.

The following roadmap describes proposed milestones, not completed functionality.

### Phase 1: Requirements and System Design

- Define the financial events to be recorded.
- Establish transaction validation and approval rules.
- Identify participating organizations and their responsibilities.
- Design the database schema.
- Define the blockchain governance model.
- Establish data privacy and public disclosure requirements.
- Create system architecture diagrams.

**Deliverable:** Approved system specification and architecture.

### Phase 2: Core Application

- Implement user authentication.
- Develop organizational and role management.
- Implement project and financial record registration.
- Build budget allocation and transaction management.
- Create initial administrative interfaces.
- Implement basic financial validation.

**Deliverable:** A functional application with a structured financial record model.

### Phase 3: Blockchain Integration

- Deploy a development blockchain network.
- Configure organizational identities.
- Implement transaction submission and validation.
- Record approved financial events on the ledger.
- Implement transaction history retrieval.
- Associate transactions with supporting evidence.
- Test transaction integrity and authorization rules.

**Deliverable:** A working prototype with blockchain-backed financial records.

### Phase 4: Public Transparency Portal

- Develop the public dashboard.
- Implement project and transaction search.
- Build fund-flow visualization.
- Display budgets, transfers, and expenditure separately.
- Add transaction verification indicators.
- Implement public disclosure controls.

**Deliverable:** A public-facing financial transparency portal.

### Phase 5: Auditing and Reconciliation

- Implement budget-to-expenditure reconciliation.
- Develop discrepancy detection.
- Add audit findings and investigation workflows.
- Implement financial record corrections and reversals.
- Test the platform against simulated financial inconsistencies.

**Deliverable:** An auditing and financial verification module.

### Phase 6: Evaluation and Deployment

- Conduct security testing.
- Evaluate transaction throughput and latency.
- Test role and organizational isolation.
- Assess recovery and backup procedures.
- Validate the accuracy of financial calculations.
- Demonstrate the complete transaction lifecycle.
- Document deployment and maintenance procedures.

**Deliverable:** An evaluated prototype ready for demonstration or a controlled pilot.

---

## Expected Impact

FundTrace aims to improve public financial accountability through several mechanisms.

**Improved traceability**

Financial records can be linked across institutions, budgets, and projects, making it easier to reconstruct the history of recorded fund movements.

**Stronger auditability**

An append-only transaction history can help auditors examine financial changes and investigate inconsistencies.

**Better public access**

A public transparency portal can make relevant government financial information easier for citizens and other stakeholders to explore.

**Improved financial reconciliation**

Structured records and validation rules can help identify discrepancies between approved budgets, recorded transfers, and reported expenditure.

**Greater institutional collaboration**

A shared ledger can provide participating organizations with a consistent history of approved financial events.

**Better-informed oversight**

Auditors, development partners, and citizens can use the available information to ask more specific questions about public expenditure and project delivery.

These are intended benefits. Their realization will depend on data quality, institutional participation, independent verification, and effective implementation.

---

## Limitations and Considerations

FundTrace is a financial transparency platform, not a substitute for sound financial governance.

Several limitations must be addressed during development.

1. **Input accuracy:** Blockchain cannot independently establish whether submitted financial information is true.
2. **External payment verification:** Confirming a real-world payment requires reliable evidence from the relevant financial system or an authorized verification process.
3. **Institutional adoption:** The platform depends on participating institutions submitting complete and timely information.
4. **Network governance:** The participating organizations must agree on node ownership, transaction validation, access permissions, and dispute resolution.
5. **Privacy:** Not every government financial record should necessarily be made public.
6. **Accounting accuracy:** Budget allocations, transfers, commitments, and expenditure must be represented separately to prevent misleading financial totals.
7. **Operational resilience:** The system requires appropriate backups, monitoring, recovery procedures, and security controls.
8. **Independent oversight:** A permissioned network controlled by a single institution may not provide the same assurance as one governed by multiple independent participants.

These considerations will inform the platform's architecture and evaluation criteria.

---

## Project Status

**Status:** Proposed / In Development

FundTrace is being designed as a prototype for blockchain-based government financial transparency and accountability.

The initial development effort will focus on establishing the financial data model, implementing the core application, and evaluating a permissioned blockchain architecture.

Features listed in this document describe the intended system and should not be interpreted as already implemented unless confirmed by the current source code and project documentation.

---

## Contributing

Contributions are welcome as the project develops.

Potential areas of contribution include:

- Frontend development.
- Backend API development.
- Blockchain integration.
- Financial data modelling.
- Security and access-control design.
- Testing and validation.
- Documentation.
- User interface and accessibility improvements.

Before contributing, review the project's development guidelines and agreed technical architecture.

Detailed contribution instructions will be added as the repository structure and development workflow are established.

---

## License

The project's license has not yet been selected.

A license should be added after the project team agrees on the intended usage, distribution, and contribution terms.   v          v

&#x20;     PostgreSQL  Blockchain  Document

&#x20;     Application   Gateway    Storage

&#x20;       Data          |          |

&#x20;                     v          |

&#x20;            PERMISSIONED        |

&#x20;            BLOCKCHAIN NETWORK  |

&#x20;                     |          |

&#x20;         +-----------+---------+|

&#x20;         |           |          |

&#x20;         v           v          v

&#x20;     Government   Independent  Verification

&#x20;        Nodes       Auditors   \& Evidence

```



\*This diagram represents a conceptual architecture. The final implementation may change as the team establishes its requirements and technology choices.\*



\### Architectural Components



\*\*Frontend\*\*



The frontend provides the administrative interface, financial dashboards, project pages, and public transparency portal.



\*\*Backend API\*\*



The backend enforces business rules, handles authentication and authorization, validates submissions, coordinates approvals, and communicates with the blockchain network.



\*\*PostgreSQL Database\*\*



The application database stores searchable metadata, user accounts, organizational information, project details, and other operational records.



It can also maintain indexed representations of ledger events to support efficient searches and dashboard queries.



The database is not the authoritative source for blockchain transaction integrity; ledger records must remain independently verifiable.



\*\*Blockchain Gateway\*\*



The gateway connects the backend to the permissioned blockchain network. It submits transactions, retrieves ledger information, and handles relevant responses.



\*\*Permissioned Blockchain Network\*\*



Authorized organizations operate network nodes according to the agreed governance model.



The network maintains the shared ledger and validates transactions according to its consensus and authorization rules.



\*\*Document Storage\*\*



Supporting documents are stored separately from the blockchain where appropriate. Access controls protect sensitive documents, while cryptographic hashes can support integrity checks.



\---



\## Blockchain Approach



FundTrace is designed around a \*\*permissioned blockchain\*\*.



Unlike a public blockchain, where participation and transaction visibility may be broadly open, a permissioned network restricts participation according to defined identities, roles, and governance rules.



This approach is suitable for exploring collaboration between government institutions and independent organizations that need to share a trusted financial history while respecting legal and confidentiality requirements.



\### Proposed Participants



The network may include:



\- Government treasury or finance authorities.

\- Participating ministries and departments.

\- Authorized public financial institutions.

\- Independent audit institutions.

\- Approved development partners, where appropriate.



Citizens and other members of the public can access permitted information through the transparency portal without necessarily operating blockchain nodes.



\### Candidate Technology: Hyperledger Fabric



\[Hyperledger Fabric](https://hyperledger-fabric.readthedocs.io/) is a candidate blockchain framework for the project.



It provides permissioned identities, organizational membership, transaction endorsement policies, and a distributed ledger.



These capabilities could support a network in which multiple organizations participate in validating financial records.



The team should confirm the framework's suitability after evaluating the required deployment complexity, governance model, transaction volume, privacy requirements, and available development resources.



\### What Should Be Stored on the Blockchain?



The ledger should contain the information necessary to establish a reliable financial history.



Potential on-chain data includes:



\- Unique transaction identifiers.

\- Transaction types.

\- Financial amounts and currencies.

\- Relevant institutional identifiers.

\- References to budgets and projects.

\- Timestamps and sequence information.

\- Authorization or endorsement references.

\- References to supporting evidence.

\- Cryptographic hashes of selected documents.

\- References to correction and reversal transactions.



The final schema must account for privacy, confidentiality, data retention requirements, and the operational cost of storing information on the ledger.



\### What Should Remain Off-Chain?



Large documents, sensitive personal information, confidential procurement details, and other information that does not need to be replicated across the network should generally remain in appropriately protected storage.



The ledger can retain references and integrity proofs where suitable.



\*\*Important:\*\* A permissioned blockchain does not automatically guarantee transparency or independence. Its trustworthiness depends on the organizations operating it, the distribution of control, the consensus configuration, and the effectiveness of its governance arrangements.



\---



\## User Roles



FundTrace will support different user roles according to their responsibilities.



| Role | Responsibilities |

|---|---|

| Government Financial Administrator | Manages authorized financial records and institutional information. |

| Budget Officer | Registers budgets, allocations, and approved revisions. |

| Transaction Approver | Reviews and authorizes transactions within assigned limits. |

| Auditor | Examines records, verifies evidence, and documents audit findings. |

| Development Partner | Monitors relevant funding commitments, disbursements, and project records. |

| Contractor or Supplier | Accesses permitted contract, invoice, and payment information. |

| Public User | Views publicly available financial records and project information. |

| System Administrator | Manages application configuration, accounts, and technical operations. |



Permissions should be assigned according to the principle of least privilege.



Where practical, transaction submission, approval, and independent audit responsibilities should be separated to reduce conflicts of interest.



\---



\## Financial Record Model



A reliable implementation must distinguish between different financial events.



FundTrace should not treat every recorded amount as money that has already been spent.



\### Proposed Financial Event Types



| Event Type | Meaning |

|---|---|

| Revenue Receipt | Money received by a government entity. |

| Budget Approval | Authorization to spend up to a specified amount for an approved purpose. |

| Budget Revision | An approved change to a budget. |

| Fund Allocation | Distribution of budget authority or funding to an institution or purpose. |

| Commitment | A financial obligation, such as an approved contract or purchase order. |

| Transfer | A recorded movement of funds between accounts or institutions. |

| Payment | A payment recorded by the relevant financial system. |

| Expenditure Verification | Confirmation that expenditure meets the defined verification requirements. |

| Reversal | A record reversing the accounting effect of an earlier transaction. |

| Correction | An additional record correcting an identified error. |



The exact definitions and accounting treatment should follow the financial rules adopted by participating institutions.



\### Example Transaction



```json

{

&#x20; "transactionId": "FT-TXN-2026-0001",

&#x20; "transactionType": "PAYMENT",

&#x20; "projectId": "FT-PRJ-2026-001",

&#x20; "reportingInstitution": "MINISTRY-001",

&#x20; "sourceInstitution": "TREASURY-001",

&#x20; "destinationInstitution": "SUPPLIER-042",

&#x20; "amount": "25000000.00",

&#x20; "currency": "MWK",

&#x20; "referenceNumber": "PAY-REF-001",

&#x20; "recordedAt": "2026-10-17T10:00:00Z",

&#x20; "verificationStatus": "PENDING",

&#x20; "evidenceReference": "DOC-REF-001",

&#x20; "correctionOf": null

}

```



This is an illustrative data structure, not a finalized schema.



The example represents a recorded payment submission with pending verification. It does not establish that a real payment occurred.



A production implementation should use appropriate monetary precision, validate currency and transaction rules, and define authoritative timestamp and identity requirements.



\---



\## Security and Transparency



Security and transparency must be considered together.



Financial information should be publicly accessible where appropriate, while sensitive information remains protected.



FundTrace will require controls in the following areas.



\### Identity and Authentication



\- Authenticate users before permitting restricted operations.

\- Associate submissions and approvals with verified institutional identities.

\- Apply role-based access control.

\- Protect administrative accounts with appropriate authentication safeguards.



\### Transaction Authorization



\- Require authorization for sensitive financial operations.

\- Apply transaction-specific approval policies.

\- Record the relevant authorization and endorsement history.

\- Separate responsibilities where appropriate.



\### Data Integrity



\- Use blockchain-backed transaction history to make unauthorized retrospective alteration more detectable.

\- Use cryptographic hashes to support document integrity checks.

\- Preserve corrections and reversals as additional records.

\- Maintain verifiable links between related financial events.



\### Privacy and Confidentiality



\- Classify financial information according to disclosure requirements.

\- Restrict confidential records to authorized users.

\- Avoid storing unnecessary personal or sensitive information on an immutable ledger.

\- Apply appropriate retention, encryption, and access-control policies to off-chain documents.



\### Monitoring and Auditing



\- Record security-relevant administrative actions.

\- Monitor failed authorization attempts and suspicious activity.

\- Support independent verification and financial reconciliation.

\- Maintain procedures for incident response and key management.



\### Limits of Blockchain



Blockchain technology protects the integrity of information after it is recorded under the network's rules. It does not independently prove that the information entered into the system was true.



For example, a fraudulent invoice can still be recorded unless validation and approval mechanisms detect the problem.



Similarly, a transaction recorded on the blockchain does not independently prove that a bank transfer occurred.



FundTrace must therefore combine ledger integrity with reliable source data, independent verification, and effective institutional governance.



\---



\## Proposed Technology Stack



The following technologies are candidates for the initial implementation. Final selections should be confirmed after a technical feasibility assessment.



| Component | Proposed Technology | Purpose |

|---|---|---|

| Frontend | Next.js | Administrative interfaces and public dashboards. |

| Programming Language | TypeScript | Shared typing across frontend and backend services. |

| Backend | NestJS | API development, validation, authorization, and business logic. |

| Application Database | PostgreSQL | Structured operational data and efficient queries. |

| Blockchain Framework | Hyperledger Fabric | Permissioned distributed ledger. |

| Authentication | OpenID Connect-compatible identity provider | User authentication and identity integration. |

| Document Storage | S3-compatible object storage | Storage of supporting financial documents. |

| API Documentation | OpenAPI / Swagger | API discovery and testing. |

| Containerization | Docker | Reproducible development and deployment environments. |

| Testing | Jest and appropriate integration-testing tools | Unit, integration, and application testing. |



The blockchain framework and supporting infrastructure should be evaluated before implementation begins.



A conventional database with cryptographically verifiable audit records should also be considered as a baseline, so the team can demonstrate which requirements genuinely benefit from a distributed ledger.



\---



\## Development Roadmap



FundTrace can be developed incrementally.



The following roadmap describes proposed milestones, not completed functionality.



\### Phase 1: Requirements and System Design



\- Define the financial events to be recorded.

\- Establish transaction validation and approval rules.

\- Identify participating organizations and their responsibilities.

\- Design the database schema.

\- Define the blockchain governance model.

\- Establish data privacy and public disclosure requirements.

\- Create system architecture diagrams.



\*\*Deliverable:\*\* Approved system specification and architecture.



\### Phase 2: Core Application



\- Implement user authentication.

\- Develop organizational and role management.

\- Implement project and financial record registration.

\- Build budget allocation and transaction management.

\- Create initial administrative interfaces.

\- Implement basic financial validation.



\*\*Deliverable:\*\* A functional application with a structured financial record model.



\### Phase 3: Blockchain Integration



\- Deploy a development blockchain network.

\- Configure organizational identities.

\- Implement transaction submission and validation.

\- Record approved financial events on the ledger.

\- Implement transaction history retrieval.

\- Associate transactions with supporting evidence.

\- Test transaction integrity and authorization rules.



\*\*Deliverable:\*\* A working prototype with blockchain-backed financial records.



\### Phase 4: Public Transparency Portal



\- Develop the public dashboard.

\- Implement project and transaction search.

\- Build fund-flow visualization.

\- Display budgets, transfers, and expenditure separately.

\- Add transaction verification indicators.

\- Implement public disclosure controls.



\*\*Deliverable:\*\* A public-facing financial transparency portal.



\### Phase 5: Auditing and Reconciliation



\- Implement budget-to-expenditure reconciliation.

\- Develop discrepancy detection.

\- Add audit findings and investigation workflows.

\- Implement financial record corrections and reversals.

\- Test the platform against simulated financial inconsistencies.



\*\*Deliverable:\*\* An auditing and financial verification module.



\### Phase 6: Evaluation and Deployment



\- Conduct security testing.

\- Evaluate transaction throughput and latency.

\- Test role and organizational isolation.

\- Assess recovery and backup procedures.

\- Validate the accuracy of financial calculations.

\- Demonstrate the complete transaction lifecycle.

\- Document deployment and maintenance procedures.



\*\*Deliverable:\*\* An evaluated prototype ready for demonstration or a controlled pilot.



\---



\## Expected Impact



FundTrace aims to improve public financial accountability through several mechanisms.



\*\*Improved traceability\*\*



Financial records can be linked across institutions, budgets, and projects, making it easier to reconstruct the history of recorded fund movements.



\*\*Stronger auditability\*\*



An append-only transaction history can help auditors examine financial changes and investigate inconsistencies.



\*\*Better public access\*\*



A public transparency portal can make relevant government financial information easier for citizens and other stakeholders to explore.



\*\*Improved financial reconciliation\*\*



Structured records and validation rules can help identify discrepancies between approved budgets, recorded transfers, and reported expenditure.



\*\*Greater institutional collaboration\*\*



A shared ledger can provide participating organizations with a consistent history of approved financial events.



\*\*Better-informed oversight\*\*



Auditors, development partners, and citizens can use the available information to ask more specific questions about public expenditure and project delivery.



These are intended benefits. Their realization will depend on data quality, institutional participation, independent verification, and effective implementation.



\---



\## Limitations and Considerations



FundTrace is a financial transparency platform, not a substitute for sound financial governance.



Several limitations must be addressed during development.



1\. \*\*Input accuracy:\*\* Blockchain cannot independently establish whether submitted financial information is true.

2\. \*\*External payment verification:\*\* Confirming a real-world payment requires reliable evidence from the relevant financial system or an authorized verification process.

3\. \*\*Institutional adoption:\*\* The platform depends on participating institutions submitting complete and timely information.

4\. \*\*Network governance:\*\* The participating organizations must agree on node ownership, transaction validation, access permissions, and dispute resolution.

5\. \*\*Privacy:\*\* Not every government financial record should necessarily be made public.

6\. \*\*Accounting accuracy:\*\* Budget allocations, transfers, commitments, and expenditure must be represented separately to prevent misleading financial totals.

7\. \*\*Operational resilience:\*\* The system requires appropriate backups, monitoring, recovery procedures, and security controls.

8\. \*\*Independent oversight:\*\* A permissioned network controlled by a single institution may not provide the same assurance as one governed by multiple independent participants.



These considerations will inform the platform's architecture and evaluation criteria.



\---



\## Project Status



\*\*Status:\*\* Proposed / In Development



FundTrace is being designed as a prototype for blockchain-based government financial transparency and accountability.



The initial development effort will focus on establishing the financial data model, implementing the core application, and evaluating a permissioned blockchain architecture.



Features listed in this document describe the intended system and should not be interpreted as already implemented unless confirmed by the current source code and project documentation.



\---



\## Contributing



Contributions are welcome as the project develops.



Potential areas of contribution include:



\- Frontend development.

\- Backend API development.

\- Blockchain integration.

\- Financial data modelling.

\- Security and access-control design.

\- Testing and validation.

\- Documentation.

\- User interface and accessibility improvements.



Before contributing, review the project's development guidelines and agreed technical architecture.



Detailed contribution instructions will be added as the repository structure and development workflow are established.



\---



\## License



The project's license has not yet been selected.



A license should be added after the project team agrees on the intended usage, distribution, and contribution terms.

