
# Railway Performance Analysis.

## Table of Content
- [Problem statement](#problem-statement)
- [Workflow](#workflow)
- [About the Dataset](#about-the-dataset)
- [Data Model](#data-model)
- [Dashboard View](#dashboard-view)
- [Visualization Representation](#visualization-representation)
- [Insights Derived](#insights-derived)

## Problem Statement

The objective is to conduct a comprehensive analysis of the overall performance of the top 5 train types and 4 major railway stations in India. This analysis aims to provide actionable insights into key performance indicators (KPIs). By leveraging Power BI, the goal is to present a visually intuitive and interactive dashboard that facilitates informed decision-making for optimizing the performance of both train types and railway stations, contributing to the enhancement of the overall efficiency and user experience within the Indian railway network.


## Workflow

- The project began with cleaning and transforming the dataset using Power Query.
- Data modeling involved connecting dimension and fact tables in a star schema, creating one-to-many relationships between the tables. A date lookup column was created and connected to the required table's column.
- Key measure columns were created using DAX to visualize key performance metrics for monitoring railway performance.
- Dashboard creation involved developing multiple visuals.
## About the Dataset

1. **Station_Lookup:** A dimension table with four columns

- Station ID: Unique identifiers for individual stations.
- Station Name: Names of individual stations.
- Station Location: Location of different stations.
- Capacity: The capacity of each station, representing the number of persons it can handle in a day.
2. **Train_Lookup:** Another dimension table with four columns

- Train ID: Unique identifiers for particular trains.
- Train Type: Names of different train types available in the dataset.
- No of Coaches: The number of coaches available in each train.
- Average per Seat Price: Average price for which tickets are offered.
3. **Ticket Sales Data:**  A fact table with four columns

- Train ID: Similar to the Train Lookup Table.
- Date: The date on which the ticket was purchased.
- Number of Ticket Sold: The number of tickets sold.
- Station ID (Departure): The unique ID of the station from which the train left for its destination.

4. **Train Performance Data:**  Another fact table with four columns

- Train ID: Similar to the Train Lookup Table.
- Date: Date of the train performance data.
- On-Time Arrival: Binary values (0 or 1) indicating whether the train arrived on time or not.
- Passenger Satisfaction: Ratings from 1 to 5, where 1 represents unsatisfied and 5 represents satisfied passengers.

## Data Model
<p align="center">
  <img src="images/Screenshot 2024-01-23 224829.png" />
</p>



## Dashboard View

<p align="center">
  <img src="images/Screenshot 2024-01-23 224705.png"/>
</p>


## Visualization Representation
- **Cards:** Total revenue earned, total stations covered, different stations covered.
- **Donut Chart:** % of train traffic at different railway stations by station name, % wise revenue earned by train type.
- **Stacked Column Chart:** On-Time Arrival vs. Late Arrival by train type.
- **Stacked Bar Chart:** Satisfaction by train type.
- **Map:** % of revenue earned location-wise.
- **Filter:** Date-wise slicer.


## Insights Derived

- Total revenue earned is Rs 1.5 billion by trains in general, with an average of 4 stations covered by each train, and different stations covered are 5.

- % train traffic chart shows that all four stations hold nearly the same amount of traffic.

- % wise revenue earned according to the train type indicates that Rajdhani Express generates the maximum revenue at 30%, while Garib Rath Express generates the minimum profit at 9.94%.

- Stacked column chart (On-Time Arrival vs. Late Arrival) reveals that Vande Bharat Express is consistently on time (84 times), while Duronto Express has the highest instances of late arrival (41 times).

- Satisfaction by train type chart shows Garib Rath and Vande Bharat Express with the maximum satisfaction at 64%, and the least satisfaction is shown by Shatabdi Express at 56.57%.

- The map indicates that Delhi shows the highest % of revenue earned at 25.72%, while Kolkata shows the lowest % at 24.32%.

- The line chart (Revenue Earned over time) shows that Quarter 4 has the highest profit, with December contributing the highest revenue in 2022. Quarter 3 has the lowest revenue, with July performing poorly. Out of all the months in 2022, February has the lowest revenue collection.