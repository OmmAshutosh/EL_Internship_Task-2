# 🛡️ Task-2: Analyze a Phishing Email Sample

## 🎯 Objective  
Identify phishing characteristics in a suspicious email and learn how to detect social engineering red flags in emails.

---

## 🧰 Tools Used

- ✉️ Email client or saved `.eml` / `.txt` phishing email file  
- 🌐 [Online Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

---

## 📝 Task Steps

### ✅ Step 1: Obtain a Sample Phishing Email

- You can find publicly available phishing email samples from:
  - [Phishing.Email](https://phishing.email/)
  - [OpenPhish](https://openphish.com/)
  - TryHackMe / CTF rooms
- Save as `.txt` or open in your email client to view raw headers.
- Link: https://github.com/OmmAshutosh/EL_Internship_Task-2/blob/105cee02ce54c895b090500ce2355dfaa0955528/phishing_sample.txt
  ![image](https://github.com/OmmAshutosh/EL_Internship_Task-2/blob/105cee02ce54c895b090500ce2355dfaa0955528/1.2.png)

---

### ✅ Step 2: Examine the Sender's Address

- **Check for spoofing**:
  - Does the "From" name match the actual email address?
  - Example:  
    ```
    From: Amazon Support <suspicious@maliciousdomain.com>
    ```
  - Look for domains that are similar but off (e.g., `amaz0n.com` instead of `amazon.com`).
   ![image](https://github.com/OmmAshutosh/EL_Internship_Task-2/blob/105cee02ce54c895b090500ce2355dfaa0955528/1.png)
---

### ✅ Step 3: Analyze Email Headers

- Copy full headers and paste into:
  - 🛠️ [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx)

- **Check for:**
  - SPF/DKIM/DMARC failures
  - Sender IP address (match with domain?)
  - Delays or unusual hops
    ![image](https://github.com/OmmAshutosh/EL_Internship_Task-2/blob/105cee02ce54c895b090500ce2355dfaa0955528/2.png)

---

### ✅ Step 4: Check for Suspicious Links or Attachments

- Hover over links in the email:
  - Does the displayed URL match the actual one?
  - Example:
    ```
    Click here to verify → https://secure-amazon.com.verify-login.ru
    ```
    ![image](https://github.com/OmmAshutosh/EL_Internship_Task-2/blob/105cee02ce54c895b090500ce2355dfaa0955528/3.png)

- **Attachments:**  
  - `.exe`, `.scr`, `.js`, `.zip` → 🚨 red flags

---

### ✅ Step 5: Look for Urgent or Threatening Language

Phishing often uses fear, urgency, or pressure:
- "Your account will be suspended"
- "Immediate action required"
- "Verify your identity now!"

---

### ✅ Step 6: Check for Grammar and Spelling Errors

- Legitimate companies rarely send emails with:
  - Poor grammar
  - Typos or awkward language

---

### ✅ Step 7: Summarize Phishing Traits Found

Create a report or table with the phishing indicators:

| 🔍 Indicator                  | 💡 Description                                      |
|------------------------------|----------------------------------------------------|
| 🧑‍💻 Fake sender address       | Spoofed domain like `support@amaz0n.net`           |
| 🌍 Mismatched links           | Displayed vs actual URLs differ                    |
| 📎 Suspicious attachment      | Attached `.exe` file attempting malware delivery   |
| ⚠️ Urgent language            | "Your account will be locked in 24 hours"         |
| 🧾 Spelling/grammar mistakes  | "Pleaze verify your acount immdiately"            |
| ❌ SPF/DKIM/DMARC failed      | Email authentication not verified                 |

---

## ✅ Deliverable

- 📄 A report listing all **phishing indicators** discovered in the email sample.

---

## 🔐 Ethical Reminder

**Do not open unknown attachments or click any live links in real phishing emails. Analyze them in a safe, sandboxed or offline environment.**

