# Garmin Connect Developer Program Partnership Proposal

---

**Applicant:** Creative Life Labo  
**Application:** Run Diary  
**Date:** January 9, 2026  
**Document Version:** 1.0

---

## Executive Summary

Run Diary is an AI-powered running journal application that leverages Garmin Connect data to provide personalized training recommendations. By integrating with the Garmin ecosystem, Run Diary transforms detailed fitness metrics into actionable coaching insights, enhancing the value proposition of Garmin wearable devices for endurance athletes.

This document outlines our application's purpose, data usage requirements, privacy practices, and the mutual benefits of this partnership.

---

## 1. Company Overview

### 1.1 About Creative Life Labo

| Item | Details |
|------|---------|
| **Company Name** | Creative Life Labo |
| **Website** | https://www.1cll.com |
| **Primary Contact** | hello@1cll.com |
| **Business Focus** | AI-powered fitness and lifestyle applications |

### 1.2 Mission Statement

Creative Life Labo is dedicated to making advanced fitness analytics accessible to everyday athletes. We believe that the wealth of data collected by modern wearable devices should translate into clear, actionable guidance that helps users achieve their goals safely and effectively.

---

## 2. Application Overview

### 2.1 Product Information

| Item | Details |
|------|---------|
| **Product Name** | Run Diary |
| **Product URL** | https://www.1cll.com/en/products/run-diary |
| **Application URL** | https://run-diary-2026.web.app |
| **Platform** | Web Application (Progressive Web App) |
| **Target Users** | Recreational to intermediate runners |
| **Languages Supported** | English, Japanese |

### 2.2 Product Description

Run Diary is an AI-powered running journal that serves as a personal running coach. The application addresses a common challenge faced by runners: while wearable devices excel at collecting comprehensive fitness data, users often struggle to interpret this data and determine optimal next steps in their training.

Run Diary bridges this gap by applying artificial intelligence to analyze training patterns and provide personalized, context-aware coaching recommendations.

### 2.3 Core Features

| Feature | Description |
|---------|-------------|
| **AI Training Suggestions** | Daily personalized workout recommendations based on recent activity, sleep quality, and recovery metrics. Offers three options: aggressive, standard, and recovery. |
| **Dynamic Pace Zone Calculation** | Continuously recalibrates pace zones using the most recent 30 days of training data, ensuring accuracy regardless of time since last race. |
| **Race Pacing Strategy** | Generates realistic finish time predictions and 5km split strategies based on training history and current fitness level. |
| **Context-Aware AI Chat** | Conversational AI coach that references actual user data when answering training-related questions. |

### 2.4 Technology Stack

| Component | Technology |
|-----------|------------|
| Frontend | Next.js (React) |
| Backend | Firebase (Google Cloud Platform) |
| AI Engine | Google Gemini AI |
| Authentication | Firebase Authentication |
| Data Storage | Cloud Firestore |

---

## 3. Garmin Connect Data Requirements

### 3.1 Requested Data Types

Run Diary requests access to the following Garmin Connect data categories to provide its core functionality:

| Data Type | Purpose | Required |
|-----------|---------|----------|
| **Activities** | Analyze running workouts (distance, duration, pace, heart rate, cadence) to identify training patterns and progress | Yes |
| **Sleep** | Factor sleep duration and quality into recovery assessment and training recommendations | Yes |
| **Heart Rate Variability (HRV)** | Assess physiological readiness and detect early signs of overtraining | Yes |
| **VO2 Max Estimates** | Calibrate dynamic pace zones and generate accurate race predictions | Yes |
| **Training Load** | Balance workout intensity with appropriate recovery periods | Recommended |
| **Body Battery / Readiness** | Determine optimal daily training intensity based on current energy levels | Recommended |

### 3.2 Data Usage Specifications

#### 3.2.1 AI Training Suggestions

**Input Data:** Activities (past 7-14 days), Sleep (past 7 days), HRV (past 7 days), Training Load

**Processing Logic:**
- Analyze cumulative training load and recent workout intensity
- Evaluate sleep quality trends and recovery indicators
- Apply evidence-based training principles (e.g., avoid consecutive high-intensity days)
- Generate three training options calibrated to current physiological state

**Output:** Daily workout recommendation with three intensity options

#### 3.2.2 Dynamic Pace Zone Calculation

**Input Data:** Activities (past 30 days), VO2 Max Estimates

**Processing Logic:**
- Collect pace and heart rate data from recent runs
- Apply regression analysis to identify current fitness trends
- Recalculate VDOT-equivalent training zones
- Adjust zones based on VO2 Max trajectory

**Output:** Updated pace zones (Easy, Marathon, Threshold, Interval, Repetition)

#### 3.2.3 Race Pacing Strategy

**Input Data:** Activities (historical), VO2 Max Estimates

**Processing Logic:**
- Analyze long run performance and tempo workout data
- Model predicted race performance based on training indicators
- Generate progressive pacing strategy (negative split optimization)
- Apply environmental adjustments (temperature, humidity) when available

**Output:** Target splits for 5km segments with adjustable pacing profiles

#### 3.2.4 Context-Aware AI Coaching

**Input Data:** All available data types (dynamically selected based on user query)

**Processing Logic:**
- Natural language processing to identify query intent
- Smart context retrieval: select only relevant data categories
- Generate personalized response using Google Gemini AI
- Maintain conversation context for follow-up questions

**Output:** Personalized coaching response with data-backed insights

---

## 4. Privacy and Data Protection

### 4.1 Privacy Policy

Our comprehensive privacy policy is publicly available at:

**English:** https://www.1cll.com/en/privacy  
**Japanese:** https://www.1cll.com/privacy

The privacy policy includes a dedicated section (Section 2A) specifically addressing Garmin Connect data handling.

### 4.2 GDPR Compliance

Run Diary is designed with GDPR compliance as a foundational requirement:

| Requirement | Implementation |
|-------------|----------------|
| **Legal Basis** | Explicit user consent required before Garmin Connect authorization |
| **Data Minimization** | Request only data necessary for stated functionality |
| **Purpose Limitation** | Data used exclusively for described features |
| **User Rights** | Full support for access, rectification, erasure, portability, and objection rights |
| **International Transfers** | Covered by Standard Contractual Clauses (SCCs) and adequacy decisions |
| **Automated Processing** | AI recommendations are advisory only; no legally binding decisions |

### 4.3 Data Security Measures

| Measure | Description |
|---------|-------------|
| **Encryption at Rest** | All data encrypted in Cloud Firestore using AES-256 |
| **Encryption in Transit** | TLS 1.3 for all data transmission |
| **Authentication** | Firebase Authentication with OAuth 2.0 |
| **Access Control** | User data isolated by Firebase Security Rules |
| **Audit Logging** | Cloud Logging for security event monitoring |

### 4.4 Data Retention and Deletion

| Policy | Details |
|--------|---------|
| **Active Account** | Data retained while account is active |
| **Account Deletion** | All user data permanently deleted upon request |
| **Garmin Disconnection** | Sync immediately stops; historical data retained until deletion requested |
| **Deletion Timeline** | Requests processed within 30 days |

### 4.5 Third-Party Data Sharing

| Commitment | Details |
|------------|---------|
| **No Sale of Data** | User data is never sold to third parties |
| **No Advertising Use** | Data is not used for advertising or marketing purposes |
| **AI Processing** | Google Gemini AI processes data solely for generating coaching responses |
| **Anonymized Analytics** | Aggregated, non-identifiable data may be used for service improvement |

---

## 5. Value Proposition for Garmin Ecosystem

### 5.1 Enhanced Device Value

Run Diary increases the practical value of Garmin wearable devices by transforming raw data into actionable insights. Users gain more utility from their Garmin investment, reinforcing the value of the Garmin ecosystem.

### 5.2 Increased User Engagement

Daily AI-generated training recommendations create consistent touchpoints with fitness data, encouraging regular engagement with both Run Diary and Garmin Connect.

### 5.3 Complementary Positioning

Run Diary is positioned as a complement to, not a replacement for, Garmin Connect:

| Garmin Connect | Run Diary |
|----------------|-----------|
| Comprehensive data recording | AI-powered data interpretation |
| Historical data visualization | Forward-looking training recommendations |
| Device management | Personalized coaching conversations |
| Social features | Individual training optimization |

### 5.4 Competitive Differentiation

| Feature | Garmin Connect | Strava | TrainingPeaks | Run Diary |
|---------|---------------|--------|---------------|-----------|
| Data Recording | ✓ | ✓ | ✓ | ✓ (via Garmin) |
| AI Training Suggestions | — | — | — | ✓ (3 daily options) |
| Dynamic Pace Zones | — | — | — | ✓ (30-day recalibration) |
| AI Chat Coach | — | — | — | ✓ (10 coach personalities) |
| Multi-language AI | — | — | — | ✓ (EN/JP) |

---

## 6. User Testimonial

> "I was recording daily runs with Garmin but always wondered, 'What should I do next?' Since using Run Diary, I wake up to AI-recommended workouts every morning. On days when my sleep was poor, recovery workouts are automatically suggested. I no longer stress about training planning."
>
> — Run Diary Beta User

---

## 7. Technical Integration

### 7.1 Integration Architecture

```
┌─────────────────┐     OAuth 2.0      ┌─────────────────┐
│  Garmin Connect │◄──────────────────►│    Run Diary    │
│       API       │    Data Sync       │   Application   │
└─────────────────┘                    └─────────────────┘
                                              │
                                              ▼
                                       ┌─────────────────┐
                                       │    Firebase     │
                                       │  Cloud Firestore│
                                       └─────────────────┘
                                              │
                                              ▼
                                       ┌─────────────────┐
                                       │  Google Gemini  │
                                       │       AI        │
                                       └─────────────────┘
```

### 7.2 API Usage Patterns

| Pattern | Frequency | Purpose |
|---------|-----------|---------|
| Initial Sync | Once | Import historical data upon connection |
| Daily Sync | 1-2x daily | Retrieve new activities and metrics |
| On-Demand | User-initiated | Refresh data before AI consultation |

### 7.3 Rate Limiting Compliance

Run Diary is designed to operate within Garmin API rate limits through:
- Efficient batch data retrieval
- Client-side caching to minimize API calls
- Background sync during off-peak hours

---

## 8. Contact Information

For questions regarding this partnership proposal or technical integration:

| Contact Type | Details |
|--------------|---------|
| **General Inquiries** | hello@1cll.com |
| **Website** | https://www.1cll.com |
| **Product Page** | https://www.1cll.com/en/products/run-diary |
| **Privacy Policy** | https://www.1cll.com/en/privacy |

---

## 9. Appendices

### Appendix A: Links Summary

| Resource | URL |
|----------|-----|
| Company Website | https://www.1cll.com |
| Run Diary Product Page | https://www.1cll.com/en/products/run-diary |
| Garmin Integration Details | https://www.1cll.com/en/products/run-diary#garmin-integration |
| Privacy Policy (English) | https://www.1cll.com/en/privacy |
| Privacy Policy (Japanese) | https://www.1cll.com/privacy |
| Application | https://run-diary-2026.web.app |

### Appendix B: Screenshots

*[Screenshots of the application can be found on the product page]*

https://www.1cll.com/en/products/run-diary

---

**Document Prepared By:** Creative Life Labo  
**Date:** January 9, 2026  
**Confidentiality:** This document is intended for Garmin Developer Program review purposes.

---

*© 2026 Creative Life Labo. All rights reserved.*
