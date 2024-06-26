---
description: >-
  Gatenox Hub provides Compliance Officers with a robust API, offering powerful
  screening capabilities for individuals, companies, and crypto addresses,
  ensuring comprehensive compliance checks.
---

# Comprehensive screening

### **Screening Individuals (KYC) and Companies (KYB)**

#### Instant screening

Gatenox Hub offers both individuals and companies screening against sanctions / PEP and criminal records.

* For Individuals - provide a surname, given names, and optional date of birth.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/individuals" method="post" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

The endpoint's body requires the following values to be included in the request:

<table><thead><tr><th>Parameter</th><th width="364">Values</th><th>Required?</th></tr></thead><tbody><tr><td>check_type</td><td>standard | premium</td><td>Yes</td></tr><tr><td>given_names</td><td></td><td>Yes</td></tr><tr><td>surname</td><td></td><td>Yes</td></tr><tr><td>date_of_birth</td><td></td><td>No</td></tr></tbody></table>



* For Companies -  specifying company name.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/companies" method="post" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

The endpoint's body requires the following values to be included in the request:

<table><thead><tr><th>Parameter</th><th width="312">Values</th><th>Required?</th></tr></thead><tbody><tr><td>check_type</td><td>standard | premium</td><td>Yes</td></tr><tr><td>company_name</td><td></td><td>Yes</td></tr></tbody></table>



Gatenox Hub offers two levels of sanctions/PEP/criminal records screening:

* Standard Screening: Users with Gatenox Hub licenses can perform free basic screenings against OFAC, EU, UN, PL, UK, and Singapore sanctions lists.
* Premium Screening: A paid service, offering advanced checks against sanctions, PEP databases, and global criminal lists, providing a thorough compliance solution.

#### **Get the results of the screening**

Download a comprehensive list of checks and details from previous screenings using the following endpoints:

**Individuals**

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/individuals" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/individuals/{id}" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

**Companies**

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/companies" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/companies/{id}" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

Associated files (if any) can be downloaded via an additional endpoint.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/attachments/{rest}" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

### **Crypto Address Verification (Blockchain Analytics)**&#x20;

#### Request a report

Verify crypto addresses by providing the blockchain and the specific address.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/crypto_address" method="post" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

#### **Get the report**

Receive a comprehensive crypto address report, including risk assessment, financial analysis (historical balance), and a list of owned tokens.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/crypto_address" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/checks/crypto_address/{id}" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

Download the detailed report in PDF format for further analysis and record-keeping.

{% swagger src="../../.gitbook/assets/gatenox_api_1.5.1.yaml" path="/api/v1/attachments/{rest}" method="get" %}
[gatenox_api_1.5.1.yaml](../../.gitbook/assets/gatenox_api_1.5.1.yaml)
{% endswagger %}

