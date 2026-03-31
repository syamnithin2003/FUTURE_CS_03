# API Security Risk Analysis (Modern SaaS Skill)

## Overview

This project presents a **read-only API Security Risk Analysis** conducted on a public API. The goal is to identify common security vulnerabilities and understand their impact in real-world SaaS applications.

---

## Scope

* Public API testing only
* Read-only requests (GET)
* No exploitation or attacks performed
* Ethical and safe analysis

---

## Tools Used

* **Postman** – API testing
* **Browser DevTools** – Header & cookie inspection

---

## API Tested

* **JSONPlaceholder**
* https://jsonplaceholder.typicode.com

---

## Methodology

### 1. API Testing (Postman)

* Sent GET requests to public endpoints
* Observed:

  * Status codes
  * Response data
  * Authentication requirements

### 2. Headers Analysis

* Inspected response headers
* Identified:

  * Security headers
  * Technology exposure
  * Rate limiting

### 3. Data Exposure Review

* Checked API responses for:

  * Sensitive data
  * Overexposed fields

### 4. Browser DevTools Analysis

* Inspected:

  * Cookies
  * Authorization tokens
  * Security configurations

---

## Key Findings

### High Risk

* No authentication required
* Sensitive cookies with SameSite=None

### Medium Risk

* Excessive data exposure
* X-XSS protection disabled
* Authorization token exposure

### Low Risk

* Binary content-type
* High rate limit threshold

---

## Recommendations

* Implement authentication (API keys / OAuth)
* Restrict data exposure (least privilege)
* Use secure cookie settings:

  * HttpOnly
  * Secure
  * SameSite=Strict
* Enable XSS protection or CSP
* Reduce rate limits
* Avoid exposing backend technologies

---

## Proof of Concept

* Screenshots of tool outputs are available in the `Proof of Concept/` folder.

---

## Ethics

This analysis was conducted under strict ethical guidelines:

* No exploitation
* No harm to systems
* Only public/demo APIs tested

---

## Created

**Yanamadala Syam Nithin**

syamnithin2003@gmail.com

---

## Conclusion

Even public APIs can expose serious vulnerabilities if not properly secured. This project highlights the importance of secure API design in modern SaaS applications.
