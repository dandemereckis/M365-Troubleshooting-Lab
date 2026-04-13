# Microsoft 365 User Lifecycle + Troubleshooting Lab
![Problem File / Conflict](screenshots/13-conflicted-copy-or-stuck-file.png)
![OneDrive Fixed](screenshots/14-onedrive-fixed.png)

### Result
OneDrive returned to a healthy sync state.

---

## Troubleshooting Scenario 4 — Shared File Access Denied
I simulated a permissions problem on a shared file.

![Access Denied](screenshots/15-access-denied-shared-file.png)

### Diagnosis
Because the shared item was reachable but access was denied, the problem pointed to permissions rather than internet or service connectivity.

### Resolution
- Reviewed sharing settings
- Re-added the correct user
- Applied the proper permission level
- Retested access

![Permissions Fixed](screenshots/16-sharing-permissions-fixed.png)

### Result
The user regained the expected access to the shared file.

---

## Troubleshooting Scenario 5 — Desktop App Sign-In Failure
I simulated a situation where Microsoft 365 worked in the browser but failed in the desktop application.

![Web vs App Testing](screenshots/17-web-vs-app-testing.png)

### Diagnosis
Since web sign-in succeeded, the issue was isolated to the local Windows device, likely involving cached credentials or stale authentication tokens.

### Resolution
- Signed out of affected Office apps
- Closed all Office apps fully
- Opened Credential Manager
- Removed relevant Microsoft/Office stored credentials
- Signed back into the desktop application

![Credential Manager](screenshots/18-credential-manager.png)
![Final Working State](screenshots/19-final-working-state.png)

### Result
Desktop app sign-in worked again after clearing stored credentials.

---

## Key Takeaways
This lab reinforced several important IT support concepts:
- Web vs desktop testing is one of the fastest ways to isolate Microsoft 365 issues
- Licensing problems can directly affect access to Microsoft 365 services
- Teams desktop issues are often local cache problems
- OneDrive sync issues are often caused by one problematic file or a stuck sync engine
- “Access Denied” usually points to permissions rather than connectivity
- Cached credentials can prevent desktop applications from accepting valid account sign-ins

## Why This Project Matters
This project reflects real tasks commonly handled by help desk and junior IT support technicians in Microsoft 365 environments. It demonstrates both administrative skills and troubleshooting logic rather than just setup steps.

## Future Improvements
If I expanded this lab in the future, I would add:
- MFA troubleshooting
- Password reset workflow testing
- Shared mailbox troubleshooting
- Conditional access / sign-in policy testing
- Multi-user collaboration scenarios

## Author
Created as part of my hands-on IT support and help desk portfolio development.
