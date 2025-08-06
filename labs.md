# GCP IAM & Compute Engine Labs (Tasks 1–7)

## 🚀 Overview
This repository documents my learning and understanding of IAM roles, service accounts, and Compute Engine access within Google Cloud Platform. Each task outlines the concept, steps executed, and key insights.

---

## 🧩 Task 1: Initial IAM Role Configuration
- Verified access permissions using `gcloud compute instances list`.
- Learned the difference between viewer and editor roles.
- Understood how IAM roles control resource visibility and access.

---

## 🧩 Task 2: IAM Role Binding
- Used `gcloud projects add-iam-policy-binding` to bind the `viewer` role.
- Saw how project-level IAM changes reflect immediately in user permissions.

---

## 🧩 Task 3: Testing Limited Access
- Switched to user2 and verified restricted access (`viewer` only).
- Attempted resource creation and observed permission-denied errors.
- Reaffirmed the importance of least privilege principle.

---

## 🧩 Task 4: Creating Custom Roles
- Created a custom `devops` role with specific compute permissions.
- Assigned both `devops` and `iam.serviceAccountUser` roles to user2.
- Successfully enabled user2 to create VM instances in Project 2.

---

## 🧩 Task 5: Introducing Service Accounts
- Created a `devops` service account to enable programmatic access.
- Assigned `iam.serviceAccountUser` to the service account.
- Prepared the account for use in automated deployments.

---

## 🧩 Task 6: Using the Service Account in a Compute Instance
- Bound `compute.instanceAdmin` to the service account.
- Created `lab-3` VM with the service account and scoped API access.
- Reinforced how access scopes work in legacy vs. IAM role contexts.

---

## 🧩 Task 7: Verifying Service Account Access
- SSH’d into `lab-3` and confirmed service account identity.
- Created another VM (`lab-4`) to test access.
- Verified all resources were accessible via `gcloud compute instances list`.

---

## 🌟 Key Takeaways
- IAM is foundational to secure, scalable cloud architecture.
- Service accounts power automated access without human intervention.
- The principle of least privilege ensures security and operational efficiency.
