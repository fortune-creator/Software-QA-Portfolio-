Title 
Authentication / Email Verification

---

Test Objective
To verify that the system correctly validates user email existence before initiating the email verification process.

---

Precondition
- User does not have an existing account in the system  
- User is on the login or email verification page  
- Internet connection is active  

---

Steps to reproduce 
1. Open the login or email verification page  
2. Enter an unregistered or invalid email address in the email input field  
3. Click on **Continue / Submit**  
4. Observe system behavior  

---

Expected Result
- System should check if the email exists in the database before proceeding  
- If email is not registered, display an error message such as:
  - “Account not found”  
  - “Invalid email address”  
- User should NOT be redirected to email verification flow  
- No verification email should be sent  

---

Actual Result 
- System proceeds to email verification flow  
- Verification email is sent to unregistered email  
- User is allowed to continue authentication process without a valid account  

---

Test Type
Functional Testing / Negative Testing  


This test case helps validate proper authentication flow control and ensures that only registered users can proceed to email verification.
