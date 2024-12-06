![image](https://github.com/user-attachments/assets/28e44f7d-9bb7-4cd5-8ab5-c46f8b1c4a71)


1.  # SYSADM1 -- Setting Up Webserver

    # Requirement: 

-   A virtual machine running Linux and Windows OS

> Task Instructions:

1.  Install IIS by adding it as a role, select necessary features,
    include monitoring tools

![image](https://github.com/user-attachments/assets/dd8e1082-7131-444a-819a-2bed90c4de77)


2.  Create a website by opening IIS Manager

    -   Right-click on the server's name and select Internet Information
        Services Manager.

    -   Right-click on Sites and select Add Website.

    -   Enter a name, description, physical path (where your website
        files will reside), IP address, port, and host name.

![image](https://github.com/user-attachments/assets/6f0bcf8e-d6e5-4c63-ab27-6fa3a321c768)

3.  Configure the Website:

    -   Right-click on your website and select Edit.

![image](https://github.com/user-attachments/assets/0d5ebb12-3867-4621-8140-6702a07b1b9f)


-   Set the Default Document to the name of your main HTML file
    \>default.html

![image](https://github.com/user-attachments/assets/54b28b02-76a0-4e50-b487-e1b86414b550)


-   Configure other settings as needed (e.g., SSL certificates,
    authentication)

![image](https://github.com/user-attachments/assets/c3b83b32-9d9e-487d-9cb0-9f28200a93be)


4.  Create a Web Page:

    -   Create an HTML file in the physical path you specified.

![image](https://github.com/user-attachments/assets/d27b0a15-9152-4a97-86ca-d9bacd6ca12e)


-   Save it as default.html or your preferred name.

![image](https://github.com/user-attachments/assets/ebc9bdce-09d6-407c-953c-6971e3594e60)


5.  Test the Web Server:

    -   Open a web browser and enter the URL of your website (e.g.,
        http://localhost).

    -   You should see your web page displayed.

![image](https://github.com/user-attachments/assets/b43f2436-e6d7-493d-ba44-55dce1e4d6d4)


When I was installing I encountered a problem on where I couldn't turn
off the firewall for my server and client handshake which was weird
because it was the first time I had a problem like this but when I
re-installed it was okay. Next is I didn't know how to connect the web
server or I couldn't search the website I created for my client access
in the client virtual machine. It was a bit challenging but I searched
it up on the internet and it said to turn off the default ISS Web Site
so I can open the website I created.

> Grading Rubric

![image](https://github.com/user-attachments/assets/e4774e68-556f-4cd3-9756-5d1975c24ed4)

