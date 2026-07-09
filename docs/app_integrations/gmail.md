---
title: Gmail
description: Step-by-step guide to set up Gmail credentials for Appse.ai integration
slug: /app-integrations/gmail/
---

import ConnectAccountButton from '@site/src/components/ConnectAccountButton';

## Introduction

Gmail is Google’s email service that allows users to send, receive, search, and manage emails efficiently. By integrating Gmail with appse ai, you can automate email-based workflows such as sending notifications, reading inbox messages, monitoring threads, and triggering actions based on email events.

:::note
Gmail uses OAuth 2.0 authentication only. Install and connect the app directly through the OAuth flow. Users do not need to manually enter client IDs or client secrets.
:::

<ConnectAccountButton
  appName="Gmail"
  authorizeUrl="https://workflow.insync.top/credentials?appCode=gmail&credentialTypeCode=gmail_oauth2_public"
/>

Click **Connect your Gmail Account** above to open the Public App authorization page and start the OAuth connection. If you are not signed in to appse ai, you will be prompted to log in or register first.

---

## Key Features

- **Send Emails**: Automatically send emails using Gmail.
- **Read Inbox Messages**: Fetch incoming emails and threads.
- **Search Emails**: Query emails using Gmail search operators.
- **Workflow Automation**: Trigger workflows based on email activity.
- **Secure OAuth Access**: Uses Google OAuth 2.0 for safe authentication.

---

### Add Credential in appse ai

- Click **Save & Authorize**.

<img src="/img/credentials/gmail/gm36.png" alt="Gmail Save and Authorize screen" width="700"/>

- You will be redirected to the Google authentication page. Select the Gmail account you want to connect.

<img src="/img/credentials/gmail/gm37.png" alt="Gmail account selection screen" width="700"/>

- Click **Continue**.

<img src="/img/credentials/gmail/gm38.png" alt="Gmail continue authorization screen" width="700"/>

- Review the requested permissions, select all the required scope checkboxes, and click **Continue**.

<img src="/img/credentials/gmail/gm57.png" alt="Gmail OAuth scopes consent screen" width="700"/>

- Once connected, you will be automatically redirected back to the appse ai platform, and the Gmail credential will be saved successfully.

- Ensure the credential shows **Successfully Validated**.

<img src="/img/credentials/gmail/gm51.png" alt="Gmail credential successfully validated" width="700"/>

---

## Support

Need help? Contact our support team at [support@appse.ai](mailto:support@appse.ai)

---
