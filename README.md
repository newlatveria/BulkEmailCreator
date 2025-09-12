Bulk Email Creator
This is a simple, browser-based tool that allows you to generate multiple email draft links for Outlook from a CSV file. It's designed to streamline the process of sending personalized emails to a list of contacts without manually creating each one.

Features
CSV Integration: Directly upload your CSV file to pull contact data.

Dynamic Placeholders: Use {{HeaderName}} syntax in your email subject and body to dynamically insert data from your CSV columns for personalized content.

Link Generation: Automatically generates individual mailto: links, each pre-filled with the recipient, subject, and body from a row in your CSV.

Visual Indicator: Once a draft link is clicked, it changes color and displays a checkmark, so you can easily track which emails have been opened.

Optional Fields: Supports optional CC, BCC, and attachment fields. Note that attachments are a manual step and are listed for reference only.

Responsive Design: The interface is built with Tailwind CSS, ensuring it is easy to use on both desktop and mobile devices.

How to Use
Follow these simple steps to generate your email drafts:

Upload a CSV File: Click the "Upload your CSV file" button and select the file containing your contact data. Ensure the first row of your CSV contains clear headers (e.g., Name, Email, Company).

View and Copy Headers: Once the file is processed, a list of your CSV headers will appear. You can click on any header name to copy its placeholder syntax (e.g., {{Name}}) to your clipboard.

Define Email Template:

Select Recipient Column: From the dropdown menu, choose the column that contains the email addresses of your recipients.

Enter Subject: Type your email subject, including placeholders if you want to personalize it.

Enter Body: Write the content of your email, using placeholders to insert data like names, account numbers, or company names.

Add Optional Columns (Optional): If your CSV has columns for carbon copy (CC), blind carbon copy (BCC), or a list of attachments, enter the corresponding column headers in the optional fields.

Generate Drafts: Click the "Generate Email Drafts" button. The application will process your data and create a list of clickable email links.

Open Your Drafts: Click on any of the generated links. Your default email client (Outlook, Gmail, etc.) will open a new draft with all the fields pre-filled. The link on the page will change color to confirm you've used it.

Technologies
HTML5: The core structure of the application.

JavaScript (ES6+): Handles file processing, dynamic content generation, and user interactions.

Tailwind CSS: A utility-first CSS framework for rapid styling and responsive design.
