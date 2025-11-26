# INVENTORY-SYSTEM-FOR-SMALL-AND-LOCLA-SHOPS
REACT AND NODE.JS WITH APPSCRIPTS
# Sakshi ERP Pro 🚀

**Sakshi ERP Pro** is a comprehensive, serverless Cloud ERP system designed for small businesses. It is built with **React (Vite)** and uses **Google Sheets** as a free, real-time database via **Google Apps Script**.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Stack](https://img.shields.io/badge/stack-React_Vite_GoogleAppsScript-orange.svg)

## ✨ Features

*   **👥 Party Management:** Manage Customers and Suppliers with opening balances.
*   **📦 Inventory/Products:** Track stock, prices, and low-stock alerts.
*   **🧾 Billing & POS:** Create Sales Invoices and Purchase Orders.
*   **💳 Payments:** Track Payments In (Receivable) and Payments Out (Payable).
*   **📄 Reports:** Export data to CSV, Print Invoices (A4/Thermal), and Email bills.
*   **🤖 AI Insights:** Built-in Gemini AI to answer questions about your business data.
*   **☁️ Cloud Sync:** Real-time data synchronization with Google Sheets.
*   **📱 Responsive:** Works perfectly on Desktop and Mobile.

---

## 🛠️ Tech Stack

*   **Frontend:** React, TypeScript, Tailwind CSS, Lucide Icons.
*   **Build Tool:** Vite (configured with `vite-plugin-singlefile`).
*   **Backend:** Google Apps Script (GAS).
*   **Database:** Google Sheets.

---

## 🚀 Deployment Guide (How to go Live)

This application does not require AWS, Vercel, or Netlify. It is hosted entirely on Google's servers for free.

### Step 1: Build the Project Locally
You need **Node.js** installed on your computer.

1.  Open your terminal in the project folder.
2.  Install dependencies:
    ```bash
    npm install
    ```
3.  Build the project into a single HTML file:
    ```bash
    npm run build
    ```
    *This will create a `dist/index.html` file. This file contains your entire React app (CSS, JS, Logic) bundled into one.*

### Step 2: Set up Google Sheets
1.  Go to [Google Sheets](https://sheets.new) and create a new sheet.
2.  Name it **"Sakshi ERP Database"**.
3.  Go to **Extensions** > **Apps Script**.

### Step 3: Configure Backend (Apps Script)
1.  In the Apps Script editor, open **`Code.gs`**.
2.  Copy the content from `GoogleAppsScript.js` (found in this repository) and paste it into `Code.gs`.
3.  Save the file (Ctrl+S).

### Step 4: Upload Frontend
1.  In Apps Script, click the **+ (Plus)** icon next to "Files" and select **HTML**.
2.  Name the file **`index`** (it becomes `index.html`).
3.  Open the `dist/index.html` file on your computer (generated in Step 1) using a text editor (Notepad/VS Code).
4.  **Copy all the code** and paste it into the Apps Script `index.html`.
5.  Save the file.

### Step 5: Deploy Live
1.  Click the blue **Deploy** button (top right) > **New deployment**.
2.  Click the **Gear Icon (⚙️)** > select **Web app**.
3.  **Description:** `Initial Deploy`.
4.  **Execute as:** `Me (your email)`.
5.  **Who has access:** `Anyone` (Important: This allows the app to function without forcing Google login for every user).
6.  Click **Deploy**.
7.  Authorize the permissions when asked (Click *Review Permissions* > *Advanced* > *Go to (Unsafe)* > *Allow*).

**🎉 Done!** You will get a `https://script.google.com/...` link. This is your Live App URL.

---

## 🔄 How to Update the App?

If you make changes to the React code:

1.  Run `npm run build` again.
2.  Copy the new code from `dist/index.html`.
3.  Paste it into the `index.html` file in the Apps Script Editor.
4.  **Crucial Step:** Click **Deploy** > **Manage deployments** > Edit (Pencil Icon) > **Version: New version** > **Deploy**.
    *   *If you don't create a "New version", your changes will not reflect on the live link.*

---
