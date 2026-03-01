# 🔐 Multiple OTP Bypass Vulnerabilities

**Program:** Bugcrowd Public Program  
**Category:** Authentication Bypass  
**Severity:** Informational  
**Status:** Resolved / Acknowledged

---

## 📌 Overview

During security testing through a bug bounty program, I identified two authentication logic vulnerabilities related to OTP verification.

Both issues allowed bypassing OTP verification under specific conditions.

The vulnerabilities were responsibly disclosed and acknowledged by the security team.

---

## 🧪 Vulnerability 1 — Sign-Up OTP Bypass

### Description

OTP verification was not properly enforced during account registration.

It was possible to complete the sign-up process without verifying the OTP.

### Impact

An attacker could:

- Create unverified accounts  
- Abuse automated registrations  
- Bypass identity verification  

### Root Cause

The backend trusted client-side verification flags instead of securely validating OTP status.

### Generalized Steps

1. Register a new account  
2. Intercept verification request  
3. Modify verification parameters  
4. Submit request  
5. Account created without OTP verification

*(Sensitive details removed)*

---

## 🔑 Vulnerability 2 — Login OTP Bypass

### Description

OTP verification after password authentication was not properly enforced.

OTP verification could be bypassed allowing dashboard access.

### Impact

An attacker with valid credentials could:

- Bypass second-factor authentication  
- Access accounts without OTP verification  

### Root Cause

OTP verification state was not strictly validated server-side.

### Generalized Steps

1. Login with valid credentials  
2. Intercept OTP verification request  
3. Modify parameters  
4. Send request  
5. Access granted

*(Sensitive details removed)*

---

## 🛡 Responsible Disclosure

These vulnerabilities were reported responsibly via Bugcrowd.

The security team:

- Acknowledged the findings  
- Reproduced the issues  
- Reviewed the impact  

---

## 📚 Lessons Learned

This research improved my understanding of:

- Authentication logic testing  
- OTP workflows  
- Request manipulation  
- Access control validation  

---

## ⚠ Disclaimer

This writeup is shared for educational purposes only.

Sensitive technical details and target information have been removed.
