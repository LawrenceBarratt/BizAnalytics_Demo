# How to Demonstrate Logistics Container Tracking in Dynatrace

## What Value This Shows in the Dynatrace Platform
- **Logistics Monitoring**: Full visibility into container transportation processes.
- **Dynatrace Platform Dashboards**: Detailed dashboards showing every step in the logistics workflow.
- **Dynatrace Workflows**: Automated tracking of container journeys with Dynatrace workflows.
- **Dynatrace Query Language (DQL)**: Query container data for KPIs and insights.

## Overview of Logistics Container Tracking

The logistics container tracking solution leverages the Dynatrace platform to provide comprehensive monitoring of container operations across multiple steps, using data from various sources, including IoT sensors, GPS tracking, and logistics platforms.

![Workflow Execution](file-j3AKsyo8iCqUCz9gx0DMtQLx)

With a single workflow trigger, Dynatrace tracks container journeys from booking to final delivery, collecting data at each step to identify potential issues and optimize operations.

---

## High-Level Overview of Tracking Flow

- **12-Step Process**: From container booking to delivery and return.
- **Data Collection**: Each step is monitored using different data sources (e.g., SAP TM, IoT, GPS).
- **Error Detection**: Errors are logged and tracked in real-time, allowing for immediate insights into potential failures.

### Example Process Breakdown:
- **Booking**: Time taken for the container booking.
- **Allocation**: Efficiency in container allocation.
- **Transport**: Container pickup and delivery, tracked via GPS.
- **Sea Transit**: Transit duration and delays at sea.
- **Return**: Delivery and container return, ensuring completeness of operations.

---

## Dynatrace Dashboards: Visualizing Key Metrics

Three dashboards are available for visualizing container tracking metrics, split into groups of steps (Steps 1-4, Steps 5-8, and Steps 9-12). These dashboards track various metrics like booking time, pickup time, loading efficiency, and more.

### Dashboard 1: Steps 1-4 (Booking, Allocation, Collection, and Inspection)

This dashboard provides insights into the first four steps of the container journey, tracking metrics such as:
- **Booking Time**
- **Allocation Efficiency**
- **Pickup Time**
- **Inspection Efficiency**

![Steps 1-4 Dashboard](file-kolcUDojK2k13wMup3jOsqMG)

---

### Dashboard 2: Steps 5-8 (Loading, Sealing, and Port Operations)

This dashboard focuses on the middle steps of the journey, including loading goods, sealing containers, and transporting to the port:
- **Loading Time**
- **Sealing Time**
- **Transport to Port**
- **Loading to Ship**

![Steps 5-8 Dashboard](file-8qhnVKNtP54iclzKUALXI2jZ)

---

### Dashboard 3: Steps 9-12 (Sea Transit, Unloading, and Delivery)

The final dashboard covers the transit and delivery phases, showing key metrics for:
- **Sea Transit**
- **Unloading at Destination Port**
- **Transport to Warehouse**
- **Delivery and Return**

![Steps 9-12 Dashboard](file-DKCwgC1EuuPDeOZsxyXIFI13)

---

## Additional Insights: Logistics Notebook

The **Logistics Notebook** provides deep insights into the cost of containers at various ports, revenue loss, and savings opportunities, offering valuable data for optimizing logistics costs.

- **Container Cost at Ports**
- **Revenue Loss**
- **Empty Container Costs**

![Logistics Notebook](file-pwzoiDiDCB8BU2CyBTUdN3z5)

---

## Prerequisites

Before starting, ensure the following:

1. **Install Workflow**: Upload the workflow JSON file to your Dynatrace tenant.
2. **Install Dashboards**: Upload all dashboard JSON files.
3. **Enable Data Collection**: Ensure you have set up Dynatrace for IoT, GPS, and REST API data collection.

## How to Set Up and Run the Workflow

### Step 1: Upload the Workflow

1. Navigate to **Workflows** in your Dynatrace tenant.
2. Click **Upload** and select the workflow JSON file.
3. Execute the workflow manually using an **On-Demand Trigger** or schedule it for periodic execution.

### Step 2: Upload Dashboards

1. Navigate to **Dashboards** in your Dynatrace tenant.
2. Click **Upload** and select the corresponding dashboard JSON files (for Steps 1-4, Steps 5-8, and Steps 9-12).
3. View the dashboards to monitor key logistics metrics in real-time.

### Step 3: Run the Workflow

1. Trigger the workflow via **On-Demand Trigger** to simulate container journeys.
2. Monitor the dashboards to observe the progression through the steps.
3. Review metrics like booking time, allocation efficiency, transport times, and more.

---

## Repository Contents

- **Workflow**: Automates container tracking and generates business events for analysis.
- **Dashboards**: Visualize business analytics for container tracking, errors, and incidents.
- **Logistics Notebook**: Provides detailed analysis of container costs, revenue loss, and savings.

---

## Key Metrics Tracked:

1. **KPIs**: Booking Time, Pickup Time, Loading Time, Transport Time, and more.
2. **Errors and Incidents**: Tracks issues detected in each step.
3. **Revenue Metrics**: 
   - **Container Revenue**: Revenue generated for each container.
   - **Revenue Lost**: Revenue lost due to errors or delays.
4. **MTTD/MTTI/MTTR**: 
   - **MTTD**: Mean Time to Detect issues.
   - **MTTI**: Mean Time to Investigate issues.
   - **MTTR**: Mean Time to Resolve issues.

## Conclusion

With Dynatrace's integrated workflow and dashboards, the Logistics Container Tracking solution provides a complete overview of container journeys, helping you make informed decisions based on real-time data,
