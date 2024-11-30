+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 2afcedfa32744466beb570586382d8c1 |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, RALPH LUIS G.        | DATE                   |          |
|                                  | PERFORMED:08/29/2024   |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE SUBMITTED:        |          |
|                                  | 08/29/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Managing Services in Windows

# Requirement: 

-   A virtual machine running Linux and Windows OS

    **Services** are background processes that run independently of user
    interactions in Windows. They provide essential system functions,
    such as network connectivity, printing, and time synchronization.
    This lab will guide you through the process of managing services
    using the Services app.

# Instructions:  {#instructions .list-paragraph}

1.  Open the Start menu and search for \"Services\"

2.  Familiarize yourself with the columns, including Service Name,
    Display Name, Status, and Startup type.

3.  Right-click on a service and select \"Start\", \"Stop\", or
    \"Restart\". Fill out the table below

  ------------------------------------------------------------------------------------------------------------------------
  **Status**   **Name of    **Screenshot**
               Service**    
  ------------ ------------ ----------------------------------------------------------------------------------------------
  Start        ActiveX      ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image2.png){width="4.146411854768154in"
               Installer    height="1.989861111111111in"}
               (AxInstSV)   

  Stop         ActiveX      ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image3.png){width="4.6360640857392825in"
               Installer    height="2.333659230096238in"}
               (AxInstSV)   

  Restart      ActiveX      ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image4.png){width="4.302683727034121in"
               Installer    height="2.239896106736658in"}
               (AxInstSV)   

  Pause        Server       ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image5.png){width="4.125575240594926in"
                            height="1.8752613735783028in"}
  ------------------------------------------------------------------------------------------------------------------------

4.  Select five network services, right-click to view its properties.
    Modify the startup setting to Manual.

> **SS**:
>
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image6.png){width="3.1464326334208224in"
> height="3.5937215660542434in"}
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image7.png){width="3.0960542432195974in"
> height="3.554728783902012in"}
>
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image8.png){width="3.1687904636920385in"
> height="3.6448884514435695in"}
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image9.png){width="3.225300743657043in"
> height="3.6815627734033245in"}
>
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image10.png){width="3.953520341207349in"
> height="4.568513779527559in"}

5.  Explore the \"General\", \"Recovery\", and \"Log On\" tabs to
    understand additional service settings.

6.  Create a batch file that will be added as a new service later on.
    Refer to the batch file code below.

> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image11.png){width="4.808325678040245in"
> height="2.0055664916885387in"}

7.  Save the batch file in Z:\\lastname_timer.bat

8.  Use the sc command to add timer.bat service in the command line
    interface.

> *sc create BatchTimerService binPath= \"path_to_your_batch_file.bat\"
> start= auto*
>
> *net start BatchTimerService*
>
> **sc create BatchTimerService binPath= "Z:/elec_timer.bat"
> start=auto**

9.  Verify that BatchTimerService has been added to the services.

> **SS:\
> **![](vertopal_2afcedfa32744466beb570586382d8c1/media/image12.png){width="7.027083333333334in"
> height="0.5777777777777777in"}
>
> ![](vertopal_2afcedfa32744466beb570586382d8c1/media/image13.png){width="5.323659230096238in"
> height="0.3854702537182852in"}

10. **Testing the Service:** Now, if you open a new command prompt, you
    should see the timer countdown without requiring your interaction.
    Once the timer finishes, you\'ll see the \"Timer finished!\"
    message.

> **SS:\
> **![](vertopal_2afcedfa32744466beb570586382d8c1/media/image14.png){width="4.583973097112861in"
> height="2.917073490813648in"}

**Rubric**

  ---------------------------------------------------------------------------------------
  **Criteria**      **Excellent       **Good (7)**    **Needs          **Unsatisfactory
                    (10)**                            Improvement      (1)**
                                                      (3)**            
  ----------------- ----------------- --------------- ---------------- ------------------
  Understanding of  Demonstrates a    Shows a solid   Has a basic      Shows little or no
  Services          deep              understanding   understanding of understanding of
                    understanding of  of services,    services, but    services.
                    the concept of    but may lack    may struggle     
                    services, their   some depth in   with specific    
                    roles, and their  specific areas. concepts.        
                    importance in                                      
                    Windows.                                           

  Service           Successfully      Demonstrates    Can perform      Struggles to
  Management Skills starts, stops,    proficiency in  basic service    perform even basic
                    restarts, and     managing        management       service management
                    configures        services, but   tasks, but may   tasks.
                    services using    may encounter   need assistance  
                    the Services app. minor           or guidance.     
                                      difficulties.                    

  Custom Service    Successfully      Can create a    Has limited      Cannot create a
  Creation          creates and       custom service, experience with  custom service.
                    manages a custom  but may         creating custom  
                    service using the encounter minor services.        
                    appropriate tools difficulties or                  
                    and techniques.   require                          
                                      assistance.                      

  Problem-Solving   Demonstrates      Can effectively May require      Struggles to
                    strong            troubleshoot    assistance to    troubleshoot and
                    problem-solving   and resolve     troubleshoot     resolve issues.
                    skills when       most issues     some issues.     
                    encountering      related to                       
                    challenges or     service                          
                    errors.           management.                      

  Documentation and Provides clear    Documents the   Provides basic   Does not provide
  Reporting         and concise       lab activities  documentation,   any documentation
                    documentation of  adequately, but but may be       or reporting.
                    the lab           may lack some   disorganized or  
                    activities,       detail or       incomplete.      
                    including         clarity.                         
                    relevant                                           
                    screenshots and                                    
                    observations.                                      

  **Score:**        **/50**                                            
  ---------------------------------------------------------------------------------------