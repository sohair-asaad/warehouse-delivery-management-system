Warehouse & Delivery Management System (C++)
An event-driven simulation of a Warehouse & Delivery Management System built in C++. The simulator processes customer orders, manages multi-warehouse inventory, schedules and assigns vehicles/drivers, dispatches shipments, and tracks deliveries until completion over discrete timesteps.

Features
Discrete-time, event-driven loop (order arrival, restock, dispatch, cancellation, maintenance, reroute).

VIP vs Standard handling:

VIP orders prioritized using a priority queue with a configurable scoring strategy (value/urgency/deadline).

Standard orders served using FCFS queues (global or per-destination).

Warehouse selection based on nearest feasible warehouse with sufficient inventory (with optional split fulfillment).

Vehicle assignment respecting capacity, availability, and refrigerated constraints for perishables.

Shipment lifecycle tracking with timestamps (RT, AT, DT, FT) and KPI computation (waiting time, transit time, utilization, on-time rate, delivered value).

Data Structures Used
Queue for chronological events execution.

Priority Queue for VIP orders.

Queue(s) for Standard orders (FCFS).

Hash Map for inventory (ItemID → Quantity).

Lists/Queues for vehicles grouped by status.

2D matrix for travel-time between nodes.

Input / Output
Input: warehouses, vehicles, initial inventory, travel-time matrix, and a list of timed events.

Output: delivered orders sorted by finish time + aggregated statistics (counts, averages, on-time rate, vehicle utilization, etc.).

Models
Interactive mode: prints upcoming events, waiting queues, vehicle statuses, inventory snapshots, and delivered orders per timestep.

Silent mode: runs the full simulation and produces output only.

Tech
Language: C++

Paradigm: OOP (Simulator, Warehouse, Order, Vehicle, Event hierarchy)

Focus: Correct scheduling + efficient use of data structures.
