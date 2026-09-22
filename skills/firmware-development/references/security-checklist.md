# Embedded Firmware Security Checklist

## Hardware
- [ ] Secure Boot enabled with signature verification
- [ ] HSM/TEE/PUF for key storage and crypto
- [ ] Debug interfaces disabled in production
- [ ] Tamper detection and response
- [ ] Memory protection (MPU, NX bits)

## Firmware Code
- [ ] MISRA/CERT compliant
- [ ] Input validation and bounds checking
- [ ] Secure coding (no unsafe funcs, stack guards)
- [ ] Compartmentalization (secure/non-secure worlds)
- [ ] Crypto library (mbedTLS, wolfSSL, etc.)

## Updates & Lifecycle
- [ ] Signed firmware images
- [ ] Encrypted OTA with version/rollback protection
- [ ] SBOM maintained
- [ ] Vulnerability monitoring process

## Testing
- [ ] Static analysis, fuzzing, pen testing
- [ ] Side-channel resistance (if applicable)
- [ ] Hardware validation

Regularly review OWASP, NIST, and vendor docs.

## Onn 4K Pro application notes (Grok, 2026-09-22)

This checklist is written for *builders* hardening their own firmware. On the Onn Pro, Google/Walmart already shipped secure boot + locked BL. Analyst view:

- Secure Boot / AVB: present; blocks custom images. Treat as constraint, not a todo.
- Debug: ADB (user-enabled) and UART (921600, labeled) exist. Production intent is locked; we have the leftovers.
- OTA: signed Google OTAs. Capture via logcat; do not sideload unsigned images.
- Do not disable security features on a device you do not own the signing keys for.
- Separate this from the 2026 Onn stick (wayne/RTD1325) unlock window.
