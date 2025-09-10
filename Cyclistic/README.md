# Case Study Project - Cyclistic

## Company Background

The marketing director of Cyclistic, a Chicago-based bicycle company, believes that the company's future success depends on maximizing the number of annual memberships. 

The marketing director established a clear goal: Design marketing strategies aimed at converting cyclists occasional into annual members. However, to do that, the marketing analyst team needs better understand how annual members and occasional cyclists differ, why cyclists
would buy a membership and how digital media might affect their marketing tactics. marketing. The marketing director and his team are interested in analyzing historical bicycle trip data from Cyclistic to identify trends.

Customers who purchase single-ride passes or all-day passes will be calls occasional cyclists. Customers who purchase annual memberships are called Cyclistic members.

## Customer Question

**1. How are annual members and occasional cyclists different in terms of bicycle use of Cyclistic?**

**2. Why would casual cyclists buy annual Cyclistic memberships?**

**3. How can Cyclistic use digital media to influence casual cyclists to become in members?**


## Business goal

Understand what differences exist in the use of Cyclistic bikes between occasional cyclists and annual members. So the marketing department could design a new marketing strategy to convert occasional cyclists into annual members.


## Dataset description

The data source provides discrete, structured and second-hand data because has been provided by Motivate International Inc., for data privacy reasons, the use of personally identifiable information of cyclists is prohibited, therefore sensitive data has been omitted.

The data model is a single fact table, without including dimension tables since at the moment it is a table with Id, start and end times of routes, latitudes and longitudes of the start and end of the route.

### Data ROCCC Schema

**R**ELIABLE – NO, are data with at least 15% of records with null data in the categorical headings of start_station_name and end_station_name. However, the times of these records have been considered since for the purpose of obtaining the descriptive statistics of the use of bicycles, categorical items are not necessary.

**O**RIGINAL – The data is NOT original or first hand, it has been compiled by Motivate International Inc..

**C**OMPREHENSIVE - The data is limited enough for the business task, so it is NOT comprehensive, we could add data such as costs and user membership limitations. It would be possible to expand the search and inform to the marketing director of Cyclistic. Desirable characteristics of the data:

    • membership prices,
    • verify if the docked bikes are used exclusively by occasional cyclists or because the data for annual members is at zero, the cost of the annual membership may not include the use of in-tub bikes.

**C**URRENT – YES, the data is updated to September 2022, current month.

**C**ITED – YES, it can be considered that the data is second hand provided by Motivate International Inc..

**Data integrity** cannot be ensured given the source as it is, however it may prompt us first to clarify the differences and trends between the two membership segments for Cyclistic.

The database is a CSV file, segmented into months, the data is from two years ago but only the immediately past twelve files have been unified into a single file that weighs approximately 289 Mb with approx. 6 million observations (records).


## Data Discovering and Visualization

### 1. How are annual members and occasional cyclists different in terms of bicycle use of Cyclistic?

The largest number of users is made up of Members cyclists (57.3%) while Casual cyclists represent the second place (42.7%).

![Casual_vs_Member](https://user-images.githubusercontent.com/56371747/204350642-80002cbf-01cf-4c2d-944c-636cbcd52c46.png)



The bicycle that Members cyclists use the most is the classic one, secondly the electric one and there are zero records in docked bicycles. Maybe because they don't include those types of bikes in the annual membership, it's needed context from stakeholders.

The bicycle most used by Casual cyclists is electric, in second place is the classic and in third place is the docked one.

![Classic_Docked_Electric_by_Member_Casual](https://user-images.githubusercontent.com/56371747/204387794-9f4baa6d-aa39-4878-8369-0bf1e098779a.png)



For long journeys, the users of both memberships prefer the electric bicycle and prefer to use the classic bike for short trips.

![Avg_Length_Casual_Member_by_day](https://user-images.githubusercontent.com/56371747/204396172-6d936279-e672-467f-a160-e17017bfaa03.png)



Casual cyclists have a higher usage time and also a higher distance traveled compared to Members cyclists.

![Avg_length_and_avg_time_Casuals_Members](https://user-images.githubusercontent.com/56371747/204397192-6bb16627-756c-4ba1-b6b6-f41ccb22d811.png)



Casual cyclists make fewer but longer trips, in contrast to Members cyclists who make more trips but they are mostly short trips than Casual cyclists.

![Captura de pantalla (242)](https://user-images.githubusercontent.com/56371747/204399115-770cf962-0366-400e-b389-75472f5eba1d.png)



Casual cyclists concentrate most of their trips on weekends, doing longer distance trips also on weekends.

![Casual_rides_avg_length](https://user-images.githubusercontent.com/56371747/204400726-766039ed-4eaf-47ef-b1f5-1c5c35d1b514.png)



Members cyclists travel longer distances on weekends compared to distances on weekdays, however they make more trips on weekdays. This indicates that during the week the trips are usually short but abundant.

![Member_rides_avg_length](https://user-images.githubusercontent.com/56371747/204401137-2929e780-70fc-4ab0-b4fa-0177d7bd9dfe.png)



The months of greatest use are concentrated in summer (June – September) for both memberships and its lowest point in winter (December – March).

![Casual_Member_avg_length_month](https://user-images.githubusercontent.com/56371747/204402678-bbb66d79-a596-4fd2-bc6a-36159eaf8e58.png)



The top five Start Stations for both memeberships are shown, being the most frequently Start Station used by Casual cyclists is Street Dr & Grand Ave, while Members use most frequently Wells St & Concord Ln.

![Captura de pantalla (249)](https://user-images.githubusercontent.com/56371747/204403001-098e6371-7e4c-41f4-842b-7f82dc794bcc.png)



The top five End Stations for both memberships are the next, the most End Station used for Casual cyclists is Street Dr & Grand Ave, for Member cyclists the Wells St & Concord Ln is most used End Station.

![Captura de pantalla (248)](https://user-images.githubusercontent.com/56371747/204403442-66d68afa-9587-46e9-8b8c-46be7272faa7.png)



### 2. Why would casual cyclists buy annual Cyclistic memberships?

The Casual cyclists have a weekend user profile, using the bicycle for longer distances and their favorite bicycle is the electric one. Maybe this Casual cyclists live far away from the Stations and have not need to used on weekdays, only use the service when they go to Downtown, it's needed more info about the profile of users like their professions, gender, distance between Bike Stations and their home or job. 

Nevertheless, having the presented information the **recommendation** is to offer discounts or promos to new Members who use Electric bikes and riding more than 2.6 mi per day, this restrictions are already accomplished by Casual cyclists.


### 3. How can Cyclistic use digital media to influence casual cyclists to become in members?

The **recommendation** is as Casual cyclists use frequently Electric bikes, the company could adapt the bike to share its battery with casual the cyclists smartphones, also could create an app that connect with Social Networks to share their track, location, accomplishment of challenges








