# Container Tracking Workflow and Dashboards

This project demonstrates a **container tracking simulation** using a custom JavaScript script integrated into Dynatrace. The workflow simulates the journey of containers from booking to final delivery, generating business events for each stage and visualizing these through three dashboards that show the progress across multiple stages.

## Workflow Overview

The container tracking process simulates the key stages of a logistics workflow:

1. **Booking and Allocation**
2. **Collection and Inspection**
3. **Loading, Sealing, and Transportation**
4. **Sea Transit and Unloading**
5. **Final Delivery and Return**

Each step is enriched with data such as container weight, product type, errors, incident tracking, and transit times. The events are ingested into Dynatrace for monitoring and visualization using dashboards that track container movements in real-time.

### Steps Included in the Workflow

1. **Container Booking**: Track when containers are booked, allocated, and prepared for pickup.
2. **Container Allocation**: Monitors allocation and container readiness.
3. **Container Collection**: Tracks pickup from the warehouse.
4. **Container Inspection**: Simulates inspection before loading.
5. **Loading Goods**: Monitors loading, including delays.
6. **Sealing**: Ensures that the container is sealed for transport.
7. **Transport to Port**: Tracks the journey to the port.
8. **Loading onto Ship**: The container is loaded onto a vessel.
9. **Sea Transit**: Monitors transit time at sea, ship weight, and delays.
10. **Arrival at Destination Port**: Tracks unloading and crane operation at the destination.
11. **Transport to Warehouse**: Tracks transport from the port to the final warehouse.
12. **Final Delivery and Return**: Tracks delivery to the customer and return of the empty container.

## Dynatrace Integration

### Script Execution

The **JavaScript code** runs inside Dynatrace, utilizing the `businessEventsClient` to ingest business events. The script simulates the journey of containers and tracks various KPIs such as:

- **Booking and Allocation Efficiency**
- **Pickup Time**
- **Sealing Time**
- **Transit Duration at Sea**
- **Delivery Time**

**Custom Attributes** are added to each step to provide further context, such as:

- Container weight
- Product type
- Price of the container
- Ship number and port of origin/destination
- Whether the container is empty or full

The script includes **error simulation** with random delays, which is tracked and visualized in the dashboards.

### Steps Grouped in Dashboards

The steps of the workflow are split across **three Dynatrace dashboards**:

1. **Dashboard 1: Step 1-4**
    - Booking
    - Allocation
    - Collection
    - Inspection

2. **Dashboard 2: Step 5-8**
    - Loading Goods
    - Sealing
    - Transport to Port
    - Loading to Ship

3. **Dashboard 3: Step 9-12**
    - Sea Transit
    - Arrival at Destination Port
    - Transport to Warehouse
    - Final Delivery and Return

## Example Use Case

This workflow can be used by logistics companies to monitor the entire lifecycle of their container shipments. It helps ensure that:

- Containers are booked, loaded, and shipped on time.
- Delays are detected early.
- KPIs are monitored for efficiency.
- Issues like transit delays or loading errors are tracked and resolved quickly.

The visualization through Dynatrace dashboards makes it easy to keep track of all stages in real-time.
