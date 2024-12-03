+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 6ddd444a101045748fb51e8a3f2854e7 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, RALPH LUIS G.        | DATE                   | /50      |
|                                  | PERFORMED:10/03/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE SUBMITTED:        |          |
|                                  | 10/03/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Monitoring Print Services in Windows Server 2019

# Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image2.png){width="7.027083333333334in"
height="3.1659722222222224in"}

2.  Connect one client to the recently created domain

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image3.png){width="4.146411854768154in"
height="1.7398261154855643in"}

3.  Install Print Services Role:

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image4.png){width="4.010976596675415in"
height="1.7814982502187227in"}

4.  Search the internet for any printer installer and convert it to iso

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image5.png){width="6.657179571303587in"
height="0.7501049868766404in"}

5.  Install and deploy it as network printer

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image6.png){width="5.021534339457568in"
height="2.0211154855643043in"}

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image7.png){width="4.552718722659668in"
height="2.6670384951881014in"}

Part 2: Monitoring Print Services

Objective: Familiarize yourself with monitoring tools available in
Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        Windows \> PrintService.

> ![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image8.png){width="4.563136482939632in"
> height="1.4897911198600176in"}

-   Review logs for print jobs, errors, and warnings.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image9.png){width="7.027083333333334in"
height="2.6131944444444444in"}

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image10.png){width="7.027083333333334in"
height="1.6381944444444445in"}

The printer could not print virtually if the port was on LPT port 1 but
it worked when I connected it to PORTPROMPT.

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image11.png){width="7.027083333333334in"
height="4.444444444444445in"}

In the left panel, expand Data Collector Sets \> System.

-   Right-click System Performance and select Start.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image12.png){width="6.928050087489064in"
height="3.7505238407699037in"}

-   Monitor performance metrics related to print services.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image11.png){width="7.027083333333334in"
height="4.444444444444445in"}

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image10.png){width="7.027083333333334in"
height="1.6381944444444445in"}

Part 3: Exploring Third-Party Monitoring Tools

1.  Research at least two third-party print monitoring tools

    -   Consider factors such as features, pricing, and compatibility
        with Windows Server 2019.

### 1. PaperCut NG (Free Version)

-   **Features:**

    -   Basic print tracking and reporting.

    -   User and group quotas.

    -   Simple print job management.

-   **Pricing:**

    -   Free version available; advanced features require a paid
        upgrade.

-   **Compatibility:**

    -   Works with Windows Server 2019.

### Print Inspector

-   **Features:**

    -   Tracks and reports on print jobs.

    -   Monitors all print servers and printers in the network.

    -   Provides detailed reports on usage by user, printer, and
        document.

-   **Pricing:**

    -   Free version available with essential features.

-   **Compatibility:**

    -   Works with Windows Server 2019.

2.  Install and Configure:

    -   Choose one of the tools to install in your environment.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image13.png){width="6.511325459317585in"
height="0.5729965004374453in"}

-   Follow the installation instructions provided by the tool\'s
    documentation.

-   Configure it to monitor your print services.

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image14.png){width="6.792614829396325in"
height="2.0940419947506563in"}

I downloaded the PrintInspector

3.  Test and Report Findings:

    -   Generate a report or dashboard from the tool.

**-So far with this app I can see the name of the document that is
printed, the date that it was printed, the status, number of pages, the
day it was submitted and the printer that was used on the document. This
is only free but with these features I think I can manage my server with
users in it especially because I can monitor their printing Queues
through this application and also their computers.**

-   Analyze the collected data (e.g., print volume, errors, user
    activity).

![](vertopal_6ddd444a101045748fb51e8a3f2854e7/media/image15.png){width="7.027083333333334in"
height="3.688888888888889in"}

Rubric

  --------------------------------------------------------------------------------------------------------------
  **Criteria**   **1                  **2 (Needs       **3                **4        **5             **Score**
                 (Unsatisfactory)**   Improvement)**   (Satisfactory)**   (Good)**   (Excellent)**   
  -------------- -------------------- ---------------- ------------------ ---------- --------------- -----------

  --------------------------------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 1: Setting Up Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Domain         No domain Domain     Domain      Domain       Domain           
  Installation**   created   created    created     configured   configured and   
                             with       correctly   well         documented       
                             errors                              thoroughly       
  ---------------- --------- ---------- ----------- ------------ ---------------- --

  ----------------------------------------------------------------------------------

  --------------------------------------------------------------------------------
  **Client       Client not  Connection   Client      Client      Client        
  Connection**   connected   attempt      connected   connected   connected and 
                             failed       but with    correctly   documented    
                                          issues                  well          
  -------------- ----------- ------------ ----------- ----------- ------------- --

  --------------------------------------------------------------------------------

  ------------------------------------------------------------------------------------
  **Print Services Role not    Role        Role        Role         Role installed, 
  Role             installed   installed   installed   installed    configured, and 
  Installation**               with issues correctly   and          documented      
                                                       configured   thoroughly      
  ---------------- ----------- ----------- ----------- ------------ --------------- --

  ------------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Printer      No          Installer    Installer   Installer   Installer      
  Installer      installer   conversion   converted   converted   converted,     
  Conversion**   found       attempted    but not     and used    used, and      
                             but failed   used                    documented     
                                                                  well           
  -------------- ----------- ------------ ----------- ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Network      Printer    Deployment   Printer      Printer     Printer        
  Printer        not        failed       deployed but deployed    deployed,      
  Deployment**   deployed                not          correctly   tested, and    
                                         functional               documented     
                                                                  well           
  -------------- ---------- ------------ ------------ ----------- -------------- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 2: Monitoring Print Services**                                          
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ------------------------------------------------------------------------------
  **Event   Event     Opened but  Logs reviewed Logs        Logs reviewed     
  Viewer    Viewer    no logs     but           reviewed    with thorough     
  Usage**   not       reviewed    superficial   with some   analysis and      
            opened                              analysis    documentation     
  --------- --------- ----------- ------------- ----------- ----------------- --

  ------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Performance   Performance   Opened but  Metrics     Metrics     Metrics       
  Monitor Usage** Monitor not   no metrics  monitored   monitored   monitored,    
                  opened        monitored   but not     with some   analyzed, and 
                                            analyzed    analysis    documented    
                                                                    thoroughly    
  --------------- ------------- ----------- ----------- ----------- ------------- --

  ----------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------
  **Print       Console   Opened but      Active jobs     Active    Active jobs   
  Management    not       functionality   viewed          jobs      viewed and    
  Console       opened    not used        superficially   viewed    documented    
  Usage**                                                 with some thoroughly    
                                                          detail                  
  ------------- --------- --------------- --------------- --------- ------------- --

  ----------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Part 3: Exploring Third-Party Tools**                                        
  --------------------------------------------------------------- -- -- -- -- -- --

  ---------------------------------------------------------------------------------

  ---------------------------------------------------------------------------------
  **Research   No tools     Research     Research on Research on  Research on    
  on Tools**   researched   incomplete   one tool    two tools    two tools,     
                                         completed   with some    detailed       
                                                     analysis     analysis, and  
                                                                  comparison     
  ------------ ------------ ------------ ----------- ------------ -------------- --

  ---------------------------------------------------------------------------------

  ----------------------------------------------------------------------------------------
  **Installation    Tool not    Installation   Tool         Tool         Tool           
  and               installed   failed         installed    installed    installed,     
  Configuration**                              but not      and          configured,    
                                               configured   configured   and documented 
                                                            with issues  thoroughly     
  ----------------- ----------- -------------- ------------ ------------ -------------- --

  ----------------------------------------------------------------------------------------

  -------------------------------------------------------------------------------
  **Reporting   No report   Report   Report      Report      Comprehensive     
  Findings**    generated   lacks    generated   generated   report with       
                            detail   but lacks   with some   thorough analysis 
                                     analysis    analysis    and documentation 
  ------------- ----------- -------- ----------- ----------- ----------------- --

  -------------------------------------------------------------------------------
