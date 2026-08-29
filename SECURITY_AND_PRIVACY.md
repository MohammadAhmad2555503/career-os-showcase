# Security and Privacy: Career OS

## Privacy Model

Career OS is local-first. It does not require cloud upload, telemetry, paid model calls, or silent external provider use.

## Key Protections

- Localhost API binding by default.
- Trusted-host, origin, CORS, and local session-token controls around mutation endpoints.
- Local SQLite data with backups/exports excluded from release packages.
- Secret scanning during project import and release packaging.
- Static-only project analysis; imported code is not executed.
- ZIP traversal, symlink/root escape, oversized content, and binary-file controls.
- Prompt-injection filtering for untrusted job and project text.
- Sensitive application answers are never inferred.
- Browser automation blocks private-network targets, CAPTCHA, password fields, unknown required fields, unsupported fields, and failed Truth Audits.

## Public Showcase Choice

This showcase repository intentionally contains documentation only. It presents the engineering story without exposing local user data, generated application material, backups, or private career records.
