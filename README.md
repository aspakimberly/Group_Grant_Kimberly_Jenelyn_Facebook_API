# Facebook Graph API Demo (OAuth 2.0)

## 📌 Project Overview

This project is a **Facebook Graph API demonstration web application** that uses **OAuth 2.0 authentication** and the **Fetch API** to retrieve user data.

The application allows users to:

* Log in using Facebook OAuth (redirect-based, no SDK)
* Fetch profile information
* Fetch profile picture
* View granted permissions
* Display raw JSON responses for debugging and demo purposes

This project is designed to satisfy **API usage, authentication, fetch implementation, and GitHub collaboration requirements**.

---

## 🛠️ Technologies Used

* HTML5
* CSS3
* JavaScript (Vanilla JS)
* Fetch API
* Facebook Graph API v24.0
* OAuth 2.0
* GitHub (Branches, Pull Requests, Collaboration)

---

## 🌐 API Information

### Base URL
https://graph.facebook.com/v24.0


---

### Endpoints Used

| Endpoint          | Method | Description                       |
| ----------------- | ------ | --------------------------------- |
| `/me`             | GET    | Fetch basic Facebook user profile |
| `/me/picture`     | GET    | Fetch profile picture             |
| `/me/permissions` | GET    | Fetch granted OAuth permissions   |

---

### Required Parameters

| Parameter      | Description                                  |
| -------------- | -------------------------------------------- |
| `access_token` | OAuth access token                           |
| `fields`       | Requested user fields (id, name, email)     |
| `type`         | Profile picture size                         |
| `redirect`     | Set to `0` to return JSON                    |

---

### Authentication

✔ OAuth 2.0  
✔ Facebook Login (Redirect-based)  
✔ Access Token  

⚠️ **Facebook Login does not work on `file://`. A local server is required.**

---

## 📄 Sample JSON Response

```json
{
  "id": "123456789",
  "name": "John Doe"
}

💻 Fetch API Implementation (JavaScript)
fetch("https://graph.facebook.com/v24.0/me?fields=id,name&access_token=YOUR_ACCESS_TOKEN")
  .then(response => response.json())
  .then(data => console.log(data));

▶️ How to Run the Project
Option 1: Live Server (Recommended)

Open project in VS Code

Install Live Server

Right-click index.html

Select Open with Live Server

Open:

http://127.0.0.1:5500

Option 2: Python Local Server
python -m http.server 5500


Open:

http://localhost:5500

🔐 How to Use the Application

Click Login

Allow Facebook permissions

Click Fetch

View profile data and raw JSON

⚠️ Important Notes

Never commit real access tokens

Use placeholders only:

YOUR_ACCESS_TOKEN_HERE


---
