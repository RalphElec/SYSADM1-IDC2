+----------------------------------+------------------------+----------+
| ![](vertopal_                    |                        |          |
| 91fc329de6f84b628539d587ad03daea |                        |          |
| /media/image1.png){width="2.4in" |                        |          |
| height="0.5881944444444445in"}   |                        |          |
|                                  |                        |          |
| SCHOOL OF INFORMATION AND        |                        |          |
| TECHNOLOGY                       |                        |          |
+----------------------------------+------------------------+----------+
| NAME: ELEC, Ralph Luis G.\       | DATE PERFORMED:        | /50      |
| TALUSIG, Nikos A.                | 11/28/2024             |          |
+----------------------------------+------------------------+----------+
| Section:IDC2                     | DATE SUBMITTED:        |          |
|                                  | 12/03/2024             |          |
+----------------------------------+------------------------+----------+

# SYSADM1 -- Capacity Management & Planning

## Part 1. A Simulated Dataset for Capacity Planning Exercise {#part-1.-a-simulated-dataset-for-capacity-planning-exercise .list-paragraph}

![](vertopal_91fc329de6f84b628539d587ad03daea/media/image2.png){width="4.749564741907261in"
height="2.4791666666666665in"}**Scenario:** A mid-sized e-commerce
website is expecting a significant surge in traffic due to an upcoming
holiday sale.

### [Projected Traffic Increase]{.underline}

-   **Expected Peak Traffic:** 5x the normal peak traffic

-   **Peak Time:** 12:00 PM - 3:00 PM on the sale day

### [System Specifications]{.underline}

-   **Server Count:** 5

-   **CPU Cores per Server:** 8

-   **RAM per Server:** 32GB

-   **Network Bandwidth per Server:** 1Gbps

### [Additional Considerations]{.underline}

-   **New Product Launch:** A highly anticipated product will be
    released during the sale.

-   **Marketing Campaign:** A major marketing campaign will be launched
    to promote the sale.

-   **Potential Cyber Threats:** Increased traffic can attract malicious
    actors.

Tasks:

1.  Review the provided server performance data and identify potential
    bottlenecks

2.  Brainstorm possible solutions to address the identified bottlenecks.
    Propose potential solutions considering hardware and software-based
    solutions.

3.  Discuss the pros and cons of each proposed solution by filling out
    the table below.

+-------------+---------------+------------+--------------+-----------+
| Proposed    |               | Cost       | Complexity   | Potential |
| Solution    | ------------- |            |              | impact on |
|             |   Pros   Cons |            |              | system    |
|             |               |            |              | pe        |
|             | ------ ------ |            |              | rformance |
|             |               |            |              |           |
|             |               |            |              |           |
|             | ------------- |            |              |           |
+=============+===============+============+==============+===========+
+-------------+---------------+------------+--------------+-----------+

Grading Rubric:

  -------------------------------------------------------------------------------
  Criteria           Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                            4pts
  ------------------ ------------------ ------------------- ---------------------
  **Problem          Accurately         Identifies the main Identifies a problem
  Identification**   identifies the     problem and         but lacks clarity or
                     primary problem    provides a basic    accuracy.
                     and provides a     explanation.        
                     detailed                               
                     explanation.                           

  **Solution         Proposes multiple  Proposes one or two Proposes a solution
  Proposal**         relevant solutions relevant solutions  but lacks feasibility
                     and provides       but lacks detailed  or relevance.
                     detailed           explanation.        
                     explanations,                          
                     including                              
                     potential                              
                     drawbacks and                          
                     benefits.                              

  **Evaluation of    Provides a         Provides a basic    Does not evaluate the
  Solutions**        thorough           evaluation of the   proposed solutions or
                     evaluation of the  proposed solutions, provides a
                     proposed           but lacks depth.    superficial
                     solutions,                             evaluation.
                     considering                            
                     factors like cost,                     
                     complexity, and                        
                     potential impact.                      

  Score:                                                    /30
  -------------------------------------------------------------------------------

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

**IMPROVED NETWORK:**

> ![](vertopal_91fc329de6f84b628539d587ad03daea/media/image3.png){width="7.275339020122485in"
> height="3.875042650918635in"}\
> In the improved topology, key potential bottlenecks include the
> dependence on the 3560 Multilayer Switch and Edge Routers for
> inter-VLAN and internet-bound traffic, as these components centralize
> data flow. While redundancy has been introduced via the primary and
> standby edge routers, the connections between the VLAN-specific
> switches (e.g., VLAN 10, VLAN 20, etc.) and the core devices may
> experience congestion during peak usage due to the limited uplink
> bandwidth. Furthermore, security risks such as unauthorized access or
> VLAN hopping persist without robust configurations like Access Control
> Lists (ACLs) and port-based security.\
> \
> To ensure scalability and optimal performance, it is recommended to
> upgrade the core switches to higher-capacity devices supporting
> multi-gigabit links and implement Link Aggregation Protocol (LACP) for
> increased bandwidth on uplinks. Introducing software-defined
> networking (SDN) can enhance traffic management and resource
> allocation dynamically. Additionally, inter-VLAN routing can be
> improved by enabling Layer 3 routing capabilities on all distribution
> switches, reducing the dependency on the core for routing. While these
> upgrades might increase initial costs, the benefits include better
> fault tolerance, reduced congestion, and improved security---essential
> for supporting growing user demands and new applications in the
> network.

  ------------------------------------------------------------------------------
  Criteria          Excellent \| 10pts Good \| 7pts        Needs Improvement \|
                                                           4pts
  ----------------- ------------------ ------------------- ---------------------
  **Network         Accurately         Identifies key      Identifies some basic
  Analysis**        identifies         network components  network components
                    potential          and some potential  but lacks a
                    bottlenecks,       bottlenecks.        comprehensive
                    security risks,                        analysis.
                    and capacity                           
                    limitations.                           

  **Scalability     Proposes multiple  Proposes some       Proposes limited
  Planning**        relevant solutions relevant            scalability
                    and provides       scalability         strategies.
                    detailed           strategies but      
                    explanations,      lacks detail.       
                    including                              
                    potential                              
                    drawbacks and                          
                    benefits.                              

  **Evaluation of   Proposes           Provides a basic    Does not evaluate the
  Solutions**       comprehensive      evaluation of the   proposed solutions or
                    scalability        proposed solutions, provides a
                    strategies,        but lacks depth.    superficial
                    including specific                     evaluation.
                    recommendations                        
                    for hardware                           
                    upgrades, software                     
                    configurations,                        
                    and network                            
                    optimizations.                         

  **Proposed        Provides a         Provides a basic    Does not provide a
  Design**          detailed and       design but lacks    clear and detailed
                    well-justified     specific details    design.
                    design, including  and justifications. 
                    network diagrams,                      
                    configuration                          
                    details, and                           
                    implementation                         
                    plans.                                 

  **Evaluation and  Provides a         Provides a basic    Does not evaluate the
  Justification**   thorough           evaluation of the   proposed solutions or
                    evaluation of the  proposed solutions, provides a
                    proposed           but lacks depth.    superficial
                    solutions,                             evaluation
                    considering                            
                    factors like cost,                     
                    complexity, and                        
                    potential impact.                      

  Score:                                                   /50
  ------------------------------------------------------------------------------
