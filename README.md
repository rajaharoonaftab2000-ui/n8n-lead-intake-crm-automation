# Lead Intake & CRM Automation with n8n

An automated lead intake and CRM workflow built with **n8n, HubSpot, Gmail, Telegram, and Google Calendar**.

This personal portfolio project demonstrates how a business can capture project enquiries through a web form, store them in a CRM, prepare a follow-up email, alert the team, and schedule a discovery call without manual data entry.

## Overview

Many businesses lose or delay leads because enquiries arrive in different places and must be copied into a CRM by hand. Follow-up emails, internal alerts, and meeting scheduling then depend on someone remembering to do them.

This workflow brings those tasks into one n8n automation. When a prospect submits the enquiry form, the workflow creates the CRM records, prepares a qualification email draft, notifies the team on Telegram, and books a discovery call in Google Calendar.

## What the Workflow Includes

- An n8n web form where prospects describe their project.
- Collection of contact details, company details, service required, budget, desired start time, and project requirements.
- A project reference for each enquiry to keep records easy to trace.
- Lead scoring and rating to help the team prioritise new enquiries.
- Automatic creation of the company, contact, and deal in HubSpot.
- A deal pipeline with stages such as New Inquiry, Qualified, and Meeting Booked.
- A qualification email prepared as a Gmail draft for review.
- A Telegram notification summarising the processed lead.
- A discovery call event created in Google Calendar.

## Workflow Process

1. **Receive the enquiry:** A prospect fills in the "Tell us about your project" form.
2. **Prepare the data:** The workflow reads the submitted fields and organises them for the next steps.
3. **Score the lead:** The lead receives a score and rating based on the submitted information, such as budget and timeline.
4. **Update the CRM:** The company, contact, and deal are created in HubSpot and placed in the sales pipeline.
5. **Prepare the follow-up:** A qualification email is saved as a draft in Gmail so it can be reviewed before sending.
6. **Alert the team:** A Telegram message shows the lead's name, company, service, rating, score, budget, and deal reference.
7. **Schedule the call:** A discovery call event is created in Google Calendar.
8. **Track progress:** The deal can be reviewed in the HubSpot pipeline as the lead moves forward.

## Connected Tools

| Tool | Purpose |
|---|---|
| n8n Form | Collect the prospect's details and project requirements |
| Lead Scoring | Calculate a score and rating for each enquiry |
| HubSpot Companies | Create or update the company record |
| HubSpot Contacts | Create the contact linked to the company |
| HubSpot Deals | Create the deal and place it in the pipeline |
| Gmail Draft | Prepare the qualification email for review |
| Telegram Alert | Notify the team about the processed lead |
| Google Calendar Event | Create the discovery call booking |

## Technology Stack

| Technology | Role |
|---|---|
| n8n | Workflow orchestration and integrations |
| n8n Form Trigger | Lead capture form |
| HubSpot CRM | Companies, contacts, deals, and pipeline stages |
| Gmail | Qualification email drafts |
| Telegram Bot API | Internal lead notifications |
| Google Calendar | Discovery call scheduling |

## Form Fields

The enquiry form collects:

- Full name
- Email address
- Phone number
- Company name
- Company website
- Project reference
- Service required
- Budget in USD
- Desired start (in days)
- Project requirements

## Demonstrated Scenario

The recorded demo shows a sample lead moving through the full workflow.

During the demo:

- The n8n workflow canvas is shown with the lead intake flow.
- A sample prospect submits the project enquiry form.
- A new company and deal appear in HubSpot under the New Inquiry stage.
- A qualification email draft is prepared in Gmail.
- A Telegram message summarises the processed lead with its score, rating, budget, and deal reference.
- A discovery call appears in Google Calendar.
- The HubSpot deals board shows the deal progressing through the pipeline.

The demo uses sample data. Each branch of the workflow should be tested separately before live use.

## Business Applications

This approach can help businesses:

- Capture every enquiry in a consistent format.
- Remove manual data entry between forms and the CRM.
- Respond to new leads faster with a prepared follow-up email.
- Help the sales team prioritise leads with scoring and ratings.
- Keep the whole team informed through instant Telegram alerts.
- Move leads to a booked discovery call with less back and forth.

These are intended applications of the workflow, not measured business results from a live client deployment.

## Setup Requirements

To adapt this project, you need:

- An n8n instance (cloud or self-hosted).
- A HubSpot account with API access for companies, contacts, and deals.
- A Gmail account connected to n8n.
- A Telegram bot and the chat ID that should receive alerts.
- A Google Calendar for discovery calls.
- Your own service list, scoring rules, and pipeline stages.

Credentials must be configured in your own n8n environment. No API keys or tokens are included in this repository.

## Configuration

1. Import the workflow JSON file into n8n.
2. Connect your HubSpot, Gmail, Telegram, and Google Calendar credentials.
3. Review the form fields and update the service options.
4. Adjust the lead scoring rules and rating thresholds to match your business.
5. Match the HubSpot pipeline and deal stages to your own pipeline.
6. Edit the qualification email template to match your tone and offer.
7. Set the Telegram chat that should receive lead alerts.
8. Select the Google Calendar and set the call duration and time zone.
9. Test the workflow with sample data before activating it.

## Testing Checklist

Before using the workflow with real leads, test:

- A complete form submission with all fields filled in.
- Missing or incorrectly formatted email and phone values.
- Very low and very high budgets to check scoring and ratings.
- The same lead submitting the form twice.
- A company that already exists in HubSpot.
- Gmail draft creation and its content.
- Telegram alert delivery.
- Calendar event creation and time zone handling.
- Failures in HubSpot, Gmail, Telegram, or Google Calendar.

## Scope and Limitations

- This is a personal portfolio demonstration using sample data.
- Lead scoring rules are examples and should be adjusted for each business.
- The follow-up email is prepared as a draft for review, not sent automatically.
- Duplicate leads and existing HubSpot records need explicit matching rules before live deployment.
- Calendar booking does not check the prospect's availability unless that logic is added.
- If one service fails, the other records may be left incomplete, so error handling should be added for live use.
- HubSpot, n8n hosting, and email limits depend on the plans used.
- Payments, a custom dashboard, and voice or WhatsApp channels are outside this project's scope.

## My Contribution

I designed the n8n workflow, built the lead capture form, configured the scoring logic and CRM integration, connected Gmail, Telegram, and Google Calendar, and tested the demonstrated lead scenario.

The project combines form-based lead capture with practical CRM and scheduling integrations.

## Author

**Haroon AI Automation**

Building practical n8n workflows, AI integrations, and business automations.

## Demo Video

Watch the lead intake workflow in action:

[Watch the Lead_Intake_Automation_90s.mp4](./Lead_Intake_Automation_90s.mp4)
