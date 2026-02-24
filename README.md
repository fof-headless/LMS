# Loan Management System (LMS) -- Module Explanation

This document explains each component of the Loan Management System flow
shown in the architecture diagram. It is structured based on the user
journey and operational lifecycle of a digital lending product.

------------------------------------------------------------------------



# 1. Acquisition & Marketing Module

## Purpose

Drives new user acquisition and tracks marketing performance.

### Components

**1. Campaign Tracking** - UTM tracking for source attribution\
- Channel performance metrics\
- CAC (Customer Acquisition Cost) tracking

**2. Referral System** - Agent referrals\
- Customer refer and earn programs\
- Commission payouts

**3. Free Loan Parameter Calculators** - EMI simulations\
- Interest previews\
- Tenure selection\
- Available on USSD, mobile app, and web

------------------------------------------------------------------------

# 2. Authentication Module

## Purpose

User identity creation and secure account access.

### Components

**1. OTP Verification** - Mobile number validation

**2. Device Fingerprinting** - Fraud detection\
- Multi‑account prevention

**3. PIN Setup** - Transaction authorization\
- Login authentication

------------------------------------------------------------------------

# 3. KYC & Compliance Module

## Purpose

Ensures regulatory compliance and user legitimacy.

### Components

**1. National ID Verification** - NIRA / OCR scanning\
- Document extraction

**2. Liveness Check** - Face match\
- Anti‑spoof detection

**3. Address Verification** - Geo‑mapping\
- Proof of residence

------------------------------------------------------------------------

# 4. Guarantor Module

## Purpose

Adds secondary repayment assurance.

### Components

-   Guarantor identity capture\
-   KYC verification\
-   Liability linking to borrower

------------------------------------------------------------------------

# 5. Financial Data Capture Module

## Purpose

Assesses borrower financial strength.

### Components

**1. Income & Financial Uploads** - Salary slips\
- Bank statements\
- Business documents

**2. Credit Bureau Checks** - Historical loans\
- Defaults\
- Credit score

**3. Mobile Money Transaction Reports** - Wallet inflows/outflows\
- Spending patterns

------------------------------------------------------------------------

# 6. Eligibility & Risk Engine

## Purpose

Core underwriting decision system.

### Functions

-   Credit scoring models\
-   Risk segmentation\
-   Interest rate assignment\
-   Loan limits calculation\
-   Tenure eligibility

Prefills last used borrower data for repeat loans.

------------------------------------------------------------------------

# 7. Loan Structuring Module

## Purpose

Defines final loan terms.

### Parameters

-   EMI amount\
-   Principal\
-   Interest\
-   Tenure selection

------------------------------------------------------------------------

# 8. Agreement & Verification Module

## Purpose

Captures legal consent.

### Components

-   Digital agreement signing\
-   OTP verification\
-   Multi factor validation

------------------------------------------------------------------------

# 9. Disbursement Module

## Purpose

Transfers funds to borrower.

### Channels

-   Mobile money wallets\
-   Banking rails\
-   Mobile apps

### Features

-   Retry logic\
-   Wallet validation\
-   Failure handling

------------------------------------------------------------------------

# 10. Loan Book Management

## Purpose

Official accounting record of all loans.

### Functions

-   Ledger creation\
-   Principal & interest tracking\
-   Regulatory reporting

Includes notification to central financial authorities where required.

------------------------------------------------------------------------

# 11. Audit Module

## Purpose

Ensures financial accuracy.

### Functions

-   Monthly reconciliation\
-   Ledger audits\
-   Disbursement vs repayment checks

------------------------------------------------------------------------

# 12. Notifications & Communication

## Purpose

Drives repayment behavior.

### Channels

-   Push notifications\
-   SMS\
-   WhatsApp\
-   IVR calls

### Use Cases

-   EMI reminders\
-   Due alerts\
-   Default warnings

------------------------------------------------------------------------

# 13. Recovery & Collections Module

## Purpose

Handles repayments and delinquency.

### 13.1 Auto Collections

-   Wallet auto debit\
-   Merchant settlements\
-   Deposit sweeps

------------------------------------------------------------------------

# 14. Default Management

If repayment failsm account is marked delinquent.

### Actions

-   Loan book update\
-   Credit bureau reporting

------------------------------------------------------------------------

# 15. Re Segmentation Engine

## Purpose

Dynamic risk reclassification.

### Buckets

-   PAR 0 (current)\
-   PAR 30\
-   PAR 90\
-   Write off risk

Updates based on payment behavior.

------------------------------------------------------------------------

# 16. Debt Collections Module

## Purpose

Manual and semiautomated recovery.

### Methods

-   Call centers\
-   Field agents\
-   Negotiated settlements

------------------------------------------------------------------------

# 17. External Collections Agency

Escalation layer for hard defaults.

### Functions

-   Legal notices\
-   Field recovery\
-   Asset seizure (if secured)

------------------------------------------------------------------------

# 18. Scheduling & Collections Workflow

## Purpose

Operational planning for recovery.

### Includes

-   Agent allocation\
-   Visit scheduling\
-   Priority queues

------------------------------------------------------------------------

# 19. Compliance Reporting

## Purpose

Regulatory transparency.

### Reports

-   Default ratios\
-   PAR metrics\
-   Recovery rates\
-   Write‑offs

Shared with regulators and credit bureaus.

------------------------------------------------------------------------

# Lifecycle Summary

1.  User acquired onboarded KYC verified\
2.  Financial data analyzed eligibility decided\
3.  Loan structured agreement signed\
4.  Funds disbursed loan booked\
5.  Notifications drive repayment\
6.  Defaults enter recovery pipeline\
7.  Collections + compliance close the loop

------------------------------------------------------------------------
