# LegacyVault

LegacyVault is a privacy-focused household asset register for Android. It keeps family, asset, and emergency-reference information in an encrypted local vault, without requiring a cloud account.

**Current Version:** v1.0

## Core capabilities

- **Family registry:** Add, edit, and remove family members. You can designate a primary member and manage their relationship status.
- **Asset registry:** Register, edit, and remove financial and physical assets, including banking, fixed deposits, brokerages, retirement funds, insurance, real estate, and liabilities.
- **Multi-currency support:** Track assets in different currencies (INR, USD, HKD, AUD, YEN, GBP, AED, EUR). Custom 3-character currency codes are also supported.
- **Global Portfolio Aggregation:** Set manual exchange rates in Settings to view your total household net worth in a single base currency (e.g., INR).
- **Currency Toggles:** Effortlessly switch between currencies on the dashboard and registry, or use the "Global View" toggle to see an aggregated summary.
- **Enhanced UI Safety:** Custom-themed delete confirmation dialogs and ergonomic edit button placement to prevent accidental data loss.
- **Privacy-First Validation:** Real-time audit of exchange rates when enabling Global View, with themed alerts for missing data.
- **Password Visibility:** Toggle visibility for sensitive fields like the vault PIN, App PIN, and transfer passphrases.
- **Optional App PIN Security:** Add an extra layer of privacy with a dedicated secondary PIN required after biometric or system unlock.
- **Themes:** Switch between dark and light themes from the app header.

## Security and authentication

- Vault contents are stored locally and encrypted with AES-256-GCM using the device-authentication flow.
- **Double-Lock (Optional):** Users can enable a secondary App PIN (4-6 digits) as a UI-level barrier. This PIN is stored inside the encrypted vault and is not recoverable if forgotten.
- On supported Android devices, the app uses the system biometric / PIN / password / pattern prompt. Device credentials are never read by the app.
- No cloud synchronisation is required for normal use.

## Backup and restore

- Export creates a password-protected `.vault` backup using a separate transfer passphrase.
- On Android, exports are stored in `Downloads/LegacyVault`.
- Import accepts a selected `.vault` file and restores the encrypted payload only after its transfer passphrase is verified.
- The transfer passphrase is separate from the vault PIN and is not included in the backup.

## Getting started

1. Open the app and unlock or create the local vault.
2. Add a primary family member.
3. Register assets, select the appropriate currency, and assign owners.
4. Optionally add nominee information and supporting notes.
5. Use **Settings** to create an encrypted backup before changing devices.
