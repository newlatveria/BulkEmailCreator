# Email Template Examples

This document provides ready-to-use email templates for common scenarios. Copy and paste these into the Bulk Email Creator Pro.

## Table of Contents
1. [Project Update Template](#project-update-template)
2. [Event Invitation Template](#event-invitation-template)
3. [Newsletter Template](#newsletter-template)
4. [Invoice Reminder Template](#invoice-reminder-template)
5. [Welcome Email Template](#welcome-email-template)
6. [Meeting Reminder Template](#meeting-reminder-template)
7. [Survey Request Template](#survey-request-template)
8. [Product Launch Template](#product-launch-template)

---

## Project Update Template

### Use Case
Weekly or monthly project status updates to team members or clients.

### Sample Data File
Use: `examples/project-updates.csv`

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name
- **Merge Mode**: No merging (one email per person)

### Subject Template
```
{{ProjectName}} - Status Update
```

### Body Template
```
Hi {{Name}},

Here's your project update for {{ProjectName}}:

Project: {{ProjectName}}
Company: {{Company}}
Due Date: {{DueDate}}
Your Role: {{Role}}

Current Status:
[Add your status update here]

Next Steps:
[Add next steps here]

Please let me know if you have any questions or concerns.

Best regards,
Project Management Team
```

### Expected Result
Each person receives a personalized email with their specific project details.

---

## Event Invitation Template

### Use Case
Invite attendees to conference sessions. If using merge mode, combine multiple sessions for the same person.

### Sample Data File
Use: `examples/event-registration.csv`

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name
- **Merge Mode**: 
  - Option 1: "Merge same recipient" (one email with all sessions)
  - Option 2: "No merging" (separate email per session)

### Subject Template
```
Your Tech Conference 2024 Schedule
```

### Body Template (for Merge Mode)
```
Dear {{Name}},

You're registered for Tech Conference 2024! Here are your sessions:

[When merged, sessions will appear as numbered entries below]

Session: {{SessionName}}
Time: {{SessionTime}}
Location: {{Room}}

Important Information:
- Conference starts at 8:30 AM
- Badge pickup at Main Hall
- Lunch provided in Cafeteria
- Parking available in Lot C

We look forward to seeing you!

Tech Conference Team
```

### Expected Result
- **With merging**: Each person gets one email listing all their registered sessions
- **Without merging**: Each person gets separate emails for each session

---

## Newsletter Template

### Use Case
Monthly newsletter to all subscribers with identical content.

### Sample Data File
Use: `examples/newsletter-subscribers.csv`

### Configuration
- **Recipient Column**: Email
- **Merge Mode**: Multi-recipient with BCC (privacy maintained)

### Subject Template
```
Monthly Newsletter - February 2024
```

### Body Template
```
Hello!

Welcome to our February newsletter.

🌟 FEATURED ARTICLES

1. The Future of AI in Business
   Learn how artificial intelligence is transforming modern workplaces.

2. 5 Productivity Tips for Remote Teams
   Maximize your team's efficiency with these proven strategies.

3. New Product Launch: CloudSync Pro
   Introducing our latest cloud collaboration platform.

📅 UPCOMING EVENTS

- March 5: Webinar on Digital Marketing Trends
- March 12: Workshop on Data Analytics
- March 20: Product Demo: CloudSync Pro

💡 TIP OF THE MONTH

"Start your day by tackling your most challenging task first. The sense of accomplishment will energize you for the rest of the day."

🔗 QUICK LINKS
- Visit our blog: [URL]
- Follow us on Twitter: [URL]
- Join our community: [URL]

You're receiving this because you subscribed on {{SubscriptionDate}}.
Preferred topic: {{PreferredTopic}}

To unsubscribe, click here: [Unsubscribe Link]

Best regards,
The Newsletter Team
```

### Expected Result
One email sent to all subscribers with everyone in BCC (maintains privacy).

---

## Invoice Reminder Template

### Use Case
Send payment reminders for overdue invoices.

### Sample Data File
Use: `examples/invoice-reminders.csv`

### Configuration
- **Recipient Column**: Email
- **Name Column**: ContactName
- **Filters**: 
  - Column: DaysOverdue
  - Operator: Not Empty
  - (Or use "Greater than" if your tool supports it)

### Subject Template
```
Payment Reminder: Invoice {{InvoiceNumber}} - {{CompanyName}}
```

### Body Template
```
Dear {{ContactName}},

This is a friendly reminder regarding invoice {{InvoiceNumber}} for {{CompanyName}}.

Invoice Details:
- Invoice Number: {{InvoiceNumber}}
- Amount Due: ${{Amount}}
- Original Due Date: {{DueDate}}
- Days Overdue: {{DaysOverdue}}

Please arrange payment at your earliest convenience. If you have already sent payment, please disregard this reminder.

Payment Options:
- Online: [Payment Portal Link]
- Bank Transfer: [Account Details]
- Check: [Mailing Address]

If you have any questions or concerns about this invoice, please contact your account manager {{AccountManager}}.

Thank you for your business!

Accounts Receivable Team
[Company Name]
[Contact Information]
```

### Expected Result
Only people with overdue invoices receive the reminder (when filters are applied).

---

## Welcome Email Template

### Use Case
Welcome new customers, team members, or subscribers.

### Sample Data File
Create a CSV with: Name, Email, AccountNumber, StartDate, AccessLink

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name
- **Merge Mode**: No merging

### Subject Template
```
Welcome to [Company Name], {{Name}}!
```

### Body Template
```
Hi {{Name}},

Welcome to [Company Name]! We're thrilled to have you on board.

Your account has been created successfully:
- Account Number: {{AccountNumber}}
- Start Date: {{StartDate}}
- Access Link: {{AccessLink}}

Getting Started:
1. Log in to your account using the link above
2. Complete your profile information
3. Explore our features with this quick tour: [Tour Link]
4. Check out our knowledge base: [Knowledge Base Link]

Need Help?
- Email: support@company.com
- Phone: 1-800-XXX-XXXX
- Live Chat: Available 9 AM - 6 PM EST

We're here to help you succeed!

Best regards,
The [Company Name] Team
```

---

## Meeting Reminder Template

### Use Case
Remind attendees about upcoming meetings.

### Sample Data File
Create a CSV with: Name, Email, MeetingTitle, DateTime, Location, MeetingLink

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name

### Subject Template
```
Reminder: {{MeetingTitle}} - {{DateTime}}
```

### Body Template
```
Hi {{Name}},

This is a reminder about our upcoming meeting:

📅 Meeting: {{MeetingTitle}}
🕐 Date & Time: {{DateTime}}
📍 Location: {{Location}}
🔗 Join Link: {{MeetingLink}}

Agenda:
1. [Agenda item 1]
2. [Agenda item 2]
3. [Agenda item 3]

Please review the attached materials before the meeting.

If you cannot attend, please let me know as soon as possible.

See you there!

[Your Name]
```

---

## Survey Request Template

### Use Case
Request feedback from customers or employees.

### Sample Data File
Create a CSV with: Name, Email, PurchaseDate, ProductName, OrderNumber

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name

### Subject Template
```
We'd love your feedback on {{ProductName}}
```

### Body Template
```
Hi {{Name}},

Thank you for your recent purchase of {{ProductName}} (Order #{{OrderNumber}}).

We hope you're enjoying your purchase! We'd love to hear about your experience.

Could you take 2 minutes to complete our quick survey?

[Survey Link]

Your feedback helps us improve our products and services.

As a thank you for completing the survey, you'll receive a 10% discount code for your next purchase.

Thank you for being a valued customer!

Best regards,
Customer Experience Team

---
Order Details:
- Product: {{ProductName}}
- Order Number: {{OrderNumber}}
- Purchase Date: {{PurchaseDate}}
```

---

## Product Launch Template

### Use Case
Announce new product launch to customers or prospects.

### Sample Data File
Create a CSV with: Name, Email, Industry, CompanySize, PreviousProduct

### Configuration
- **Recipient Column**: Email
- **Name Column**: Name

### Subject Template
```
Introducing [New Product Name] - Perfect for {{Industry}}
```

### Body Template
```
Hi {{Name}},

Big news! We're excited to announce the launch of [New Product Name], designed specifically for companies in the {{Industry}} industry.

🚀 What's New?
- Feature 1: [Description]
- Feature 2: [Description]
- Feature 3: [Description]

Why You'll Love It:
✓ Benefit 1
✓ Benefit 2
✓ Benefit 3

Special Launch Offer:
As an existing customer who uses {{PreviousProduct}}, you get:
- 20% off for the first 3 months
- Free migration assistance
- Priority support

[CTA Button: Learn More]
[CTA Button: Schedule a Demo]

This offer expires on [Date], so don't miss out!

Have questions? Reply to this email or call us at [Phone Number].

Best regards,
The [Company Name] Team

P.S. - Companies with {{CompanySize}} employees have seen [specific benefit]. Want to learn how? [Link]
```

---

## Tips for Using These Templates

### Customization
1. Replace [bracketed content] with your actual information
2. Adjust formality based on your audience
3. Add your branding and signature
4. Include relevant links and contact information

### Variables
- Always use exact column names from your CSV
- Check the "Template Analysis" panel to verify variables
- Preview first email before generating all

### Testing
1. Test with a small sample (3-5 emails) first
2. Send to yourself to check formatting
3. Verify all links work
4. Check on both desktop and mobile email clients

### Best Practices
- Keep subject lines under 50 characters
- Front-load important information
- Use clear call-to-action buttons/links
- Include unsubscribe option for marketing emails
- Personalize beyond just name when possible

---

## Template Checklist

Before generating emails, verify:

- [ ] Subject template uses correct variable names
- [ ] Body template includes all necessary variables
- [ ] Variables are properly formatted: `{{VariableName}}`
- [ ] Greeting and signature are appropriate
- [ ] Links are included and correct
- [ ] Contact information is present
- [ ] Preview looks good
- [ ] Spelling and grammar checked
- [ ] Merge mode selected correctly
- [ ] Filters applied if needed

---

**Need more templates?** Check out our community repository or submit your own templates to help other users!
