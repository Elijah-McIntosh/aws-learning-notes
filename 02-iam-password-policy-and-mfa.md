# IAM: Password Policy & Multi-Factor Authentication (MFA)

## Password Policies

Strong passwords = higher security for your AWS account.

AWS allows you to **configure a custom password policy** for IAM users.

### Password Policy Options

You can set requirements such as:

- Minimum password length  
- Require uppercase letters  
- Require lowercase letters  
- Require numbers  
- Require special characters  
- Allow IAM users to change their own password  
- Enforce password expiration  
- Prevent password reuse  

These settings help ensure that all IAM users follow secure password practices.

---

## Multi-Factor Authentication (MFA)

Multi-Factor Authentication adds an extra layer of protection.

### MFA =  
**Something you know (password)**  
+  
**Something you have (physical or digital MFA device)**

### Why MFA Matters

Even if a password is compromised, MFA prevents unauthorized access to:

- IAM users  
- The root account  

MFA is essential for protecting AWS accounts from high-impact security risks.

---

## MFA Device Options in AWS

AWS supports multiple MFA device types:

### 🔹 Virtual MFA Apps (Phone-Based)
- Google Authenticator  
- Authy  

### 🔹 Hardware MFA Devices (Physical)
- YubiKey  
- Key fob tokens (Gemalto, etc.)  

These generate time-based one-time codes required at login.

---

# ✅ What I Learned (Hands-On)

### Today I learned how to:

- **Set up an AWS IAM Password Policy** using the console  
- Configure requirements like minimum length, complexity, expiration, and reuse prevention  
- **Enable MFA for IAM users and the root account**  
- Use a virtual MFA app to connect and complete MFA setup  
- Understand how password policies + MFA work together for stronger security  
- Apply AWS best practices for identity protection  

These hands-on steps helped reinforce how IAM security settings protect the AWS environment.

---

## Summary

- **Password policies** protect IAM credentials.  
- **MFA** protects the account even if passwords are stolen.  
- Using both together is an AWS security best practice.  

This builds the foundation for secure IAM management and prepares you for more advanced identity topics.
