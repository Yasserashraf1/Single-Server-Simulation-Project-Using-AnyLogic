# Single-Server-Simulation-Project-Using-AnyLogic
## Overview
This project aims to simulate a Single Server Queuing System using AnyLogic software. The goal is to model and simulate the behavior of customers arriving, waiting in a queue, receiving service, and exiting the system. The simulation will help in understanding key performance indicators of the system, such as queue length, server utilization, and customer waiting times.

## Instructions
The project simulates a Single Server Queuing System and extracts important system parameters for analysis. This kind of simulation is a simple yet powerful application commonly found in the industry.
Process
* 1. Create the Model:
The model simulates customer arrivals, service times, and the overall flow through the system.
* 2. Design the Process Flowchart:
We use AnyLogic's Process Modeling Library to model the system. The following blocks were used:
* **Source**: Represents customer arrivals at the queue.
* **Queue**: Represents the waiting line for the server.
* **Delay**: Represents the time taken to serve each customer.
* **Sink**: Represents customers exiting the system after receiving service.
* **timeMeasureStart**: Marks the starting point for measuring system time.
* **timeMeasureEnd**: Marks the ending point for measuring system time.
* 3. Connect the Blocks:
We connected the blocks in a logical sequence:
  * **Source → Queue → Delay → Sink.**
*4. Configure the Blocks:
* **Source:**
  * Set arrival rate as Customer per minute.
  * The inter-arrival times follow a uniform_discr(1, 8) distribution.
* **Queue:**
  * Queue capacity is set to 15 (maximum customers allowed to wait).
* **Delay**:
  * Service times follow an exponential(1, 0) distribution, representing the average service time per customer.
* 5. Run the Simulation:
After setting up the model, we ran the simulation and observed the animation showing customers arriving, waiting, and exiting the system. The system dynamically processes customer flow through the queue and service point.

## Parameter Extraction
We used several nodes and paths to represent the physical space and movements within the model:
* **Point Node:**
Represents a single location where an agent can reside. In this case, it is used to represent the entrance and service point.
* **Path:**
Defines the movement of agents between nodes, connecting entrance, waiting room, and service point.
* **Rectangle Node:**
Represents a rectangular space where agents can wait, used to model the waiting room.

## Data Visualization:
* Bar Chart:
  * The orange bar represents cashier utilization, using the value from delay.statsUtilization.mean() as input.
  * The green bar represents the average queue length, using the value from queue.statsSize.mean() as input.
* Histogram:
* Visualizes the time spent in the system for each customer, using data from timeMeasureEnd.distribution().

## Simulation Components
* **Entrance:**
  * Type: Point Node
  * Use: Represents customers arriving at the system.
* **Waiting Room:**
  * Type: Rectangle Node
  * Use: Represents the queue or waiting area for the server.
* **Service Point:**
  * Type: Point Node
  * Use: Represents the point of service (i.e., the server or cashier).
    
## Conclusion
The simulation successfully models a Single Server Queuing System and provides insights into key system metrics, such as average queue length, server utilization, and customer time spent in the system. The use of AnyLogic's modeling tools, along with visualizations like bar charts and histograms, helps in analyzing system performance effectively.
