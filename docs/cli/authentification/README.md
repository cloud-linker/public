# Authentification

CloudLinker uses **OAuth authentication via SSO** to securely authenticate users. This ensures seamless login while keeping your credentials safe. Multi-Factor Authentication (**MFA**) is supported but optional.

### **Prerequisites**

* Ensure you have the **CloudLinker CLI (`clctl`)** installed. [Installation Guide →](../../introduction/getting-started/)
* Have an active **CloudLinker account**.

### **Step 1: Run the Login Command**

To authenticate with CloudLinker, run:

```sh
clctl auth login
```

This will open your **default web browser** and redirect you to the CloudLinker **SSO authentication page**.

### **Step 2: Authenticate via SSO**

1. Enter your **CloudLinker credentials** on the login page.
2. If enabled, complete the **Multi-Factor Authentication (MFA)** step.
3. Once authenticated, CloudLinker will securely store your session in your **local keychain**.

After a successful login, you can close the browser window and return to the CLI.

### **Step 3: Verify Authentication**

To check if you are logged in, run:

```sh
clctl auth login
```

If you are already authenticated, the CLI will confirm your login status. Otherwise, it will prompt you to log in again.

### **Logging Out**

To log out and remove your authentication session, run:

```sh
clctl auth logout
```

This will clear your session from the **local keychain**, requiring you to log in again the next time you use the CLI.
