# Quick Start Guide

Get up and running with Bulk Email Creator Pro in 5 minutes!

## 🎯 What You'll Learn

By the end of this guide, you'll be able to:
- Upload your data file
- Create a personalized email template
- Generate email drafts
- Send your first batch of emails

**Time required**: 5-10 minutes

---

## Step 1: Download and Open (30 seconds)

1. Download `bulk-email-creator-enhanced.html`
2. Double-click the file
3. It opens in your default web browser
4. No installation needed!

**Supported browsers**: Chrome, Firefox, Safari, Edge

---

## Step 2: Prepare Your Data (2 minutes)

Create a simple CSV file or use one of our examples.

### Option A: Use Example File

Download any file from the `examples/` folder:
- `project-updates.csv` - Project status emails
- `newsletter-subscribers.csv` - Newsletter campaign
- `event-registration.csv` - Event invitations
- `invoice-reminders.csv` - Payment reminders

### Option B: Create Your Own

**Minimum required**:
- First row: Column headers
- Second row onwards: Your data
- At least one column with email addresses

**Example** (save as `my-emails.csv`):
```csv
Name,Email,Company
John Smith,john@example.com,Acme Corp
Jane Doe,jane@example.com,Tech Inc
```

### Pro Tips 💡
- Keep column names simple (no special characters)
- One email address per cell
- Include all data you want to reference in emails
- Save as CSV (not Excel format) for best compatibility

---

## Step 3: Upload Your File (30 seconds)

1. Click **"Upload your file"** button
2. Select your CSV or Excel file
3. Wait for success message: "✅ Loaded X rows with Y columns"
4. Review the **Data Preview** table

**What you'll see**:
- Preview of first 3 rows
- List of available variables
- Column count and row count

**Troubleshooting**:
- "No data rows found" → Make sure row 1 has headers, row 2 has data
- Columns look wrong → Try saving as CSV instead of XLSX

---

## Step 4: Configure Email Settings (2 minutes)

### A. Select Recipient Column
1. Find dropdown labeled **"Recipient Column"**
2. Select the column with email addresses
3. (Usually auto-detected if column name contains "email")

### B. Set Subject Line
1. Click in **"Email Subject"** field
2. Type your subject
3. Add variables by clicking tags (e.g., `{{Name}}`)

**Example**:
```
Hello {{Name}}, your update is ready
```

### C. Write Email Body
1. Click in **"Email Body"** field
2. Type your message
3. Use **"Insert Greeting"** button for quick start
4. Add variables where needed

**Example**:
```
Dear {{Name}},

Your account at {{Company}} is now active.

Best regards,
Support Team
```

### Quick Tips 💡
- Click variable tags to copy them
- Green badges in sidebar = variables you're using
- Preview panel shows which variables are detected

---

## Step 5: Choose Merge Mode (30 seconds)

Select how emails should be combined:

### Option 1: No Merging (Recommended for first use)
- ✅ Select this radio button
- Creates one email per row
- Each person gets their own personalized email

### Option 2: Merge Same Recipient
- Combines rows with same email address
- Creates numbered sections
- Good for: Multiple items for same person

### Option 3: Multi-Recipient
- All recipients in one email
- Good for: Newsletters, announcements
- Choose TO (public) or BCC (private)

**For now**: Stick with "No Merging" until you're comfortable.

---

## Step 6: Preview First Email (30 seconds)

Before generating all emails:

1. Click **"👁️ Preview First Email"** button (or press Ctrl+P)
2. Review the preview modal:
   - TO: Email address
   - Subject: Check variables replaced correctly
   - Body: Verify formatting and content
3. Close preview

**Look for**:
- Variables replaced with actual data? ✅
- Spelling correct? ✅
- Formatting looks good? ✅

**If something's wrong**: Close preview, fix your template, preview again.

---

## Step 7: Generate Emails (30 seconds)

Ready to create your email drafts?

1. Click **"✉️ Generate All Drafts"** button (or press Ctrl+G)
2. Wait for processing (progress bar appears)
3. See success message: "✅ Generated X email drafts"

**What you'll see**:
- List of all generated emails
- Each showing: recipient, subject, CC/BCC info
- Buttons to copy or view details

---

## Step 8: Send Emails (1-2 minutes)

For each email you want to send:

1. Click the email link
2. Your default email client opens (Gmail, Outlook, etc.)
3. Review the email one more time
4. Add attachments if needed (these can't be auto-added)
5. Click Send

**After clicking**:
- Email turns green ✓
- Marked as "Opened" so you can track progress

### Batch Sending Tips
- Send a few test emails first
- Check spam folder on test emails
- If sending many emails, pace yourself (email clients may have limits)
- For large batches (50+), consider using BCC merge mode

---

## Step 9: Export for Records (30 seconds)

Save your email drafts for reference:

**Option 1: Export TXT**
1. Click **"💾 Export TXT"**
2. Downloads text file with all emails
3. Good for: Simple backup

**Option 2: Export CSV**
1. Click **"📊 Export CSV"**
2. Downloads spreadsheet with all data
3. Good for: Further processing, CRM import

---

## Step 10: Save Template (Optional - 30 seconds)

If you'll use this email format again:

1. Click **"💾 Save Template"** (or press Ctrl+S)
2. Enter a name (e.g., "Weekly Project Update")
3. Click OK

**Next time**:
1. Upload your new data file
2. Click **"📂 Load Template"**
3. Select your saved template
4. All settings restored instantly!

---

## ✅ Success Checklist

You've mastered the basics if you can:
- [x] Upload a CSV file
- [x] See data preview
- [x] Create email template with variables
- [x] Preview first email
- [x] Generate all drafts
- [x] Send test emails
- [x] Export results

---

## 🚀 Next Steps

Ready to level up? Try these advanced features:

### Filters (10 minutes)
Only send to specific people:
1. Click **"+ Add Filter"**
2. Select column, operator, and value
3. See filtered count update

**Example**: Only send to people in "Sales" department

### CC/BCC Recipients (5 minutes)
Add additional recipients:
1. Find CC or BCC section
2. Either select column OR type emails manually
3. Preview to verify

### Multi-Recipient Mode (5 minutes)
Send one email to many people:
1. Select **"Multi-recipient"** merge mode
2. Choose TO or BCC placement
3. Generate - you get 1 email instead of many

### Template Library (5 minutes)
Browse `TEMPLATES.md` for ready-to-use examples:
- Newsletter template
- Invoice reminder
- Meeting invitation
- Product launch
- And more!

---

## 💡 Best Practices

### Before You Start
✅ Clean your data (remove duplicates, fix typos)
✅ Test with 3-5 rows first
✅ Use meaningful column names
✅ Include all data you might reference

### While Creating
✅ Use preview feature
✅ Check variable spelling
✅ Keep subject lines under 50 characters
✅ Test links before sending

### When Sending
✅ Send test to yourself first
✅ Check spam folder
✅ Verify attachments manually
✅ Pace large batches (don't spam!)
✅ Export for records

### Template Tips
✅ Save templates for recurring emails
✅ Use descriptive template names
✅ Keep a backup of your templates
✅ Share templates with your team

---

## 🆘 Common Issues & Solutions

### "File won't upload"
- Check file format (CSV, XLSX, XLS only)
- Try saving Excel file as CSV
- Check for special characters in filename

### "No data rows found"
- Ensure row 1 has column headers
- Ensure row 2+ has actual data
- Check file isn't empty

### "Variables not replaced"
- Verify spelling matches column name exactly
- Check capitalization
- Ensure using double braces: `{{Name}}`

### "Email links too long"
- Shorten email body
- Use fewer recipients per email
- Export to CSV and use mail merge tool instead

### "Invalid email addresses"
- Red chips indicate invalid emails
- Fix in your CSV file
- Re-upload corrected file

---

## 📚 Learn More

### Documentation
- **README.md** - Complete feature guide
- **TEMPLATES.md** - Ready-to-use email templates
- **ACCESSIBILITY.md** - Accessibility features

### Video Tutorials (Coming Soon)
- Getting started walkthrough
- Advanced filtering techniques
- Template management tips

### Get Help
- GitHub Issues - Report bugs
- GitHub Discussions - Ask questions
- Documentation - Detailed guides

---

## 🎓 Practice Exercise

Try this complete workflow:

**Scenario**: Send personalized welcome emails to new team members

**Your Task**:
1. Create CSV with: Name, Email, Department, StartDate
2. Add 3 fake team members
3. Upload to tool
4. Create welcome email template
5. Preview first email
6. Generate all drafts
7. Export to TXT for review

**Sample subject**: `Welcome to the team, {{Name}}!`

**Sample body**:
```
Hi {{Name}},

Welcome to the {{Department}} team!

Your start date is {{StartDate}}. We're excited to have you on board!

Best,
HR Team
```

**Expected result**: 3 personalized welcome emails ready to send

---

## ⏱️ 5-Minute Challenge

Can you complete this in 5 minutes?

1. ⏲️ Start timer
2. Download `examples/newsletter-subscribers.csv`
3. Upload to tool
4. Create simple newsletter email
5. Generate drafts
6. ⏲️ Stop timer

**Under 5 minutes?** You're a pro! 🎉

---

**Congratulations!** 🎉 You're now ready to use Bulk Email Creator Pro for your email campaigns. 

**Questions?** Check the full README.md or open an issue on GitHub.

**Happy emailing!** ✉️
