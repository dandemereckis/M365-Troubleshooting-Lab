# Microsoft 365 User Lifecycle + Troubleshooting Lab

## Overview
This lab simulates the work of an IT support technician managing and troubleshooting a Microsoft 365 user account in a cloud-based environment. The project demonstrates core help desk tasks including user creation, license assignment, application validation, file sharing, and troubleshooting common Microsoft 365 problems.

## Objectives
- Create and manage a Microsoft 365 user account
- Assign and verify a Microsoft 365 license
- Validate access to Outlook, Teams, and OneDrive
- Configure and test file sharing
- Troubleshoot common Microsoft 365 issues
- Document findings and resolutions clearly

## Tools and Platforms Used
- Microsoft 365 Admin Center
- Outlook
- Microsoft Teams
- OneDrive
- Microsoft 365 web portal
- Windows Credential Manager
- Windows Task Manager

## Skills Demonstrated
- User administration
- License management
- Microsoft 365 app troubleshooting
- OneDrive sync troubleshooting
- Permissions troubleshooting
- Web vs desktop app isolation
- Credential/cache cleanup
- Structured documentation

## Lab Environment
- Microsoft 365 test tenant
- Admin account for user and license management
- Test user account for end-user validation
- Windows lab machine / VM for desktop app testing

## Scenario Summary
In this lab, I simulated the lifecycle of a Microsoft 365 user from account creation through application access validation. After confirming normal access, I intentionally created several common support issues and worked through the troubleshooting process to restore functionality.

---

## Phase 1 — User Creation
I created a new Microsoft 365 test user in the Admin Center and confirmed the account appeared under Active Users.

![User Created](screenshots/01-admin-center-user-created.png)

### Actions Performed
- Opened Microsoft 365 Admin Center
- Navigated to Active Users
- Created a new test user
- Recorded account details for testing

### Outcome
The user account was successfully created and ready for license assignment.

---

## Phase 2 — License Assignment
I assigned a Microsoft 365 license to the user so the account could access Microsoft 365 services such as Outlook, Teams, and OneDrive.

![License Assigned](screenshots/02-license-assigned.png)

### Actions Performed
- Opened the user account in Admin Center
- Assigned an available Microsoft 365 license
- Verified the license saved successfully

### Outcome
The test user became eligible to use assigned Microsoft 365 applications and services.

---

## Phase 3 — Application Validation
I tested the newly created user account by signing into core Microsoft 365 services.

### Outlook Validation
![Outlook Working](screenshots/03-outlook-working.png)

### Teams Validation
![Teams Working](screenshots/04-teams-working.png)

### OneDrive Validation
![OneDrive Working](screenshots/05-onedrive-working.png)

### Actions Performed
- Signed into Outlook
- Signed into Teams
- Signed into OneDrive
- Confirmed the account could access core services

### Outcome
The user account was working normally before troubleshooting scenarios were introduced.

---

## Phase 4 — Shared File Configuration
I created a shared file scenario to simulate common collaboration and permissions issues.

![Shared File Created](screenshots/06-shared-file-created.png)

### Actions Performed
- Created a test folder in OneDrive
- Created a test file inside the folder
- Shared the item with another user
- Assigned a specific permission level

### Outcome
The shared file environment was ready for access testing and permissions troubleshooting.

---

## Troubleshooting Scenario 1 — License Removed
To simulate a common support issue, I removed the user’s assigned license and tested application behavior.

![License Removed Error](screenshots/07-license-removed-error.png)

### Diagnosis
The user could no longer properly access Microsoft 365 services after the license was removed. This demonstrated that licensing directly affects service availability.

### Resolution
I reassigned the correct Microsoft 365 license and allowed time for changes to propagate.

![License Restored](screenshots/08-license-restored.png)

### Result
Application access was restored after the license was re-applied.

---

## Troubleshooting Scenario 2 — Teams Desktop App Failure
I tested a common issue where the desktop application fails while the web version still works.

![Teams App Failure](screenshots/09-teams-app-failure.png)
![Web vs App Testing](screenshots/17-web-vs-app-testing.png)

### Diagnosis
Because Teams worked in the browser but not in the desktop application, the issue was isolated to the local app rather than the Microsoft 365 account, license, or cloud service.

### Resolution
- Fully closed Teams
- Ended remaining Teams processes in Task Manager
- Cleared the Teams local cache
- Reopened the application

![Teams Cache Path](screenshots/10-teams-cache-path.png)
![Teams Working Again](screenshots/11-teams-working-again.png)

### Result
Teams launched successfully after cache cleanup.

---

## Troubleshooting Scenario 3 — OneDrive Sync Issue
I worked through a common sync problem in OneDrive.

![OneDrive Sync Problem](screenshots/12-onedrive-sync-problem.png)

### Diagnosis
The issue appeared as a sync delay / sync pending condition. I started by restarting OneDrive to reset the sync engine, then reviewed whether a single problematic file was blocking synchronization.

### Resolution
- Restarted OneDrive
- Checked for a stuck file, conflicted copy, invalid filename, or file path issue
- Corrected the issue and verified sync resumed

![Problem File / Conflict](screenshots/13-conflicted-copy-or-stuck-file.png)
![OneDrive Fixed](screenshots/14-onedrive-fixed.png)

### Result
OneDrive returned to a healthy sync state.

---

## Troubleshooting Scenario 4 — Shared File Access Denied
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
