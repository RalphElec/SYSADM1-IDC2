![image](https://github.com/user-attachments/assets/6c096b31-489d-4265-b021-9bbe5ed8491e)


1.  # SYSADM1 -- Monitoring Print Services in Windows Server 2019

    # Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

![image](https://github.com/user-attachments/assets/02a81ff6-2442-4505-bee5-5df63a1354aa)



2.  Connect one client to the recently created domain

![image](https://github.com/user-attachments/assets/65a0a389-486d-4889-867a-63ed3da99a28)


3.  Install Print Services Role:

![image](https://github.com/user-attachments/assets/bc7a1502-a13c-4347-a0ac-41b97e65eebb)

4.  Search the internet for any printer installer and convert it to iso

![image](https://github.com/user-attachments/assets/3f6779ba-3f69-4ec7-bc90-f2e385f9e529)


5.  Install and deploy it as network printer

![image](https://github.com/user-attachments/assets/6d5865bf-b7c7-47b2-8bef-b21b2f333e51)

![image](https://github.com/user-attachments/assets/04cf813a-5d5d-440f-af57-3f99341a62e5)


Part 2: Monitoring Print Services

> Objective: Familiarize yourself with monitoring tools available in
> Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        > Windows \> PrintService.

![image](https://github.com/user-attachments/assets/918f0762-1d84-4465-b711-b0e79742560a)

-   Review logs for print jobs, errors, and warnings.

![image](https://github.com/user-attachments/assets/c61b6210-0364-420b-8ff9-6432638e334b)

![image](https://github.com/user-attachments/assets/fa575d67-7e76-4ccf-8ac9-b76835df379f)

> The printer could not print virtually if the port was on LPT port 1
> but it worked when I connected it to PORTPROMPT.

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

![image](https://github.com/user-attachments/assets/f0f82a9d-3f12-4102-850b-f5aed8363a17)

> In the left panel, expand Data Collector Sets \> System.

-   Right-click System Performance and select Start.

![image](https://github.com/user-attachments/assets/d82114a9-3879-4297-831e-3c621cf11361)

-   Monitor performance metrics related to print services.

![image](https://github.com/user-attachments/assets/a06eb25c-d60d-4b55-a8f3-7b0710c5bc13)

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

![image](https://github.com/user-attachments/assets/075134cc-6b13-4dda-ac28-9c087b151fea)

> Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        > with Windows Server 2019.

### 1. PaperCut NG (Free Version)

-   **Features:**

    -   Basic print tracking and reporting.

    -   User and group quotas.

    -   Simple print job management.

-   **Pricing:**

    -   Free version available; advanced features require a paid
        > upgrade.

-   **Compatibility:**

    -   Works with Windows Server 2019.

### Print Inspector

-   **Features:**

    -   Tracks and reports on print jobs.

    -   Monitors all print servers and printers in the network.

    -   Provides detailed reports on usage by user, printer, and
        > document.

-   **Pricing:**

    -   Free version available with essential features.

-   **Compatibility:**

    -   Works with Windows Server 2019.

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

![image](https://github.com/user-attachments/assets/1cccf642-4400-46c4-9503-db496a4bb79e)

-   Follow the installation instructions provided by the tool\'s
    > documentation.

-   Configure it to monitor your print services.

![image](https://github.com/user-attachments/assets/dc1dbea7-ba4f-4155-aa65-748319a1d676)

> I downloaded the PrintInspector

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

> **-So far with this app I can see the name of the document that is
> printed, the date that it was printed, the status, number of pages,
> the day it was submitted and the printer that was used on the
> document. This is only free but with these features I think I can
> manage my server with users in it especially because I can monitor
> their printing Queues through this application and also their
> computers.**

-   Analyze the collected data (e.g., print volume, errors, user
    > activity).

![image](https://github.com/user-attachments/assets/3dd7bde0-1b0e-4092-8550-a2148aa9100f)

![image](https://github.com/user-attachments/assets/40b6eab8-33a9-4dcd-90e1-a9deb785e2ee)

![Uploading image.png…]()
