# Bulk Email Creator Pro - Enhanced Edition

A powerful, browser-based tool for generating personalized email drafts from CSV or Excel files. Create hundreds of customized emails in seconds with advanced merge options, template management, and accessibility features.

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![No Backend Required](https://img.shields.io/badge/backend-none-orange)

## ✨ Features

### Core Functionality
- 📁 **File Support**: Upload CSV, XLSX, or XLS files
- 🏷️ **Variable Substitution**: Use `{{ColumnName}}` placeholders for personalization
- 📧 **Email Fields**: Support for TO, CC, BCC, Subject, Body, and Attachments
- 🔍 **Data Filtering**: Apply filters to target specific recipients
- 👁️ **Live Preview**: See how your first email will look before generating all
- 💾 **Multiple Export Formats**: Export to TXT or CSV

### Advanced Features
- 🔄 **Three Merge Modes**:
  - No merging (one email per row)
  - Merge same recipient (combine rows for same email address)
  - Multi-recipient (all recipients in one email with shared body)
- 📝 **Template Management**: Save and load email templates
- ⏪ **Undo/Redo**: Restore cleared emails with Ctrl+Z
- ✅ **Email Validation**: Real-time validation with invalid email detection
- ⌨️ **Keyboard Shortcuts**: Efficient workflow with hotkeys
- 📊 **Statistics Dashboard**: Track rows, filters, variables, and more
- 🎨 **Modern UI**: Clean, dark-themed interface with toast notifications

### Accessibility Features
- ♿ **Screen Reader Support**: ARIA labels and skip-to-content link
- ⌨️ **Full Keyboard Navigation**: All features accessible via keyboard
- 🔍 **Focus Indicators**: Clear visual focus states
- 📱 **Responsive Design**: Works on desktop, tablet, and mobile
- 🔧 **Sticky Sidebar**: Important info stays visible while scrolling

## 🚀 Quick Start

1. **Download**: Save `bulk-email-creator-enhanced.html` to your computer
2. **Open**: Double-click the file to open in your web browser (Chrome, Firefox, Edge, Safari)
3. **Upload Data**: Click "Upload your file" and select your CSV or Excel file
4. **Configure**: Set up recipient column, subject, and body templates
5. **Generate**: Click "Generate All Drafts" to create your emails
6. **Send**: Click any email link to open in your default email client

No installation, no server, no backend required! Everything runs locally in your browser.

## 📖 Detailed Usage Guide

### 1. Preparing Your Data File

Your CSV or Excel file should have:
- **First row**: Column headers (e.g., Name, Email, Company)
- **Subsequent rows**: Data for each recipient

Example CSV:
```csv
Name,Email,Company,Role
John Smith,john@example.com,Acme Corp,Manager
Jane Doe,jane@example.com,Tech Inc,Developer
Bob Johnson,bob@example.com,Design Co,Designer
```

### 2. Uploading Your File

1. Click the **"Upload your file"** button
2. Select your CSV, XLSX, or XLS file
3. Wait for the file to load (you'll see a success message)
4. Review the **Data Preview** to ensure it loaded correctly

**Tip**: The preview shows the first 3 rows. Check that columns aligned properly.

### 3. Using Variables

Variables are placeholders that get replaced with data from each row.

#### How to Use Variables:
1. Look at the **"Available Variables"** section
2. Click any variable to copy it (e.g., `{{Name}}`)
3. Paste into your subject or body template

#### Example:
**Subject Template**: `Hello {{Name}}, your invoice is ready`

**For John Smith**: `Hello John Smith, your invoice is ready`
**For Jane Doe**: `Hello Jane Doe, your invoice is ready`

#### Best Practices:
- ✅ Use exact column names with proper capitalization
- ✅ Check the "Template Analysis" panel to see which variables are detected
- ✅ Green badges = used in template, Gray badges = available but unused
- ❌ Avoid typos in variable names (they won't be replaced)

### 4. Configuring Email Settings

#### Recipient Column (Required)
Select the column containing email addresses. The tool will auto-detect columns with "email" or "mail" in the name.

#### Name Column (Optional)
Select the column with recipient names for greeting insertion.

#### CC Recipients
You can add CC recipients in two ways:
1. **From spreadsheet**: Select a column containing CC emails (different per row)
2. **Manual entry**: Type email addresses that will be CC'd on ALL emails
   - Press Enter, comma, or space to add each email
   - Both methods can be combined

#### BCC Recipients
Works the same as CC - from spreadsheet column and/or manual entry.

#### Subject Template
Enter your subject line with variables. Example:
```
Your {{Month}} invoice from {{Company}}
```

#### Body Template
Enter your email body with variables. Use the helper buttons:
- **Insert Greeting**: Adds `Dear {{Name}},` (or `Hello,` if no name column)
- **Insert Signature**: Adds professional closing

Example body:
```
Dear {{Name}},

Your account at {{Company}} has been activated. Your account number is {{AccountNumber}}.

If you have any questions, please don't hesitate to reach out.

Best regards,
Customer Success Team
```

#### Attachments Column (Optional)
Select a column that contains attachment filenames. This will add a reminder in each email (you'll still need to attach files manually when sending).

### 5. Understanding Merge Modes

#### Mode 1: No Merging (Default)
- Creates one email per row
- Best for: Individual, personalized communications

**Example**: 100 rows = 100 separate email drafts

#### Mode 2: Merge Same Recipient
- Combines multiple rows with the same email address
- Creates numbered sections in the body

**Example**: 
If you have:
```
john@example.com, Item A
john@example.com, Item B
jane@example.com, Item C
```

You get **2 emails**:
- One to john@example.com with sections for Item A and Item B
- One to jane@example.com with Item C

**Use cases**:
- Weekly status reports with multiple updates
- Order confirmations with multiple items
- Task assignments for the same person

#### Mode 3: Multi-Recipient (New!)
- Combines ALL recipients into ONE email
- Uses first row's data for variable substitution
- Choose TO or BCC placement

**TO Field Option**: All recipients visible to each other
```
TO: john@example.com, jane@example.com, bob@example.com
```

**BCC Field Option**: Recipients hidden from each other
```
TO: john@example.com
BCC: jane@example.com, bob@example.com
```

**Example**: 50 rows = 1 email with 50 recipients

**Use cases**:
- Company-wide announcements
- Newsletter broadcasts
- Team updates
- Event invitations
- Mass notifications with identical content

**Important**: Variables are filled from the first row only. Use this mode when the message content is the same for everyone.

### 6. Filtering Data

Apply filters to generate emails only for specific rows.

#### How to Add Filters:
1. Click **"+ Add Filter"**
2. Select a column
3. Choose an operator:
   - **Equals**: Exact match
   - **Contains**: Partial match
   - **Not Empty**: Has any value
   - **Empty**: Has no value
4. Enter a value (except for Empty/Not Empty)

#### Filter Examples:

**Example 1**: Only send to managers
- Column: `Role`
- Operator: `Equals`
- Value: `Manager`

**Example 2**: Only send to people with a phone number
- Column: `Phone`
- Operator: `Not Empty`

**Example 3**: Only send to New York contacts
- Column: `City`
- Operator: `Contains`
- Value: `New York`

#### Multiple Filters:
All filters must match (AND logic). A row must pass all filters to be included.

**Tip**: The filter stats show how many rows match: `45 of 100 rows match filters`

### 7. Preview Before Generating

Before creating all emails, preview the first one:

1. Click **"👁️ Preview First Email"** (or press Ctrl+P)
2. Review the TO, CC, BCC, Subject, and Body
3. Check that variables were replaced correctly
4. Close the preview and adjust your template if needed

**Why preview?**
- Catch typos in variable names
- Verify formatting looks good
- Test your message before generating hundreds of emails

### 8. Generating Email Drafts

1. Click **"✉️ Generate All Drafts"** (or press Ctrl+G)
2. Wait for processing (progress bar appears at top)
3. Review generated emails in the list

Each email draft shows:
- Recipient email address
- CC/BCC if applicable
- Subject line
- Special indicators (Merged, Multi-recipient, etc.)
- Attachment reminders

#### Email Actions:
- **Click the email**: Opens in your default email client
- **Copy button** (📋): Copies the mailto link to clipboard
- **Variables button** (▼): Shows all data for that email

**After opening**: The email turns green with a ✓ checkmark so you can track which ones you've sent.

### 9. Exporting Emails

#### Export to TXT
- Click **"💾 Export TXT"**
- Downloads a text file with all email details
- Includes mailto links and full content
- Good for: Record keeping, backup, manual processing

#### Export to CSV
- Click **"📊 Export CSV"**
- Downloads a spreadsheet with columns: To, CC, BCC, Subject, Body, Attachments, Mailto Link
- Good for: Further processing, mail merge tools, CRM import

### 10. Template Management

Save time by saving your frequently used email templates.

#### Saving a Template:
1. Set up your subject, body, and settings
2. Click **"💾 Save Template"** (or press Ctrl+S)
3. Enter a name for your template
4. Click OK

**What gets saved:**
- Subject and body text
- Column selections (recipient, name, CC, BCC)
- Manual CC/BCC emails
- Merge mode settings
- All configuration

#### Loading a Template:
1. Click **"📂 Load Template"**
2. Browse your saved templates
3. Click a template card to load it
4. Delete templates you no longer need with the trash icon

**Use cases:**
- Monthly newsletter template
- Invoice notification template
- Welcome email template
- Meeting reminder template

### 11. Keyboard Shortcuts

Speed up your workflow with these shortcuts:

| Shortcut | Action |
|----------|--------|
| `Ctrl/Cmd + G` | Generate all emails |
| `Ctrl/Cmd + P` | Preview first email |
| `Ctrl/Cmd + S` | Save current template |
| `Ctrl/Cmd + Z` | Undo last clear |
| `?` | Toggle help panel |

**Note**: Ctrl for Windows/Linux, Cmd (⌘) for Mac

### 12. Undo Feature

Made a mistake? Undo is here to help.

1. If you accidentally click **"Clear All"**, press **Ctrl+Z** or click the **Undo button** (↶)
2. Your emails are restored
3. Up to 10 undo states are saved

**Tip**: The undo button is disabled when there's nothing to undo.

## 🎯 Common Use Cases & Examples

### Use Case 1: Weekly Status Reports

**Scenario**: Send personalized weekly reports to team members

**Data File**:
```csv
Name,Email,TasksCompleted,HoursWorked,NextWeek
Alice,alice@company.com,12,40,Project A kickoff
Bob,bob@company.com,8,35,Client meeting prep
Carol,carol@company.com,15,42,Code review session
```

**Subject**: `Your Weekly Report - Week of {{Date}}`

**Body**:
```
Hi {{Name}},

Here's your summary for this week:
- Tasks Completed: {{TasksCompleted}}
- Hours Worked: {{HoursWorked}}

Next week's priority: {{NextWeek}}

Great work!
```

**Settings**: No merging, one email per team member

### Use Case 2: Event Invitations with RSVP

**Scenario**: Invite clients to a product launch event

**Data File**:
```csv
Name,Email,Company,VIPStatus
John Smith,john@acme.com,Acme Corp,Yes
Jane Doe,jane@techco.com,Tech Co,No
```

**Subject**: `You're Invited: Product Launch Event{{#if VIPStatus}} - VIP Access{{/if}}`

**Body**:
```
Dear {{Name}},

We're excited to invite you to our annual product launch event!

Company: {{Company}}
{{#if VIPStatus}}VIP Access: Early entry at 5:00 PM{{/if}}

Please RSVP by clicking here: [RSVP Link]

Looking forward to seeing you!
```

**Settings**: No merging

### Use Case 3: Monthly Newsletter

**Scenario**: Send newsletter to all subscribers

**Data File**:
```csv
Email,Subscribed
subscriber1@email.com,Yes
subscriber2@email.com,Yes
subscriber3@email.com,Yes
...
```

**Subject**: `Newsletter - February 2024`

**Body**:
```
Hello Subscriber,

Welcome to our February newsletter!

[Newsletter content here - same for everyone]

Unsubscribe: [Link]
```

**Settings**: 
- **Merge Mode**: Multi-recipient with BCC
- Result: One email with all subscribers in BCC (privacy maintained)

### Use Case 4: Order Confirmations with Multiple Items

**Scenario**: Customer ordered multiple items, send one confirmation

**Data File**:
```csv
Email,OrderNumber,Item,Quantity,Price
customer@email.com,12345,Widget A,2,29.99
customer@email.com,12345,Widget B,1,49.99
customer@email.com,12345,Widget C,3,19.99
```

**Subject**: `Order Confirmation #{{OrderNumber}}`

**Body**:
```
Thank you for your order!

Order Number: {{OrderNumber}}

Items will be listed below (from merged rows)

Shipping information will be sent separately.
```

**Settings**: 
- **Merge Mode**: Merge same recipient
- Result: One email with all three items listed in numbered sections

### Use Case 5: Follow-up Emails with Filters

**Scenario**: Follow up only with contacts who haven't responded

**Data File**:
```csv
Name,Email,Responded,LastContact
Alice,alice@email.com,No,2024-01-15
Bob,bob@email.com,Yes,2024-01-20
Carol,carol@email.com,No,2024-01-10
```

**Filter Setup**:
- Column: `Responded`
- Operator: `Equals`
- Value: `No`

**Result**: Emails generated only for Alice and Carol

## ♿ Accessibility Features

### For Screen Reader Users

- **Skip to Content Link**: Press Tab when page loads to skip navigation
- **ARIA Labels**: All regions and controls properly labeled
- **Semantic HTML**: Proper heading hierarchy and landmarks
- **Alt Text**: All icons and images have descriptive text

### For Keyboard Users

- **Full Keyboard Navigation**: Tab through all controls
- **Focus Indicators**: Clear visual outlines on focused elements
- **Keyboard Shortcuts**: Access common actions via hotkeys
- **No Mouse Required**: Every feature accessible via keyboard

### For Users with Low Vision

- **High Contrast**: Dark theme with sufficient contrast ratios
- **Scalable Text**: Zoom without breaking layout
- **Clear Typography**: Readable Inter font family
- **Visual Feedback**: Toast notifications and color-coded states

### For Motor Impairments

- **Large Click Targets**: Buttons sized for easy clicking
- **No Precision Required**: Forgiving interaction areas
- **Sticky Sidebar**: Reduces scrolling needs
- **Undo Functionality**: Mistakes easily reversible

## 🔒 Privacy & Security

- **No Data Upload**: Everything runs in your browser
- **No Server**: Files never leave your computer
- **No Tracking**: No analytics or external connections
- **Local Storage Only**: Templates saved in browser localStorage
- **Open Source**: Code is transparent and auditable

## 🛠️ Technical Details

### Browser Compatibility
- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

### Dependencies
- Tailwind CSS (via CDN)
- PapaParse (CSV parsing)
- SheetJS (Excel parsing)

All dependencies loaded via CDN - no installation needed.

### File Size Limits
- Recommended: Up to 10,000 rows
- Browser memory is the only limitation
- Large files may be slow to process

## 📝 Tips & Best Practices

### Email Deliverability
- Keep TO/CC recipient count under 50 for best deliverability
- Use BCC for mass emails to avoid spam filters
- Personalize subject lines to improve open rates
- Test with a small batch before sending to all

### Data Preparation
- Clean your data before uploading (remove duplicates, fix typos)
- Use consistent column naming
- Include all necessary data in your spreadsheet
- Test with a small sample file first

### Template Creation
- Save templates after you perfect them
- Use descriptive template names
- Include your organization name in templates
- Create templates for recurring email types

### Performance
- Apply filters to reduce processing time
- Preview first before generating all emails
- Clear old emails before generating new batches
- Close other browser tabs for faster performance

### Workflow Efficiency
- Learn the keyboard shortcuts
- Use the sticky sidebar for reference
- Save time with template presets
- Export results for record keeping

## 🐛 Troubleshooting

### "No data rows found"
- Check that your file has headers in row 1
- Ensure there's data in row 2 and beyond
- Try saving as CSV and re-uploading

### Variables not replaced
- Check spelling matches column name exactly
- Ensure variable uses double curly braces: `{{Name}}`
- Verify column exists in "Available Variables"

### Email links don't work
- Some email clients have URL length limits
- Try shorter body text or fewer recipients
- Export to CSV and use a mail merge tool instead

### File won't upload
- Check file format (CSV, XLSX, XLS only)
- Try saving as CSV if Excel file fails
- Check for special characters in file name

### Emails not generating
- Verify recipient column is selected
- Check that filters aren't excluding all rows
- Ensure recipient column has valid emails

## 📄 License

MIT License - free to use, modify, and distribute.

## 🤝 Contributing

This is an open source project. Contributions welcome!

- Report bugs via GitHub Issues
- Suggest features via GitHub Discussions
- Submit pull requests for improvements

## 📞 Support

- **Documentation**: This README
- **Examples**: See `examples/` folder
- **Issues**: GitHub Issues page
- **Discussions**: GitHub Discussions

## 🎓 Learning Resources

### Example Files
Check the `examples/` folder for:
- Sample CSV files
- Template examples
- Use case demonstrations

### Video Tutorials (Coming Soon)
- Getting started guide
- Advanced merge techniques
- Template management

## 🗺️ Roadmap

Future enhancements under consideration:
- [ ] HTML email body support
- [ ] Conditional content blocks
- [ ] Email scheduling integration
- [ ] More export formats
- [ ] Collaboration features
- [ ] Cloud template sync

## 📊 Changelog

### Version 2.0 (Current)
- ✨ Added multi-recipient merge mode
- ✨ Improved accessibility features
- ✨ Sticky sidebar for better UX
- ✨ Enhanced keyboard shortcuts
- ✨ Better error handling
- 🐛 Fixed email validation edge cases

### Version 1.0
- Initial release
- Basic email generation
- Template variables
- CSV/Excel support

---

**Made with ❤️ for productive email workflows**

*No installation. No backend. Just pure browser-based magic.* ✨
