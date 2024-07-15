# Event Tracking Management and User Analysis OLAP Platform

**Project description:** 
- Implement event tracking management, auto testing and monitoring modules to manage events life cycle and realize data governance. Manage 5 business lines with 40k events and 230 monthly average users.
- Using clickhouse OLAP with advanced data structure like linked list and directed graph to instantly analyze daily tens of billions of events data, design asynchronous, routing engine, partitioning and other methods to improve query efficiency by 30%, monthly average users 90.



### 1. Event Tracking Management

<img src="images/event/manage.jpg?raw=true"/>

- Frame Design: Promote event tracking framework optimization, unified management of global properties and events, and improve events development efficiency and quality.
- Event Manage: Implement events management module, covering the whole process from the generation of requirements to the implementation, and link to auto-testing and monitoring modules to improve the events quality.
- Event Autotest: Build the auto-testing function, and summarize test cases based on historical bugs, covering 4 scenarios with a 50% test cases coverage rate and 30% improvement in testing efficiency.
- Event Monitor: Establish scheduling to monitor the quality of tracking events, implement status to show the health of the events,  and send alert emails to the responsible person regularly.
  

### 2. User Analysis OLAP
<img src="images/event/user.jpg?raw=true"/>

- Event Analysis: Establish events action analysis function, support flexible dimensions combination to visualize pv, uv and duration time, and improve the efficiency of product function analytics.
- User Behavior: Implement single user path visualization function, and combine with commodity data to present browsing events, help customer service badcase analysis efficiency increased by 30%.
- Sankey Path: Build the function to depict the session flow, present the nodes and links of actions mapping relationship by using sankey diagram intuitively, and help UED optimize visitor experience.
- Funnel Analysis: Establish funnel exploration function to visualize users steps to a task, support open or closed toggle and multi-dimensional analysis, and improve the path to conversion.




