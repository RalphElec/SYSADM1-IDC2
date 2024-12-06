+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| eb528649dc584db888b05e3bfeb54e7c |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, RALPH LUIS G.        | DATE                   | /50      |
|                                  | PERFORMED:11/14/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE SUBMITTED:        |          |
|                                  | 11/14/2024             |          |
+----------------------------------+------------------------+----------+

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

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image3.png){width="7.027083333333334in"
height="6.701388888888889in"}

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image4.png){width="7.027083333333334in"
height="2.2756944444444445in"}

2.  **Install Kerberos Server Packages on VM1 (Kerberos Server):**

    -   In VM1, install the Kerberos Key Distribution Center (KDC) and
        admin server:

*bash*

*sudo apt install krb5-kdc krb5-admin-server --y*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image5.png){width="7.027083333333334in"
height="4.360416666666667in"}

3.  **Install Kerberos Client Package on VM2 (Kerberos Client):**

    -   In VM2, install the Kerberos client software:

*bash*

*sudo apt install krb5-user --y*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image6.png){width="7.027083333333334in"
height="4.2347222222222225in"}

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image7.png){width="7.027083333333334in"
height="1.8395833333333333in"}

-   During installation, when prompted, enter the Kerberos realm you
    plan to set up, e.g., MYLAB.LOCAL.

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image8.png){width="7.027083333333334in"
height="3.3229166666666665in"}

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image9.png){width="7.027083333333334in"
height="4.2340277777777775in"}

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

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image10.png){width="7.027083333333334in"
height="3.286111111111111in"}

2.  **Initialize the Kerberos Database:**

    -   Create the database for the Kerberos realm:

*bash*

*sudo krb5_newrealm*

-   You will be prompted to set a password for the Kerberos database.

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image11.png){width="7.027083333333334in"
height="5.585416666666666in"}

3.  **Start and Enable the Kerberos Services:**

    -   Start the KDC and admin server, and ensure they start
        automatically on boot:

*bash*

*sudo systemctl start krb5-kdc*

*sudo systemctl start krb5-admin-server*

*sudo systemctl enable krb5-kdc*

*sudo systemctl enable krb5-admin-server*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image12.png){width="7.027083333333334in"
height="1.0659722222222223in"}

**Step 3: Set Up a Kerberos User Principal**

1.  **Create a New User Principal:**

    -   Run the following command to create a test user in the Kerberos
        realm:

*bash*

*sudo kadmin.local -q \"addprinc testuser@MYLAB.LOCAL\"*

-   Set a password for testuser.

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image13.png){width="7.027083333333334in"
height="1.1736111111111112in"}

2.  **Verify the User Principal:**

    -   To confirm the principal is created, list all principals:

*bash*

*sudo kadmin.local -q \"listprincs\"*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image14.png){width="7.027083333333334in"
height="1.6694444444444445in"}

**Step 4: Configure the Kerberos Client (VM2)**

1.  **Edit the Kerberos Configuration File on VM2:**

    -   Open /etc/krb5.conf for editing on VM2:

*bash*

*sudo nano /etc/krb5.conf*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image15.png){width="7.027083333333334in"
height="3.895138888888889in"}

-   Set the default realm to MYLAB.LOCAL and point to the KDC and admin
    server on VM1. The configuration should match what you set on VM1.

**Step 5: Test Kerberos Authentication**

1.  **Request a Kerberos Ticket for the User on VM2:**

    -   In the terminal on VM2, request a ticket for testuser:

*bash*

*kinit <testuser@MYLAB.LOCAL>*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image16.png){width="7.027083333333334in"
height="0.36736111111111114in"}*\
**There was an error on trying to find my default realm even though I
established the connection already.***

-   Enter the password you set for testuser.

2.  **Verify the Ticket:**

    -   Check if the ticket was issued by listing active Kerberos
        tickets:

*bash*

*klist*

![](vertopal_eb528649dc584db888b05e3bfeb54e7c/media/image17.png){width="6.678015091863517in"
height="0.7917771216097987in"}

-   You should see details about the ticket, such as the principal and
    expiration time, confirming successful Kerberos authentication.
