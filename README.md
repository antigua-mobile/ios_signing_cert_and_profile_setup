# iOS signing certificate and provisioning profile setup
GitHub action for setting up the iOS signing certificate and the provisioning profile for manual code signing.

## Involved steps
1. Installs the signing certificate into the keychain
2. Copies the provisioning profile to the expected location.

## Usage
Add the following step to your GitHub Actions workflow:

```yaml
- name: Setup iOS signing certificate and provisioning profile
  uses: antigua-mobile/ios_signing_certificate_and_profile_setup@v1.0
  with:
    ios_signing_certificate_p12_base64:    # Base64-encoded signing certificate file
    ios_signing_certificate_p12_password:  # Password for the signing certificate
    ios_provisioning_profile_base64:       # Base64-encoded provisioning profile
```