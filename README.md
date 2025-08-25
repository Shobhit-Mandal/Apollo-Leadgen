Apollo Lead Scraper Workflow (n8n)
📌 Overview

This n8n workflow automates the process of extracting verified contact details from Apollo (via Apify’s Apollo Scraper) and saves them directly into Google Sheets.
It is designed for agencies or teams who want to collect targeted lead data (emails, job titles, LinkedIn profiles, company details, etc.) without manual effort.

The workflow runs through a form submission, scrapes data, processes it, and updates a Google Sheet in real-time.

⚙️ Workflow Steps

Form Trigger

Users input:

Apollo URL (search or people filter link from Apollo)

Maximum Results (e.g., 100)

Google Sheet Name (destination sheet name)

Google Sheets (Create Sheet)

Creates a new sheet (if it doesn’t already exist) with the given name.

HTTP Request (Apify - Apollo Scraper)

Calls the Apify actor microworlds~apollo-scraper with parameters:

include_email = true

contact_email_status_v2_verified = true

max_result = user input

url = Apollo URL from form

Edit Fields

Extracts and maps relevant fields:

First/Last Name

LinkedIn URL

Title

Email (verified only)

Organization details (name, website, LinkedIn, domain)

Location (country, state, city)

Departments & Seniority

Google Sheets (Append/Update)

Saves all extracted records into the specified Google Sheet.

📊 Data Captured

Personal Info: First name, Last name, LinkedIn, Email (verified only), Job Title, Seniority

Organization Info: Name, Website, LinkedIn, Domain, Location

Additional Info: Departments, City, State, Country

🚀 Setup Instructions

Import the Workflow

Open n8n → Workflows → Import from File → Upload Apollo.json.

Configure Credentials

Google Sheets OAuth2 API → Add your Google account.

Apify API Token → Replace placeholder with your Apify token in the HTTP Request headers.

Publish Form

Copy the form webhook URL from the Form Trigger node.

Share it with your team/clients to input Apollo search URLs.

Run the Workflow

Upon form submission, the workflow automatically runs and populates your chosen Google Sheet.

🛠 Requirements

n8n (latest version)

Google Account with Sheets access

Apify Account with Apollo Scraper access (microworlds~apollo-scraper)

🔑 Notes

Only verified emails are captured (contact_email_status_v2_verified = true).

The workflow dynamically creates or updates Google Sheets per user input.

Max results are limited by your Apify actor/plan.

Ensure correct Apollo URLs (people/company search links) are provided for best results.
