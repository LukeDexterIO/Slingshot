# Slingshot - AI Automated Spear Phishing with Zapier

## Overview
By utilizing Zapier, JotForm, and MailGun, ethical hackers can create highly detailed spear phishing emails quickly and en masse. Many possible options exist, and this project will continue to receive advancements.

## Requirements
- JotForm Account
- Zapier account (premium trial)
- OpenAI API Account
- Unused domain name
- MailGun Account

---

## Quick Setup Instructions

### Step 1: JotForm
We will start with creating the interface for our machine with Jotform. Head over to [JotForm](https://jotform.com) and sign up.

We will create a **classic form** with the Full Name, Email, Long Text (for Target Description and/or OSINT data), and 2 dropdown menus - 1 for the sending email, and the other for the link we want the user to click.

---

## Step 2: Setting Up Zapier
Head over to [Zapier](https://zapier.com) and create an account.

### Creating a Zap
Navigate to **Zaps** > **Create New Zap**
- Step 1 **Trigger Event** > **JotForm**
- Step 2 **Action Event** > **ChatGPT - Create Email Body**
- Step 3 **Action Event** > **ChatGPT - Create Email Subject**
- Step 4 **Action Event** > **ChatGPT - Convert Email Body to HTML for MailGun**
- Step 5 **Action Event** > **MailGun - Send Email** (Step 3 will show you how to set this up)

---

## Step 3: MailGun SMTP Setup
We will use MailGun as our SMTP server in order to send our email.
1. Login to [MailGun](https://mailgun.com) and set up your domain.
2. Configure domain settings.
3. Add DNS records to your domain provider.
4. Grab the **API Key** under API Security and use it to authenticate MailGun with Zapier

---

