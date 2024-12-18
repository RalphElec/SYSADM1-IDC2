![image](https://github.com/user-attachments/assets/ab8cce58-a03f-46e6-9a34-2c46d770b3fc)


# SYSADM1 -- Capacity Management & Planning

## Part 1. A Simulated Dataset for Capacity Planning Exercise {#part-1.-a-simulated-dataset-for-capacity-planning-exercise .list-paragraph}

![image](https://github.com/user-attachments/assets/c240ef06-aecb-4d55-8afe-dcf8dac82242)


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

![image](https://github.com/user-attachments/assets/97a50250-7b99-4862-a712-150a37013580)


Grading Rubric:

  ------------------------------------------------------------------------------
  Criteria           Excellent \| 10pts Good \| 7pts       Needs Improvement \|
                                                           4pts
  ------------------ ------------------ ------------------ ---------------------
  **Problem          Accurately         Identifies the     Identifies a problem
  Identification**   identifies the     main problem and   but lacks clarity or
                     primary problem    provides a basic   accuracy.
                     and provides a     explanation.       
                     detailed                              
                     explanation.                          

  **Solution         Proposes multiple  Proposes one or    Proposes a solution
  Proposal**         relevant solutions two relevant       but lacks feasibility
                     and provides       solutions but      or relevance.
                     detailed           lacks detailed     
                     explanations,      explanation.       
                     including                             
                     potential                             
                     drawbacks and                         
                     benefits.                             

  **Evaluation of    Provides a         Provides a basic   Does not evaluate the
  Solutions**        thorough           evaluation of the  proposed solutions or
                     evaluation of the  proposed           provides a
                     proposed           solutions, but     superficial
                     solutions,         lacks depth.       evaluation.
                     considering                           
                     factors like cost,                    
                     complexity, and                       
                     potential impact.                     

  Score:                                                   /30
  ------------------------------------------------------------------------------

**Part 2. Network Scalability Analysis**

Recall the e-commerce website scenario we discussed earlier. Given the
expected surge in traffic, analyze the provided network topology
diagram. Identify potential bottlenecks and areas where scalability
might be a concern. Propose specific strategies to improve the
network\'s scalability and performance to ensure a seamless user
experience during the peak traffic period. Consider factors such as
increased user demand, new applications, and security threats.

**[Problems:]{.underline}**

1.  **Single ISP Dependency**

    -   A single point of failure for internet connectivity. If the ISP
        experiences an outage, the entire network will lose access to
        the internet.

2.  **Lack of Redundancy in Core Switch and Edge Routers**

    -   Any failure in the core switch or edge router will result in a
        total network outage, severely impacting business continuity.

3.  **Limited Scalability**

    -   Adding more devices in the future will be challenging due to the
        current network design, requiring substantial reconfiguration or
        hardware upgrades.

4.  **Potential Bottleneck**

    -   A single core switch and single-port connections increase the
        risk of network congestion during traffic surges, degrading
        performance for users.

5.  **Shared VLAN**

    -   Without VLAN segmentation and security measures like Access
        Control Lists (ACLs), the network lacks isolation between
        servers, making it prone to unintended access and lateral
        movement during breaches.

6.  **Security Risks**

    -   The absence of explicit security measures (e.g., firewalls,
        ACLs) leaves the network open to attacks such as Distributed
        Denial of Service (DDoS) and unauthorized access.

Addressing these issues will require implementing redundancy, improving
scalability, segmenting VLANs, and adding robust security protocols to
ensure a reliable and secure network infrastructure.

**[Proposed Network and Improvements]{.underline}**

The improved topology resolves many of the identified problems in the
original network design.

1.  **Single ISP Dependency**

    The topology includes two Edge Routers (Primary and Standby)
    connected to two ISPs. This ensures redundancy at the ISP level. If
    one ISP link or router fails, the other can take over, eliminating
    the single point of failure for internet connectivity.

**Estimated Costs**:

-   ISP redundancy (annual cost): **PHP 280,000--1,120,000**

-   Additional edge router: **PHP 112,000--280,000**

2.  **Lack of Redundancy in Core Switch and Edge Routers**

The topology now features two multilayer core switches (3560-24PS)
interconnected, providing failover capabilities. Two edge routers
(primary and standby) are deployed, further improving fault tolerance.
If one fails, the other ensures continuous network operation.

**Estimated Costs**:

-   Core switch (per unit): **PHP 168,000--448,000**

-   Edge router: **PHP 112,000--280,000**

3.  **Limited Scalability**

The design includes multiple 2960 switches across VLANs. These switches
are connected to the core switches, enabling scalability. The layout
allows for easy addition of more switches or devices without remaking
the network architecture.

Dynamic configurations, such as DHCP, will be implemented to enhance
scalability, eliminating the need for manual configuration when adding
new devices.

**Estimated Costs**:

-   Layer 2 switches (per unit): **PHP 8,540**

-   DHCP setup and configuration: **PHP 15,800**

4.  **Potential Bottleneck**

```{=html}

```
-   The switches are connected using multiple links, preventing
    single-port congestion.

-   Devices are evenly distributed across VLANs, reducing traffic load
    on any single switch.

-   The inclusion of redundant uplinks between switches and the core
    reduces the likelihood of traffic bottlenecks.

-   Addition of load balancing to avoid traffic congestion on the
    multi-layer switches.

**Estimated Costs**:

-   Load balancer: **PHP 75,000**

-   Redundant uplinks: **PHP 12,000 -- PHP 20,000**

5.  **Shared VLAN**

```{=html}

```
-   VLAN segmentation has been implemented effectively, with VLANs
    clearly labeled (e.g., VLAN 10, VLAN 20, VLAN 30, etc.) for specific
    server and device groups.

-   This separation ensures that devices and servers only interact as
    intended, reducing unintended communication.

-   Security measures such as ACLs can be applied to control access
    between VLANs.

**Estimated Costs**:

-   VLAN segmentation: **PHP 0--28,000 (mainly tasks)**

6.  **Security Risk**

```{=html}

```
-   The inclusion of *5506-X ASA firewalls* ensures that the network is
    protected from external threats like DDoS attacks and unauthorized
    access.

-   VLAN segmentation adds another layer of internal security by
    isolating traffic.

-   The redundant setup and structured architecture allow for more
    efficient deployment of ACLs and firewall policies to protect
    sensitive data.

**Estimated Costs**:

-   Firewalls (per unit): **PHP 75,320**

**Overall Assessment**

The new topology addresses the original design's shortcomings by
implementing redundancy, improving scalability, enhancing traffic
handling, and reinforcing network security. It's a well-rounded,
fault-tolerant design suitable for a robust enterprise network.

**IMPROVED NETWORK:**

![image](https://github.com/user-attachments/assets/4227eb1a-3ab6-4a83-8102-3d0f014e6b9c)

![image](https://github.com/user-attachments/assets/1d251876-56b7-4428-af4f-9b521c470bb0)

