# Gated Content Setup Plugin — Team Sharing Guide

**Version:** 0.1.0  
**Author:** Rob Walter  
**Date:** June 2026  
**For:** SundaySky Marketing & Operations Teams

---

## What Is This?

The **gated-content-setup** plugin automates the 7-phase workflow for setting up gated PDF content assets across our marketing stack (WordPress, Gravity Forms, HubSpot, Salesforce, and LeanData).

Instead of manually tracking steps across 5 systems, the plugin generates an interactive workflow guide with:
- ✅ Campaign names pre-generated using our naming convention
- ✅ Copy buttons for all values you need to paste between systems
- ✅ Progress checkboxes for all 7 phases
- ✅ Step-by-step instructions for each system
- ✅ Estimated timelines

**Setup time:** ~55 minutes per asset (vs. remembering all the steps manually)

---

## Who Should Use This?

- **Marketing Operations** — Setting up new gated content assets
- **Demand Generation** — Coordinating content downloads with campaigns
- **Revenue Operations** — Managing Salesforce and LeanData configuration
- **Anyone** involved in the gated content workflow

---

## Installation Instructions

### Step 1: Download the Plugin File
Get the `gated-content-setup.plugin` file from:
- **Email** — attachment from Rob
- **Shared Folder** — [insert team folder location if applicable]
- **Slack** — File pinned in #marketing-ops (or similar)

### Step 2: Install in Cowork
1. Open **Claude Cowork** on your desktop
2. Go to **Settings** (gear icon in top right)
3. Select **Capabilities** or **Plugins**
4. Click **"Install Plugin"** or **"Add Plugin"**
5. Select the `gated-content-setup.plugin` file
6. Click **Install**

### Step 3: Verify Installation
1. In Claude, type **"/"** to open the command menu
2. Look for **gated-content-setup** in the skills list
3. If you see it, you're ready to go! ✅

---

## How to Use

### Quick Start
1. Tell Claude: **"Set up a new gated content asset"** or invoke the **gated-content-setup** skill
2. Provide the asset details:
   - **Formal asset title** — How it appears in communications (e.g., "Customer Onboarding: The Personalized Video & AI Playbook")
   - **Short name** — For campaign naming, no spaces (e.g., "CustomerOnboarding")
   - **Asset type** — CaseStudy, Guide, Report, Playbook, or Webinar
   - **Asset URL** — Direct link to the PDF in HubSpot TOFU Assets folder
   - **Landing page URL** — Where the form is hosted
   - **Quarter/Year** — When this asset is launching (optional; defaults to today)

### What You Get
Claude will generate an **interactive workflow document** showing:
- Your campaign name (generated automatically)
- All 7 phases with step-by-step instructions
- Copy buttons for every value you need to paste elsewhere
- Checkboxes to track your progress
- Estimated time for each phase

### The 7 Phases
1. **Salesforce Campaign Creation** (5 min)
2. **HubSpot Campaign Setup** (5 min)
3. **Autoresponder Email Setup** (10 min)
4. **WordPress Page Update** (5 min)
5. **HubSpot Form Submission Workflow** (15 min)
6. **Form Testing Checklist** (10 min)
7. **LeanData Configuration** (10 min)

---

## Campaign Naming Convention

All campaigns follow this format: `(YY)Q(Q)_{ShortName}_{AssetType}`

**Examples:**
- `26Q2_CustomerOnboarding_Playbook`
- `26Q2_VideoPersonalization_Guide`
- `26Q1_Insurance_CaseStudy`
- `25Q4_DataGovernance_Report`

The plugin generates this automatically—no manual naming required.

---

## Key Features

| Feature | Benefit |
|---------|---------|
| **Copy Buttons** | Paste exact values without typos |
| **Pre-filled Names** | Campaign name generated using our naming convention |
| **Checkboxes** | Track progress across all 7 phases |
| **Inline Instructions** | All steps in one document, no switching between tabs |
| **Estimated Timeline** | Know how long each phase takes |
| **Interactive Artifact** | Everything in Claude—no downloads or external files |

---

## Example Workflow

Here's what happens when you use the skill:

1. **You:** "I need to set up a new gated content asset"
2. **Claude:** Asks for asset details (title, short name, type, URLs, quarter)
3. **You:** Provide the information
4. **Claude:** 
   - Generates campaign name: `26Q2_CustomerOnboarding_Playbook`
   - Creates interactive workflow with all 7 phases
   - Displays with copy buttons and checkboxes
5. **You:** 
   - Follow Phase 1: Create Salesforce campaign (use copy button for name)
   - Follow Phase 2: Create HubSpot campaign (use copy button for name)
   - Continue through all 7 phases
   - Check off each step as you complete it
6. **Result:** All 5 systems are configured and synced ✅

---

## Troubleshooting

### "I don't see the gated-content-setup skill"
- Make sure the plugin is installed (check Settings → Plugins)
- Try refreshing Cowork (close and reopen the app)
- If still missing, re-install the plugin

### "The copy buttons aren't working"
- Make sure you're using Claude Cowork (not Claude.ai in a browser)
- Try copying manually if buttons fail
- Report the issue to Rob

### "I'm stuck on a phase"
- Check the reference materials in the plugin (naming convention, workflow details)
- Review the step-by-step instructions for that system
- Reach out to the team on Slack with the phase number

### "The campaign name looks wrong"
- Double-check the short name and asset type you provided
- Asset type must be exactly: CaseStudy, Guide, Report, Playbook, or Webinar
- If unsure, ask Rob to regenerate with corrected details

---

## Common Questions

**Q: Do I need to be a developer to use this?**  
A: No. Just tell Claude what you need and follow the interactive instructions.

**Q: Can I modify the workflow?**  
A: The interactive document is yours to customize. Edit it as needed for your asset.

**Q: What if our setup process changes?**  
A: Contact Rob—the plugin can be updated to reflect new workflows.

**Q: Can I use this for multiple assets?**  
A: Yes! Run the skill once for each asset. Each one gets its own interactive workflow.

**Q: How long does it take to set up an asset?**  
A: About 55 minutes per asset (HubSpot workflow creation is the longest step).

**Q: What if I need to set this up for a different organization?**  
A: The plugin is built for SundaySky's workflow. For other orgs, you'd need to customize the templates.

---

## What's Included in the Plugin?

- **1 Skill** — gated-content-setup (main workflow automation)
- **Reference Materials** — Campaign naming guide and detailed 7-phase requirements
- **Documentation** — Full README and quick-start guide
- **Pre-built Instructions** — Step-by-step guidance for all 5 systems

---

## Support & Feedback

**Questions?** Reach out to Rob Walter (rob.walter@sundaysky.com) or your manager.

**Found a bug or have a suggestion?** Let Rob know—this plugin will continue to improve based on team feedback.

**Want to share improvements with the team?** Suggest updates via Slack or email.

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 0.1.0 | June 2026 | Initial release with all 7 phases, copy buttons, and progress tracking |

---

## Next Steps

1. ✅ Install the plugin (follow "Installation Instructions" above)
2. ✅ Try it with your next gated content asset
3. ✅ Give feedback to Rob
4. ✅ Share with teammates who need it

---

**Happy automating! 🚀**

Questions? Slack Rob or check the Reference Materials in the plugin.
