Bug Report

---

Bug ID
BUG-001

---

Title
System triggers email verification for unregistered users without prior account validation

---

Module
Authentication / Email Verification

---

Severity
High

---

Priority
High

---

Environment
Web Application / Mobile Web  
Browser: Chrome (latest version)  
OS: Windows / Android (any applicable test device)

---

Preconditions
- User does not have an existing account in the system  
- User is on the login or email verification screen  
- Network connection is stable  

---

Steps to Reproduce
1. Navigate to the login or email verification page  
2. Enter an unregistered or invalid email address in the email input field  
3. Click on **Continue / Submit**  
4. Observe system behavior  

---

Expected Result
- System should validate whether the email exists in the database before proceeding  
- If the email is not registered, an appropriate error message should be displayed, such as:
  - “Account not found”  
  - “Invalid email address”  
- User should not be allowed to proceed to the email verification step  
- No verification email should be triggered  

---

Actual Result
- System accepts the unregistered email input  
- User is redirected to the email verification flow  
- A verification code is sent to the entered email address  
- User proceeds in the authentication flow without a valid account  

---

Impact
- Users without valid accounts are able to enter the verification process  
- Authentication flow is bypassed due to missing validation check  
- Unnecessary verification emails are generated  
- Potential risk of abuse in authentication logic  
- Confusing user experience and inconsistent system behavior  

---

Evidence
- Verification email is received for unregistered email addresses  
- System transitions to verification step without account existence validation
