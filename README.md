
---
# Oracle HCM Fusion – Annual Leave Absence Plan (Saudi Arabia)

## Overview

This document describes the configuration of an **Annual Leave Absence Plan** for a Saudi Arabian enterprise in Oracle HCM Cloud.

## Configuration Steps

### 1. Create the Accrual Plan

Create the accrual plan:

* **Plan Name:** `MSA SA VACATION PLAN`

This plan is responsible for calculating and awarding employees' annual leave entitlement.

### 2. Create the Eligibility Profile

Create an eligibility profile to determine which workers are enrolled in the plan.

* **Eligibility Profile:** `MSA SA PROFILE`

Assign the appropriate worker criteria according to the organization's business requirements.

### 3. Configure Length of Service (LOS) Rules

Create Length of Service rules to grant different annual leave entitlements based on an employee's completed years of service.

| Rule   | Length of Service | Annual Entitlement |
| ------ | ----------------- | ------------------ |
| Rule A | Less than 5 years | 21 days            |
| Rule B | 5 years or more   | 30 days            |

These rules are added to the **Length of Service Matrix** used by the accrual plan.

### 4. Create the Absence Type

Create a generic absence type linked to the accrual plan.

* **Absence Type:** `MSA SA VACATION TYPE`

Associate this absence type with **MSA SA VACATION PLAN** so that workers can request annual leave and have their balances deducted automatically.

## Business Rules

* Workers with **less than 5 years** of service receive **21 days** of annual leave per year.
* Workers with **5 years or more** of service receive **30 days** of annual leave per year.
* Eligibility is determined using the **MSA SA PROFILE** eligibility profile.
* Leave accrual is managed by the **MSA SA VACATION PLAN**.
* Employees submit leave requests using the **MSA SA VACATION TYPE** absence type.

## Objects Created

| Object Type              | Name                   |
| ------------------------ | ---------------------- |
| Accrual Plan             | `MSA SA VACATION PLAN` |
| Eligibility Profile      | `MSA SA PROFILE`       |
| Absence Type             | `MSA SA VACATION TYPE` |
| Length of Service Rule A | `< 5 Years → 21 Days`  |
| Length of Service Rule B | `≥ 5 Years → 30 Days`  |

---
All Plans!
https://youtu.be/5e1zd-B7vGQ

