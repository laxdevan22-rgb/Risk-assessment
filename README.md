## EXPERIMENT - 4

## ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS
```
NAME: V.Lakshita Rai
REG.NO: 212225220054
```

## AIM

To identify storage assets in **AWS S3**, identify possible vulnerabilities and threats, and assess their **likelihood, impact, and risk level**.

**1\. Software / Cloud Services Required**

- AWS Account
- Microsoft Azure Account
- Web Browser
- Internet Connection

Cloud Services Used

| **Cloud Platform** | **Storage Service** |
| ------------------ | ------------------- |
| AWS                | Amazon S3           |
| Microsoft Azure    | Azure Blob Storage  |

# PART A — AWS S3 STORAGE ASSESSMENT

**Step 1: Login to AWS**

1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.

**Step 2: Select the S3 Bucket**

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:
   - Bucket name
   - AWS Region
   - Number/type of objects
     
<img width="1917" height="907" alt="Screenshot 2026-09-11 221747" src="https://github.com/user-attachments/assets/b384bb1f-7c5e-403c-8dad-87da4928f14e" />

**Step 3: Check Block Public Access**

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

**Record:**

- ON → Secure configuration
- OFF → Potential public-access risk

<img width="1917" height="903" alt="Screenshot 2026-09-11 225406" src="https://github.com/user-attachments/assets/5153d8b7-05be-4a80-a2aa-2945a7a06025" />

**Step 4: Check Bucket Versioning**

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:
   - Enabled
   - Disabled

**Security purpose**

Versioning helps recover previous versions of objects after accidental deletion or modification.

<img width="1915" height="902" alt="Screenshot 2026-09-11 225346" src="https://github.com/user-attachments/assets/08106332-dedf-431f-bfc5-0ce446835bff" />


**Step 5: Check Default Encryption**

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

Possible configurations include:

- SSE-S3
- SSE-KMS
- DSSE-KMS

**Security purpose**

Encryption protects stored data from unauthorized disclosure.

<img width="1917" height="917" alt="Screenshot 2026-09-11 225437" src="https://github.com/user-attachments/assets/99f8289e-ac85-4d0e-aa35-733e6bb0d85d" />


**Step 6: Check Bucket Policy**

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

Record:

- Policy exists
- No policy

**Note**

A missing bucket policy is **not automatically a vulnerability**. Access may be controlled through IAM and other AWS security mechanisms.

<img width="1917" height="912" alt="Screenshot 2026-09-11 225510" src="https://github.com/user-attachments/assets/d20b6ba5-ee1d-4038-ab4e-6dd3f571eb13" />


**Step 7: Check Object Ownership and ACL**

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

- ACLs are disabled.
- Objects are owned by the bucket owner.
- Access is controlled using policies.

<img width="1917" height="906" alt="Screenshot 2026-09-11 225608" src="https://github.com/user-attachments/assets/a5dedf03-1844-4afd-8278-c486863cd223" />


**Step 8: Check Server Access Logging**

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:
   - Enabled
   - Disabled

**Security purpose**

Logging helps investigate suspicious or unauthorized access to the bucket.

<img width="1917" height="912" alt="Screenshot 2026-09-11 225650" src="https://github.com/user-attachments/assets/851ace72-737f-451c-9bb7-891f3efa41c4" />


**PART B — AWS RISK ASSESSMENT**

After checking the S3 configuration, identify possible vulnerabilities and threats.

**Risk Formula**

**Risk Score = Likelihood × Impact**

Use the following scale.

**Likelihood**

| **Score** | **Description** |
| --------- | --------------- |
| 1         | Very Low        |
| 2         | Low             |
| 3         | Medium          |
| 4         | High            |
| 5         | Very High       |

## Sample AWS Risk Assessment

Students must use their **actual configuration** while preparing the final table.

| **Asset** | **Vulnerability**         | **Threat**                                       | **Likelihood** | **Impact** | **Risk Score** | **Risk Level** | **Recommended Mitigation** |
| --------- | ------------------------- | ------------------------------------------------ | -------------- | ---------- | -------------- | -------------- | -------------------------- |
| S3 Bucket | Versioning disabled       | Accidental/malicious data deletion               | 3              | 4          | 12             | High           | Enable versioning          |
| S3 Bucket | Access logging disabled   | Difficult investigation of unauthorized activity | 3              | 3          | 9              | Medium         | Enable appropriate logging |
| S3 Bucket | Public access enabled\*   | Unauthorized data access                         | 4              | 5          | 20             | Critical       | Enable Block Public Access |
| S3 Bucket | Weak access permissions\* | Unauthorized modification/access                 | 3              | 4          | 12             | High           | Apply least privilege      |

## RESULT

**The storage assets in AWS S3 is identified and analyzed. Various security configurations, vulnerabilities, threats, likelihood, and impacts were evaluated. Risk scores were calculated using the Likelihood × Impact method, and appropriate security mitigation measures were recommended.**
