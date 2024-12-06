![image](https://github.com/user-attachments/assets/e8ac0df9-ea83-47ea-a71e-5b421c255b0c)

# SYSADM1 -- Kerberos Lab Activity: A step-by-step Guide

**Objective:**

Set up a basic Kerberos authentication system to understand how Kerberos
manages secure logins through ticket-based access.

**Setup Requirements:**

-   Two VMs in Oracle VM, both running a Linux distribution like Ubuntu
    or CentOS.

-   VM1: Kerberos Server

-   VM2: Kerberos Client

**Step 1: Initial Setup and Package Installation**

1.  **Update Packages on Both VMs:**

    -   Open a terminal on each VM and run:

*bash*

*sudo apt update && sudo apt upgrade --y*

***VM1:**\
*![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image2.png){width="7.027083333333334in"
height="6.56875in"}

***VM2:***

![image](https://github.com/user-attachments/assets/39bc09b5-5fc8-4695-9aed-fda456962e0e)


![image](https://github.com/user-attachments/assets/770e565f-d552-47f3-9abd-f28963778477)


2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y*
![image](https://github.com/user-attachments/assets/3648176b-7c5c-4335-99e6-4d43e71166cb)



3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y*

![image](https://github.com/user-attachments/assets/aa6dd014-6c02-4b27-89d2-3721a4207663)


![image](https://github.com/user-attachments/assets/fa0eba51-209d-473f-8b9a-9e352fb4b563)


-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

![image](https://github.com/user-attachments/assets/c61a88fe-f996-4c40-9ea3-8db62d916c88)


![image](https://github.com/user-attachments/assets/523e4477-e3ae-4c78-b6ab-eb1ace997a91)


**Step 2: Configure the Kerberos Server (VM1)**

1.  **Edit the Kerberos Configuration File:**

    -   Open /etc/krb5.conf for editing:

*bash*

*sudo nano /etc/krb5.conf*

-   Set the realm as MYLAB.LOCAL. You should also specify the KDC and
    admin server as VM1's hostname or IP address:

ini

\[libdefaults\]

default_realm = MYLAB.LOCAL

\[realms\]

MYLAB.LOCAL = {

kdc = \<VM1_IP_or_hostname\>

admin_server = \<VM1_IP_or_hostname\>

}

-   Save and close the file (Ctrl+X, then Y, and Enter to confirm).

![image](https://github.com/user-attachments/assets/d51a1409-0da2-4649-9744-8f7e129a8e3e)


2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

![image](https://github.com/user-attachments/assets/db546a89-20c2-4e44-8c8d-909d49fb2661)


3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*
![image](https://github.com/user-attachments/assets/cc2fdd96-1dfc-49a3-acc5-60058e524678)


**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

![image](https://github.com/user-attachments/assets/ed0bb0d4-c4f9-49e2-a4e5-744a08a735ff)


2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"*

![image](https://github.com/user-attachments/assets/807df621-9057-4daf-97de-17d5bbf3ae8f)

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

![image](https://github.com/user-attachments/assets/3b0d136c-7fb9-40f1-b37e-b39470622c03)


-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit <testuser@MYLAB.LOCAL>*

![image](https://github.com/user-attachments/assets/24aa1a9e-a1b9-47d4-b0b4-fcd193e13e44)

**There was an error on trying to find my default realm even though I
established the connection already.***

-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist*

![image](https://github.com/user-attachments/assets/566bce01-89a0-4d37-90ee-2c5604e8ce0c)

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
