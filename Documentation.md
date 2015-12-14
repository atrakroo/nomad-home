![http://i.imgur.com/lsB8tfr.png](http://i.imgur.com/lsB8tfr.png)



# Documentation #

---



> # Table of Contents #
> 



# Description #


A community based carpooling and assistance application. It connects AUC students together using Facebook and tailor-made networks. Passengers looking for a ride can be matched with members going to and from their desired destinations or nearby locations. Private events and networks can be created so people can quickly find, join and get to where they want to be faster and easier. Students can subscribe to upcoming and trending events allowing them to carpool with event subscribers. Students can request their peers' assistance via facebook and the application's proprietary system for specific networks and get map based locations of all relevant assistance or emergency locations and their respective routes within a specified radius. Students that opt to use buses for their main mode of transportation to and from campus can also have an easier time locating where their buses are and how far they are from their respective locations and alert students if there is going to be an unexpected delay. Students can collectively save time, save money and resources. They will improve their impact on the environment by making it greener due to lower carbon emissions and together they will solve Cairo's significant traffic problem all in one simple, free app.





# Features #

> ## Carpooling ##



Students using the carpooling feature of this application will have two choices to choose from:

  * **Driver:** Students driving to and from campus choose this option; They input the time and date of their carpooling instance, they are then required to input their start and end locations. Their start location is pinpointed via GPS or typing in their address which queries the Google Maps API and displays their address onscreen via the aforementioned map. Their end location is determined by entering the address/location and is calculated using the same methods. These details are then sent to the server and are stored in a MySQL database for future passenger queries. The driver then sees a Results page with passengers that fit the given criteria; Usually passengers are matched if they are within a 5-km radius of the driver's start and end position. The driver can choose up to 3 other passenger for his/her carpooling instance, when it is finalized the passengers get notified of this available instance. This instance is started once both parties have confirmed they are ready to start. Carpooling instances have a set expiry time in case they aren't matched with passengers.

  * **Passenger:** Students that wish to use the carpooling service as passengers go through through a similar process as their driver counterparts. They input their time, date, start and end locations. This information is then cross referenced with the driver entries on the database; If there are any results that are within a 5-km radius of the passenger's start and end location. They are sent back to the user on the Results page and they can choose whichever result they see fit. When a user confirms the carpooling instance a notification is sent to the driver and upon confirmation from the driver the carpooling instance is started. If there aren't any results at the current time, the application asks the user if he/she wants to save their query in order to be notified if there are any drivers that fit their criteria in the future. If there are any, the passenger is notified of these results. However if the query remains unmatched it will expire in the same manner as driver entires.


Both the Driver and Passenger results pages show the Student's preferred network and Facebook friend results first. The rest of the community results are displayed afterwards.



> ## Assistance ##

> The assistance module allows students to communicate with their fellow peers in preferred networks or with their facebook friends in order to provide services for each other and the community. If a student needs a specific item or service provided, he/she starts the assistance module and enters the details of their request. The request gets sent to users in the networks and their Facebook friends via an API request and it gets completed once both parties acknowledge the service is concluded. Users will also have the option of knowing emergency locations such as hospitals, police stations, mechanics etc within a specific radius based on the user's location.

> ## Networks ##

> A feature that came up as inherent evolution of the application's infrastructure was the implementation of networks. When user's sign up for the application they are classified differently. Students, Faculty, Administrators have different privileges and requirements. Therefore, the development of networks was important to maintain and provide different facilities to different users. While at its core, users essentially retain the same functionality from the Network feature; not all users can influence what others have created. For example, users can create **Network Events**; this translates to users creating their carpooling instances based on a shared event or situation that affects a certain strata of users. Faculty professors can create revision session, exam and make up carpooling instances. Students in their respective courses are automatically notified and can carpool accordingly. Only faculty can edit/influence instance they create or in their appropriate domain. TAs can create instances for office hours. Different clubs can create instance for their events. AUC administration can create instances for different major university events etc.

> ## Bus Tracking ##

> Students opting to use the bus as their main mode of transportation to or from campus can use this feature to get an effectively accurate location of where their bus is. Bus drivers will be provided with an Android tablet that updates its location via GPS using the buses' onboard WiFi access point. These tablets will have a unique ID that'll be cross referenced to the name of the bus and Students or Faculty can subscribe to buses of their choice and see where their location is to be there on time as accurately as possible. Drivers can notify users subscribed to their buses about possible delays and emergency situations which would give them time to seek other forms of transportation (for example finding carpooling instances) faster.
# Account Creation #

Users go through a set up process. They log in using their AUC credentials by providing their AUC email and password, their ID and based on this information they are given their classification. They are then prompted to connect their facebook accounts. Next step includes choosing a network to subscribe to. Finally the user provides their schedule based on the AUC UMTWR scheme and they are ready to interact with the community.