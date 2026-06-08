GROUP PROJECT OF DISTRIBUTED COMPUTING SYSTEMS 

RESPECTIVELY MADE FOR OUR BEAUTIFUL LECTURER, ASSOC. PROF. DR. WAN NOR SHUHADAH BINTI WAN NIK

## Project Title

Distributed System Simulation on Unisza.edu.my using Naming Service such as SPB, Kelip, Portal, Multithreading and Data Replication

## Project Description

This project simulates a distributed computing system using Python. The simulation demonstrates three core distributed system concepts:

1. Structured Naming Service
2. Multithreaded Request Processing
3. Data Replication with Eventual Consistency

The naming service resolves human-readable service names into network addresses. Multiple threads are used to simulate concurrent client requests, while replicated nodes synchronize data updates using an eventual consistency model.

---

## Project Structure

```text
project/
│
├── naming_service.py
├── server_node.py
├── replica_manager.py
└── main.py
```

### Module Description

#### naming_service.py

Contains the structured naming table and name resolution functionality.

#### server_node.py

Handles service lookup requests and measures lookup latency.

#### replica_manager.py

Manages replica synchronization and replication delays.

#### main.py

Coordinates the simulation, starts threads, collects performance metrics, and displays results.

---

## Software Requirements

* Python 3.x
* Google Colab or Visual Studio Code

Required Python Libraries:

* threading
* time
* random

No external packages are required.

---

## How to Run

### Google Colab

1. Create the following files:

   * naming_service.py
   * server_node.py
   * replica_manager.py
   * main.py

2. Copy the provided source code into each file.

3. Execute the simulation:

```python
!python main.py
```

### Visual Studio Code

Open a terminal in the project folder and run:

```bash
python main.py
```

---

## Expected Output

The simulation displays:

* Service name resolution results
* Replica synchronization updates
* Lookup latency values
* Replication delay values
* Average lookup latency
* Average replication delay
* Final replica values
* Success rate

Example:

```text
service1.unisza.edu.my resolved to 192.168.1.10:5000
Replica A updated to 2 after 307.05 ms

Average Lookup Latency: 105.54 ms
Average Replication Delay: 225.98 ms

Final Replica Values:
{'A': 2, 'B': 2, 'C': 2}

Success Rate: 100%
```

---

## Consistency Model

This simulation implements Eventual Consistency.

Updates are propagated to replicas asynchronously. Although replicas may receive updates at different times, all replicas eventually converge to the same final value.

---

## Performance Metrics

The following metrics are collected:

1. Lookup Latency

   * Time required to resolve a service name.

2. Replication Delay

   * Time required to synchronize data between replicas.

3. Success Rate

   * Percentage of successful service resolutions.

---

## Conclusion

The simulation demonstrates how distributed systems perform name resolution, process concurrent requests using multithreading, and maintain replicated data using eventual consistency. The modular implementation improves readability and maintainability while providing a practical demonstration of distributed computing concepts.
