# HTML Injection via Unsanitized User Input

## Attack Category
Client-Side Injection

## Environment
Ethical lab environment (TryHackMe)

---

## Scenario Overview
A web application accepted user input via a search field and reflected it back to the page without sanitization.

---

## Root Cause
- User-controlled input was rendered directly into HTML
- No input sanitization or output encoding was applied
- Browser interpreted attacker-supplied HTML as trusted markup

---

## Attack Flow
1. Identify input field that reflects user input
2. Inspect frontend source code
3. Confirm lack of sanitization
4. Inject custom HTML payload
5. Payload rendered successfully by the browser

---

## Impact
- Arbitrary HTML injection
- Malicious links can be injected
- Phishing opportunities
- Foundation for XSS escalation

---

## Mitigation
- Input validation on server-side
- Output encoding
- Use of secure templating engines
- Content Security Policy (CSP)

---

## Key Takeaway
HTML Injection is often dismissed as low-risk but can be a stepping stone to more severe client-side attacks when combined with poor security controls.
