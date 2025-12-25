---

# Facebook Graph API Demo (OAuth 2.0)

## Project Overview

This project is a web application that demonstrates how to use the **Facebook Graph API** with **OAuth 2.0 authentication**. Users can log in using Facebook, retrieve basic profile information, view their profile picture, and check the permissions granted to the application.

The data is fetched using **JavaScript’s Fetch API** and displayed both visually and as raw JSON for easier understanding and debugging.

---

## Technologies Used

* HTML
* CSS
* JavaScript (Vanilla JS)
* Fetch API
* Facebook Graph API (v24.0)
* OAuth 2.0
* GitHub

---

## API Details

### Base URL

```
https://graph.facebook.com/v24.0
```

### Endpoints Used

| Endpoint          | Method | Description                    |
| ----------------- | ------ | ------------------------------ |
| `/me`             | GET    | Fetch user profile information |
| `/me/picture`     | GET    | Fetch profile picture          |
| `/me/permissions` | GET    | Fetch granted permissions      |

### Required Parameters

* `access_token` – OAuth access token
* `fields` – Requested user data
* `type` – Profile picture size
* `redirect` – Set to `0` to return JSON

---

## Authentication

* OAuth 2.0
* Facebook Login (redirect-based)

⚠️ Facebook login does not work using `file://`. A local or hosted server is required.

---

## Sample Fetch Request

```javascript
fetch("https://graph.facebook.com/v24.0/me?fields=id,name&access_token=YOUR_ACCESS_TOKEN")
  .then(response => response.json())
  .then(data => console.log(data));
```

---

## How to Run the Project

### Option 1: Live Server (Recommended)

1. Open the project in VS Code
2. Install **Live Server**
3. Right-click `index.html` → **Open with Live Server**

### Option 2: Python Server

```bash
python -m http.server 5500
```

Open `http://localhost:5500`

---

## Usage

1. Click **Login** using Facebook
2. Allow permissions
3. Click **Fetch**
4. View profile data and JSON response

---

## Important Notes

* Do not commit real access tokens
* Use placeholders such as:

```
YOUR_ACCESS_TOKEN_HERE
```

---

## GitHub Collaboration

* One shared repository
* Each member worked on their own branch
* Meaningful commits were made
* Pull Requests were used for merging
* Branches were cleaned after completion

---
