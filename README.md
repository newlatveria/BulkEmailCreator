# 📧 Bulk Email Creator

> Transform your CSV data into personalized email drafts in seconds! No server required, no data uploaded, 100% privacy-focused.

![Version](https://img.shields.io/badge/version-2.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![No Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)

## ✨ What Makes This Special?

**Bulk Email Creator** is a powerful, client-side web application that generates personalized email drafts from CSV files. Perfect for sending newsletters, invoices, event invitations, or any mass communication where each recipient needs a personalized touch.

### 🎯 Key Features

- 🚀 **Lightning Fast** - Process hundreds of emails in seconds
- 🔒 **100% Private** - All processing happens in your browser, no data leaves your computer
- 🎨 **Smart Templates** - Use `{{placeholders}}` to personalize every email
- 🔄 **Merge Magic** - NEW! Combine multiple rows for the same recipient into one email
- 📎 **Full Control** - Support for CC, BCC, and attachment references
- 💅 **Beautiful UI** - Modern, responsive design that works on any device
- 🎯 **One-Click Generation** - Create mailto links that open directly in Outlook or your default email client
- 📋 **Easy Copying** - Copy mailto links with a single click for batch processing

## 🚀 Quick Start

### Installation

1. **Download** the `bulkemailer.html` file
2. **Open** it in any modern web browser (Chrome, Firefox, Edge, Safari)
3. **Done!** No installation, no setup, no server required

### Basic Usage

1. **Prepare Your CSV**
   ```csv
   Email,Name,Company,Amount
   john@example.com,John Smith,Acme Corp,$1,500
   jane@example.com,Jane Doe,Tech Inc,$2,300
   ```

2. **Upload Your File**
   - Click "Upload your CSV file" and select your file
   - Headers are automatically detected

3. **Create Your Template**
   - Select the recipient email column
   - Write your subject: `Invoice for {{Company}}`
   - Write your body:
     ```
     Dear {{Name}},
     
     Your invoice for {{Amount}} is ready.
     
     Best regards,
     The Team
     ```

4. **Generate!**
   - Click "Generate Email Drafts"
   - Click any email to open it in your email client
   - Or copy the mailto link for later use

## 🎭 Advanced Features

### 🔄 Merge Multiple Rows

Have multiple transactions for the same person? Enable the **"Merge multiple rows per recipient"** checkbox!

**Before (CSV):**
```csv
Email,Name,Invoice,Amount
john@example.com,John,INV-001,$500
john@example.com,John,INV-002,$750
john@example.com,John,INV-003,$300
```

**After (One Email):**
```
--- Entry 1 ---
Invoice INV-001 for $500

--- Entry 2 ---
Invoice INV-002 for $750

--- Entry 3 ---
Invoice INV-003 for $300
```

### 📎 Advanced Fields

- **CC Column** - Copy other recipients on specific emails
- **BCC Column** - Blind copy recipients
- **Attachments Column** - Track which files need to be manually attached

### 🏷️ Template Variables

Use `{{ColumnName}}` anywhere in your subject or body to insert CSV data:

- `{{FirstName}}` - Personalize greetings
- `{{Company}}` - Reference organizations
- `{{AccountNumber}}` - Include account details
- `{{Any_Column}}` - Use ANY column from your CSV!

**Pro Tip:** Click the teal header tags to copy placeholders to your clipboard!

## 🎨 Use Cases

### 📬 Monthly Invoices
Generate personalized invoice emails with amounts, due dates, and account details.

### 🎉 Event Invitations
Send customized event invitations with personal RSVP links and event details.

### 📊 Report Distribution
Distribute monthly reports to stakeholders with personalized metrics.

### 💼 Sales Outreach
Create personalized cold emails at scale with company-specific details.

### 🎓 Student Communications
Send grade reports, assignment feedback, or course updates to students.

### 📧 Newsletter Campaigns
Generate newsletter drafts with personalized content for different segments.

## 🛠️ Technical Details

### Built With
- **Pure HTML/CSS/JavaScript** - No frameworks, no dependencies
- **Tailwind CSS** - Beautiful, modern styling via CDN
- **FileReader API** - Secure client-side file processing
- **Mailto Protocol** - Native email client integration

### Browser Support
- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera
- ✅ Any modern browser with ES6+ support

### Security & Privacy
- 🔒 **All processing is local** - Your CSV never leaves your computer
- 🔒 **No server uploads** - No backend, no API calls, no tracking
- 🔒 **No data storage** - Nothing is saved or cached
- 🔒 **Open source** - Inspect the code yourself!

## 📖 Tips & Tricks

### CSV Formatting
- ✅ First row must be headers
- ✅ Use commas to separate columns
- ✅ Remove commas from data fields (or use quotes)
- ✅ Keep email addresses clean and valid

### Email Client Tips
- **Outlook** - Mailto links work perfectly
- **Gmail Web** - Set Chrome to handle mailto links
- **Apple Mail** - Works natively on macOS
- **Copy Link Option** - Use when mailto doesn't work

### Best Practices
1. **Test First** - Generate 1-2 emails and test them before bulk creation
2. **Check Spam** - Verify emails don't land in spam folders
3. **Proofread Templates** - Double-check your placeholders
4. **Save Templates** - Keep your subject/body templates in a text file
5. **Batch Process** - Generate in batches of 50-100 for easier management

## 🤝 Contributing

Found a bug? Have a feature idea? Contributions are welcome!

1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📝 License

Apache License Version 2.0 - Feel free to use, modify, and distribute!

## 🙏 Acknowledgments

- Built with ❤️ for anyone who's ever had to send personalized bulk emails
- Inspired by the need for simple, privacy-focused tools
- Thanks to the open-source community for making great tools accessible

## 📞 Support

Need help? Have questions?

- 📖 Check this README first
- 🐛 Report bugs via GitHub Issues
- 💡 Share your use cases and success stories!

---

**Happy Emailing! 🚀**

Made with ☕ and determination to make email management easier.

