+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 31847508807040dfbb0d358df70a94cd |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME:                            | DATE PERFORMED:        |          |
+----------------------------------+------------------------+----------+
| Section:                         | DATE SUBMITTED:        |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Linux

# Requirement: 

-   A virtual machine running Linux

![](vertopal_31847508807040dfbb0d358df70a94cd/media/image2.png){width="4.135416666666667in"
height="1.8020833333333333in"}

Complete this lab as follows:

1.  Use the service --status-all command to list all active and inactive
    services.

List down active and inactive services in the table below. Provide five
(5) services for each column.

  -----------------------------------------------------------------------
  **Active**                             **Inactive**
  -------------------------------------- --------------------------------
  alsa-utils.service                     Bluetooth.service

  anacron.service                        console-sh.service

  apparmor.service                       grub-common.service

  apport.service                         sssd.service

  cron.service                           Plymouth.service
  -----------------------------------------------------------------------

SS:\
![](vertopal_31847508807040dfbb0d358df70a94cd/media/image3.png){width="2.177387357830271in"
height="1.156411854768154in"}\
![](vertopal_31847508807040dfbb0d358df70a94cd/media/image4.png){width="1.3335192475940507in"
height="0.44797900262467194in"}\
![](vertopal_31847508807040dfbb0d358df70a94cd/media/image5.png){width="2.000278871391076in"
height="0.1771084864391951in"}

2.  Start the Bluetooth service using the systemctl command.

Ex. sudo systemctl start httpd

![](vertopal_31847508807040dfbb0d358df70a94cd/media/image6.png){width="4.359946412948381in"
height="1.1875in"}

3.  Check the status of the Bluetooth service. What is its status?\
    The status of Bluetooth is inactive(dead).

SS:\
![](vertopal_31847508807040dfbb0d358df70a94cd/media/image7.png){width="7.027083333333334in"
height="2.165277777777778in"}

4.  Check the status of the cups services. Since when was it running?\
    the cups service was running 8 mins ago starting from 9:10am
    computer time.

SS:\
![](vertopal_31847508807040dfbb0d358df70a94cd/media/image8.png){width="7.027083333333334in"
height="2.838888888888889in"}

5.  Stop cups services.

> ![](vertopal_31847508807040dfbb0d358df70a94cd/media/image9.png){width="6.928050087489064in"
> height="1.5731364829396326in"}

6.  Verify if the service was stopped.

> ![](vertopal_31847508807040dfbb0d358df70a94cd/media/image10.png){width="1.2918471128608924in"
> height="0.29170713035870516in"}\
> ![](vertopal_31847508807040dfbb0d358df70a94cd/media/image11.png){width="7.027083333333334in"
> height="0.4111111111111111in"}

7.  Restart the cups services

![](vertopal_31847508807040dfbb0d358df70a94cd/media/image12.png){width="6.532162073490814in"
height="0.6667596237970254in"}

8.  Verify if the service was restarted.

![](vertopal_31847508807040dfbb0d358df70a94cd/media/image13.png){width="7.027083333333334in"
height="3.15in"}
