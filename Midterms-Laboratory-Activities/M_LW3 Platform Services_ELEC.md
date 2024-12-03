+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 2b5f8265b9124aed80c81053531d265b |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, RALPH LUIS G.        | DATE PERFORMED:        | /50      |
|                                  | 10/17/2024             |          |
+----------------------------------+------------------------+----------+
| Section: IDC2                    | DATE SUBMITTED:        |          |
|                                  | 10/17/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Platform Services

# Requirement: 

-   A virtual machine running Windows Server

    **Objective/s:**

    To analyze IIS logs in the Event Viewer to identify critical web
    service metrics, understand common error codes, and learn how to
    monitor the health of web applications.

**Instructions**

**Part 1: Opening Event Viewer and Loading Logs**

1.  Access the event viewer in the server.

2.  From the event viewer, explore the windows log and list down its
    major categories

Here are the 5 major categories of windows logs:

-Application

-Security

-Setup

-System

-Forwarded events

![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image2.png){width="1.6356452318460193in"
height="1.177247375328084in"}

**Part 2: Filtering and Analyzing IIS Events**

1.  Apply filter to the windows log categories to display errors for the
    past 12 hours.

![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image3.png){width="5.604948600174978in"
height="2.5211854768153983in"}

![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image4.png){width="5.646616360454943in"
height="3.0925535870516185in"}

![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image5.png){width="5.650404636920385in"
height="3.1621937882764652in"}

2.  **Identify Critical Events** or recurring events.

> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image6.png){width="5.729966097987751in"
> height="2.8545647419072617in"}
>
> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image7.png){width="6.367390638670166in"
> height="2.6913068678915137in"}
>
> There were no critical events in my web server when I filtered it
> although there are some recurring events when I went back to the
> errors. These were event error 8200 and 1014 have 9 errors each, 8198
> having 6, 7023 and 46 having 2 each.
>
> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image8.png){width="6.33421697287839in"
> height="2.2919860017497813in"}
>
> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image9.png){width="6.5009076990376204in"
> height="2.5107666229221346in"}
>
> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image10.png){width="6.521743219597551in"
> height="2.1252963692038493in"}
>
> ![](vertopal_2b5f8265b9124aed80c81053531d265b/media/image11.png){width="6.511325459317585in"
> height="1.614808617672791in"}

3.  **Analyze the Events**:

    -   For each critical or recurring event, **record the following
        details**:

        -   **Event ID**

        -   **Source**

        -   **Timestamp**

        -   **Description**

+---------+---------+-------------+------------------------------------+
| EVENT   | SOURCE  | TIME STAMP  | DESCRIPTION                        |
| ID      |         |             |                                    |
+=========+=========+=============+====================================+
| 8200    | Secur   | 10/17/2024  | License Acquisition failure or     |
|         | ity-SPP | 8:27:52 AM  | First login - Unable to connect to |
|         |         |             | machine                            |
|         |         |             |                                    |
|         |         |             | ![](vertopal_2b5f8265b912          |
|         |         |             | 4aed80c81053531d265b/media/image12 |
|         |         |             | .png){width="2.2086417322834646in" |
|         |         |             | height="0.4792333770778653in"}     |
+---------+---------+-------------+------------------------------------+
| 1014    | Secur   | 10/17/2024  | Acquisition of end user license    |
|         | ity-SPP | 8:27:52 AM  | failed                             |
|         |         |             |                                    |
|         |         |             | ![](vertopal_2b5f8265b912          |
|         |         |             | 4aed80c81053531d265b/media/image13 |
|         |         |             | .png){width="3.1150185914260717in" |
|         |         |             | height="0.41672462817147854in"}    |
+---------+---------+-------------+------------------------------------+
| 8198    | Secur   | 10/17/2024  | License Activation failed          |
|         | ity-SPP | 8:27:52 AM  |                                    |
|         |         |             | ![](vertopal_2b5f8265b912          |
|         |         |             | 4aed80c81053531d265b/media/image14 |
|         |         |             | .png){width="3.7192694663167103in" |
|         |         |             | height="0.4896511373578303in"}     |
+---------+---------+-------------+------------------------------------+
| 7023    | Service | 10/17/2024  | The windows time service           |
|         | Control | 8:25:20 AM  | terminated with following error:   |
|         | Manager |             | An attempt was made to logon, but  |
|         |         |             | the network logon service was not  |
|         |         |             | started                            |
|         |         |             |                                    |
|         |         |             | ![](vertopal_2b5f8265b91           |
|         |         |             | 24aed80c81053531d265b/media/image1 |
|         |         |             | 5.png){width="4.458955599300087in" |
|         |         |             | height="0.4896511373578303in"}     |
+---------+---------+-------------+------------------------------------+
| 46      | Time    | 10/17/2024  | The time service encountered an    |
|         | Service | 8:25:20 AM  | error and was forced to shut down. |
|         |         |             | An attempt was made to logon, but  |
|         |         |             | the network logon service was not  |
|         |         |             | started                            |
|         |         |             |                                    |
|         |         |             | ![](vertopal_2b5f8265b91           |
|         |         |             | 24aed80c81053531d265b/media/image1 |
|         |         |             | 6.png){width="5.479931102362205in" |
|         |         |             | height="0.4375612423447069in"}     |
+---------+---------+-------------+------------------------------------+

**Part 3: Troubleshooting and Solution Development**

1.  Review the logs and check for recurring errors.

2.  Is there a specific time or pattern to these errors?

3.  Draft a Troubleshooting Report:

    -   Based on the events found, create a short report with the
        following sections:

**Report Structure**

**1.** Overview

-   A brief summary of the issue and scope of your analysis.

> Based on the screenshots that I provided, this paper focuses on
> analyzing the common mistakes in the system logs. As the first one of
> two primary issues the error is associated with the Event Sources:
> \`Security-SPP\`, \`Time-Service\`, including \`Service Control
> Manager\`. My goal for this assessment to be able to define patterns
> existing in these errors and to indicate possible causes of the errors
> with the necessary actions for resolution.

**2.** Key Findings

-   List the critical events you found.

\- Event ID 8198 (Security-SPP): Many security incidences were reported
at intervals of seconds to five minutes. This could be related to issues
of software protection or licensing as well.

\- Event ID 1014 (Security-SPP): The Figure below shows DNS client
errors, this is suggestive of problems with DNS name resolution.

\- Event ID 8200 (Security-SPP): The third mistake coming from the
Software Protection Platform, other regularly originate from problems
with the software licensing or activation.

\- Event ID 46 (Time-Service):\* Network or service authentication
problems and time synchronization issues that can affect the efficiency
of the network.

\- Event ID 7023 (Service Control Manager): A service was indicated to
be not set up properly and may have to be looked at more closely.

**3.** Root Causes and Solutions

-   Describe the likely cause of each error and how you would fix it.

\- Security-SPP Errors (Event IDs 8198, 8200, 1014):

\- Cause: They often stem from problems within software protection or
licensing, most of the time. Such errors occur when Windows has failed
to activate the software it uses; this can be as a result of corrupt
files, network connection problems or because of varied licenses from
those initially installed.

\- Solution:

Check the Windows activation status and make sure that your system is
legal. Ensure there is a check on the Software Protection Platform
service for update or reactivation problems. After reviewing event id
1014 it needs to flush out the DNS cache and check the DNS settings.

\- Time-Service Errors (Event ID 46):

\- Cause: The time synchronization service seems to be not working
properly probably due to the issues of connectivity of the NTP service
or bad time setting.

\- Solution:

See that time settings of the system running the program are well set.
Check the settings of the Windows Time service and make sure it can
reach the NTP server. Another way is set up the system time from time
server by the command either restart or manually synchronize the time by
using the command \`w32tm /resync\`

\- Service Control Manager Errors (Event ID 7023):

\- Cause: This event indicates a service terminated unexpectedly. This
could be due to incorrect configurations, insufficient permissions, or
missing dependencies.

\- Solution:

Look up and check the service logs and confirm all dependency are well
configured. Restart the service and ensure it is set to the appropriate
startup type.

Last steps:\
1. Perform the recommended solutions starting with the licensing and
network configuration steps.

2.After applying the fixes, monitor the logs to ensure the errors are
resolved and no new issues arise.

**Part 4: Reflection Questions**

1.  What are the most common causes of a **503 Service Unavailable**
    error?

-   I did not encounter this error while I was doing the task but the
    503 error will occur when the server is overloaded like there are
    too many requests and the server lacks for example CPU memory to
    handle it and most common than not the cause might be because of a
    scheduled maintenance that the administrator wasn't aware about.

2.  How would you **monitor login attempts** to detect potential
    security threats?

-   To monitor login attempts for security threats I would enable
    detailed logging of authentication events, this includes the
    successful and failed attempts and to do this I will be using tools
    like SIEM (Security Information and Event Management) systems. I
    will also analyze logs for patterns such as repeated failed logins,
    unusual IP addresses, and logins from unexpected locations or
    devices, and so that I will be notified I will set up alerts for
    suspicious activities like brute-force attempts.

3.  Why is **monitoring logs** in Event Viewer important for
    administrators?

-   I think monitoring logs in event viewer is essential for
    administrators because it provides real-time insights on system
    performance, security events, and potential issues. By tracking the
    logs, admins can easily detect hardware failures, software errors,
    security breaches, and configuration problems, allowing for
    troubleshooting and maintaining the system's integrity.

Grading Rubric

  ---------------------------------------------------------------------------------------------------------------------------------------
  **Criteria**        **Excellent**     **Good**          **Needs                           **Poor**                         **Points**
                                                          Improvement**                                                      
  ------------------- ----------------- ----------------- --------------- ----------------- ------------- ------------------ ------------
  **Log Analysis**    Identifies all    Identifies most   Identifies some                   Fails to                         /10
                      key events (503,  key events with   events, but                       identify key                     
                      404, 500, etc.)   minor errors in   with incomplete                   events or                        
                      with accurate     details.          or incorrect                      provides                         
                      event details.                      details.                          incorrect                        
                                                                                            details.                         

  **Troubleshooting   Proposes logical, Solutions are     Solutions are                     Solutions are                    /10
  Solutions**         effective         mostly correct    somewhat vague                    unclear or                       
                      solutions to all  but miss some key or incomplete.                    incorrect.                       
                      identified        points.                                                                              
                      issues.                                                                                                

  **Report Structure  Well-organized    Report is mostly  Report is                         Report is                        /10
  & Clarity**         report with all   organized with    disorganized or                   unclear or                       
                      sections clearly  minor formatting  missing                           incomplete.                      
                      completed.        issues.           sections.                                                          

  **Recommendations   Provides          Recommendations                   Recommendations                 Fails to provide   /10
  for Monitoring**    thoughtful,       are relevant but                  are vague or                    relevant           
                      proactive         lack depth.                       incomplete.                     recommendations.   
                      recommendations                                                                                        
                      to prevent future                                                                                      
                      issues.                                                                                                

  **Participation &   Actively engaged  Participated but                  Minimal                         Did not            /10
  Effort**            in the activity,  required some                     participation,                  participate        
                      followed          guidance.                         needed                          meaningfully.      
                      instructions                                        significant help.                                  
                      thoroughly.                                                                                            

  **Score**                                                                                                                  **/50**
  ---------------------------------------------------------------------------------------------------------------------------------------
