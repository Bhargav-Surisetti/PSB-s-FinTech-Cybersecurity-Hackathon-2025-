# FraudShield+  
*PSB’s FinTech Cybersecurity Hackathon 2025 – Solution Approach*  

## Overview  
FraudShield+ is an advanced fraud detection engine designed to secure **mobile and internet banking platforms** during user registration and login. It combines **behavioral biometrics, FIDO2 password-less authentication, and continuous monitoring of SIM, device, and geolocation data** to detect and prevent fraudulent access.  

This solution was developed and submitted at **PSB’s FinTech Cybersecurity Hackathon 2025** by *Team Arjuna*.  

---

## Problem Statement  
Impersonated registrations and fraudulent device logins remain major threats in digital banking.  
- **Issue**: Standard OTP-based security is vulnerable to interception, phishing, SIM swaps, and device spoofing.  
- **Impact**: Account takeovers, monetary loss, and reduced consumer trust.  
- **Target Users**: Bank customers using mobile/internet banking and fraud analysis teams at financial institutions.  

---

## Proposed Solution – FraudShield+  
FraudShield+ integrates seamlessly with existing banking systems to provide a **multi-layered defense** against fraud.  

### Core Functionalities  
1. **Real-Time Risk Scoring**  
   - Compares login/registration attempts with user profiles (device, SIM, location, behavior).  
   - Generates a dynamic risk score.  

2. **Adaptive Authentication**  
   - Blocks high-risk attempts, auto-approves low-risk, and challenges medium-risk with biometrics/FIDO2.  

3. **Admin Intelligence Dashboard**  
   - Provides real-time insights, alerts, and location mismatch maps for fraud analysts.  

---

## Technical Architecture  

**Tech Stack**  
- **Backend**: Python (Flask)  
- **AI/ML**: TensorFlow, Scikit-learn, Pandas  
- **Database**: PostgreSQL, MongoDB  
- **Authentication**: FIDO2 / WebAuthn  
- **Dashboard**: Streamlit / Dash  
- **Geolocation & Notifications**: Geopy, IPStack API, Twilio (SMS), Firebase (Push), Gmail SMTP  
- **Deployment**: Docker, AWS EC2  

**Data Flow**  
1. User attempts registration/login.  
2. System collects device, SIM, geolocation, and behavioral data.  
3. Features extracted → Risk Scoring Engine calculates weighted risk.  
4. Based on risk: Approve, challenge, or block.  
5. Event logged and displayed in the admin dashboard.  

---

## Risk Scoring Engine  
A **rule-based weighted model** enhanced with ML-based behavioral anomaly detection.  

- New SIM swap (<72 hrs): +40  
- Untrusted/new device: +30  
- Location mismatch (>300 km): +20  
- Behavioral anomalies (>20% deviation): +20  
- Threat Intelligence match: +10  

---

## Innovation & Value Proposition  
- 🔐 **Multi-Layered Defense** – Device, SIM, location, behavior, and threat intelligence.  
- 🌍 **Inclusive Design** – Supports both feature phones (IVR/SMS) and smartphones (FIDO2).  
- ⚡ **Proactive Security** – Stops fraud **before** it occurs.  
- 🛡️ **Privacy-Compliant** – Alerts without exposing sensitive data.  
- ☁️ **Cloud-Native Scalability** – Built for real-world deployment.  

---

## Files in this Repository  
- `FraudShield+.pdf` → Full solution approach document.  
- (Optional) Code/Prototype (if added later).  

---

## Outcome  
Although not shortlisted, FraudShield+ demonstrated a **robust, future-proof fraud detection model** with strong potential for real-world banking applications.  

---

## Team  
👨‍💻 **Team Arjuna**  
PSB’s FinTech Cybersecurity Hackathon 2025  
