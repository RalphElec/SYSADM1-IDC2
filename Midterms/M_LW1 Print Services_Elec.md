+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 5dd0a0ac437140a8884849d50def90a6 |                        |          |
| /media/image9.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+==================================+========================+==========+
| NAME: ELEC,RALPH LUIS G.         | DATE                   | /50      |
|                                  | PERFORMED:10/03/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE SUBMITTED:        |          |
|                                  | 10/03/2024             |          |
+----------------------------------+------------------------+----------+

1.  # SYSADM1 -- Monitoring Print Services in Windows Server 2019

    # Requirement: 

-   A virtual machine running Linux and Windows OS

Part 1: Setting Up Print Services

1.  Install and configure **print.srv** domain

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image2.png){width="7.027083333333334in"
> height="3.1659722222222224in"}

2.  Connect one client to the recently created domain

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image1.png){width="4.146411854768154in"
> height="1.7398261154855643in"}

3.  Install Print Services Role:

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image8.png){width="4.010976596675415in"
> height="1.7814982502187227in"}

4.  Search the internet for any printer installer and convert it to iso

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image3.png){width="6.657179571303587in"
> height="0.7501049868766404in"}

5.  Install and deploy it as network printer

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image13.png){width="5.021534339457568in"
> height="2.0211154855643043in"}
>
> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image10.png){width="4.552718722659668in"
> height="2.6670384951881014in"}

Part 2: Monitoring Print Services

> Objective: Familiarize yourself with monitoring tools available in
> Windows Server 2019.

1.  Event Viewer:

    -   Open Event Viewer (run eventvwr.msc).

    -   Navigate to Applications and Services Logs \> Microsoft \>
        > Windows \> PrintService.

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image7.png){width="4.563136482939632in"
> height="1.4897911198600176in"}

-   Review logs for print jobs, errors, and warnings.

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image5.png){width="7.027083333333334in"
> height="2.6131944444444444in"}
>
> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image12.png){width="7.027083333333334in"
> height="1.6381944444444445in"}
>
> The printer could not print virtually if the port was on LPT port 1
> but it worked when I connected it to PORTPROMPT.

2.  Performance Monitor:

    -   Open Performance Monitor (run perfmon).

![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image15.png){width="7.027083333333334in"
height="4.444444444444445in"}

> In the left panel, expand Data Collector Sets \> System.

-   Right-click System Performance and select Start.

![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image4.png){width="6.928050087489064in"
height="3.7505238407699037in"}

-   Monitor performance metrics related to print services.

![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image15.png){width="7.027083333333334in"
height="4.444444444444445in"}

3.  Using Print Management Console:

    -   Open Print Management from Server Manager.

    -   View active print jobs and their status.

    -   Use the Printers node to check the status of all printers.

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image12.png){width="7.027083333333334in"
> height="1.6381944444444445in"}
>
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

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image6.png){width="6.511325459317585in"
> height="0.5729965004374453in"}

-   Follow the installation instructions provided by the tool\'s
    > documentation.

-   Configure it to monitor your print services.

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image11.png){width="6.792614829396325in"
> height="2.0940419947506563in"}
>
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

> ![](vertopal_5dd0a0ac437140a8884849d50def90a6/media/image14.png){width="7.027083333333334in"
> height="3.688888888888889in"}
>
> Rubric

+-------+------------+-----------+-----------+------+---------+------+
| > **  | > **1      | > **2     | > **3     | >    | > **5   | > *  |
| Crite | > (Unsatis | > (Needs  | > (Satisf |  **4 | >       | *Sco |
| ria** | factory)** | > Impro   | actory)** | >    |  (Excel | re** |
|       |            | vement)** |           | (Goo | lent)** |      |
|       |            |           |           | d)** |         |      |
+=======+============+===========+===========+======+=========+======+
+-------+------------+-----------+-----------+------+---------+------+

+---------------------------------------------------------------+---+---+---+---+---+---+
| > **Part 1: Setting Up Print Services**                       |   |   |   |   |   |   |
+===============================================================+===+===+===+===+===+===+
+---------------------------------------------------------------+---+---+---+---+---+---+

+----------+--------+---------+---------+----------+---------------+---+
| >        | > No   | >       | >       | > Domain | > Domain      |   |
| **Domain | >      |  Domain |  Domain | > co     | > configured  |   |
| > Instal | domain | >       | >       | nfigured | > and         |   |
| lation** | > c    | created | created | > well   | > documented  |   |
|          | reated | > with  | > co    |          | > thoroughly  |   |
|          |        | >       | rrectly |          |               |   |
|          |        |  errors |         |          |               |   |
+==========+========+=========+=========+==========+===============+===+
+----------+--------+---------+---------+----------+---------------+---+

+----------+---------+----------+-----------+----------+------------+---+
| >        | >       | > Co     | > Client  | > Client | > Client   |   |
| **Client |  Client | nnection | >         | > c      | >          |   |
| > Conn   | > not   | >        | connected | onnected |  connected |   |
| ection** | > co    |  attempt | > but     | > c      | > and      |   |
|          | nnected | > failed | > with    | orrectly | >          |   |
|          |         |          | > issues  |          | documented |   |
|          |         |          |           |          | > well     |   |
+==========+=========+==========+===========+==========+============+===+
+----------+---------+----------+-----------+----------+------------+---+

+------------+--------+---------+---------+-----------+---------------+---+
| > **Print  | > Role | > Role  | > Role  | > Role    | > Role        |   |
| > Services | > not  | > in    | > in    | >         | > installed,  |   |
| > Role     | > ins  | stalled | stalled | installed | > configured, |   |
| > Inst     | talled | > with  | > co    | > and     | > and         |   |
| allation** |        | >       | rrectly | > c       | > documented  |   |
|            |        |  issues |         | onfigured | > thoroughly  |   |
+============+========+=========+=========+===========+===============+===+
+------------+--------+---------+---------+-----------+---------------+---+

+-----------+-------+-----------+----------+----------+-------------+---+
| >         | > No  | >         | > I      | > I      | > Installer |   |
| **Printer | >     | Installer | nstaller | nstaller | >           |   |
| >         |  inst | > c       | > c      | > c      |  converted, |   |
| Installer | aller | onversion | onverted | onverted | > used, and |   |
| > Con     | >     | >         | > but    | > and    | >           |   |
| version** | found | attempted | > not    | > used   |  documented |   |
|           |       | > but     | > used   |          | > well      |   |
|           |       | > failed  |          |          |             |   |
+===========+=======+===========+==========+==========+=============+===+
+-----------+-------+-----------+----------+----------+-------------+---+

+------------+--------+----------+----------+---------+-------------+---+
| >          | > P    | > De     | >        | >       | > Printer   |   |
|  **Network | rinter | ployment |  Printer | Printer | > deployed, |   |
| > Printer  | > not  | > failed | >        | > d     | > tested,   |   |
| > De       | > de   |          | deployed | eployed | > and       |   |
| ployment** | ployed |          | > but    | > co    | >           |   |
|            |        |          | > not    | rrectly |  documented |   |
|            |        |          | > fu     |         | > well      |   |
|            |        |          | nctional |         |             |   |
+============+========+==========+==========+=========+=============+===+
+------------+--------+----------+----------+---------+-------------+---+

+---------------------------------------------------------------+---+---+---+---+---+---+
| > **Part 2: Monitoring Print Services**                       |   |   |   |   |   |   |
+===============================================================+===+===+===+===+===+===+
+---------------------------------------------------------------+---+---+---+---+---+---+

+--------+--------+----------+----------+----------+----------------+---+
| > *    | >      | > Opened | > Logs   | > Logs   | > Logs         |   |
| *Event |  Event | > but no | >        | >        | > reviewed     |   |
| >      | >      | > logs   | reviewed | reviewed | > with         |   |
| Viewer | Viewer | >        | > but    | > with   | > thorough     |   |
| > U    | > not  | reviewed | > sup    | > some   | > analysis and |   |
| sage** | >      |          | erficial | >        | >              |   |
|        | opened |          |          | analysis |  documentation |   |
+========+========+==========+==========+==========+================+===+
+--------+--------+----------+----------+----------+----------------+---+

+-----------+-----------+---------+---------+----------+------------+---+
| > **Pe    | > Pe      | >       | >       | >        | > Metrics  |   |
| rformance | rformance |  Opened | Metrics |  Metrics | >          |   |
| > Monitor | > Monitor | > but   | > mo    | > m      | monitored, |   |
| > Usage** | > not     | > no    | nitored | onitored | >          |   |
|           | > opened  | >       | > but   | > with   |  analyzed, |   |
|           |           | metrics | > not   | > some   | > and      |   |
|           |           | > mo    | > a     | >        | >          |   |
|           |           | nitored | nalyzed | analysis | documented |   |
|           |           |         |         |          | >          |   |
|           |           |         |         |          | thoroughly |   |
+===========+===========+=========+=========+==========+============+===+
+-----------+-----------+---------+---------+----------+------------+---+

+------------+--------+-----------+-----------+--------+------------+---+
| > **Print  | > C    | > Opened  | > Active  | >      | > Active   |   |
| >          | onsole | > but     | > jobs    | Active | > jobs     |   |
| Management | > not  | > func    | > viewed  | > jobs | > viewed   |   |
| > Console  | >      | tionality | > supe    | >      | > and      |   |
| > Usage**  | opened | > not     | rficially | viewed | >          |   |
|            |        | > used    |           | > with | documented |   |
|            |        |           |           | > some | >          |   |
|            |        |           |           | >      | thoroughly |   |
|            |        |           |           | detail |            |   |
+============+========+===========+===========+========+============+===+
+------------+--------+-----------+-----------+--------+------------+---+

+---------------------------------------------------------------+---+---+---+---+---+---+
| > **Part 3: Exploring Third-Party Tools**                     |   |   |   |   |   |   |
+===============================================================+===+===+===+===+===+===+
+---------------------------------------------------------------+---+---+---+---+---+---+

+---------+----------+---------+----------+-----------+-------------+---+
| > **R   | > No     | > R     | >        | >         | > Research  |   |
| esearch | > tools  | esearch | Research |  Research | > on two    |   |
| > on    | > re     | > inc   | > on one | > on two  | > tools,    |   |
| >       | searched | omplete | > tool   | > tools   | > detailed  |   |
| Tools** |          |         | > c      | > with    | > analysis, |   |
|         |          |         | ompleted | > some    | > and       |   |
|         |          |         |          | >         | >           |   |
|         |          |         |          |  analysis |  comparison |   |
+=========+==========+=========+==========+===========+=============+===+
+---------+----------+---------+----------+-----------+-------------+---+

+------------+-------+---------+----------+-----------+-------------+---+
| > **In     | >     | > Insta | > Tool   | > Tool    | > Tool      |   |
| stallation |  Tool | llation | > i      | >         | >           |   |
| > and      | > not | >       | nstalled | installed |  installed, |   |
| > Confi    | >     |  failed | > but    | > and     | >           |   |
| guration** |  inst |         | > not    | > c       | configured, |   |
|            | alled |         | > co     | onfigured | > and       |   |
|            |       |         | nfigured | > with    | >           |   |
|            |       |         |          | > issues  |  documented |   |
|            |       |         |          |           | >           |   |
|            |       |         |          |           |  thoroughly |   |
+============+=======+=========+==========+===========+=============+===+
+------------+-------+---------+----------+-----------+-------------+---+

+---------+---------+-------+----------+-----------+----------------+---+
| > **Re  | > No    | > R   | > Report | > Report  | >              |   |
| porting | >       | eport | > g      | >         |  Comprehensive |   |
| > Fin   |  report | >     | enerated | generated | > report with  |   |
| dings** | > ge    | lacks | > but    | > with    | > thorough     |   |
|         | nerated | > d   | > lacks  | > some    | > analysis and |   |
|         |         | etail | >        | >         | >              |   |
|         |         |       | analysis |  analysis |  documentation |   |
+=========+=========+=======+==========+===========+================+===+
+---------+---------+-------+----------+-----------+----------------+---+
