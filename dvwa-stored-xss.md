# DVWA Stored XSS Lab

## Vulnerability
Stored Cross-Site Scripting (XSS)

## Environment
- Application: DVWA
- Security Level: Low
- Target: localhost

## Testing

### Normal Input
Name:
`Test`

Message:
`Hello DVWA`

The message was stored and displayed on the guestbook.

### XSS Test
Payload:
`<script>alert('XSS')</script>`

Result:
A JavaScript alert appeared when the stored message was rendered.

## Impact
An attacker may be able to store malicious JavaScript that executes in the browser of users who view the affected page.

## Mitigation
- Properly encode output before rendering it in HTML.
- Validate and sanitize user input where appropriate.
- Use a suitable Content Security Policy (CSP).
- Avoid inserting untrusted data into HTML without contextual escaping.
