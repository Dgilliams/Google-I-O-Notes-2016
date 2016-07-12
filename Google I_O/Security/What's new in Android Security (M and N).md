# What's new in Android Security (M and N)
Thursday May 19th, 2016. 9am
# Speaker: Adrian Ludwig
- Best speaker so far, this guy was awesome

## The new
- File based Encryption
- Media Server Hardening
- Automatic Updates

# Presently
- 1 billion device scans per day looking at 8 billion apps checked per day

## Key features Today
- Permissions
- Keystore
- Authentication
- Secure networking
- storage encryption
- verified boot
- sandboxing

## Runtime Permissions new with Marshmallow
- Permissions requested at runtime
- users can control individual permissions
- ...
- simplified installation process
- easier application upgrades
- more understandable for users

// Code for requesting permission

### UX Considerations
- providing context can improve success rates
- google apps following design guidelines
  - 85% say "yes"
  - 15.8% no which is 40% lower than average
  - 3% never ask again which is 50% lower than average

## Keystore
- Hardware backend key storage
- backs disk encryption keys and user authentication verification
- apps can securely create and store RSA, ECDSA, AES and HMAC keys
- can be configured to only allow usage of keys within a given time window of user authentication (Marshmallow +)
- Required as of N

### New feature
- Key attestation (N+ new hardware)
- remotely verify that the attested key is in a secure ...

// Insert keystore code sample

- Use keystore with built in auth for cryptographic keys (L+)
- attestation can be used to check hardware CTS compatibility

## Authentication: Easier
- with fingerprint, secure lock screen usage has increased to 90%+ on nexus phones
- smart lock's on-body detection reduces lock screen prompts by 50%
- Authentication tied to app secrets (e.g. keystore)
- Credential verification in hardware (e.g. Trustzone)

### APIs in <Arshmallow
- Fingerprint APIs to prompt authentication
- Keystore policies based on how recently the user unlocked

// Insert Fingerprint Code Example

### Best Practices
 - Use Android Keystore auth-bound keys to check if the user recently authenticated
 - if the device has a fingerprint scanner, use the fingerprint API to test for user presence, otherwise use createConfirmDeviceCredentialIntent()

## Network APIS: Secure Traffic
 - Protect your apps by always using HTTPS
 - android:usesCleartextTraffic (Marshmallow)

 Block insecure traffic in your app
 Update Manifest to block insecure traffic (Marshmallow)

 <manifest ..>
 insert code

### Network APIS: managing trust
- Testing and deploting SSL/TTS

### Block insecure traffic in your app
- domain level rules
<network-security-config>

### debug only CAs
- Connet to youre developer infastructure without any code
- eliminate debugging related ode in your release build
-avoid writing custom code that removes security for debug builds and shipping it
  - we do see apps ship with that code mistakenly left in!

insert Debug-only CAs code
<debug-overrides>


### Restricting trust
- limit the certificates you want to trust

insert specifiying trusted CAs

### Pinning certificates
- to identify a specific certificate that you expect to associate with a specific service

insert codeeee
- he says use caution and instead use the built in if possible

### for everyione
- use android:usesCleartextTraffic and Network Security Coding to avoid insecure traffic
- user installed CAs no longer trusted by default
- Debugging SSL is simple, declarative syntax
- The CA store will be the same on all Android devices

### best practices
- Consider further restricting the CAs you trust
- consider certificate pinning

## Storage Encryption
- encryption required for all capable devices (Marshmallow+)
- Backend by hardware (Required for N+)
 - if root of trust changed you cant decrypt the data
- better UX with Direct Boot (N+)

### For users
- Boot directly to the lock screen
- calls SMS and talkback alarms work after device reboot before unlock
- per user disk encryption

### For developers
- Two types of storage
  - device protected and credential protected
- by default, all application is Credential Encrypted
- directBootAware run before first user unlock and can use device encrypted storage

### Direct Boot Sample
- Mark individual components as Direct Boot aware

### Direct Boot best practices
- most appropriate for apps that depend on time sensitive alerts
- limit data you store in Device protected storage
  - avoid strong lived credentials in DP storage
  - create limited purpose tokens (e.g. receive mail not sent it)
  - Encrypt sensitive data you receive to be decrypted only after unlock

## Verified Boot
- required on M+ for capable devices
- Strictly enforcing mode on N+
- Error correction (N+)

### Checking device health
- Call the SafteyNet API to confirm CTS compatibility and check for evidence of tampering
- check the patch level string (android.os.Build.VERSION.SECURITY_PATCH)

### Security Updates
- Security patch level introduced in M, available K+
- a date to see if the device is up to date

### SafteyNet sample
- perform the attestation via Play services
// Insert safety net example

## Sandboxing
- SELinux
- Seccomp (required in N+)
- mediaserver hardening
- increase randomness for ASLR
- Library load order radomization
0 Android integrity monitoring

### Seccomp
- attack surgace reduction tool to protect the system against compromises in your app
----- shitttt

insert example
- look online for mini jail for more info

### Developer effects
- Cross Sandbox/ proc/PID access removed
...

### DEvice admin APIS
- Limitation introduced to reduce abuse
  - No longer able to change an existing passwork

### SYSTEM_ALERT_WINDOW
-

Android.com/security
Source.android.com/security
