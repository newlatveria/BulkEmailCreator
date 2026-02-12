# 📊 Sample Data Files Guide

This package includes **4 sample data files** with 30 rows each, perfect for testing the Bulk Email Creator Pro tool.

---

## 📁 File Overview

### 1. `sample_data.csv` (General Customer Data)
**Use Case:** Customer outreach, account updates, product announcements

**Columns:**
- `ID` - Customer ID (CUST-1000 to CUST-1029)
- `First Name` - Customer first name
- `Last Name` - Customer last name
- `Email` - Email address (format: firstname.lastname###@example.com)
- `Company` - Company name (30 realistic company names)
- `Department` - Department (Sales, Marketing, Engineering, etc.)
- `Phone` - Phone number (US format)
- `Product` - Product purchased
- `Status` - Account status (Active, Pending, Completed, etc.)
- `Amount` - Purchase amount ($100 - $10,000)
- `Date` - Transaction date (2024)
- `Priority` - Priority level (High, Medium, Low)
- `Region` - Geographic region
- `Account Manager` - Assigned manager name
- `Notes` - Additional notes

**Example Email Template:**
```
Subject: Update on your {{Product}} account

Dear {{First Name}} {{Last Name}},

Thank you for your recent purchase of {{Product}} on {{Date}}.

Your account ({{ID}}) is currently {{Status}} and managed by {{Account Manager}}.

Amount: {{Amount}}
Priority: {{Priority}}
Region: {{Region}}

Please don't hesitate to reach out if you need assistance.

Best regards,
Customer Success Team
```

---

### 2. `sample_data.xlsx` (Excel Version - Same Data)
**Identical to sample_data.csv but in Excel format**

Perfect for testing Excel file upload functionality. Contains the same customer data with formatted columns and bold headers.

---

### 3. `sample_data_events.xlsx` (Event Invitations)
**Use Case:** Event invitations, RSVPs, conference management

**Columns:**
- `Attendee ID` - Unique attendee identifier (ATT-2000 to ATT-2029)
- `First Name` - Attendee first name
- `Last Name` - Attendee last name
- `Email` - Email address
- `Event Name` - Name of the event (Annual Gala, Product Launch, etc.)
- `Event Date` - Event date (March-June 2024)
- `Event Time` - Event start time
- `Venue` - Event location
- `Ticket Type` - VIP, General, Student, or Early Bird
- `Dietary Preference` - Food restrictions
- `Guest Count` - Number of guests (1-4)
- `RSVP Status` - Confirmed, Pending, Declined, or Waitlist
- `Special Requests` - Accessibility or other requests

**Example Email Template:**
```
Subject: You're Invited! {{Event Name}} - {{Event Date}}

Dear {{First Name}} {{Last Name}},

We're excited to invite you to {{Event Name}}!

📅 Date: {{Event Date}}
⏰ Time: {{Event Time}}
📍 Venue: {{Venue}}
🎫 Ticket Type: {{Ticket Type}}

Your Details:
• Attendee ID: {{Attendee ID}}
• Guest Count: {{Guest Count}}
• Dietary Preference: {{Dietary Preference}}
• RSVP Status: {{RSVP Status}}

Special Requests: {{Special Requests}}

We look forward to seeing you there!

Best regards,
Events Team
```

**Use the MERGE feature!** Filter by Event Name and merge to send one email per event with all attendees listed.

---

### 4. `sample_data_invoices.csv` (Invoice/Billing Data)
**Use Case:** Payment reminders, invoice notifications, billing updates

**Columns:**
- `Invoice Number` - Unique invoice ID (INV-2024000 to INV-2024029)
- `Company Name` - Customer company
- `Contact Name` - Billing contact person
- `Contact Email` - Billing email address
- `Invoice Date` - Date invoice was issued
- `Due Date` - Payment due date (30 days after invoice date)
- `Amount` - Subtotal amount
- `Tax` - Tax amount
- `Total` - Total amount due
- `Payment Status` - Paid, Unpaid, Overdue, or Partial
- `Payment Method` - How payment should be made
- `Currency` - USD, EUR, GBP, or CAD
- `Terms` - Payment terms (Net 30, Net 60, etc.)
- `Project` - Related project/product
- `Account Manager` - Manager handling the account
- `Notes` - Additional information

**Example Email Template:**
```
Subject: Invoice {{Invoice Number}} - Payment {{Payment Status}}

Dear {{Contact Name}},

This is a reminder regarding Invoice {{Invoice Number}} for {{Company Name}}.

Invoice Details:
• Invoice Date: {{Invoice Date}}
• Due Date: {{Due Date}}
• Amount: {{Amount}}
• Tax: {{Tax}}
• Total: {{Total}}

Payment Status: {{Payment Status}}
Payment Terms: {{Terms}}
Currency: {{Currency}}
Preferred Method: {{Payment Method}}

Project: {{Project}}
Account Manager: {{Account Manager}}

Notes: {{Notes}}

If you have any questions, please contact {{Account Manager}}.

Thank you for your business!

Accounts Receivable
```

**Filter Tip:** Filter by "Payment Status" = "Overdue" to send reminders only to late payments!

---

## 🎯 Quick Start Examples

### Example 1: Send to Only VIP Customers
1. Load `sample_data.csv`
2. Add Filter: `Priority` = `High`
3. Generate emails (will create ~10 emails instead of 30)

### Example 2: Event Invitations by Event
1. Load `sample_data_events.xlsx`
2. Add Filter: `Event Name` = `Annual Gala`
3. Check ✅ "Merge multiple rows per recipient"
4. Generate (combines multiple RSVPs per person)

### Example 3: Payment Reminders
1. Load `sample_data_invoices.csv`
2. Add Filter: `Payment Status` = `Unpaid`
3. Add Filter: `Due Date` < (today's date)
4. Generate overdue payment reminders

### Example 4: Regional Marketing
1. Load `sample_data.csv`
2. Add Filter: `Region` = `North America`
3. Add Filter: `Status` = `Active`
4. Generate targeted regional campaign

---

## 💡 Testing Tips

### Test Variable Replacement
Create a template with multiple variables:
```
Hello {{First Name}},

Your {{Product}} order ({{ID}}) is {{Status}}.
```

### Test Filtering
- Try multiple filters at once
- Use "Contains" for partial matches
- Use "Not Empty" to exclude blank fields

### Test Merging
- Use `sample_data_events.xlsx`
- Filter by one event name
- Enable merge to see multiple rows combined

### Test Preview
- Click "Preview First Email" before generating all
- Verify variables are replacing correctly
- Check formatting and spacing

### Test Different Formats
- Try all file types (CSV, XLSX)
- Compare processing speeds
- Verify all columns load correctly

---

## 📝 Data Statistics

**Total Records:** 120 rows across 4 files (30 each)

**sample_data.csv:**
- Companies: 30 unique companies
- Departments: 12 different departments
- Products: 10 different products
- Regions: 4 geographic regions

**sample_data_events.xlsx:**
- Events: 7 different events
- Venues: 6 different locations
- Ticket Types: 4 types
- Dietary Preferences: 7 options

**sample_data_invoices.csv:**
- Date Range: January-March 2024
- Amount Range: $500 - $55,000
- Currencies: 4 (USD, EUR, GBP, CAD)
- Payment Methods: 5 options

---

## 🔧 Customization Ideas

### Add Your Own Data
1. Open any file in Excel or text editor
2. Replace names, emails, companies with real data
3. Keep the same column structure
4. Save and upload to the tool

### Combine Files
- Merge multiple CSV files into one large dataset
- Use Excel to combine sheets
- Test with larger datasets (100+, 1000+ rows)

### Create New Columns
- Add "CC Email" column for auto-CC
- Add "Attachment" column for reminder notes
- Add custom fields specific to your use case

---

## 🚀 Advanced Use Cases

### A/B Testing
1. Duplicate rows and add "Version" column
2. Create two email templates
3. Filter by version A or B
4. Compare response rates

### Scheduled Campaigns
1. Add "Send Date" column
2. Filter by today's date
3. Generate only emails scheduled for today

### Multi-language
1. Add "Language" column
2. Create templates in multiple languages
3. Filter by language before generating

### Follow-up Sequences
1. Add "Stage" column (Stage 1, Stage 2, etc.)
2. Filter by stage
3. Send appropriate follow-up message

---

## ⚠️ Important Notes

- **Email addresses are fake** - All emails use @example.com domain
- **Data is randomly generated** - Names, companies, amounts are fictional
- **Safe for testing** - No real customer data included
- **Repeatable** - You can modify and regenerate files as needed

---

## 📞 Having Issues?

**File won't load?**
- Ensure file extension is correct (.csv, .xlsx)
- Try opening in Excel first to verify data
- Check for special characters in column names

**Variables not replacing?**
- Check spelling matches column names exactly
- Column names are case-sensitive
- Use the clickable header tags to avoid typos

**Too many/few emails generated?**
- Check your filters - they might be too restrictive
- Verify recipient column contains valid emails
- Look for blank rows in your data

---

<div align="center">

**🎉 Happy Testing! 🎉**

These sample files are designed to help you explore all features of Bulk Email Creator Pro.

Try different combinations, experiment with filters, and see what works best for your use case!

</div>
