# Omnis Privacy Policy

**Effective date:** October 6, 2026
**Last updated:** October 6, 2026

This policy explains how **Omnis**, a macOS app published by **David Akhmedbayev** ("we", "us"), handles your information. It covers the Omnis app for macOS and nothing else.

> ### At a glance
>
> - **On-device by default.** Out of the box, Omnis records, transcribes, summarizes, searches, and answers questions entirely on your Mac.
> - **We don't have your data.** There is no Omnis server, no account, and no cloud sync. We never receive your recordings, transcripts, screen content, or chats.
> - **Cloud AI is your choice.** Your content leaves your Mac only if *you* turn on Apple Private Cloud Compute. When you do, it goes from your Mac to Apple, not through us.
> - **No tracking, no ads, no selling.** We don't track you across apps or websites, show ads, or sell or share your personal information.
> - **You're in control.** Delete a session and its data is gone. Delete the app and its container and everything is gone.

---

## 1. What Omnis does

Omnis is an AI assistant for meetings and your screen. It lives in a floating panel above the Dock and lets you:

- Record **sessions** (meetings, calls, videos) from your microphone and/or your Mac's system audio, with a live transcript.
- Get AI-generated titles, summaries, and topic sections when a session ends, and edit summaries by chatting.
- Get suggested replies during a live call ("auto answer").
- Ask questions about what's on your screen.
- Ask questions across your past sessions and chats.

## 2. Information Omnis processes

Everything below is created and stored **on your Mac**, inside Omnis's sandboxed app container (using Apple's SwiftData and the app container), unless you turn on Apple Private Cloud Compute (Section 4).

| Data | What it is | Where it lives |
|---|---|---|
| **Audio recordings** | Your microphone and/or system/call audio, saved as AAC files. Recordings can include the voices of other people on a call. | App container on your Mac |
| **Transcripts** | Text produced on-device by Apple's Speech framework. The first time you transcribe, macOS may download a speech model from Apple. | App container on your Mac |
| **Screen content** | When you ask a question that needs it, Omnis captures the **frontmost window only** (never Omnis's own panel), extracts text with on-device OCR, and reads any QR codes. The image is discarded as soon as the text has been extracted. | Processed on your Mac; only the extracted text is kept, with your chat |
| **Questions, chats, AI answers, and summaries** | What you ask, and what Omnis answers or writes. | App container on your Mac |
| **Session details** | Titles, dates, and durations. | App container on your Mac |
| **Search index** | Text embeddings created on-device with Apple's NaturalLanguage framework so you can search past sessions and chats. | App container on your Mac |
| **Settings** | Your preferences. | macOS UserDefaults on your Mac |
| **Downloaded AI models** | The on-device language model you choose. | App container on your Mac |

### What we do **not** collect

Because Omnis has no server and no account system, **we (the developer) do not receive or store** any of the following:

- Your recordings, transcripts, screen content, chats, summaries, or search index
- Your name, email address, or any account details (there are no accounts)
- Your location, contacts, or device identifiers
- Usage analytics, advertising identifiers, or tracking data

Omnis contains no analytics, advertising, or crash-reporting SDKs.

**Crash reports via Apple.** If you have chosen in your Mac's settings to share analytics with app developers, or you are a TestFlight tester who submits feedback, Apple may give us crash reports, basic diagnostic information, and any feedback (including screenshots) you choose to submit. This is handled by Apple under [Apple's Privacy Policy](https://www.apple.com/legal/privacy/), and we use it only to fix bugs. You can turn this sharing off in **System Settings › Privacy & Security › Analytics & Improvements**. TestFlight also shares testers' names and email addresses with us so we can manage the beta.

## 3. How your information is used

Omnis uses the information above only to provide the features you use:

- **Recordings** are transcribed and can be played back.
- **Transcripts** power live notes, highlights, auto answer, summaries, titles, and topic sections.
- **Screen content** is used to answer the question you asked about your screen.
- **Chats, summaries, and the search index** let you ask questions across past sessions.
- **Settings** make the app work the way you configured it.

Omnis doesn't use your information for advertising, profiling, or anything else. We don't use your content to train AI models, and we couldn't, because we never receive it.

## 4. On-device AI and optional cloud processing

### Default: on your Mac

By default, all AI processing happens on your Mac:

- **Bonsai language models** (open-weight models by Prism ML) run locally using Apple's MLX framework.
- **Apple's on-device Foundation Model** handles live notes, highlights, auto answer, and describing screen content.
- **Transcription, OCR, QR reading, and search embeddings** use Apple's on-device frameworks.

In this mode your recordings, transcripts, screen content, and chats do not leave your Mac. The only network connections are model downloads, described below.

### Optional: Apple Private Cloud Compute

If you choose it in Omnis's settings, some AI requests may be processed by Apple's **Private Cloud Compute** instead of on your Mac. If Private Cloud Compute isn't available, Omnis falls back to on-device processing. Requests sent to Private Cloud Compute are handled by Apple under Apple's terms. We do not receive them.

- Apple Privacy Policy: <https://www.apple.com/legal/privacy/>
- About Private Cloud Compute: <https://security.apple.com/blog/private-cloud-compute/>

### Network connections Omnis makes

Omnis connects only to:

| Service | When | What it can see |
|---|---|---|
| **Hugging Face** | When you download an on-device model | Standard request information such as your IP address and the model requested. None of your content is sent. [Hugging Face Privacy Policy](https://huggingface.co/privacy) |
| **Apple** | Speech-model downloads managed by macOS, and Private Cloud Compute if you turn it on | Handled under [Apple's Privacy Policy](https://www.apple.com/legal/privacy/) |

Omnis makes no other network connections.

## 5. Permissions

macOS asks for your permission before Omnis can use these features. Both are optional. If you decline, Omnis still works with fewer features.

- **Microphone.** Used to transcribe your side of a conversation. You can pause or turn off the microphone at any time during a session.
- **Screen & System Audio Recording.** Used to capture call or system audio during a session, and to capture the frontmost window **only when you ask a screen-related question**.

You can change either permission at any time in **System Settings › Privacy & Security**.

## 6. Recording other people: your responsibility

Omnis can record and transcribe other people on a call, and auto answer can suggest replies based on what they say. **You are responsible for following the laws that apply to you, including getting any consent required before recording a conversation.**

Recording laws vary. Some places allow recording when one participant (you) consents. Others, including several U.S. states and many countries, require **every** participant to consent. Workplace rules and data-protection laws such as the GDPR may also apply, especially if you record for work. When in doubt, tell everyone you're recording and get their agreement. This section is general information, not legal advice.

## 7. Storage, security, and retention

### How your data is protected

- **App Sandbox.** Omnis runs in Apple's App Sandbox, which limits what the app can access on your Mac. Its data is stored in its own container.
- **Hardened Runtime.** Omnis is built with Apple's Hardened Runtime, which helps protect it from code injection and tampering.

Your data's security also depends on your Mac. We recommend a strong login password and FileVault disk encryption. No system is perfectly secure, and we can't guarantee the security of data on your device or with Apple.

### How long data is kept

- **On your Mac:** until you delete it. Deleting a session deletes its audio, transcript, summary, and search-index entries. Screen images are never stored. Only the text extracted from them is kept, with your chat.
- **Downloaded models:** until you delete the app.
- **Everything:** uninstalling Omnis and removing its container (`~/Library/Containers/com.david.Omnis`) deletes all Omnis data.
- **With Private Cloud Compute:** governed by Apple's policies.
- **Feedback emails you send us:** see Section 8.

Because we never receive your local data, **we cannot access, recover, or delete it for you.** If you delete it, it's gone.

## 8. Feedback emails

Omnis has a feedback button that opens a **pre-filled email draft** in your Mail app. The draft contains the question you asked and the AI's answer. **Nothing is sent unless you choose to send it**, and you can edit or remove anything first.

If you send it, we receive the email at david.akhmedbayev@icloud.com, including your email address, your name (if your email shows it), and whatever the message contains. Please check the draft before sending, since AI answers may include details from your transcripts or screen.

We use feedback emails only to reply to you and improve Omnis. We keep them until your issue is resolved, plus 90 days, then delete them. You can ask us to delete them sooner. Our email is hosted by Apple iCloud Mail, which stores it on our behalf.

**Legal basis (EU/UK):** our legitimate interest in answering your message and improving the app. You can object at any time.

## 9. Your rights

Depending on where you live, including under the GDPR, UK GDPR, and the California Consumer Privacy Act (as amended by the CPRA), you may have rights to **access, correct, delete, or port** your personal information, to **object to or restrict** its processing, and to **withdraw consent**.

### Exercising your rights on your Mac

Since your Omnis data lives only on your Mac, you control it directly:

- **Access and portability:** view your sessions, transcripts, summaries, and chats in Omnis. Use the Share button on a session or chat to export its text. Audio files are standard AAC files in the app's container.
- **Correction:** edit summaries and titles in the app.
- **Deletion:** delete individual sessions, or uninstall the app and remove its container.
- **Objection / withdrawing consent:** turn off microphone or screen permissions, or turn off Private Cloud Compute.

For data held by Apple or Hugging Face, contact that company using the links in Section 4.

### Contacting us

For anything we hold, such as feedback emails or TestFlight details, or for questions about your rights, email **david.akhmedbayev@icloud.com**. We'll respond within the time the law requires (generally one month under the GDPR and UK GDPR, and 45 days under the CCPA). We may need to verify your identity first. California residents may use an authorized agent. We will never discriminate against you for exercising your rights.

**Complaints:** if you're in the EU or UK, you can complain to your local data-protection authority (in the UK, the Information Commissioner's Office, <https://ico.org.uk>). We'd appreciate the chance to help first.

## 10. Children

Omnis is not directed at children under 13, or under 16 in the European Economic Area and UK, and we do not knowingly collect personal information from them. Since we don't receive app data at all, the only way we could get a child's information is through a feedback email. If you believe a child has sent us information, contact us and we'll delete it.

## 11. International users and data transfers

Omnis itself doesn't transfer your data anywhere. Its default processing happens on your Mac, wherever you are.

Data crosses borders only if you:

- **Use Apple Private Cloud Compute,** under Apple's policies.
- **Send us a feedback email.** It is stored in Apple iCloud Mail, which may process data in the United States and other countries.

## 12. We do not sell or share your personal information

We **do not sell** your personal information, and we **do not share** it for cross-context behavioral advertising, as those terms are defined under the CCPA/CPRA. We have not done so in the past 12 months. We do not use or disclose sensitive personal information for any purpose that would give you a right to limit it.

Omnis does **not track** you as defined by Apple's App Tracking Transparency framework. We don't link data from Omnis with data from other companies' apps, websites, or offline properties for targeted advertising or advertising measurement, and we don't share data with data brokers. Omnis contains no advertising.

## 13. Changes to this policy

If we change this policy, we'll post the new version at <https://davidakh.github.io/Omnis-Privacy/> and update the "Last updated" date. If a change materially affects how your data is handled, such as adding a new third-party service, we'll also tell you in the app or in the release notes before it takes effect.

## 14. Contact us

**David Akhmedbayev**
Privacy requests and app feedback: david.akhmedbayev@icloud.com
