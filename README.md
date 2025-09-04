# Cloudflare Bypass Scraper API

[![API Version](https://img.shields.io/badge/version-1.0.0-blue)](https://rapidapi.com/pdftask-pdftask-default/api/cloudflare-bypass-scraper) [![License](https://img.shields.io/badge/license-MIT-green)](LICENSE) [![RapidAPI](https://img.shields.io/badge/RapidAPI-Cloudflare%20Bypass-blue)](https://rapidapi.com/pdftask-pdftask-default/api/cloudflare-bypass-scraper)

Fetch **raw HTML** from any webpage, even if it’s behind **Cloudflare protection** or relies on **JavaScript rendering**. Ideal for **developers, SEO specialists, and automation tools**.

---

## 🚀 Features

- **Cloudflare bypass** – Access pages behind Cloudflare firewall.  
- **JavaScript support** – Fetch client-side rendered content.  
- **Raw HTML output** – Clean, ready-to-use HTML.  
- **Proxyless** – No additional setup required.  
- **Multi-language support** – Easy integration with Python, Node.js, Bash, and more.  

---

## 📌 API Endpoint

```

GET /get-html?url={TARGET\_URL}

````

### Parameters

| Name  | Type   | Required | Description                                   |
|-------|--------|---------|-----------------------------------------------|
| url   | string | ✅       | The target webpage to scrape (e.g. `https://example.com`) |

---

## 💻 Example Usage

### Bash / cURL
```bash
curl --request GET \
  --url 'https://api.rapidapi.com/get-html?url=https://example.com' \
  --header 'X-RapidAPI-Key: YOUR_API_KEY'
````

### Python

```python
import requests

url = "https://api.rapidapi.com/get-html?url=https://example.com"
headers = {"X-RapidAPI-Key": "YOUR_API_KEY"}
response = requests.get(url, headers=headers)
print(response.text)
```

### JavaScript (Node.js)

```javascript
const fetch = require('node-fetch');

const url = "https://api.rapidapi.com/get-html?url=https://example.com";
fetch(url, { headers: { "X-RapidAPI-Key": "YOUR_API_KEY" } })
  .then(res => res.text())
  .then(console.log)
  .catch(console.error);
```

---

## 📄 Example Response

```json
{
  "html": "<!DOCTYPE html><html><head><title>Example Domain</title></head><body>...</body></html>"
}
```

---

## ⚠️ Error Handling

* **400** – URL missing
* **500** – Failed to fetch page (timeout, blocked, etc.)

Example:

```json
{
  "error": "Failed to fetch HTML content",
  "details": "Navigating frame was detached"
}
```

---

## 🔗 RapidAPI Page

For subscriptions, pricing, and live testing: [Cloudflare Bypass Scraper API on RapidAPI](https://rapidapi.com/pdftask-pdftask-default/api/cloudflare-bypass-scraper)

---

## 💡 Tips

* Use this API for **SEO monitoring, web scraping, data extraction**, and **automation scripts**.
* Supports **multiple programming languages** – just pass your API key in the headers.
* No proxy setup required; ready to integrate instantly.

```

