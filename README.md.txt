# InfluenceFlow AI
### AI-Powered Instagram Influencer Research & Email Outreach Automation

## 1. Project Overview
InfluenceFlow AI is an automation system built using n8n that streamlines influencer research, AI-based lead analysis, personalized email drafting, reply management, and follow-up tracking.

It uses Google Gemini for AI-powered analysis and email generation, Google Sheets as an influencer CRM, and Gmail for creating email drafts.

## 2. Technologies Used
- n8n – Workflow automation
- Google Gemini API – AI analysis, classification, and content generation
- Google Sheets – Influencer CRM and lead tracking
- Gmail – Email draft creation

## 3. Workflow Architecture

### Workflow 1: Influencer Research & AI Analysis
- Accepts influencer information as input.
- Uses Gemini to analyze and score the influencer.
- Generates an AI summary and recommendation.
- Stores the result in Google Sheets.

### Workflow 2: Personalized Email Automation
- Retrieves influencer records from Google Sheets.
- Generates personalized collaboration email content using Gemini.
- Creates an email draft in Gmail.
- Updates the CRM status.

### Workflow 3: Reply Management
- Checks incoming Gmail messages on a scheduled basis.
- Uses Gemini to classify incoming messages.
- Filters unrelated messages.
- Updates the CRM and prepares reply drafts for relevant messages.

### Workflow 4: Follow-up Automation
- Runs on a scheduled basis.
- Retrieves eligible leads from Google Sheets.
- Creates follow-up email drafts in Gmail.
- Updates the CRM status to Follow-up Due.

## 4. CRM Structure
The Google Sheet contains:
- Name
- Username
- Niche
- Followers
- Email
- Location
- AI Score
- AI Summary
- Recommendation
- Status

Lead statuses are used to track progress through the outreach process.

## 5. Setup Requirements
1. Import the four JSON workflow files into n8n.
2. Configure Google Gemini API credentials.
3. Connect Google Sheets and select the CRM spreadsheet.
4. Connect the Gmail account.
5. Verify node configurations and execute the workflows.

## 6. Important Implementation Notes
- Google Gemini is used in place of Claude for the current implementation.
- Influencer information is supplied as sample/manual input. Automated Instagram scraping is not implemented.
- The workflows create Gmail drafts rather than automatically sending emails, allowing human review before sending.
- The reply and follow-up workflows should be tested with genuine, authorized test messages before production use.
- Sample influencer contact details are placeholders and must not be used for real outreach.

## 7. Responsible Usage
The system is designed to use publicly available or authorized influencer information. Email drafts should be reviewed and approved by a human before sending. Outreach should respect recipient consent, opt-out requests, and applicable platform policies.

## 8. Project Deliverables
- Four n8n workflow JSON exports
- Google Sheets influencer CRM
- AI-generated influencer analysis
- Personalized email draft automation
- Reply classification and draft workflow
- Scheduled follow-up draft workflow

## 9. Conclusion
InfluenceFlow AI demonstrates how AI and workflow automation can simplify influencer lead management and outreach while maintaining human oversight of email communication.