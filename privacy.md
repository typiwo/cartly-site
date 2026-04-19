---
layout: default
title: Privacy Policy
permalink: /privacy/
---

# Privacy Policy

**Effective date:** April 17, 2026
**Last updated:** April 17, 2026

This Privacy Policy explains how Cartly ("**Cartly**," "**we**," "**us**," or "**our**") collects, uses, shares, and protects information when you use the Cartly mobile app (the "**Service**"). By using Cartly, you agree to this Policy.

## 1. Who we are

Cartly is operated by **Tyler Piwowarski**, an individual sole proprietor based in California, United States. In this Policy, "we" refers to this operator acting under the Cartly brand. If you have any questions, you can reach us at **privacy@usecartly.com**.

## 2. Information we collect

We intentionally collect as little data as possible. The information we collect is:

**Account information**
- Your email address (provided by Apple Sign In or Google Sign In). If you use Apple's "Hide My Email" feature, this will be a relay address (`...@privaterelay.appleid.com`) that forwards to your real inbox. We cannot see or unmask your real email in that case.
- Your first name (if you choose to share it during Apple Sign In).
- A unique user identifier we use internally to associate your data with your account.

**Dietary preferences**
- Your selected diet type (e.g., standard, keto, vegan).
- Your dietary alert toggles (e.g., avoid seed oils, gluten-free, dairy-free, nut-free).

**Scan and cart data**
- The text analysis results from your grocery scans (score, ingredients summary, highlights, nutrition details).
- Products you add to your cart or save.

**Subscription status**
- Whether you have an active Cartly Pro subscription, its plan type (monthly/annual), its expiration date, and the Apple transaction identifier. **All payment information is handled by Apple, not by Cartly.** We never see your credit card, bank details, or billing address.

**Camera and photo library access (only when you scan)**
- When you tap to scan a grocery item, iOS will prompt you to allow Cartly to use your **camera** and/or **photo library**. You choose whether to grant access. We only access the single photo you capture or select — we do not browse, scan, or retain any other photos from your library. You can revoke access anytime in **iOS Settings → Privacy → Photos / Camera → Cartly**.

### What we do *not* collect

We do not collect or store:
- Your precise or approximate location.
- Your contacts, calendar, health data (HealthKit), or other photos from your library.
- Your advertising identifier (IDFA), device fingerprint, or persistent tracking identifiers.
- Crash reports, usage analytics, session recordings, or telemetry from third-party SDKs.

We currently do **not** use any third-party analytics, advertising, or attribution SDKs.

## 3. How we use your information

We use your information solely to:
- Provide the scanning, scoring, search, and cart features.
- Personalize your dietary alerts based on the preferences you set.
- Validate your Cartly Pro subscription.
- Respond to support requests sent to privacy@usecartly.com.
- Comply with legal obligations.

We do not sell your personal information. We do not use your personal information for advertising or for profiling outside the scope of the Service.

## 4. How your photo is handled when you scan

When you capture or select a photo to scan:
1. The photo is read into memory on your device and encoded as base64.
2. It is sent over a TLS-encrypted connection to our Supabase Edge Function.
3. The Edge Function forwards it to the Google Gemini API for analysis.
4. The text analysis is returned to your device and saved to your scan history.

**Cartly does not save your photo.** The image is never written to our database, to Supabase Storage, to server-side logs, or to any cache we control. Only the resulting text analysis (score, ingredients, highlights, etc.) is retained in your scan history.

Google Gemini's retention and use of the image is governed by Google's terms — see Section 5 below.

## 5. Third-party services we use

The Service relies on a small number of third parties. Each handles the data described below under its own privacy terms.

**Supabase** (database, authentication, and server-side functions; hosted on AWS)
Supabase stores your account, dietary preferences, scan history, cart, and subscription status. Data is encrypted at rest and in transit. See the [Supabase Privacy Policy](https://supabase.com/privacy).

**Google Gemini API** (AI analysis of scans and product information)
When you scan or search for a product, the image and/or text is sent to Google's Gemini API through our Edge Function so the AI can analyze it. **Cartly uses the paid (billed) tier of the Gemini API.** Under Google's paid-tier Gemini API terms, Google does **not** use the content you submit — prompts, images, or the responses Google generates — to train or improve their AI models. Google may retain the content for a limited period for abuse detection, safety, and legal-compliance purposes, but not for machine-learning training. See the [Google Gemini API Additional Terms of Service](https://ai.google.dev/gemini-api/terms) and the [Google Privacy Policy](https://policies.google.com/privacy).

**Apple** (Sign in with Apple, StoreKit for subscriptions)
Apple handles authentication when you sign in with Apple and handles all payment processing for Cartly Pro. Apple's handling of that data is governed by [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).

**Google** (Sign in with Google, if you choose it)
If you sign in with Google, Google handles that authentication. See the [Google Privacy Policy](https://policies.google.com/privacy).

## 6. How long we keep your data

- **Account record, dietary preferences, scan history, cart, saved products, and local subscription-status row:** retained while your account is active, and permanently deleted within **30 days** of account deletion. The 30-day window exists to cover routine encrypted backups; in practice, tapping **Delete Account** in Settings wipes your data from the live database immediately.
- **Photos submitted for scanning:** not retained by Cartly at any point (not saved to our database, to Supabase Storage, or to any server log). Google's retention of the image is governed by its Gemini API terms linked above.
- **Subscription financial records:** held by Apple, not by us. When your Cartly account is deleted, our copy of your subscription-status row is deleted, but any active Apple subscription continues until you cancel it in your Apple ID Settings (it simply stops being associated with a Cartly account).

## 7. Your rights and choices

You can:
- **Delete your account** at any time from inside the app: **Settings → Delete Account**. This permanently removes your scan history, cart, dietary preferences, and account record.
- **Revoke camera or photo-library access** at any time in iOS **Settings → Privacy → Camera / Photos → Cartly**.
- **Cancel your Cartly Pro subscription** at any time in your iOS **Apple ID Account Settings → Subscriptions**.
- **Request a copy of your data** ("data portability") by emailing privacy@usecartly.com. We will send you your account, dietary preferences, scan history, cart, and subscription-status row in a machine-readable format within 30 days.
- **Correct inaccurate data** by emailing privacy@usecartly.com or editing in the app where applicable.
- **Object to or restrict processing** of your data in certain circumstances — email us at privacy@usecartly.com and we will respond.

## 8. European Economic Area, United Kingdom, and Switzerland (GDPR / UK GDPR)

If you are in the EEA, the United Kingdom, or Switzerland, the General Data Protection Regulation (or the UK GDPR) gives you specific rights.

**Data controller.** Tyler Piwowarski, operating Cartly, is the data controller for the personal data described in this Policy. You can reach the controller at privacy@usecartly.com.

**Legal bases we rely on.**
- **Performance of a contract** (GDPR Art. 6(1)(b)) — to provide the Service you asked for.
- **Consent** (Art. 6(1)(a)) — for the optional dietary alert personalization you configure.
- **Legitimate interests** (Art. 6(1)(f)) — to keep the Service secure and prevent abuse.

**Your rights.** You have the right to access, rectify, erase, restrict, or object to our processing, the right to data portability, and the right to withdraw consent. Email privacy@usecartly.com to exercise any of these.

**Right to lodge a complaint.** You also have the right to complain to your local data protection supervisory authority.

**International transfers.** Your data is stored and processed in the United States (Supabase / AWS) and transmitted to Google's Gemini API for analysis. Where required, we rely on Standard Contractual Clauses and our providers' own transfer mechanisms.

## 9. California residents (CCPA / CPRA)

If you are a California resident, the California Consumer Privacy Act, as amended by the CPRA, gives you specific rights.

**Categories of personal information we collect.** Identifiers (email, user ID); customer-account information (name, subscription status); commercial information (products you've scanned, saved, or added to cart); internet/other electronic network activity (interaction with the Service); and user content (photos you submit for scanning, processed in real time and not retained by Cartly).

**Categories of sources.** Directly from you; from Apple or Google at sign-in; and generated by your use of the Service.

**Purposes.** Only to provide and secure the Service, as described in Section 3.

**Third parties we share with.** Service providers only, as listed in Section 5. **We do not sell your personal information, and we do not share it for cross-context behavioral advertising.** We have not done so in the past 12 months.

**Your rights under the CCPA/CPRA.** You have the right to know what we collect, to delete your personal information, to correct inaccurate information, to opt out of sale or sharing (not applicable — we do neither), to limit the use of sensitive personal information (we do not collect sensitive personal information), and not to be discriminated against for exercising these rights.

**How to exercise your rights.** Email privacy@usecartly.com, or use **Settings → Delete Account** in the app. We will respond within 45 days. We verify requests by matching the email address on your account.

## 10. Children's privacy

Cartly is not directed at children under 13, and we do not knowingly collect personal information from children under 13. If you are a parent or guardian and believe your child has created an account, email privacy@usecartly.com and we will delete the account and any associated data.

Cartly is rated **4+** on the App Store because it contains no objectionable content, but the service itself is intended for general audiences 13 and older.

## 11. Apple Sign In and "Hide My Email"

If you sign in with Apple and choose **Hide My Email**, Apple gives us an anonymized relay email address (ending in `@privaterelay.appleid.com`) instead of your real email. Messages we send to that address are forwarded by Apple to your real inbox. We cannot see your real email address and cannot unmask it. Deleting your Cartly account works the same way whether you use a real or relay email.

If you later revoke Cartly's access to Sign in with Apple (iOS **Settings → Apple ID → Password & Security → Apps Using Apple ID → Cartly → Stop Using Apple ID**), we will delete your Cartly account on receipt of Apple's revocation notification.

## 12. Security

We protect your data with industry-standard measures:
- TLS 1.2+ for all network traffic between your device, our Edge Functions, and third-party APIs.
- Encryption at rest for all data stored in Supabase / AWS.
- JSON Web Token (JWT) authentication on every request.
- Row-Level Security policies that ensure each user's data is only readable and writable by that user.
- A single server-side Gemini API key that is never exposed to the client.

No system is perfectly secure. If we discover a breach affecting your personal information, we will notify you as required by applicable law.

## 13. Changes to this Policy

We may update this Policy from time to time. If we make a material change, we will update the Effective Date at the top and notify you in the app or by email. Your continued use of the Service after an update constitutes acceptance of the updated Policy.

A diff history of every change is publicly visible in the Git history of the repository that hosts this page.

## 14. Contact

For questions or requests about this Policy or your data, email:

**privacy@usecartly.com**

Tyler Piwowarski, operating Cartly
California, United States
