# HyperTract Mail (HT Mail)


HT Mail is a personal project exploring whether a self-hosted mail server can bring email to the native BlackBerry Hub experience without a paid email provider or cloud-hosted mailbox.

> **Status:** Early development. Local-network email works with a BlackBerry 10 device. Internet-facing access and external email delivery are not yet complete.

## Project goals

- Run the infrastructure on hardware I already own.
- Use the native BlackBerry 10 Hub as the primary mail client.
- Manage account authentication with LDAP.
- Encrypt mail access and submission connections.
- Keep the project strictly ₹0, without paid hosting or subscriptions.
- Share documentation for other BlackBerry and self-hosting enthusiasts.

## Current architecture

| Component | Purpose |
| --- | --- |
| Debian 13 | Server operating system |
| Postfix | SMTP mail transfer and submission |
| Dovecot | IMAP access, Maildir storage and LDAP-backed authentication |
| OpenLDAP | User directory and authentication |
| OpenSSL private CA | Internal server certificate chain |
| Radicale | Self-hosted CalDAV/CardDAV service under exploration |
| BlackBerry 10 Hub | Primary mail client |

## What works

- [x] Debian-based mail server installed and running.
- [x] LDAP-backed user authentication.
- [x] IMAP over TLS.
- [x] Authenticated SMTP submission over STARTTLS.
- [x] Local delivery to Maildir.
- [x] BlackBerry 10 Hub connected over the home Wi-Fi network.
- [x] Internal server certificate chain validated in connection tests.

## Work in progress

- [ ] Reliable access from outside the home network using a genuinely free solution.
- [ ] Investigate ISP IPv6 and carrier-grade NAT limitations.
- [ ] Test contacts and calendar integration with BlackBerry 10.
- [ ] Improve installation and maintenance documentation.
- [ ] Add reviewed, sanitized example configurations and troubleshooting guides.

## Current limitations

HT Mail is currently a **local-network experiment**, not a production public email service. External connectivity, public DNS, internet-wide deliverability, spam protection, backups, monitoring and operational hardening still need work.

The project uses `ht.home.arpa` for internal infrastructure and `ht.mail` for experimental mailbox addresses. These names should not be assumed to be publicly resolvable or suitable for general internet email delivery.

## Security

Security and privacy are core goals, but this project has not undergone an independent security audit. Do not use it for sensitive or business-critical communication.

**Never commit:**
- Private keys, CA keys, or recovery backups.
- Passwords, password hashes, LDAP bind credentials, tokens or session secrets.
- Real mailboxes, message contents, address books or personal data.
- Unredacted logs, private network inventories or machine-specific configuration.

Only publish reviewed, sanitized examples. See [SECURITY.md](SECURITY.md) for reporting guidance.

## Hardware

The current server runs on repurposed laptop hardware. The client target is a BlackBerry Z10 running BlackBerry 10 OS 10.3.3 (build 3216).

## Why?

BlackBerry 10 has a distinctive native communication experience. This project explores preserving that experience with infrastructure I can run and understand myself.

## Contributing

Documentation feedback, testing ideas and discussions from self-hosting and BlackBerry enthusiasts are welcome. Please open an issue before proposing major changes.

## License

No license has been selected yet. Until one is added, all rights are reserved by the copyright holder; do not assume the repository is licensed for reuse.
