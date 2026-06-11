# Gated Content Setup Workflow - May 26, 2026

## ✅ Phase 1: Salesforce Campaign Creation (COMPLETE)

Both campaigns have been created in Salesforce:

| Asset | Campaign Name | Campaign ID | Type | Active | Start Date | Status |
|-------|---------------|-------------|------|--------|-----------|--------|
| Customer Onboarding Playbook | `26Q2_CustomerOnboarding_Playbook` | `701Pa00001S5lk9IAB` | Content Download | ✓ | 2026-05-26 | Active |
| Video Personalization Buyers Guide | `26Q2_VideoPersonalization_Guide` | `701Pa00001S6Td4IAF` | Content Download | ✓ | 2026-05-26 | Active |

---

## 📋 Phase 2: HubSpot Campaign Setup

**For Both Assets:**

1. **Navigate to HubSpot Campaigns**
   - Go to HubSpot → Marketing → Campaigns
   - Click "Create campaign"

2. **Create Campaign 1: Customer Onboarding Playbook**
   - **Campaign name:** `26Q2_CustomerOnboarding_Playbook` (must match Salesforce exactly)
   - **Landing page link:** https://sundaysky.com/ebook/customer-onboarding-guide/
   - **Campaign type:** Content Download
   - **Save & continue**

3. **Create Campaign 2: Video Personalization Buyers Guide**
   - **Campaign name:** `26Q2_VideoPersonalization_Guide` (must match Salesforce exactly)
   - **Landing page link:** https://sundaysky.com/ebook/video-personalization-tech-buyers-guide/
   - **Campaign type:** Content Download
   - **Save & continue**

---

## 📧 Phase 3: Autoresponder Email Setup

You need to clone and customize the autoresponder email template for each asset.

### Email 1: Customer Onboarding Playbook

**Steps:**
1. In HubSpot, navigate to **Marketing → Emails**
2. Find your existing autoresponder email template
3. Click **Actions → Clone**
4. **Name it:** `Autoresponder - 26Q2_CustomerOnboarding_Playbook`
5. **Edit the email:**
   - Update the email subject and copy to reference the Customer Onboarding Playbook
   - **Find the asset link** in the email template
   - **Replace it with:** https://info.sundaysky.com/hubfs/TOFU%20Assets/SundaySky_CustomerOnboardingPlaybook.pdf
   - Make sure the link is in the CTA button or prominent location
6. **Save & test the email**

### Email 2: Video Personalization Buyers Guide

**Steps:**
1. In HubSpot, navigate to **Marketing → Emails**
2. Find your existing autoresponder email template
3. Click **Actions → Clone**
4. **Name it:** `Autoresponder - 26Q2_VideoPersonalization_Guide`
5. **Edit the email:**
   - Update the email subject and copy to reference the Video Personalization Buyers Guide
   - **Find the asset link** in the email template
   - **Replace it with:** https://info.sundaysky.com/hubfs/TOFU%20Assets/SundaySky_VideoPersonalizationBuyersGuide.pdf
   - Make sure the link is in the CTA button or prominent location
6. **Save & test the email**

---

## 🌐 Phase 4: WordPress Page Update

**For Asset 1: Customer Onboarding Playbook**

1. **In WordPress Admin:**
   - Navigate to **Resources** section
   - Find the page: **Customer Onboarding Guide**
   - Locate the **placeholder Gravity Form**
   - **Replace the form** with your newly cloned form that corresponds to this asset
   - **Verify:** The form should have the dropdown/logic for the Customer Onboarding Playbook
   - **Publish the page**

**For Asset 2: Video Personalization Buyers Guide**

1. **In WordPress Admin:**
   - Navigate to **Resources** section
   - Find the page: **Video Personalization Tech Buyers Guide**
   - Locate the **placeholder Gravity Form**
   - **Replace the form** with your newly cloned form that corresponds to this asset
   - **Verify:** The form should have the dropdown/logic for the Video Personalization Guide
   - **Publish the page**

---

## ⚙️ Phase 5: Create HubSpot Form Submission Workflow

**Create a custom workflow to handle post-form submission automation for each asset.**

### Workflow 1: Customer Onboarding Playbook

**Steps:**
1. In HubSpot, navigate to **Automation → Workflows**
2. Find the most recent content download workflow (from the previous asset)
3. Click **Actions → Clone** to create a duplicate
4. **Rename it:** `26Q2_CustomerOnboarding_Playbook`
5. **Edit the workflow:**
   - **Step 1:** Change the form trigger to the cloned Gravity Form for Customer Onboarding Playbook
   - **Step 2:** Update the autoresponder email to: `Autoresponder - 26Q2_CustomerOnboarding_Playbook_AUTORESPONDER`
   - **Step 3:** Update the Salesforce campaign to: `26Q2_CustomerOnboarding_Playbook`
   - **Step 4:** Change the task description/language to reference: *Customer Onboarding: The Personalized Video & AI Playbook*
   - **Step 5:** Update the Slack notification message to include: *Customer Onboarding: The Personalized Video & AI Playbook*
6. **Save & turn on the workflow**

### Workflow 2: Video Personalization Buyers Guide

**Steps:**
1. In HubSpot, navigate to **Automation → Workflows**
2. Find the most recent content download workflow
3. Click **Actions → Clone** to create a duplicate
4. **Rename it:** `26Q2_VideoPersonalization_Guide`
5. **Edit the workflow:**
   - **Step 1:** Change the form trigger to the cloned Gravity Form for Video Personalization Guide
   - **Step 2:** Update the autoresponder email to: `Autoresponder - 26Q2_VideoPersonalization_Guide_AUTORESPONDER`
   - **Step 3:** Update the Salesforce campaign to: `26Q2_VideoPersonalization_Guide`
   - **Step 4:** Change the task description/language to reference: *Video Personalization: The Tech Buyer's Guide*
   - **Step 5:** Update the Slack notification message to include: *Video Personalization: The Tech Buyer's Guide*
6. **Save & turn on the workflow**

---

## ✔️ Phase 6: Form Testing Checklist

**Test Each Form End-to-End:**

### Customer Onboarding Playbook Form Test
- [ ] Navigate to https://sundaysky.com/ebook/customer-onboarding-guide/
- [ ] Submit the form with test data
- [ ] Verify form submission appears in HubSpot
- [ ] Confirm the autoresponder email is sent
- [ ] Click the asset link in the email → verify it opens the PDF
- [ ] Confirm the Gravity Form redirect works (if configured)
- [ ] Check that the form is associated with the `26Q2_CustomerOnboarding_Playbook` campaign

### Video Personalization Buyers Guide Form Test
- [ ] Navigate to https://sundaysky.com/ebook/video-personalization-tech-buyers-guide/
- [ ] Submit the form with test data
- [ ] Verify form submission appears in HubSpot
- [ ] Confirm the autoresponder email is sent
- [ ] Click the asset link in the email → verify it opens the PDF
- [ ] Confirm the Gravity Form redirect works (if configured)
- [ ] Check that the form is associated with the `26Q2_VideoPersonalization_Guide` campaign

---

## 🎯 Phase 7: LeanData Configuration

**Update the LeanData routing to include both campaigns in the Content Downloads condition.**

### Campaign 1: 26Q2_CustomerOnboarding_Playbook

**Steps:**
1. In LeanData, open the lead graph
2. Go to the **"Route to Cadences"** decision branch
3. Update the **"Content Downloads"** condition and add: `26Q2_CustomerOnboarding_Playbook`
4. Save changes

### Campaign 2: 26Q2_VideoPersonalization_Guide

**Steps:**
1. In LeanData, open the lead graph
2. Go to the **"Route to Cadences"** decision branch
3. Update the **"Content Downloads"** condition and add: `26Q2_VideoPersonalization_Guide`
4. Save changes

**Note:** Changes may take a few minutes to propagate through LeanData.

---

## 📊 Master Checklist

Track your progress:

### Asset 1: Customer Onboarding Playbook
- [x] Salesforce campaign created (`26Q2_CustomerOnboarding_Playbook`)
- [ ] HubSpot campaign created
- [ ] Autoresponder email cloned and customized
- [ ] WordPress page updated with form
- [ ] Form testing completed
- [ ] HubSpot form submission workflow created
- [ ] LeanData "Most Recent Campaign" configured
- [ ] LeanData SDR routing configured
- [ ] LeanData SalesLoft cadence linked

### Asset 2: Video Personalization Buyers Guide
- [x] Salesforce campaign created (`26Q2_VideoPersonalization_Guide`)
- [ ] HubSpot campaign created
- [ ] Autoresponder email cloned and customized
- [ ] WordPress page updated with form
- [ ] Form testing completed
- [ ] HubSpot form submission workflow created
- [ ] LeanData "Most Recent Campaign" configured
- [ ] LeanData SDR routing configured
- [ ] LeanData SalesLoft cadence linked

---

## 📝 Notes

- **HubSpot Campaign Names Must Match Salesforce Exactly** — This ensures proper lead attribution and reporting
- **Asset URLs** — These are the direct HubSpot-hosted PDFs; make sure links are in the autoresponder emails
- **Form Testing is Critical** — Test each form to ensure the complete flow works before marking as live
- **LeanData Timeline** — Once updated, it may take a few minutes for rules to propagate

---

## Next Steps

1. Create HubSpot campaigns (5 min)
2. Clone and customize autoresponder emails (10 min)
3. Update WordPress pages (5 min)
4. Create HubSpot form submission workflows (15 min)
5. Test form flows (10 min)
6. Configure LeanData (10 min)

**Total estimated time:** ~55 minutes for both assets

Questions? Let me know what needs adjustment!
