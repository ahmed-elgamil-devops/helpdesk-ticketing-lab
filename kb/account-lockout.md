# KB: User account keeps locking out

**Symptom:** the user is locked out again shortly after a password reset.

**Cause:** a device or service still uses the old password (phone mail app, saved
Windows credentials, a disconnected RDP session, a mapped drive or a scheduled task).

**Steps**
1. Verify the user's identity.
2. On the domain controller, run `04-Find-LockedUsers.ps1` or check Security event 4740 to find the source computer.
3. On that device, remove or update the saved password (Credential Manager, phone mail settings, RDP sessions).
4. Unlock the account and reset the password if needed (`03-Reset-UserPassword.ps1`).
5. Ask the user to update the password on all their devices.

**Escalate** to L2 if the source is a server or a service account.
