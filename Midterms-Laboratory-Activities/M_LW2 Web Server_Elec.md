+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 08070d448dd4464ca2eeb1fe3748b146 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, RALPH LUIS G.        | DATE                   | /50      |
|                                  | PERFORMED:10/10/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE                   |          |
|                                  | SUBMITTED:10/10/2024   |          |
+----------------------------------+------------------------+----------+

1.  # SYSADM1 -- Setting Up Webserver

    # Requirement: 

-   A virtual machine running Linux and Windows OS

> Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image2.png){width="5.182292213473316in"
height="3.5900229658792653in"}

2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image3.png){width="6.21875in"
height="5.854166666666667in"}

3.  Configure the Website:

    -   Right-click on your website and select Edit.

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image4.png){width="5.59375in"
height="3.34375in"}

-   Set the Default Document to the name of your main HTML file
    \>default.html

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image5.png){width="3.4166666666666665in"
height="2.5625in"}

-   Configure other settings as needed (e.g., SSL certificates,
    authentication)

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image6.png){width="7.027083333333334in"
height="4.722222222222222in"}

4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

> ![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image7.png){width="3.652083333333333in"
> height="1.52377624671916in"}

-   Save it as default.html or your preferred name.

> ![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image8.png){width="6.604166666666667in"
> height="2.28125in"}

5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

![](vertopal_08070d448dd4464ca2eeb1fe3748b146/media/image9.png){width="7.027083333333334in"
height="5.611111111111111in"}

When I was installing I encountered a problem on where I couldn't turn
off the firewall for my server and client handshake which was weird
because it was the first time I had a problem like this but when I
re-installed it was okay. Next is I didn't know how to connect the web
server or I couldn't search the website I created for my client access
in the client virtual machine. It was a bit challenging but I searched
it up on the internet and it said to turn off the default ISS Web Site
so I can open the website I created.

> Grading Rubric

  ----------------- ------------ -----------------------------------------------
  **Criteria**      **Points**   **Description**

  Web Server        15           Correctly installs IIS or another web server on
  Installation                   the virtual machine.

  Website           15           Successfully configures the website with the
  Configuration                  correct physical path, IP address, port, and
                                 default document.

  Successful Access 15           Successfully accesses the web page from the
                                 client computer using the correct URL.

  Troubleshooting   15           Demonstrates ability to troubleshoot common
                                 issues, such as network connectivity problems
                                 or configuration errors.

  Documentation     10           Provides clear and concise documentation of the
                                 installation, configuration, and testing
                                 process.

  Total             /70          
  ----------------- ------------ -----------------------------------------------
