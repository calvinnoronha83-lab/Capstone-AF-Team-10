# Capstone Project Team 10 - Patient Support Agent

## 🏥 Project Overview

This repository contains the implementation of a **Patient Support Agent** built with Salesforce Agentforce for a multinational healthcare provider. The agent streamlines patient interactions, reduces call volume by 15-20%, and ensures consistent, accurate, and compliant information delivery.

### Use Case
**Global Healthcare Provider**: Introducing an Agentic Solution for Patient Support and Compliance

A multinational healthcare provider serving millions of patients worldwide needs to balance high patient service demand with strict regulatory oversight. The Patient Support Agent addresses:
- High operational costs from human-only support
- Inconsistent information delivery
- Challenges in quickly providing up-to-date and compliant information
- Lack of efficient data integration across patient record systems

### Goals
- **Short-term**: Reduce inbound calls related to common FAQs (insurance benefits, appointment procedures) by 15–20% in the first quarter
- **Long-term**: Evolve into a "Personal Health Navigator" with proactive health reminders, prescription refill management, and guidance through complex care pathways

---

## 📁 Repository Structure

```
.
├── README.md                              # This file
├── index.html                             # Patient Support Agent landing page
├── README_HTML.md                          # HTML page setup instructions
├── Patient_Support_Agent_Objects_Analysis.md  # Complete Salesforce objects analysis
├── Custom_Objects_Recommendation.md         # Custom objects specifications
├── Custom_Objects_Quick_Reference.md        # Quick reference guide
├── Health_Cloud_Objects_Reference.md       # Health Cloud objects (if enabled)
├── Health_Cloud_Summary.md                 # Health Cloud quick reference
├── Health_Cloud_Check_Queries.soql         # Queries to check Health Cloud
├── Org_Audit_Queries.soql                  # Org audit queries
├── force-app/                              # Salesforce DX project files
│   └── (Salesforce metadata)
├── manifest/                               # Package manifest
├── scripts/                                # Utility scripts
│   ├── apex/                              # Apex code samples
│   └── soql/                              # SOQL query examples
└── config/                                 # Project configuration
```

---

## 🚀 Quick Start

### 1. Landing Page Setup

The `index.html` file provides a beautiful healthcare-themed landing page for hosting your Patient Support Agent.

**To deploy:**
1. Push `index.html` to your repository
2. Enable GitHub Pages in repository Settings → Pages
3. Update the agent URL in `index.html` (see `README_HTML.md` for details)

**Live Demo**: [View the landing page](https://calvinnoronha83-lab.github.io/Capstone-AF-Team-10/)

### 2. Salesforce Objects Setup

#### If Health Cloud is NOT Enabled (Recommended for MVP):
Use custom objects as specified in `Custom_Objects_Recommendation.md`:

**Phase 1 Objects (Required):**
- `Insurance_Policy__c` - Patient insurance policies
- `Insurance_Benefit__c` - Benefits under each policy
- `Insurance_Benefit_Item__c` - Service-specific coverage
- `Patient_Interaction__c` - Track all patient interactions
- `Agent_Conversation__c` - AI agent conversation logs

**Phase 2 Objects (Long-term):**
- `Prescription__c` - Prescription management
- `Prescription_Refill_Request__c` - Refill tracking
- `Health_Reminder__c` - Proactive reminders
- `Compliance_Log__c` - Compliance audit trail

#### If Health Cloud IS Enabled:
Use Health Cloud objects as specified in `Health_Cloud_Objects_Reference.md`:
- `HealthCloudGA__MemberPlan__c` - Insurance policies
- `HealthCloudGA__CoverageBenefit__c` - Benefits
- `HealthCloudGA__CoverageBenefitItem__c` - Service coverage

**Check Health Cloud Status:**
```sql
SELECT COUNT() FROM HealthCloudGA__Contact__c
```

---

## 📚 Documentation

### Core Documentation
- **[Patient Support Agent Objects Analysis](Patient_Support_Agent_Objects_Analysis.md)** - Complete analysis of all Salesforce objects needed
- **[Custom Objects Recommendation](Custom_Objects_Recommendation.md)** - Detailed custom object specifications with all fields
- **[Custom Objects Quick Reference](Custom_Objects_Quick_Reference.md)** - Quick reference guide

### Health Cloud Documentation (If Applicable)
- **[Health Cloud Objects Reference](Health_Cloud_Objects_Reference.md)** - Complete Health Cloud object reference
- **[Health Cloud Summary](Health_Cloud_Summary.md)** - Quick Health Cloud reference

### Setup Guides
- **[HTML Landing Page Setup](README_HTML.md)** - Instructions for deploying the landing page
- **[Org Audit Queries](Org_Audit_Queries.soql)** - Queries to audit your Salesforce org
- **[Health Cloud Check Queries](Health_Cloud_Check_Queries.soql)** - Queries to verify Health Cloud

---

## 🛠️ Technology Stack

- **Salesforce Platform**: Core CRM and data management
- **Salesforce Agentforce**: AI-powered patient support agent
- **Salesforce Health Cloud** (Optional): Enhanced healthcare objects
- **HTML/CSS/JavaScript**: Landing page frontend
- **GitHub Pages**: Hosting for landing page

---

## 📋 Implementation Checklist

### Phase 1: MVP (First Quarter)
- [ ] Review and understand use case requirements
- [ ] Audit Salesforce org (run `Org_Audit_Queries.soql`)
- [ ] Check if Health Cloud is enabled (run `Health_Cloud_Check_Queries.soql`)
- [ ] Create custom objects (if Health Cloud not enabled)
  - [ ] `Insurance_Policy__c`
  - [ ] `Insurance_Benefit__c`
  - [ ] `Insurance_Benefit_Item__c`
  - [ ] `Patient_Interaction__c`
  - [ ] `Agent_Conversation__c`
- [ ] Set up field history tracking on critical fields
- [ ] Create page layouts and validation rules
- [ ] Set up Knowledge Base with FAQs
- [ ] Configure Agentforce agent
- [ ] Deploy landing page (`index.html`)
- [ ] Connect agent URL to landing page
- [ ] Test agent functionality
- [ ] Measure baseline metrics (call volume, escalations)

### Phase 2: Long-term Roadmap
- [ ] Implement prescription management objects
- [ ] Add health reminder functionality
- [ ] Integrate with all patient data systems
- [ ] Build care pathway management
- [ ] Enhance compliance tracking
- [ ] Expand to proactive health navigation

---

## 🔐 Security & Compliance

- **HIPAA Compliance**: All patient data handling follows HIPAA guidelines
- **Field History Tracking**: Enabled on critical fields for audit trails
- **Compliance Logging**: Track all data access and modifications
- **Secure Integration**: Use Named Credentials for external system integration

---

## 📊 Key Metrics

### Short-term Goals (Q1)
- **15-20% reduction** in inbound calls for common FAQs
- **Measurable reduction** in manual agent escalations
- **Full compliance** with regulatory requirements
- **Improved patient trust** through consistent information delivery

### Long-term Vision
- **Personal Health Navigator**: Proactive health management
- **Reduced preventable readmissions**: Through better patient engagement
- **Complete data integration**: Across all patient record systems
- **Complex care pathway guidance**: For chronic conditions

---

## 🤝 Team

**Capstone Project Team 10**

---

## 📞 Support

For questions or issues:
1. Review the documentation files in this repository
2. Check Salesforce documentation for Agentforce
3. Consult with your Salesforce administrator

---

## 📝 License

This project is part of a Capstone project for educational purposes.

---

## 🔗 Useful Links

- [Salesforce Agentforce Documentation](https://help.salesforce.com/s/articleView?id=sf.ai_agentforce_overview.htm)
- [Salesforce Health Cloud Documentation](https://help.salesforce.com/s/articleView?id=sf.health_cloud.htm)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

---

## 📈 Project Status

**Current Phase**: Planning & Setup  
**Next Steps**: Object creation and Agentforce configuration

---

**Last Updated**: February 2026
