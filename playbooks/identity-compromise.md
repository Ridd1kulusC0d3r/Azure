# Playbook — Suspected Identity Compromise

## Trigger

Use when a hunt or detection indicates suspicious Microsoft Entra sign-in or privileged identity activity.

## 1. Establish identity context

Review:

- account type and privilege
- normal sign-in geography and applications
- recent authentication failures and successes
- recent MFA and authentication-method changes
- role assignments or PIM activity

## 2. Build a timeline

Correlate:

- SigninLogs
- AuditLogs
- AzureActivity
- Defender XDR identity / alert evidence where available

## 3. Scope impact

Determine whether the identity:

- accessed privileged resources
- changed directory roles
- created or modified application credentials
- performed unusual Azure control-plane operations
- appears in other security alerts

## 4. Test benign explanations

Check expected administrative work, automation, approved travel, VPN / proxy behavior and known service accounts.

## 5. Escalate

Escalate when activity is inconsistent with the account baseline, involves privileged actions, affects multiple resources, or correlates with other high-confidence security evidence.

## 6. Preserve evidence

Record query time ranges, relevant IDs, timestamps, entities and analyst conclusions before logs age out or response actions change state.

## 7. Feed back

Convert confirmed behaviors into:

- threat-intelligence notes
- new threat scenarios
- hunt improvements
- detection tuning
- coverage updates
