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
