# **Chapter III: Requirements Specification**
## **3.1. User Stories**

<p style="text-align: justify;">
  User Stories describe system requirements from the end-user perspective, prioritizing the functionality and value that each action provides. In the GlassGo project, stories were formulated based on the needs identified during the user analysis and empathy stages, with the goal of ensuring a consistent, efficient, and human-centered experience for the people interacting with the platform.
</p>

<p style="text-align: justify;">
  Each story clearly defines who the user is, what they want to achieve, and their goal. It also includes verifiable acceptance criteria that ensure compliance with the expected behavior.
</p>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="text-align: center;">Epic / Story ID</th>
    <th style="text-align: center;">Title</th>
    <th style="text-align: center;">Description</th>
    <th style="text-align: center;">Acceptance Criteria</th>
    <th style="text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="text-align: center;">E-1</td>
    <td style="text-align: center;">Order and Customer Management</td>
    <td style="text-align: justify;">
      As a system, I want to centralize authentication so that different roles can access it securely.
    </td>
    <td style="text-align: center;">N/A</td>
    <td style="text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="text-align: center;">US-1</td>
    <td style="text-align: center;">Digital Order Entry</td>
    <td style="text-align: justify;">
      As a distributor, you want to record customer orders in a digital system to have centralized control and reduce manual errors.
    </td>
    <td style="text-align: justify;">
      Given the distributor accesses the system, when a new order is entered, then the order is correctly stored with the date, customer, and total amount.
    </td>
    <td style="text-align: center;">E-1</td>
  </tr>
  <tr>
    <td style="text-align: center;">US-2</td>
    <td style="text-align: center;">Modification of Existing Orders</td>
    <td style="text-align: justify;">
      As a distributor, I want to edit the information of an active order so that I can correct errors or update data before dispatch.
    </td>
    <td style="text-align: justify;">
      Given an order with “Pending” status, when the distributor updates the order information, then the system records the changes and maintains an edit history.
    </td>
    <td style="text-align: center;">E-1</td>
  </tr>
  <tr>
    <td style="text-align: center;">US-3</td>
    <td style="text-align: center;">Deletion of Canceled Orders</td>
    <td style="text-align: justify;">
      As a distributor, I want to delete canceled orders so that the database remains organized.
    </td>
    <td style="text-align: justify;">
      Given an order with “Canceled” status, when the distributor selects the delete option, then the system removes the record and updates the list of active orders.
    </td>
    <td style="text-align: center;">E-1</td>
  </tr>
  <tr>
    <td style="text-align: center;">US-4</td>
    <td style="text-align: center;">Customer Data Management</td>
    <td style="text-align: justify;">
      As a distributor, I want to register customer information so that I can maintain contact and track orders.
    </td>
    <td style="text-align: justify;">
      Given that the distributor accesses the customer module, when customer data is entered, then the system saves the information in the database.
    </td>
    <td style="text-align: center;">E-1</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-2</td>
    <td style="padding: 10px; text-align: center;">Shipment Tracking and Monitoring</td>
    <td style="padding: 10px; text-align: justify;">
      This epic covers shipment traceability, incident logging, real-time location tracking, and delivery status management. It focuses on the distributor and the carrier <em>(Jorge)</em>.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-11</td>
    <td style="padding: 10px; text-align: center;">Start of Trip</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to record the start of the trip <strong>so that</strong> the order is marked as “In transit.”
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> an order with “Pending shipment” status, <strong>When</strong> the carrier selects “Start trip,” <strong>Then</strong> the system changes the order status to “In transit” and logs the departure time.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-12</td>
    <td style="padding: 10px; text-align: center;">Automatic Location Logging</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> the system to automatically record my location periodically <strong>so that</strong> route traceability is maintained.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the trip is in progress, <strong>When</strong> the system detects a GPS signal, <strong>Then</strong> it stores the coordinates with timestamp and associated order.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-13</td>
    <td style="padding: 10px; text-align: center;">Real-Time Map Visualization</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to visualize the carrier’s location <strong>so that</strong> I can monitor shipment status.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the order is in transit, <strong>When</strong> the distributor opens the tracking map, <strong>Then</strong> the system displays the vehicle’s real-time location.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-14</td>
    <td style="padding: 10px; text-align: center;">Impact Incident Reporting</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to record an impact or damage detected during the trip <strong>so that</strong> I can notify the distributor.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that an impact event occurs, <strong>When</strong> the carrier reports the incident, <strong>Then</strong> the system logs the event with time, location, and damage type.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-15</td>
    <td style="padding: 10px; text-align: center;">Automatic Incident Notification</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to receive an automatic alert when an incident occurs <strong>so that</strong> I can take immediate action.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a registered impact event, <strong>When</strong> the report is confirmed, <strong>Then</strong> the distributor receives a notification on their dashboard and via email.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-16</td>
    <td style="padding: 10px; text-align: center;">End of Trip</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to record the end of the trip <strong>so that</strong> delivery completion is confirmed.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the order is “In transit,” <strong>When</strong> “End trip” is selected, <strong>Then</strong> the system updates the order to “Delivered” and records the arrival time.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-17</td>
    <td style="padding: 10px; text-align: center;">Delivery Confirmation with Photo Evidence</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to attach a photograph when confirming delivery <strong>so that</strong> I can provide proof of product condition.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the order is being delivered, <strong>When</strong> the carrier uploads an image,  <strong>Then</strong> the system saves the photo and links it to the delivered order.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-18</td>
    <td style="padding: 10px; text-align: center;">Trip History</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to view my delivery history <strong>so that</strong> I can review dates, routes, and times.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that previous trips exist, <strong>When</strong> the carrier accesses the history, <strong>Then</strong> the system displays a list with details of each delivery.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-19</td>
    <td style="padding: 10px; text-align: center;">Delay Alert Notifications</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to receive alerts when a shipment is delayed <strong>so that</strong> I can notify the customer.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that an order exceeds the estimated delivery time, <strong>When</strong> the system detects the delay, <strong>Then</strong> a notification is generated with the cause and estimated delay.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-20</td>
    <td style="padding: 10px; text-align: center;">Completed Route Report Generation</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to generate a completed trip report <strong>so that</strong> I can keep proof of fulfillment.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that a trip has ended, <strong>When</strong> the carrier requests a report, <strong>Then</strong> the system generates a document with times, route, incidents, and completed deliveries.
    </td>
    <td style="padding: 10px; text-align: center;">E-2</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-3</td>
    <td style="padding: 10px; text-align: center;">Incident and Communication Management</td>
    <td style="padding: 10px; text-align: justify;">
      This epic addresses the management of carriers, route assignment, availability control, and trip safety.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-21</td>
    <td style="padding: 10px; text-align: center;">Carrier Registration</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> an administrator, <strong>I want</strong> to register new carriers in the system <strong>so that</strong> I can assign deliveries in an organized manner.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the administrator accesses the carriers module, <strong>When</strong> the required data is entered, <strong>Then</strong> the system stores the record and confirms profile creation.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-22</td>
    <td style="padding: 10px; text-align: center;">Automatic Route Assignment</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> the system to assign routes based on proximity and availability <strong>so that</strong> delivery time is optimized.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that pending orders exist, <strong>When</strong> the system processes the assignment, <strong>Then</strong> it assigns the optimal route to an available carrier.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-23</td>
    <td style="padding: 10px; text-align: center;">Carrier Data Editing</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> an administrator, <strong>I want</strong> to update a carrier’s information <strong>so that</strong> the data remains accurate and up to date.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that a carrier is registered, <strong>When</strong> their data is edited,<strong>Then</strong> the system updates the information without losing the delivery history.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-24</td>
    <td style="padding: 10px; text-align: center;">Driver Availability Control</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to know which carriers are available <strong>so that</strong> I can assign orders based on their status.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that active carriers exist, <strong>When</strong> the distributor checks the list, <strong>Then</strong> the system displays status <em>(Available, In Transit, Resting)</em>.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-25</td>
    <td style="padding: 10px; text-align: center;">License and Document Registration</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to upload my license and required documents <strong>so that</strong> I can comply with legal requirements.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the carrier updates their profile, <strong>When</strong> documents are uploaded, <strong>Then</strong> the system validates and stores the files.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-26</td>
    <td style="padding: 10px; text-align: center;">Manual Route Assignment</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to manually assign a specific route <strong>so that</strong> I can manage exceptional cases.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that an order has no route assigned, <strong>When</strong> a manual assignment is made, <strong>Then</strong> the system records it and updates the route map.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-27</td>
    <td style="padding: 10px; text-align: center;">Planned Route Visualization</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to view my planned route before starting the trip <strong>so that</strong> I can plan time and trajectory.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the order is assigned, <strong>When</strong> the carrier views the route, <strong>Then</strong> the system displays the path with stops and total distance.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-28</td>
    <td style="padding: 10px; text-align: center;">Overload or Excess Weight Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a distributor, <strong>I want</strong> to receive alerts if an order exceeds the allowed weight <strong>so that</strong> transport damage is prevented.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that an order is being generated, <strong>When</strong> the system detects excess weight, <strong>Then</strong> it displays a warning before confirming the load.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-29</td>
    <td style="padding: 10px; text-align: center;">Automatic Distance and Estimated Time Calculation</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to know the total distance and estimated delivery time <strong>so that</strong> I can better plan my workday.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that a route is assigned, <strong>When</strong> the trip begins, <strong>Then</strong> the system displays estimated time and distance based on GPS data.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-30</td>
    <td style="padding: 10px; text-align: center;">Delivery Validation by Priority Order</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As</strong> a carrier, <strong>I want</strong> to complete deliveries in the assigned order <strong>so that</strong> the route is optimized and confusion is avoided.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the route has a defined sequence, <strong>When</strong> delivery begins, <strong>Then</strong> the system blocks out-of-order deliveries until previous ones are completed.
    </td>
    <td style="padding: 10px; text-align: center;">E-3</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-4</td>
    <td style="padding: 10px; text-align: center;">Communication and Notifications</td>
    <td style="padding: 10px; text-align: justify;">
      Focuses on the exchange of information between distributors, carriers, and customers through alerts and messaging.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-31</td>
    <td style="padding: 10px; text-align: center;">Order Confirmation Notification</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> customer, <strong>I want</strong> to receive a confirmation message when my order is accepted <strong>so that</strong> I can be assured of the process.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a registered order, <strong>When</strong> the distributor confirms it, <strong>Then</strong> the system sends an automatic notification to the customer.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-32</td>
    <td style="padding: 10px; text-align: center;">Shipping Start Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> customer, <strong>I want</strong> to receive a notification when my order is on the way <strong>so that</strong> I can prepare for delivery.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a confirmed order, <strong>When</strong> the carrier starts the trip,<strong>Then</strong> the customer receives a notification with an estimated arrival time.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-33</td>
    <td style="padding: 10px; text-align: center;">Delivery Completion Notification</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to receive a notification when the carrier completes a delivery <strong>so that</strong> I can update the order status.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> the carrier finishes the trip, <strong>When</strong> they confirm the delivery, <strong>Then</strong> the system sends an automatic confirmation to the distributor’s dashboard.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-34</td>
    <td style="padding: 10px; text-align: center;">Internal Messaging Channel</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> carrier, <strong>I want</strong> to communicate directly with the distributor <strong>so that</strong> I can report issues or ask questions.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> there is an active shipment, <strong>When</strong> the carrier sends a message, <strong>Then</strong> the distributor receives it in the internal communication panel.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-35</td>
    <td style="padding: 10px; text-align: center;">Vehicle Maintenance Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to receive automatic maintenance notifications <strong>so that</strong> I can ensure fleet availability.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a vehicle reaches its mileage limit, <strong>When</strong> the system detects this condition, <strong>Then</strong> it generates an automatic alert in the administrative dashboard.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-36</td>
    <td style="padding: 10px; text-align: center;">Pending Payment Reminders</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> customer, <strong>I want</strong> to receive automatic payment reminders <strong>so that</strong> I can avoid delays.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> an order delivered without payment, <strong>When</strong> 48 hours pass, <strong>Then</strong> the system sends a reminder to the customer’s email.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-37</td>
    <td style="padding: 10px; text-align: center;">Unread Message Report</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to know if a message was read <strong>so that</strong> I can confirm information receipt.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a notification is sent, <strong>When</strong> the recipient views it, <strong>Then</strong> the system marks the message as “Read.”
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-38</td>
    <td style="padding: 10px; text-align: center;">Mobile Push Notification Activation</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> carrier, <strong>I want</strong> to receive push notifications on my phone <strong>so that</strong> I don’t depend on email.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> the app is installed, <strong>When</strong> a relevant event occurs, <strong>Then</strong> an immediate notification is sent to the mobile device.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-39</td>
    <td style="padding: 10px; text-align: center;">Communication History Log</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to keep a historical record of
      all communications <strong>so that</strong> I can maintain internal control.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a conversation is generated, <strong>When</strong> messages are exchanged, <strong>Then</strong> the system saves the history with date, time, and users.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-40</td>
    <td style="padding: 10px; text-align: center;">Route Deviation Alert Notification</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to receive alerts if a vehicle deviates
      from the assigned route <strong>so that</strong> I can prevent incidents.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> a route is mapped, <strong>When</strong> the system detects a deviation, <strong>Then</strong> it immediately sends a notification to the control panel.
    </td>
    <td style="padding: 10px; text-align: center;">E-4</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-5</td>
    <td style="padding: 10px; text-align: center;">System Analysis and Reporting</td>
    <td style="padding: 10px; text-align: justify;">
      This epic allows generating statistics, metrics, and automated reports for decision-making.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-41</td>
    <td style="padding: 10px; text-align: center;">Delivery Report Generation</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to generate reports of completed deliveries <strong>so that</strong> I can evaluate logistic performance.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that delivery records exist, <strong>When</strong> a report is requested, <strong>Then</strong> the system generates a document with totals and compliance percentages.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-42</td>
    <td style="padding: 10px; text-align: center;">Performance Metrics Visualization</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to view performance indicators <strong>so that</strong> I can improve planning.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that shipping data exists, <strong>When</strong> the distributor accesses the dashboard, <strong>Then</strong> metrics of time, incidents, and customer satisfaction are displayed.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-43</td>
    <td style="padding: 10px; text-align: center;">Advanced Analysis Filters</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to apply filters by date, area, or carrier <strong>so that</strong> I can obtain segmented reports.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that historical data exists, <strong>When</strong> filters are applied, <strong>Then</strong> the system updates charts and tables.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-44</td>
    <td style="padding: 10px; text-align: center;">Report Export</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to export reports in PDF or Excel <strong>so that</strong> I can share them with executives.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that a report is generated, <strong>When</strong> “Export” is selected, <strong>Then</strong> the system downloads the file in the chosen format.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-45</td>
    <td style="padding: 10px; text-align: center;">Delay Pattern Detection</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to identify patterns in delays <strong>so that</strong> I can optimize routes.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that delayed deliveries exist, <strong>When</strong> an analysis is generated, <strong>Then</strong> the system highlights sections with the highest incidence.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-46</td>
    <td style="padding: 10px; text-align: center;">Critical Alerts Dashboard</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to view all active alerts on a dashboard <strong>so that</strong> I can prioritize actions.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that incidents are registered, <strong>When</strong> the panel is accessed, <strong>Then</strong> alerts are displayed by type and severity.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-47</td>
    <td style="padding: 10px; text-align: center;">Customer Satisfaction Analysis</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to know customer satisfaction levels <strong>so that</strong> I can measure service quality.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that surveys have been completed, <strong>When</strong> a report is generated, <strong>Then</strong> the system calculates an average satisfaction index.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-48</td>
    <td style="padding: 10px; text-align: center;">Generated Reports History</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to access previous reports <strong>so that</strong> I can compare results.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that prior reports exist, <strong>When</strong> the history is consulted, <strong>Then</strong> reports are listed with date and author.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-49</td>
    <td style="padding: 10px; text-align: center;">Monthly Compliance Indicator</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> distributor, <strong>I want</strong> to view my monthly delivery compliance rate <strong>so that</strong> I can evaluate progress.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that delivery data exists, <strong>When</strong> the monthly dashboard loads, <strong>Then</strong> the overall compliance percentage is displayed.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-50</td>
    <td style="padding: 10px; text-align: center;">Incidents and Damage Report</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As an</strong> administrator, <strong>I want</strong> to generate a consolidated report of incidents <strong>so that</strong> I can analyze causes and trends.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that impact events are recorded, <strong>When</strong> the report is generated, <strong>Then</strong> the system classifies incidents by type and frequency.
    </td>
    <td style="padding: 10px; text-align: center;">E-5</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-6</td>
    <td style="padding: 10px; text-align: center;">Business Web and Visitor Experience</td>
    <td style="padding: 10px; text-align: justify;">
      Stories focused on visitors to the GlassGo website and institutional communication.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-51</td>
    <td style="padding: 10px; text-align: center;">General Information Display</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to know the service description <strong>so that</strong> I understand its purpose.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor accesses the website, <strong>When</strong> they visit the “About GlassGo” section, <strong>Then</strong> they see information about the company and its objectives.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-52</td>
    <td style="padding: 10px; text-align: center;">Access to Landing Page Sections</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to navigate easily between sections <strong>so that</strong> I can explore the content.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor is on the main page, <strong>When</strong> they select a menu link, <strong>Then</strong> the system redirects them to the corresponding section.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-53</td>
    <td style="padding: 10px; text-align: center;">Contact Form</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to contact the team <strong>so that</strong> I can request additional information.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor is in the “Contact” section, <strong>When</strong> they complete and submit the form, <strong>Then</strong> the system confirms the submission and notifies the administrator.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-54</td>
    <td style="padding: 10px; text-align: center;">Success Stories Display</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to see client testimonials <strong>so that</strong> I can trust the solution.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor accesses the “Success Stories” section, <strong>When</strong> they select a testimonial, <strong>Then</strong> the system displays the client’s story and results. -->
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-55</td>
    <td style="padding: 10px; text-align: center;">Brochure Download Access</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to download a brochure <strong>so that</strong> I can review information offline.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor is on the site, <strong>When</strong> they select “Download Brochure,” <strong>Then</strong> the system correctly downloads the PDF file.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-56</td>
    <td style="padding: 10px; text-align: center;">Responsive Display on Mobile Devices</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> the site to be adaptable <strong>so that</strong> it displays correctly on any device.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor accesses the site from a mobile device, <strong>When</strong> the site loads, <strong>Then</strong> the content adjusts to the screen size.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-57</td>
    <td style="padding: 10px; text-align: center;">Quick Access to Social Media</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to access the project’s social media <strong>so that</strong> I can follow updates.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor is on the main page, <strong>When</strong> they select a social media icon, <strong>Then</strong> the system opens the corresponding link.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-58</td>
    <td style="padding: 10px; text-align: center;">Team Location Map</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to see the company’s physical location <strong>so that</strong> I can know the office address.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor is in “Contact,” <strong>When</strong> they view the map, <strong>Then</strong> the system displays the correct location using Google Maps.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-59</td>
    <td style="padding: 10px; text-align: center;">Visible Privacy Policy</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> visitor, <strong>I want</strong> to know the privacy policy <strong>so that</strong> I understand how my data is handled.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the visitor accesses the footer, <strong>When</strong> they select “Privacy Policy,” <strong>Then</strong> the system displays the full, updated text.
    </td>
    <td style="padding: 10px; text-align: center;">E-6</td>
  </tr>
</table>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">Epic / Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Acceptance Criteria</th>
    <th style="padding: 10px; text-align: center;">Related to <em>(Epic ID)</em></th>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">E-7</td>
    <td style="padding: 10px; text-align: center;">RESTful API and Technical Support</td>
    <td style="padding: 10px; text-align: justify;">
      Technical stories related to the GlassGo API.
    </td>
    <td style="padding: 10px; text-align: center;">N/A</td>
    <td style="padding: 10px; text-align: center;">N/A</td>
  </tr>
  <tr>
    <td style="padding: 10px; text-align: center;">US-60</td>
    <td style="padding: 10px; text-align: center;">Impact Data Registration via API</td>
    <td style="padding: 10px; text-align: justify;">
      <strong>As a</strong> developer, <strong>I want</strong> to register impact and location data via a POST request <strong>so that</strong> the system is updated in real time.
    </td>
    <td style="padding: 10px; text-align: justify;">
      <strong>Given</strong> that the IoT client sends valid data, <strong>When</strong> the API receives the request, <strong>Then</strong> it stores the event with its identifier and timestamp.
    </td>
    <td style="padding: 10px; text-align: center;">E-7</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>

## **3.2. Impact Mapping**

<p style="text-align: justify;">
  Impact Mapping was used as a strategic tool to connect business objectives with the expected actions and behaviors of users. This method allowed us to identify the main actors, their impact on achieving goals, and the deliverables necessary to drive those changes. In the context GlassGo, the impact map facilitated alignment between Business Goals and the requirements of the digital product, ensuring that each development directly contributes to fulfilling the project’s objectives.
</p>

<p align="center">
    <img src="../src/assets/chapter3/impact-mapping/impact-mapping.png" width="50%">
</p>

<div style="page-break-after: always;"></div>

## **3.3 Product Backlog**

<p style="text-align: justify;">
  The Product Backlog is the prioritized list of features, improvements, and technical requirements that will guide the incremental development of the GlassGo system. It was created based on the User Stories and the results of the Impact Mapping, with the purpose of structuring the development team’s work in an organized manner, aligned with user needs and business goals. Each backlog item represents a concrete feature, evaluated according to its priority and complexity, allowing for effective planning of future project iterations.
</p>

<table style="width:100%; border-collapse: collapse;">
  <tr>
    <th style="padding: 10px; text-align: center;">#Order</th>
    <th style="padding: 10px; text-align: center;">User Story ID</th>
    <th style="padding: 10px; text-align: center;">Title</th>
    <th style="padding: 10px; text-align: center;">Description</th>
    <th style="padding: 10px; text-align: center;">Story Points</th>
  </tr>
  <!-- 1 -->
  <tr>
    <td style="padding: 10px; text-align: center;">1</td>
    <td style="padding: 10px; text-align: center;">US-1</td>
    <td style="padding: 10px; text-align: center;">Digital Order Registration</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to register customer orders to have centralized control, reduce manual errors, and improve traceability.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 2 -->
  <tr>
    <td style="padding: 10px; text-align: center;">2</td>
    <td style="padding: 10px; text-align: center;">US-2</td>
    <td style="padding: 10px; text-align: center;">Order Modification</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to modify existing orders to correct errors, keep information updated, and ensure accuracy before dispatch.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 3 -->
  <tr>
    <td style="padding: 10px; text-align: center;">3</td>
    <td style="padding: 10px; text-align: center;">US-3</td>
    <td style="padding: 10px; text-align: center;">Deletion of Canceled Orders</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to delete canceled orders to keep the database clean, reduce confusion, and maintain administrative order.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 4 -->
  <tr>
    <td style="padding: 10px; text-align: center;">4</td>
    <td style="padding: 10px; text-align: center;">US-4</td>
    <td style="padding: 10px; text-align: center;">Customer Registration</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to register customer information to contact them easily, personalize deliveries, and improve customer loyalty.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 5 -->
  <tr>
    <td style="padding: 10px; text-align: center;">5</td>
    <td style="padding: 10px; text-align: center;">US-5</td>
    <td style="padding: 10px; text-align: center;">Advanced Order Search</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to search orders using filters to access information quickly, compare results, and optimize queries.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 6 -->
  <tr>
    <td style="padding: 10px; text-align: center;">6</td>
    <td style="padding: 10px; text-align: center;">US-6</td>
    <td style="padding: 10px; text-align: center;">Order Receipt Confirmation</td>
    <td style="padding: 10px; text-align: justify;">
      As a customer, I want to confirm receipt of my orders to validate their contents, reduce disputes, and maintain a reliable history.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 7 -->
  <tr>
    <td style="padding: 10px; text-align: center;">7</td>
    <td style="padding: 10px; text-align: center;">US-7</td>
    <td style="padding: 10px; text-align: center;">Order History</td>
    <td style="padding: 10px; text-align: justify;">
      As a customer, I want to view my order history to review past purchases, control expenses, and plan new orders.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 8 -->
  <tr>
    <td style="padding: 10px; text-align: center;">8</td>
    <td style="padding: 10px; text-align: center;">US-8</td>
    <td style="padding: 10px; text-align: center;">Automatic Total Calculation</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want the system to automatically calculate totals and discounts to save time, avoid errors, and issue accurate invoices.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 9 -->
  <tr>
    <td style="padding: 10px; text-align: center;">9</td>
    <td style="padding: 10px; text-align: center;">US-9</td>
    <td style="padding: 10px; text-align: center;">Stock Validation</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want the system to validate stock before registering an order to avoid overselling, ensure compliance, and improve inventory control.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 10 -->
  <tr>
    <td style="padding: 10px; text-align: center;">10</td>
    <td style="padding: 10px; text-align: center;">US-10</td>
    <td style="padding: 10px; text-align: center;">Order Export</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to export orders to PDF or Excel to share information, generate reports, and keep a digital backup.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 11 -->
  <tr>
    <td style="padding: 10px; text-align: center;">11</td>
    <td style="padding: 10px; text-align: center;">US-11</td>
    <td style="padding: 10px; text-align: center;">Start of Trip</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to record the start of the trip to update the status, generate traceability, and maintain logistical control.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 12 -->
  <tr>
    <td style="padding: 10px; text-align: center;">12</td>
    <td style="padding: 10px; text-align: center;">US-12</td>
    <td style="padding: 10px; text-align: center;">Automatic Location Logging</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want my location to be recorded automatically to save time, reduce errors, and guarantee tracking.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 13 -->
  <tr>
    <td style="padding: 10px; text-align: center;">13</td>
    <td style="padding: 10px; text-align: center;">US-13</td>
    <td style="padding: 10px; text-align: center;">Real-Time Map</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to visualize the carrier’s location in real time to monitor shipments, respond to incidents, and meet deadlines.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 14 -->
  <tr>
    <td style="padding: 10px; text-align: center;">14</td>
    <td style="padding: 10px; text-align: center;">US-14</td>
    <td style="padding: 10px; text-align: center;">Incident Reporting</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to report impact incidents to notify damages, activate alerts, and prevent future disputes.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 15 -->
  <tr>
    <td style="padding: 10px; text-align: center;">15</td>
    <td style="padding: 10px; text-align: center;">US-15</td>
    <td style="padding: 10px; text-align: center;">Automatic Incident Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to receive automatic alerts for incidents to react quickly, prevent losses, and protect customer relationships.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 16 -->
  <tr>
    <td style="padding: 10px; text-align: center;">16</td>
    <td style="padding: 10px; text-align: center;">US-16</td>
    <td style="padding: 10px; text-align: center;">End of Trip</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to record the end of a trip to confirm delivery, close records, and generate evidence.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 17 -->
  <tr>
    <td style="padding: 10px; text-align: center;">17</td>
    <td style="padding: 10px; text-align: center;">US-17</td>
    <td style="padding: 10px; text-align: center;">Photo Evidence</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to attach photographic evidence of deliveries to prove fulfillment, reduce disputes, and improve trust.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 18 -->
  <tr>
    <td style="padding: 10px; text-align: center;">18</td>
    <td style="padding: 10px; text-align: center;">US-18</td>
    <td style="padding: 10px; text-align: center;">Trip History</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to consult my trip history to evaluate performance, plan workdays, and review past incidents.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 19 -->
  <tr>
    <td style="padding: 10px; text-align: center;">19</td>
    <td style="padding: 10px; text-align: center;">US-19</td>
    <td style="padding: 10px; text-align: center;">Delay Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to receive delay alerts to inform customers, reschedule deliveries, and maintain transparency.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 20 -->
  <tr>
    <td style="padding: 10px; text-align: center;">20</td>
    <td style="padding: 10px; text-align: center;">US-20</td>
    <td style="padding: 10px; text-align: center;">Completed Route Report</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to generate a completed route report to document deliveries, analyze efficiency, and maintain evidence.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 21 -->
  <tr>
    <td style="padding: 10px; text-align: center;">21</td>
    <td style="padding: 10px; text-align: center;">US-21</td>
    <td style="padding: 10px; text-align: center;">Carrier Registration</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to register new carriers to assign routes, manage availability, and ensure coverage.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 22 -->
  <tr>
    <td style="padding: 10px; text-align: center;">22</td>
    <td style="padding: 10px; text-align: center;">US-22</td>
    <td style="padding: 10px; text-align: center;">Automatic Route Assignment</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want the system to assign routes automatically to reduce times, balance loads, and optimize logistics.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 23 -->
  <tr>
    <td style="padding: 10px; text-align: center;">23</td>
    <td style="padding: 10px; text-align: center;">US-23</td>
    <td style="padding: 10px; text-align: center;">Carrier Editing</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to edit carrier data to keep information updated, prevent errors, and update permissions.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 24 -->
  <tr>
    <td style="padding: 10px; text-align: center;">24</td>
    <td style="padding: 10px; text-align: center;">US-24</td>
    <td style="padding: 10px; text-align: center;">Availability Control</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to know drivers’ availability to plan deliveries, assign orders, and avoid overload.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 25 -->
  <tr>
    <td style="padding: 10px; text-align: center;">25</td>
    <td style="padding: 10px; text-align: center;">US-25</td>
    <td style="padding: 10px; text-align: center;">License Registration</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to upload my license documents to meet legal requirements, avoid penalties, and maintain trust.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 26 -->
  <tr>
    <td style="padding: 10px; text-align: center;">26</td>
    <td style="padding: 10px; text-align: center;">US-26</td>
    <td style="padding: 10px; text-align: center;">Manual Route Assignment</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to manually assign routes to handle exceptions, personalize deliveries, and maintain flexibility.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 27 -->
  <tr>
    <td style="padding: 10px; text-align: center;">27</td>
    <td style="padding: 10px; text-align: center;">US-27</td>
    <td style="padding: 10px; text-align: center;">Planned Route Visualization</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to visualize my planned route to organize stops, save fuel, and meet deadlines.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 28 -->
  <tr>
    <td style="padding: 10px; text-align: center;">28</td>
    <td style="padding: 10px; text-align: center;">US-28</td>
    <td style="padding: 10px; text-align: center;">Overload Alert</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to receive overload alerts to prevent damage, comply with regulations, and improve safety.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 29 -->
  <tr>
    <td style="padding: 10px; text-align: center;">29</td>
    <td style="padding: 10px; text-align: center;">US-29</td>
    <td style="padding: 10px; text-align: center;">Distance and Time Calculation</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to know trip distance and estimated time to plan breaks, save resources, and improve punctuality.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 30 -->
  <tr>
    <td style="padding: 10px; text-align: center;">30</td>
    <td style="padding: 10px; text-align: center;">US-30</td>
    <td style="padding: 10px; text-align: center;">Priority Delivery Order</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to deliver in priority order to maintain consistency, reduce errors, and complete optimal routes.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 31 -->
  <tr>
    <td style="padding: 10px; text-align: center;">31</td>
    <td style="padding: 10px; text-align: center;">US-31</td>
    <td style="padding: 10px; text-align: center;">Order Confirmation to Customer</td>
    <td style="padding: 10px; text-align: justify;">
      As a customer, I want to receive order confirmation to ensure reliability, register the purchase, and plan inventory.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 32 -->
  <tr>
    <td style="padding: 10px; text-align: center;">32</td>
    <td style="padding: 10px; text-align: center;">US-32</td>
    <td style="padding: 10px; text-align: center;">Shipping Start Alert</td>
    <td style="padding: 10px; text-align: justify;">
      As a customer, I want to receive an alert when my order is on the way to anticipate its arrival, avoid waiting, and improve experience.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 33 -->
  <tr>
    <td style="padding: 10px; text-align: center;">33</td>
    <td style="padding: 10px; text-align: center;">US-33</td>
    <td style="padding: 10px; text-align: center;">Delivery Completion Notification</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to receive delivery confirmation to validate fulfillment, close the order, and update reports.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 34 -->
  <tr>
    <td style="padding: 10px; text-align: center;">34</td>
    <td style="padding: 10px; text-align: center;">US-34</td>
    <td style="padding: 10px; text-align: center;">Internal Messaging Channel</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to communicate with the distributor to solve issues, coordinate deliveries, and reduce errors.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 35 -->
  <tr>
    <td style="padding: 10px; text-align: center;">35</td>
    <td style="padding: 10px; text-align: center;">US-35</td>
    <td style="padding: 10px; text-align: center;">Maintenance Alerts</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to receive maintenance alerts to schedule revisions, avoid failures, and ensure safety.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 36 -->
  <tr>
    <td style="padding: 10px; text-align: center;">36</td>
    <td style="padding: 10px; text-align: center;">US-36</td>
    <td style="padding: 10px; text-align: center;">Payment Reminder</td>
    <td style="padding: 10px; text-align: justify;">
      As a customer, I want to receive payment reminders to avoid delays, keep a clean history, and maintain benefits.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 37 -->
  <tr>
    <td style="padding: 10px; text-align: center;">37</td>
    <td style="padding: 10px; text-align: center;">US-37</td>
    <td style="padding: 10px; text-align: center;">Read Confirmation</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to know if my messages were read to confirm reception, improve communication, and plan actions.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 38 -->
  <tr>
    <td style="padding: 10px; text-align: center;">38</td>
    <td style="padding: 10px; text-align: center;">US-38</td>
    <td style="padding: 10px; text-align: center;">Mobile Push Notifications</td>
    <td style="padding: 10px; text-align: justify;">
      As a carrier, I want to receive push notifications on my mobile to respond quickly, reduce calls, and stay informed.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 39 -->
  <tr>
    <td style="padding: 10px; text-align: center;">39</td>
    <td style="padding: 10px; text-align: center;">US-39</td>
    <td style="padding: 10px; text-align: center;">Communication History</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to save communication history for auditing messages, solving conflicts, and meeting policies.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 40 -->
  <tr>
    <td style="padding: 10px; text-align: center;">40</td>
    <td style="padding: 10px; text-align: center;">US-40</td>
    <td style="padding: 10px; text-align: center;">Route Deviation Alert</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to receive alerts if a vehicle deviates to prevent losses, act quickly, and improve safety.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 41 -->
  <tr>
    <td style="padding: 10px; text-align: center;">41</td>
    <td style="padding: 10px; text-align: center;">US-41</td>
    <td style="padding: 10px; text-align: center;">Delivery Report</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to generate delivery reports to evaluate performance, detect failures, and improve processes.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 42 -->
  <tr>
    <td style="padding: 10px; text-align: center;">42</td>
    <td style="padding: 10px; text-align: center;">US-42</td>
    <td style="padding: 10px; text-align: center;">Performance Metrics</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to visualize performance metrics to analyze times, optimize routes, and make decisions.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 43 -->
  <tr>
    <td style="padding: 10px; text-align: center;">43</td>
    <td style="padding: 10px; text-align: center;">US-43</td>
    <td style="padding: 10px; text-align: center;">Advanced Filters</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to apply advanced filters to get segmented reports, compare periods, and detect patterns.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 44 -->
  <tr>
    <td style="padding: 10px; text-align: center;">44</td>
    <td style="padding: 10px; text-align: center;">US-44</td>
    <td style="padding: 10px; text-align: center;">Report Export</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to export reports to PDF or Excel to share data, store results, and maintain records.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 45 -->
  <tr>
    <td style="padding: 10px; text-align: center;">45</td>
    <td style="padding: 10px; text-align: center;">US-45</td>
    <td style="padding: 10px; text-align: center;">Delay Analysis</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to identify delay patterns to optimize routes, allocate resources, and improve efficiency.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 46 -->
  <tr>
    <td style="padding: 10px; text-align: center;">46</td>
    <td style="padding: 10px; text-align: center;">US-46</td>
    <td style="padding: 10px; text-align: center;">Critical Alerts Panel</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to view critical alerts to prioritize incidents, make quick decisions, and prevent damage.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 47 -->
  <tr>
    <td style="padding: 10px; text-align: center;">47</td>
    <td style="padding: 10px; text-align: center;">US-47</td>
    <td style="padding: 10px; text-align: center;">Customer Satisfaction</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to measure customer satisfaction to understand perceptions, fix issues, and improve loyalty.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 48 -->
  <tr>
    <td style="padding: 10px; text-align: center;">48</td>
    <td style="padding: 10px; text-align: center;">US-48</td>
    <td style="padding: 10px; text-align: center;">Report History</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to access past reports to compare periods, observe evolution, and maintain historical control.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 49 -->
  <tr>
    <td style="padding: 10px; text-align: center;">49</td>
    <td style="padding: 10px; text-align: center;">US-49</td>
    <td style="padding: 10px; text-align: center;">Monthly Compliance</td>
    <td style="padding: 10px; text-align: justify;">
      As a distributor, I want to view my monthly compliance rate to measure performance, set goals, and improve service.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 50 -->
  <tr>
    <td style="padding: 10px; text-align: center;">50</td>
    <td style="padding: 10px; text-align: center;">US-50</td>
    <td style="padding: 10px; text-align: center;">Incident Report</td>
    <td style="padding: 10px; text-align: justify;">
      As an administrator, I want to generate incident reports to detect causes, prioritize improvements, and reduce risks.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 51 -->
  <tr>
    <td style="padding: 10px; text-align: center;">51</td>
    <td style="padding: 10px; text-align: center;">US-51</td>
    <td style="padding: 10px; text-align: center;">Website General Information</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to learn about the GlassGo service to understand its purpose, evaluate benefits, and decide on contacting the team.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 52 -->
  <tr>
    <td style="padding: 10px; text-align: center;">52</td>
    <td style="padding: 10px; text-align: center;">US-52</td>
    <td style="padding: 10px; text-align: center;">Section Navigation</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to navigate easily between sections to explore content, understand the product, and stay engaged.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 53 -->
  <tr>
    <td style="padding: 10px; text-align: center;">53</td>
    <td style="padding: 10px; text-align: center;">US-53</td>
    <td style="padding: 10px; text-align: center;">Contact Form</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to contact the team to resolve questions, request a quote, and evaluate options.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 54 -->
  <tr>
    <td style="padding: 10px; text-align: center;">54</td>
    <td style="padding: 10px; text-align: center;">US-54</td>
    <td style="padding: 10px; text-align: center;">Success Stories</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to read success stories to trust the product, learn about results, and support my purchase decision.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
  <!-- 55 -->
  <tr>
    <td style="padding: 10px; text-align: center;">55</td>
    <td style="padding: 10px; text-align: center;">US-55</td>
    <td style="padding: 10px; text-align: center;">Brochure Download</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to download a brochure to review information, share it, and analyze it offline.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 56 -->
  <tr>
    <td style="padding: 10px; text-align: center;">56</td>
    <td style="padding: 10px; text-align: center;">US-56</td>
    <td style="padding: 10px; text-align: center;">Responsive Design</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want the site to be responsive to view it on any device, avoid errors, and improve the experience.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 57 -->
  <tr>
    <td style="padding: 10px; text-align: center;">57</td>
    <td style="padding: 10px; text-align: center;">US-57</td>
    <td style="padding: 10px; text-align: center;">Social Media Access</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to access social media to follow updates, strengthen connection, and share content.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 58 -->
  <tr>
    <td style="padding: 10px; text-align: center;">58</td>
    <td style="padding: 10px; text-align: center;">US-58</td>
    <td style="padding: 10px; text-align: center;">Location Map</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to see the company's location to know its office, verify trust, and plan a visit.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 59 -->
  <tr>
    <td style="padding: 10px; text-align: center;">59</td>
    <td style="padding: 10px; text-align: center;">US-59</td>
    <td style="padding: 10px; text-align: center;">Privacy Policy</td>
    <td style="padding: 10px; text-align: justify;">
      As a visitor, I want to read the privacy policy to understand data handling, trust the platform, and meet regulations.
    </td>
    <td style="padding: 10px; text-align: center;">5</td>
  </tr>
  <!-- 60 -->
  <tr>
    <td style="padding: 10px; text-align: center;">60</td>
    <td style="padding: 10px; text-align: center;">US-60</td>
    <td style="padding: 10px; text-align: center;">Impact Data API</td>
    <td style="padding: 10px; text-align: justify;">
      As a developer, I want to register impact data via API to update information, guarantee traceability, and maintain IoT synchronization.
    </td>
    <td style="padding: 10px; text-align: center;">3</td>
  </tr>
</table>

<div style="page-break-after: always;"></div>