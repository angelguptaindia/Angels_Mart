# Angels Mart 🛒

A clean, responsive, and lightweight grocery store web application powered dynamically by a live **Google Sheets** backend.

🔗 **Live Demo**: [https://angelguptaindia.github.io/Angels_Mart/](https://angelguptaindia.github.io/Angels_Mart/)

---

## 🌟 Features

- **Live Google Sheets Integration**: Inventory is fetched dynamically from a published Google Sheet (CSV format) without needing a dedicated backend server or database.
- **Dual View Modes**: Seamless toggle between responsive **Grid View** (cards) and compact **List View**.
- **Stock & Availability Controls**:
  - Out-of-stock items are visually flagged with an "Out of Stock" badge and muted styling.
  - Prompts a confirmation modal if a customer attempts to add an out-of-stock item.
  - Checkout confirmation modal allows customers to choose whether to include or exclude out-of-stock items in their final receipt.
- **Dynamic Pricing & Discounts**:
  - Calculates discounted prices automatically based on percentage discounts.
  - Highlights active discount tags.
- **Itemized Bill & Receipt**:
  - Modal displaying an itemized checkout receipt table with quantities, prices, total savings, and grand total.
- **Robust CSV Parser**:
  - Handles quoted entries containing commas, Unix/Windows line endings (`\r\n`), and sanitized currency symbols (`$`, `,`).
- **Zero Heavy Dependencies**: Built with pure HTML5, modern CSS3, and Vanilla JavaScript.

---

## 📋 Google Sheet Data Format

Your Google Sheet should include the following headers in the first row:

| Item Code | Item Name | Item Cost | Item Stock | Discount |
| :--- | :--- | :--- | :--- | :--- |
| `SUP-1001` | Canned Beans 400g | 19.92 | 0 | 0 |
| `SUP-1002` | Sparkling Water 1.5L | 1.74 | 10 | 0 |
| `SUP-1003` | Spinach 250g | 32.44 | 2 | 5 |

### How to publish your Google Sheet:
1. Open your Google Sheet.
2. Go to **File** > **Share** > **Publish to web**.
3. Under the *Link* tab, select your sheet and choose **Comma-separated values (.csv)** as the export format.
4. Click **Publish** and copy the generated link.
5. In `index.html`, set the `GOOGLE_SHEET_URL` constant:
   ```javascript
   const GOOGLE_SHEET_URL = "YOUR_PUBLISHED_CSV_LINK_HERE";
   ```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/angelguptaindia/Angels_Mart.git
cd Angels_Mart
```

### 2. Run Locally

You can open `index.html` directly in any modern browser:

```bash
open index.html
```

Or run a lightweight local HTTP server using Python:

```bash
# Python 3
python3 -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) in your web browser.

---

## 🛠️ Tech Stack

- **HTML5**: Semantic document structure
- **CSS3**: Custom variables, responsive grid/flexbox layouts, micro-interactions, modal overlays
- **JavaScript (ES6+)**: Fetch API, dynamic DOM manipulation, state management for cart and view modes

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
