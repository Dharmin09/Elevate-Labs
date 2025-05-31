# 📧 Task 2: Phishing Email Analysis Report

This task involves analyzing a suspicious email to identify phishing characteristics and learn how to detect social engineering tactics in real-world scenarios.

---

## ⚠️ Phishing Indicators Found

| #  | Phishing Characteristic      | Observation |
|----|------------------------------|-------------|
| 1. | **Spoofed Email Address**    | Appears as `apple.security@support-apple.com`, which is not a legitimate Apple domain. |
| 2. | **Mismatched URLs**          | Link text looks like Apple support, but URL is `support-verify-account.com`, which is suspicious. |
| 3. | **Urgent/Threatening Language** | "Your Apple ID will be permanently locked" – uses fear to provoke immediate action. |
| 4. | **Suspicious Link**          | Non-HTTPS link to an unknown domain, not related to Apple. |
| 5. | **Generic Greeting**         | Uses "Dear Customer" instead of the recipient's real name. |
| 6. | **Grammar Issues**           | Minor grammatical and flow issues in the body of the email. |
| 7. | **Header Analysis Findings** | Return-Path, Reply-To, and SPF/DKIM do not match Apple’s verified infrastructure. |
| 8. | **Unusual Sending Server/IP**| Email originated from an unknown IP in Eastern Europe. |

---

## 🛠️ Tools Used

- **Email Header Analyzer**: [MXToolbox Email Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

---

## ✅ Conclusion

This email is a **phishing attempt**. It displays multiple red flags, including:
- Spoofed sender address
- Suspicious and mismatched links
- Fear-based urgency
- Failed authentication in headers

⚠️ **Do not click** on any link or respond. Always verify directly from the official source.

---

> 🔐 Stay alert. Think before you click.
