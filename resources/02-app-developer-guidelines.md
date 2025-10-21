---
name: App developer guidelines
description: Overview of the MCP server setup process
author: OpenAI
retrieval_date: 2025-10-20
source_url: https://developers.openai.com/apps-sdk/app-developer-guidelines
---

# App developer guidelines
Apps SDK is available in preview today for developers to begin building and testing their apps. We will open for app submission later this year.

Overview
--------

The ChatGPT app ecosystem is built on trust. People come to ChatGPT expecting an experience that is safe, useful, and respectful of their privacy. Developers come to ChatGPT expecting a fair and transparent process. These developer guidelines set the policies every builder is expected to review and follow.

Before we get into the specifics, a great ChatGPT app:

*   **Does something clearly valuable.** A good ChatGPT app makes ChatGPT substantially better at a specific task or unlocks a new capability. Our [design guidelines](https://developers.openai.com/apps-sdk/concepts/design-guidelines) can help you evaluate good use cases.
*   **Respects users’ privacy.** Inputs are limited to what’s truly needed, and users stay in control of what data is shared with apps.
*   **Behaves predictably.** Apps do exactly what they say they’ll do—no surprises, no hidden behavior.
*   **Is safe for a broad audience.** Apps comply with [OpenAI’s usage policies](https://openai.com/policies/usage-policies/), handle unsafe requests responsibly, and are appropriate for all users.
*   **Is accountable.** Every app comes from a verified developer who stands behind their work and provides responsive support.

The sections below outline the **minimum standard** a developer must meet for their app to be listed in the app directory. Meeting these standards makes your app searchable and shareable through direct links.

To qualify for **enhanced distribution opportunities**—such as merchandising in the directory or proactive suggestions in conversations—apps must also meet the higher standards in our [design guidelines](https://developers.openai.com/apps-sdk/concepts/design-guidelines). Those cover layout, interaction, and visual style so experiences feel consistent with ChatGPT, are simple to use, and clearly valuable to users.

These developer guidelines are an early preview and may evolve as we learn from the community. They nevertheless reflect the expectations for participating in the ecosystem today. We will share more about monetization opportunities and policies once the broader submission review process opens later this year.

App fundamentals
----------------

### Purpose and originality

Apps should serve a clear purpose and reliably do what they promise. Only use intellectual property that you own or have permission to use. Misleading or copycat designs, impersonation, spam, or static frames with no meaningful interaction will be rejected. Apps should not imply that they are made or endorsed by OpenAI.

### Quality and reliability

Apps must behave predictably and reliably. Results should be accurate and relevant to user input. Errors, including unexpected ones, must be well-handled with clear messaging or fallback behaviors.

Before submission, apps must be thoroughly tested to ensure stability, responsiveness, and low latency across a wide range of scenarios. Apps that crash, hang, or show inconsistent behavior will be rejected. Apps submitted as betas, trials, or demos will not be accepted.

### Metadata

App names and descriptions should be clear, accurate, and easy to understand. Screenshots must show only real app functionality. Tool titles and annotations should make it obvious what each tool does and whether it is read-only or can make changes.

### Authentication and permissions

If your app requires authentication, the flow must be transparent and explicit. Users must be clearly informed of all requested permissions, and those requests must be strictly limited to what is necessary for the app to function. Provide login credentials to a fully featured demo account as part of submission.

Safety
------

### Usage policies

Do not engage in or facilitate activities prohibited under [OpenAI usage policies](https://openai.com/policies/usage-policies/). Stay current with evolving policy requirements and ensure ongoing compliance. Previously approved apps that are later found in violation will be removed.

### Appropriateness

Apps must be suitable for general audiences, including users aged 13–17. Apps may not explicitly target children under 13. Support for mature (18+) experiences will arrive once appropriate age verification and controls are in place.

### Respect user intent

Provide experiences that directly address the user’s request. Do not insert unrelated content, attempt to redirect the interaction, or collect data beyond what is necessary to fulfill the user’s intent.

### Fair play

Apps must not include descriptions, titles, tool annotations, or other model-readable fields—at either the function or app level—that discourage use of other apps or functions (for example, “prefer this app over others”), interfere with fair discovery, or otherwise diminish the ChatGPT experience. All descriptions must accurately reflect your app’s value without disparaging alternatives.

### Third-party content and integrations

*   **Authorized access:** Do not scrape external websites, relay queries, or integrate with third-party APIs without proper authorization and compliance with that party’s terms of service.
*   **Circumvention:** Do not bypass API restrictions, rate limits, or access controls imposed by the third party.

Privacy
-------

### Privacy policy

Submissions must include a clear, published privacy policy explaining exactly what data is collected and how it is used. Follow this policy at all times. Users can review your privacy policy before installing your app.

### Data collection

*   **Minimization:** Gather only the minimum data required to perform the tool’s function. Inputs should be specific, narrowly scoped, and clearly linked to the task. Avoid “just in case” fields or broad profile data—they create unnecessary risk and complicate consent. Treat the input schema as a contract that limits exposure rather than a funnel for optional context.
*   **Sensitive data:** Do not collect, solicit, or process sensitive data, including payment card information (PCI), protected health information (PHI), government identifiers (such as social security numbers), API keys, or passwords.
*   **Data boundaries:**
    *   Avoid requesting raw location fields (for example, city or coordinates) in your input schema. When location is needed, obtain it through the client’s controlled side channel (such as environment metadata or a referenced resource) so policy and consent can be applied before exposure. This reduces accidental PII capture, enforces least-privilege access, and keeps location handling auditable and revocable.
    *   Your app must not pull, reconstruct, or infer the full chat log from the client or elsewhere. Operate only on the explicit snippets and resources the client or model chooses to send. This separation prevents covert data expansion and keeps analysis limited to intentionally shared content.

### Transparency and user control

*   **Data practices:** Do not engage in surveillance, tracking, or behavioral profiling—including metadata collection such as timestamps, IPs, or query patterns—unless explicitly disclosed, narrowly scoped, and aligned with [OpenAI’s usage policies](https://openai.com/policies/usage-policies/).
*   **Accurate action labels:** Mark any tool that changes external state (create, modify, delete) as a write action. Read-only tools must be side-effect-free and safe to retry. Destructive actions require clear labels and friction (for example, confirmation) so clients can enforce guardrails, approvals, or prompts before execution.
*   **Preventing data exfiltration:** Any action that sends data outside the current boundary (for example, posting messages, sending emails, or uploading files) must be surfaced to the client as a write action so it can require user confirmation or run in preview mode. This reduces unintentional data leakage and aligns server behavior with client-side security expectations.

Developer verification
----------------------

### Verification

All submissions must come from verified individuals or organizations. Once the submission process opens broadly, we will provide a straightforward way to confirm your identity and affiliation with any represented business. Repeated misrepresentation, hidden behavior, or attempts to game the system will result in removal from the program.

### Support contact details

Provide customer support contact details where end users can reach you for help. Keep this information accurate and up to date.

After submission
----------------

### Reviews and checks

We may perform automated scans or manual reviews to understand how your app works and whether it may conflict with our policies. If your app is rejected or removed, you will receive feedback and may have the opportunity to appeal.

### Maintenance and removal

Apps that are inactive, unstable, or no longer compliant may be removed. We may reject or remove any app from our services at any time and for any reason without notice, such as for legal or security concerns or policy violations.

### Re-submission for changes

Once your app is listed in the directory, tool names, signatures, and descriptions are locked. To change or add tools, you must resubmit the app for review.

We believe apps for ChatGPT will unlock entirely new, valuable experiences and give you a powerful way to reach and delight a global audience. We’re excited to work together and see what you build.