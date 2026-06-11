---
name: gated-content-setup
description: |
  Automate setup for gated PDF content across WordPress, Gravity Forms, HubSpot, Salesforce, and LeanData. When marketing creates a new PDF asset for gating, this skill creates the Salesforce campaign via API and provides an interactive workflow document with copy buttons for all campaign names, URLs, and field values. Covers all 7 phases: Salesforce campaign creation, HubSpot setup, autoresponder email, WordPress form updates, HubSpot workflow automation, form testing, and LeanData routing configuration.
compatibility: Requires access to Salesforce API
---

# Gated Content Setup Automation

When marketing creates a new PDF for gated content distribution, you need to set up infrastructure across multiple systems. This skill automates the Salesforce campaign creation and provides a complete interactive workflow guide.

## Overview

The complete workflow has 7 phases:

1. **Salesforce Campaign Creation** — Automated via API
2. **HubSpot Campaign Setup** — Campaign creation with asset linking
3. **Autoresponder Email Setup** — Email template cloning and customization
4. **WordPress Page Update** — Form replacement and configuration
5. **HubSpot Form Submission Workflow** — Automation workflow creation
6. **Form Testing Checklist** — End-to-end form validation
7. **LeanData Configuration** — Route to Cadences condition update

## How to use this skill

When marketing hands you a new PDF asset for gating, I'll:

**Step 1: Collect Asset Information**

I need:
- **Formal asset title** (e.g., "Customer Onboarding: The Personalized Video & AI Playbook")
- **Short name** (e.g., "CustomerOnboarding" — used in campaign naming)
- **Asset type** (CaseStudy, Guide, Report, Playbook, or Webinar)
- **Asset URL** (from HubSpot TOFU Assets folder after upload)
- **Landing page URL** (from Head of Demand Gen)
- **Year/Quarter** (for campaign naming; defaults to today)

**Step 2: Create Salesforce Campaign**

I'll create the campaign with:
- Naming convention: `(YY)Q(Q)_{ShortName}_{AssetType}`
- Type: Content Download
- Status: Active
- Start Date: Today

**Step 3: Provide Interactive Workflow Guide**

I'll generate an interactive HTML workflow document with:
- All 7 phases with inline checkboxes
- Copy buttons for all campaign names, URLs, and field values
- Step-by-step instructions for HubSpot, WordPress, and LeanData
- Estimated timeline for each phase

## Naming Convention Reference

**Format:** `(YY)Q(Q)_{ShortName}_{AssetType}`

- `YY` = Two-digit year (e.g., 26 for 2026)
- `Q` = Quarter number (1-4)
- `ShortName` = Asset identifier (e.g., CustomerOnboarding, VideoPersonalization)
- `AssetType` = One of: CaseStudy, Guide, Report, Playbook, Webinar

**Examples:**
- `26Q2_CustomerOnboarding_Playbook`
- `26Q2_VideoPersonalization_Guide`
- `26Q1_Alliant_CaseStudy`
- `25Q4_Insurance_Report`

## Key Details & Requirements

### Salesforce Campaign
- **Type:** Content Download (required)
- **Active checkbox:** Must be checked
- **Start Date:** Set to today
- **Status:** Active

### HubSpot Campaign
- Name must match Salesforce exactly
- Campaign type: Content Download
- Must add asset file using "Add assets" link

### Autoresponder Email
- Naming convention: `{CampaignName}_AUTORESPONDER`
- Example: `26Q2_CustomerOnboarding_Playbook_AUTORESPONDER`
- Asset link: Direct to PDF in HubSpot TOFU Assets folder

### WordPress Form
- HubSpot Form Name must match campaign name
- Redirect URL: Landing page + `?thankYou=true`
- Example: `https://sundaysky.com/ebook/customer-onboarding-guide/?thankYou=true`

### HubSpot Form Submission Workflow
- Clone the most recent content download workflow
- Update 5 elements:
  1. Form trigger (to new Gravity Form)
  2. Autoresponder email (to new _AUTORESPONDER email)
  3. Salesforce campaign field (to new campaign name)
  4. Task language (to include formal asset title)
  5. Slack notification (to include formal asset title)

### LeanData Configuration
- Go to **Route to Cadences** decision branch
- Update **Content Downloads** condition
- Add campaign name to the condition
- Save changes

## Quick Reference Checklist

When you complete setup, you'll have:

- [ ] Salesforce campaign created (Type: Content Download, Active: Yes)
- [ ] HubSpot campaign created and linked
- [ ] Autoresponder email cloned with _AUTORESPONDER naming
- [ ] WordPress page updated with form
- [ ] HubSpot form submission workflow created
- [ ] Form tested end-to-end
- [ ] LeanData Route to Cadences condition updated

## Common Questions

**Q: What's the formal asset title used for?**
A: It's used in the HubSpot workflow's task descriptions and Slack notifications so the team knows which asset triggered the workflow.

**Q: Can I update LeanData programmatically?**
A: Not yet — LeanData doesn't have an API. The workflow guide provides step-by-step UI instructions for the Content Downloads condition update.

**Q: What if HubSpot API access becomes available?**
A: The skill will be updated to automate HubSpot campaign, email, and workflow creation. For now, follow the interactive workflow document.

**Q: How long does setup take?**
A: About 55 minutes per asset (5 min HubSpot campaigns, 10 min emails, 5 min WordPress, 15 min workflow, 10 min testing, 10 min LeanData).

## How to Get Started

Tell me:
1. Asset name, short name, type, URL, quarter/year, landing page link
2. Formal asset title (how it should appear in communications)

I'll create the Salesforce campaign and provide you with the interactive workflow document to complete the remaining 6 phases.
