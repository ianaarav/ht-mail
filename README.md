# HyperTract Mail (HT Mail)

HT Mail is a personal, for-fun project where I experiment with running my own email and directory services. I built it to learn how self-hosted infrastructure works, and to explore the different pieces involved in operating my own mail and LDAP services.

> **Status:** Early development. Local email delivery and mail access are working. External access and general internet email delivery are not yet complete.

## What I'm exploring

- Running my own email and LDAP services on hardware I already own.
- Learning how Postfix, Dovecot, OpenLDAP and TLS certificates work together.
- Experimenting with my own certificate authority and trusted certificates.
- Understanding authentication, mail delivery, storage and server administration.
- Keeping the project free of cost by using existing hardware and avoiding paid hosting or subscriptions.
- Documenting the experiment and sharing what I learn.

## Current architecture

| Component | Purpose |
| --- | --- |
| Debian 13 | Server operating system |
| Postfix | SMTP mail transfer and submission |
| Dovecot | IMAP access, Maildir storage and LDAP-backed authentication |
| OpenLDAP | User directory and authentication |
| OpenSSL private CA | Internal server certificate chain |
| Radicale | Self-hosted CalDAV/CardDAV service under exploration |

## What works

- [x] Debian-based mail server installed and running.
- [x] LDAP-backed user authentication.
- [x] IMAP over TLS.
- [x] Authenticated SMTP submission over STARTTLS.
- [x] Local delivery to Maildir.
- [x] Internal server certificate chain validated in connection tests.

## Work in progress

- [ ] Reliable access from outside the home network using a genuinely free solution.
- [ ] Investigate ISP IPv6 and carrier-grade NAT limitations.
- [ ] Explore further service integrations.
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

The server runs on repurposed laptop hardware.

## Why?

Mostly curiosity and the fun of building something myself. I wanted to understand how email servers, LDAP, certificates and self-hosted infrastructure fit together.

## Contributing

Documentation feedback, testing ideas and discussions from the self-hosting community are welcome. Please open an issue before proposing major changes.

## License

No license has been selected yet. Until one is added, all rights are reserved by the copyright holder; do not assume the repository is licensed for reuse.
