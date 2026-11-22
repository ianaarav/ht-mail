# Security Policy

## Project status

HT Mail is an experimental, self-hosted project. It is not production-hardened and has not received an independent security audit. Do not rely on it for sensitive or business-critical communication.

## Reporting a vulnerability

Please do not publish secrets or exploit details in a public issue. For a suspected vulnerability, contact the repository owner privately through GitHub's available private contact options.

Include:
- A concise description of the affected component.
- The potential impact.
- Reproduction steps that do not expose real user data or credentials.

## Never publish

Do not commit or attach:
- Private keys, CA private keys, certificate backups or recovery material.
- Passwords, password hashes, LDAP bind credentials, API tokens or session secrets.
- Mailbox contents, personal data, address books or real user records.
- Unredacted logs, private IP inventories or machine-specific configuration.

Before publishing configuration examples, replace credentials, hostnames, addresses and identifiers with clearly marked placeholders, and review the complete diff.

## Responsible use

Only test systems and accounts you own or have explicit permission to assess. Security improvements are welcome, but please coordinate disclosure privately first.
