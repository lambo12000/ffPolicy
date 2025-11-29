# Directory Overview

This directory contains a set of policies for the Firefox web browser, defined in the `policies/policies.json` file. These policies can be used to customize and lock down various Firefox settings.

# Key Files

*   `policies/policies.json`: A JSON file containing the Firefox policies. This file is the core of the repository and defines all the custom settings.

# Usage

The `policies/policies.json` file can be used to configure Firefox in an enterprise or personal setting. To use these policies, you would typically place the `policies.json` file in a specific directory within the Firefox installation.

For more information on how to use Firefox policies, refer to the official Mozilla documentation:
*   [Firefox Policy Templates](https://mozilla.github.io/policy-templates/)
*   [Customizing Firefox using policies.json](https://support.mozilla.org/en-US/kb/customizing-firefox-using-policiesjson)

# Policy Management

This project is managed by an AI agent. When making changes to the policies, please adhere to the following guidelines:

*   **Never remove existing policies without explicit permission.** When asked to add new policies, always append them to the existing configuration.
*   **Always verify the policy names and values.** Refer to the official Firefox policy documentation to ensure correctness.
*   **Commit changes with descriptive messages.** This helps to maintain a clear history of the project.

## Recent Changes

*   Enabled auto-updates.
*   Added policies for HttpsOnlyMode, PostQuantumKeyAgreement, SSLVersionMin, DisableFormHistory, DisablePasswordReveal, NetworkPrediction, and SearchSuggestEnabled.
*   Disabled telemetry and AI features.
*   Enabled DNS-over-HTTPS using Cloudflare.
*   Added policies for tracking protection.
*   Removed the "Notifications" policy as it is only available via Group Policy on Windows.
*   Removed the "privacy.resistFingerprinting" preference due to stability reasons.