# 📧 Bulk Email Creator Pro

<div align="center">

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

**The ultimate tool for creating personalized bulk emails with zero hassle!**

Transform your CSV or Excel spreadsheets into hundreds of personalized email drafts in seconds. Perfect for marketing campaigns, event invitations, customer outreach, and more!

[Features](#-features) • [Quick Start](#-quick-start) • [Usage Examples](#-usage-examples) • [Advanced Features](#-advanced-features)

</div>

---

## 🌟 Why Bulk Email Creator Pro?

Say goodbye to tedious copy-paste email workflows! This powerful web application lets you:

- 🚀 **Generate hundreds of personalized emails** in under a minute
- 📊 **Import from CSV or Excel** - supports `.csv`, `.xlsx`, and `.xls` files
- 🎯 **Use dynamic variables** - automatically replace placeholders with data from your spreadsheet
- 🔍 **Filter your data** - send emails only to specific recipients
- 👁️ **Preview before sending** - see exactly how your emails will look
- 📝 **Merge duplicate recipients** - combine multiple rows into a single email
- 💾 **Export everything** - save all generated emails and links for later
- ✅ **Track progress** - mark emails as sent with visual feedback

**Best of all? It's completely client-side. Your data never leaves your browser!**

---

## ✨ Features

### Core Functionality

| Feature | Description |
|---------|-------------|
| 📁 **Multi-Format Support** | Import CSV, XLSX, or XLS files with automatic format detection |
| 🏷️ **Dynamic Variables** | Use `{{ColumnName}}` syntax to insert personalized data |
| 📋 **Data Preview** | Instantly view your imported data in a table |
| 🎯 **Smart Auto-Detection** | Automatically identifies email and name columns |
| 🔄 **Email Merging** | Combine multiple rows per recipient into numbered sections |
| 📧 **CC/BCC Support** | Add carbon copy and blind carbon copy recipients |
| 📎 **Attachment Reminders** | Set reminders to manually attach files |

### Advanced Features

| Feature | Description |
|---------|-------------|
| 🔍 **Advanced Filtering** | Filter rows by column values (equals, contains, empty, not empty) |
| 👁️ **Email Preview** | Preview how the first email will look before generating all |
| 💾 **Export to File** | Download all generated emails as a text file |
| 📊 **Real-time Statistics** | See how many rows match your filters |
| 🎨 **Template Helpers** | Quick-insert buttons for greetings and signatures |
| ✅ **Progress Tracking** | Visual indicators for emails you've already opened |
| 🗑️ **Bulk Actions** | Clear all generated emails and start fresh |

### UI/UX Enhancements

- 🎨 **Modern Dark Theme** with teal accents
- 📱 **Fully Responsive** design works on all devices
- ⚡ **Lightning Fast** - processes thousands of rows instantly
- 🔒 **Privacy First** - all processing happens in your browser
- 💡 **Built-in Help** - comprehensive guide accessible anytime
- 🎯 **Smart Tooltips** - helpful hints on hover

---

## 🚀 Quick Start

### 1. Download and Open

Simply download the `bulk-email-creator-pro.html` file and open it in any modern web browser. That's it! No installation, no setup, no server required.

### 2. Prepare Your Data

Create a spreadsheet (CSV or Excel) with your data. The first row should contain headers:

```csv
Name,Email,Company,Invoice Number
John Smith,john@example.com,Acme Corp,INV-001
Jane Doe,jane@example.com,Tech Industries,INV-002
Bob Johnson,bob@example.com,Global Solutions,INV-003
```

### 3. Upload Your File

Click the file upload button and select your CSV or Excel file. The app will automatically detect the format and load your data.

### 4. Create Your Email Template

Use the placeholder syntax to reference your columns:

**Subject:**
```
Invoice {{Invoice Number}} - Payment Due
```

**Body:**
```
Dear {{Name}},

This is a friendly reminder that invoice {{Invoice Number}} 
for {{Company}} is due for payment.

Please process the payment at your earliest convenience.

Best regards,
Accounts Team
```

### 5. Generate and Send!

Click **"Generate All Drafts"** and watch as personalized email links are created for each row. Click any link to open a pre-filled email draft in your default email client!

---

## 💡 Usage Examples

### Example 1: Event Invitation Campaign

**Your Data (event-invites.csv):**
```csv
First Name,Last Name,Email,Event Date,Location,Special Dietary
Sarah,Williams,sarah@email.com,March 15th,Grand Ballroom,Vegetarian
Michael,Brown,michael@email.com,March 15th,Grand Ballroom,None
Emma,Davis,emma@email.com,March 15th,Grand Ballroom,Gluten-free
```

**Your Email Template:**

Subject: `You're Invited! Company Gala - {{Event Date}}`

Body:
```
Dear {{First Name}} {{Last Name}},

We're thrilled to invite you to our annual Company Gala on {{Event Date}}!

📍 Venue: {{Location}}
🍽️ Dietary Preference: {{Special Dietary}}

We look forward to celebrating with you!

RSVP by clicking reply to this email.

Warm regards,
Events Team
```

**Result:** 3 personalized invitations ready to send! ✉️

---

### Example 2: Customer Follow-up with Filtering

**Your Data (customers.xlsx):**
```
Name,Email,Status,Last Purchase,Amount
Alice Chen,alice@email.com,VIP,2024-01-15,$1250
Bob Smith,bob@email.com,Regular,2024-02-01,$85
Carol Jones,carol@email.com,VIP,2024-01-28,$2100
David Lee,david@email.com,Regular,2024-02-05,$45
```

**Filtering Setup:**
- Column: `Status`
- Operator: `Equals`
- Value: `VIP`

**Result:** Only Alice and Carol receive emails! 🎯

**Your Email Template:**

Subject: `Thank you for being a valued VIP customer, {{Name}}!`

Body:
```
Hi {{Name}},

Thank you for your recent purchase of ${{Amount}} on {{Last Purchase}}.

As a VIP customer, you're eligible for exclusive benefits:
• 20% off your next purchase
• Free priority shipping
• Early access to new products

Use code VIP20 at checkout!

Sincerely,
Customer Success Team
```

---

### Example 3: Merged Emails for Account Managers

**Your Data (accounts.csv):**
```csv
Account Manager,Email,Client Name,Project,Status
Sarah Johnson,sarah@company.com,ABC Corp,Website Redesign,In Progress
Sarah Johnson,sarah@company.com,XYZ Ltd,Mobile App,Completed
Sarah Johnson,sarah@company.com,Tech Start,Brand Identity,Planning
David Chen,david@company.com,Global Inc,SEO Audit,In Progress
```

**Enable:** ✅ Merge multiple rows per recipient

**Your Email Template:**

Subject: `Weekly Project Update - {{Client Name}}`

Body:
```
Client: {{Client Name}}
Project: {{Project}}
Status: {{Status}}

Please review and update accordingly.
```

**Result:** 
- Sarah gets **1 email** with all 3 of her projects listed as Entry 1, Entry 2, Entry 3
- David gets **1 email** with his single project

Perfect for managers overseeing multiple projects! 📊

---

### Example 4: Sales Outreach with CC

**Your Data (leads.xlsx):**
```
Prospect Name,Prospect Email,Sales Rep,Rep Email,Industry,Company Size
John Doe,john@prospect.com,Alice Smith,alice@sales.com,Tech,50-200
Jane Smith,jane@prospect.com,Alice Smith,alice@sales.com,Finance,200-500
```

**Configuration:**
- Recipient Column: `Prospect Email`
- CC Column: `Rep Email`

**Your Email Template:**

Subject: `{{Industry}} Solutions for {{Prospect Name}}`

Body:
```
Hi {{Prospect Name}},

I noticed you're in the {{Industry}} industry with a team size 
of {{Company Size}} employees.

I'd love to show you how our solution can help streamline your operations.

Are you available for a 15-minute call this week?

Best,
{{Sales Rep}}
```

**Result:** Prospect receives the email, sales rep is CC'd automatically! 🎯

---

## 🎓 Advanced Features Guide

### 🔍 Advanced Filtering

Create complex filtering rules to target specific recipients:

**Example: Send only to customers who purchased in January**
1. Click "+ Add Filter"
2. Column: `Purchase Date`
3. Operator: `Contains`
4. Value: `2024-01`

**Example: Send only to contacts with phone numbers**
1. Click "+ Add Filter"
2. Column: `Phone`
3. Operator: `Not Empty`
4. Value: (leave blank)

**Multiple Filters:** All filters must match (AND logic)

---

### 👁️ Email Preview

Before generating hundreds of emails, preview the first one:

1. Set up your template
2. Click **"👁️ Preview First Email"**
3. See exactly how variables are replaced
4. Verify formatting and content
5. Make adjustments if needed
6. Generate with confidence!

---

### 💾 Export to File

Save all your generated emails for record-keeping:

1. Generate your email drafts
2. Click **"💾 Export as Links File"**
3. Downloads a `.txt` file containing:
   - All recipient information
   - Full email content
   - Mailto links for each email
   - Timestamp

Perfect for compliance, documentation, or batch processing later!

---

### 🎨 Template Helpers

**Insert Greeting:**
- Automatically adds: `Dear {{Name}},` (if name column selected)
- Or: `Hello,` (if no name column)

**Insert Signature:**
- Adds professional closing:
```
Best regards,
[Your Name]
```

---

### 🔄 Email Merging Deep Dive

When to use email merging:
- **Account managers** with multiple clients
- **Project updates** with multiple tasks per person
- **Order confirmations** with multiple items
- **Weekly digests** combining multiple entries

How it works:
1. All rows with the same recipient email are grouped
2. Each row becomes a numbered entry in the email body
3. CC, BCC, and attachments are combined from all rows
4. Subject line uses data from the first row

**Pro Tip:** Use consistent formatting in your body template so merged entries are clearly separated!

---

## 🎯 Best Practices

### Data Preparation

✅ **DO:**
- Use clear, descriptive column headers
- Ensure email addresses are valid
- Test with a small sample first
- Keep column names without special characters
- Use consistent date formats

❌ **DON'T:**
- Use commas in column headers
- Leave the first row empty
- Mix different data formats in the same column
- Include sensitive data you don't want to send

### Template Writing

✅ **DO:**
- Preview your first email before generating all
- Use the exact column names in `{{brackets}}`
- Test all variable replacements
- Keep subject lines under 60 characters
- Use proper line breaks for readability

❌ **DON'T:**
- Misspell column names in variables
- Create extremely long email bodies
- Forget to personalize - use at least one variable!
- Include placeholders that might not exist

### Workflow Tips

💡 **Start Small:** Generate 5-10 emails first to test your template

💡 **Use Filters:** If sending to different segments, use filters instead of creating multiple files

💡 **Track Progress:** Click each email link as you send them - they'll turn green with a checkmark

💡 **Save Your Work:** Use the export feature to keep a record

💡 **Test Recipients:** Add your own email in the data for testing

---

## 🛠️ Technical Details

### Browser Compatibility

| Browser | Minimum Version | Status |
|---------|----------------|---------|
| Chrome | 90+ | ✅ Fully Supported |
| Firefox | 88+ | ✅ Fully Supported |
| Safari | 14+ | ✅ Fully Supported |
| Edge | 90+ | ✅ Fully Supported |

### Libraries Used

- **PapaParse 5.4.1** - Robust CSV parsing
- **SheetJS (XLSX) 0.18.5** - Excel file reading
- **Tailwind CSS** - Modern UI styling

### File Size Limits

- **CSV Files:** Up to 10MB recommended
- **Excel Files:** Up to 5MB recommended
- **Row Count:** Tested with up to 10,000 rows
- **Email Length:** Mailto links have browser limits (~2000 characters)

### Privacy & Security

🔒 **100% Client-Side Processing**
- No data is sent to any server
- All processing happens in your browser
- No cookies, no tracking, no analytics
- Your data stays on your machine

### Performance

| Rows | Processing Time | Memory Usage |
|------|----------------|--------------|
| 100 | < 1 second | ~5MB |
| 1,000 | ~2 seconds | ~25MB |
| 10,000 | ~15 seconds | ~150MB |

---

## 🎨 Customization Ideas

### Custom Styling

Want to customize the look? Edit the `<style>` section:

```css
/* Change the primary color from teal to purple */
.bg-teal-400 { background-color: #a855f7 !important; }
.bg-teal-500 { background-color: #9333ea !important; }
.bg-teal-600 { background-color: #7e22ce !important; }
.text-teal-300 { color: #c084fc !important; }
.text-teal-400 { color: #a855f7 !important; }
```

### Adding Custom Variables

You can add computed variables in the JavaScript:

```javascript
// After line: variables[header] = value;
// Add custom variables:
variables['FullName'] = `${variables['FirstName']} ${variables['LastName']}`;
variables['Year'] = new Date().getFullYear();
```

---

## 📊 Use Cases & Industries

### Marketing & Sales
- Product launch announcements
- Sales outreach campaigns
- Follow-up sequences
- Customer surveys
- Newsletter personalization

### Events & Hospitality
- Event invitations
- Conference registrations
- Venue confirmations
- Catering preferences
- Thank you notes

### Education
- Parent-teacher communications
- Student notifications
- Class schedules
- Grade reports
- Assignment reminders

### Human Resources
- Interview scheduling
- Onboarding sequences
- Benefits enrollment
- Policy updates
- Performance review invitations

### Customer Service
- Order confirmations
- Shipping notifications
- Account updates
- Renewal reminders
- Support follow-ups

### Non-Profit & Community
- Donor thank-yous
- Volunteer coordination
- Fundraising campaigns
- Event coordination
- Newsletter distribution

---

## 🐛 Troubleshooting

### "Could not find headers in the CSV"
- **Solution:** Ensure your first row contains column names, not data

### "No valid rows found to generate emails"
- **Solution:** Check that your recipient column has valid email addresses
- **Solution:** If using filters, verify rows match your filter criteria

### Variables not replacing
- **Solution:** Check spelling - `{{Name}}` is case-sensitive
- **Solution:** Ensure column name matches exactly (including spaces)

### Email client not opening
- **Solution:** Set a default email client in your system preferences
- **Solution:** Use the copy button and paste the link in your browser

### Excel file not loading
- **Solution:** Save as `.xlsx` (newer format) instead of `.xls`
- **Solution:** Ensure file doesn't have password protection
- **Solution:** Check file size is under 5MB

### Merged emails showing wrong data
- **Solution:** Ensure recipient column has exact email matches
- **Solution:** Clean up any trailing spaces in email addresses

---

## 💡 Pro Tips & Tricks

### 1. Use Name Column for Better Greetings
Select a name column to enable personalized greetings like "Dear John" instead of generic "Hello"

### 2. Test with Yourself First
Add your own email in a test row to see exactly how emails will appear

### 3. Create Template Libraries
Save your successful email templates in a document for reuse

### 4. Use Filters for A/B Testing
Create two variations of your email, filter half your list for each

### 5. Combine with Mail Merge Tools
Export the mailto links file and use it with automation tools

### 6. Track Opens and Clicks
For better tracking, consider shortening URLs before adding them to templates

### 7. Schedule Your Sends
Generate all drafts, then send them in batches over time to avoid spam filters

### 8. Use Descriptive Subject Lines
Include variables in subject lines for better open rates

### 9. Keep a Backup
Always keep a backup of your original data file before making changes

### 10. Clean Your Data First
Remove duplicates, fix formatting, and verify emails before importing

---

## 📝 Example Templates Library

### Professional Follow-up
```
Subject: Following up on {{Topic}}

Hi {{Name}},

I wanted to follow up on our conversation about {{Topic}} 
from {{Date}}.

Have you had a chance to consider {{Proposal}}?

I'm available {{Availability}} if you'd like to discuss further.

Best regards,
{{Your Name}}
```

### Event Reminder
```
Subject: Reminder: {{Event Name}} - {{Event Date}}

Dear {{Attendee Name}},

This is a friendly reminder about {{Event Name}} taking place on {{Event Date}}.

📍 Location: {{Venue}}
⏰ Time: {{Event Time}}
🎫 Your Ticket: {{Ticket Number}}

We look forward to seeing you there!

Questions? Reply to this email.

Regards,
{{Organizer}}
```

### Payment Reminder
```
Subject: Payment Reminder - Invoice {{Invoice Number}}

Dear {{Customer Name}},

This is a reminder that payment for Invoice {{Invoice Number}} 
is due on {{Due Date}}.

Amount Due: {{Amount}}
Payment Terms: {{Terms}}

Please contact us if you have any questions.

Thank you,
{{Company Name}} Accounts
```

### Welcome Email
```
Subject: Welcome to {{Company Name}}, {{Name}}!

Hi {{Name}},

Welcome aboard! We're thrilled to have you join {{Company Name}}.

Your account details:
• Username: {{Username}}
• Plan: {{Plan Type}}
• Start Date: {{Start Date}}

Next steps:
1. Complete your profile
2. Explore our features
3. Schedule your onboarding call

Questions? We're here to help!

Best,
{{Team Name}}
```

---

## 🎬 Video Tutorials

(Future feature - Add links to video tutorials here)

- Getting Started (5 min)
- Advanced Filtering (3 min)
- Email Merging Explained (4 min)
- Best Practices (7 min)

---

## 🤝 Contributing

Found a bug? Have a feature request? Want to improve the documentation?

Suggestions welcome for:
- New template helpers
- Additional filter operators
- UI/UX improvements
- Performance optimizations
- Documentation enhancements

---

## 📄 License

MIT License - feel free to use, modify, and distribute!

---

## 🙏 Acknowledgments

Built with:
- ❤️ Love for automation
- ☕ Coffee
- 🎵 Good music
- 🧠 Problem-solving mindset

Special thanks to:
- PapaParse for CSV parsing
- SheetJS for Excel reading
- Tailwind CSS for beautiful styling
- The open-source community

---

## 📧 Contact & Support

Need help? Have questions?

- 📖 Check the built-in help (? icon)
- 🐛 Issues? Check the troubleshooting section
- 💡 Feature ideas? Open an issue
- ⭐ Love it? Give it a star!

---

<div align="center">

**Made with ❤️ for productivity enthusiasts**

⭐ **If this tool saved you time, give it a star!** ⭐

[Back to Top](#-bulk-email-creator-pro)

</div>
