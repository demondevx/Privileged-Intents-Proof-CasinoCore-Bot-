# 📜 Privileged Intents Proof — CasinoCore Bot

Hello Discord Trust & Safety Team,

This document provides detailed justification for why **CasinoCore** requires the following privileged intents:

* **Server Members Intent**
* **Message Content Intent**

Each section explains the exact bot features that rely on the intent along with demonstration proofs.

---

# 🧠 About CasinoCore

CasinoCore is a comprehensive **economy, banking, court roleplay, and server management bot** that provides advanced automation systems including:

* Economy & banking
* Court & legal roleplay system
* Police & license system
* Role-based salary automation
* Case management workflows
* Chat-based rewards
* Custom replies
* Store & inventory system

Many of these systems require verifying roles, processing interactions, and temporarily reading message content to function correctly.

---

# 👥 Server Members Intent (GUILD_MEMBERS)

## Why This Intent Is Required

CasinoCore relies heavily on role-based permissions and automated role management.
The bot must access member objects to verify roles, assign roles, and remove roles when permissions or licenses change.

## Features That Require Server Members Intent

### Role Assignment & Verification

* Assigning **Judge**, **Chief Justice**, and **Police** roles
* Verifying permissions before executing restricted commands
* Checking role hierarchy for court and police actions

### License Systems

* Assigning lawyer licenses
* Assigning police licenses after exam
* Removing roles when license expires
* Revoking licenses by judge command

### Automated Role Removal

* License expiration automation
* Premium role assignment/removal
* Salary system role verification

### Permission Enforcement

* Restricting commands to:

  * Judges
  * Chief Justice
  * Police
  * Admins
* Verifying role access before executing sensitive actions

Without Server Members intent, CasinoCore cannot:

* Assign or revoke roles
* Validate permissions
* Enforce role-based command access
* Run license expiration automation

---

## 🎥 PROOF 1 — Server Members Intent

Proof Videos and screenshots:
-  [📷 Screenshot 1 - Role Restriction](https://i.postimg.cc/MHqtQHGr/svimg.png)
- [🎥 Video 1 - Role Assignment](https://youtube.com/shorts/DW8JfLtQMQc)
- [🎥 Video 2 - License/Role Revoke Action](https://youtube.com/shorts/MgXiEgHrqsM)
- [🎥 Video 3 - System Configuration](https://youtube.com/shorts/jkgRzzRWUFk)

**Show:**

* Assigning Judge / Police role via command
* Bot checking role permissions
* Bot removing role on license expiry or revoke

**Caption:**
*Demonstration of role-based permission and automated role management requiring Server Members intent.*

---

# 💬 Message Content Intent (MESSAGE_CONTENT)

## Why This Intent Is Required

CasinoCore uses message content **only for specific server features** such as chat economy rewards and custom reply triggers.
The bot does NOT read messages outside of these features.

Message content is processed **temporarily** and never stored.

---

## Features That Require Message Content Intent

### Chat Economy System

* Detecting when users send messages
* Rewarding chat money
* Enforcing cooldowns
* Preventing spam rewards

### Custom Reply System

* Triggering custom responses based on keywords
* Fail reply detection
* Server automation responses

### Court Roleplay System

* Processing case details submitted by users
* Reading evidence text
* Handling court workflows

### Interaction Workflows

* Reading user input for structured systems like:

  * Case submission
  * Evidence submission
  * Court notes

Without Message Content intent, these features cannot function.

---

## 🎥 PROOF 2 — Message Content Intent (Chat Economy)

**Type:** Video


- [🎥 Video 1 - User getting rewarded for chat](https://youtube.com/shorts/sF14tIG-_XE)
- [🎥 Video 1 - User getting rewarded for chat 2nd pov](https://youtube.com/shorts/WCNGdVqet3g?feature=share)

**Show:**

* User chatting
* Bot rewarding chat money
* Cooldown working

**Caption:**
*Demonstration of chat-based economy system that requires Message Content intent.*

---

## 🎥 PROOF 3 — Custom Replies

**Type:** Screenshot 
-  [📷 Screenshot 1 - Custom Replies Setup](https://i.postimg.cc/hGJKkPKX/msg1.png)

**Show:**

* Custom reply triggered by message
* Fail reply example

**Caption:**
*Custom reply system that processes user message content.*

---

## 🎥 PROOF 4 — Court / Roleplay System

**Type:** Video and screenshots
- [🎥 Video 1 - Evidence Submission](https://youtube.com/shorts/Upj-803EkRs)
- [🎥 Video 2 - Court Decision](https://youtube.com/shorts/F7mhMUb7pDM)
- [📷 Screenshot 1 - Case Submission](https://i.postimg.cc/G22vwDHr/court1.png)
- [📷 Screenshot 2 - Case Evidence Submission](https://i.postimg.cc/gJJ3FhrC/court2.png)
- [📷 Screenshot 3 - Case Submitted](https://i.postimg.cc/k44W3SB3/court3.png)
- [📷 Screenshot 4 - Evidence Submitted](https://i.postimg.cc/W330LZhR/court4.png)
- [📷 Screenshot 5 - Case Decision Modal](https://i.postimg.cc/B6629FX0/court5.png)
- [📷 Screenshot 6 - Case Submitted](https://i.postimg.cc/VN4XVgsp/court6.png)


**Show:**

* Case submission
* Evidence text
* Judge decision

**Caption:**
*Roleplay and court system features that rely on message content and role verification.*

---

# 🔒 Data Storage & Privacy

CasinoCore is designed with privacy and minimal data usage principles.

## Data We Store

We only store non-sensitive operational data required for features:

* Guild IDs
* User IDs
* Economy balances
* Case records
* License status
* Configuration settings
* Transaction logs
* Premium status

## Data We DO NOT Store

* Message content history
* User conversations
* DMs
* Personal user data
* Presence/activity tracking
* Message logs

Message content is processed **ephemerally in memory** and never stored permanently.

---

## Data Usage Purpose

Stored data is used only to operate core features:

* Running economy and banking
* Managing court cases
* Enforcing permissions
* Tracking licenses
* Processing transactions
* Server configuration

---

## Data Retention

Data remains only while the server actively uses the bot.
Server owners may request deletion at any time.

---

## 🎥 PROOF 5 — Privacy

**Type:** Screenshot

**Show:**

* No message logging
* No DM reading
* Temporary processing only

**Caption:**
*Bot processes message content temporarily and does not store user messages.*

---

# 🛡 Security Practices

* MongoDB with authentication
* Access control enforcement
* No third-party data sharing
* No selling of user data
* Minimal data collection principle
* Secure role-based permission system

---

# 📞 Contact

Support Server:
https://discord.gg/AR8HkshRtW

Privacy Policy:
https://github.com/demondevx/CasinoCore/blob/main/PrivacyPolicy.md

Developer Contact:
https://discord.com/users/555652788592443392

Email:
[support@demondev.org](mailto:support@demondev.org)

---

# ✅ Final Summary

CasinoCore requires privileged intents strictly for core functionality:

**Server Members Intent**

* Role assignment
* License management
* Permission enforcement
* Role expiration automation

**Message Content Intent**

* Chat economy rewards
* Custom replies
* Court roleplay workflows

The bot processes only necessary data, does not store message content, and follows strict privacy practices.

Thank you for reviewing our request.

---

**CasinoCore Development Team**
