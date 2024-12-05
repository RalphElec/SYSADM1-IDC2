![image](https://github.com/user-attachments/assets/a4f08be1-d5c9-4937-ade8-830336407cd9)


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

Problems:
1.	Single ISP Dependency
o	A single point of failure for internet connectivity. If the ISP experiences an outage, the entire network will lose access to the internet.
2.	Lack of Redundancy in Core Switch and Edge Routers
o	Any failure in the core switch or edge router will result in a total network outage, severely impacting business continuity.
3.	Limited Scalability
o	Adding more devices in the future will be challenging due to the current network design, requiring substantial reconfiguration or hardware upgrades.
4.	Potential Bottleneck
o	A single core switch and single-port connections increase the risk of network congestion during traffic surges, degrading performance for users.
5.	Shared VLAN
o	Without VLAN segmentation and security measures like Access Control Lists (ACLs), the network lacks isolation between servers, making it prone to unintended access and lateral movement during breaches.
6.	Security Risks
o	The absence of explicit security measures (e.g., firewalls, ACLs) leaves the network open to attacks such as Distributed Denial of Service (DDoS) and unauthorized access.
Addressing these issues will require implementing redundancy, improving scalability, segmenting VLANs, and adding robust security protocols to ensure a reliable and secure network infrastructure.







Proposed Network and Improvements
The improved topology resolves many of the identified problems in the original network design. 
1.	Single ISP Dependency
The topology includes two Edge Routers (Primary and Standby) connected to two ISPs. This ensures redundancy at the ISP level. If one ISP link or router fails, the other can take over, eliminating the single point of failure for internet connectivity.

Estimated Costs:
•	ISP redundancy (annual cost): PHP 280,000–1,120,000
•	Additional edge router: PHP 112,000–280,000

2.	 Lack of Redundancy in Core Switch and Edge Routers
The topology now features two multilayer core switches (3560-24PS) interconnected, providing failover capabilities. Two edge routers (primary and standby) are deployed, further improving fault tolerance. If one fails, the other ensures continuous network operation.
Estimated Costs:
•	Core switch (per unit): PHP 168,000–448,000
•	Edge router: PHP 112,000–280,000


3.	Limited Scalability
The design includes multiple 2960 switches across VLANs. These switches are connected to the core switches, enabling scalability. The layout allows for easy addition of more switches or devices without remaking the network architecture.
Dynamic configurations, such as DHCP, will be implemented to enhance scalability, eliminating the need for manual configuration when adding new devices.
Estimated Costs:
•	Layer 2 switches (per unit): PHP 8,540
•	DHCP setup and configuration: PHP 15,800

4.	Potential Bottleneck
•	The switches are connected using multiple links, preventing single-port congestion.
•	Devices are evenly distributed across VLANs, reducing traffic load on any single switch.
•	The inclusion of redundant uplinks between switches and the core reduces the likelihood of traffic bottlenecks.
•	Addition of load balancing to avoid traffic congestion on the multi-layer switches. 

Estimated Costs:
•	Load balancer: PHP 75,000
•	Redundant uplinks: PHP 12,000 – PHP 20,000

5.	Shared VLAN
•	VLAN segmentation has been implemented effectively, with VLANs clearly labeled (e.g., VLAN 10, VLAN 20, VLAN 30, etc.) for specific server and device groups.
•	This separation ensures that devices and servers only interact as intended, reducing unintended communication.
•	Security measures such as ACLs can be applied to control access between VLANs.
Estimated Costs:
•	VLAN segmentation: PHP 0–28,000 (mainly tasks)

6.	Security Risk
•	The inclusion of 5506-X ASA firewalls ensures that the network is protected from external threats like DDoS attacks and unauthorized access.
•	VLAN segmentation adds another layer of internal security by isolating traffic.
•	The redundant setup and structured architecture allow for more efficient deployment of ACLs and firewall policies to protect sensitive data.
Estimated Costs:
•	Firewalls (per unit): PHP 75,320


Overall Assessment
The new topology addresses the original design’s shortcomings by implementing redundancy, improving scalability, enhancing traffic handling, and reinforcing network security. It’s a well-rounded, fault-tolerant design suitable for a robust enterprise network. 

IMPROVED NETWORK:
![image](https://github.com/user-attachments/assets/328f2393-36f9-4330-bd3e-629b6e9dfab4)


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
