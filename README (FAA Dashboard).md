# Insights from my Tableau dashboard [FAA Wildlife Strikes, 2000-2015](https://public.tableau.com/views/FAAWildlifeStrikes2015_17460449973190/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

<div class='tableauPlaceholder' id='viz1746142263811' style='position: relative'><noscript><a href='#'><img alt='FAA Reported Wildlife Strikes, 2000-2015 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;FA&#47;FAAWildlifeStrikes2015_17460449973190&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='FAAWildlifeStrikes2015_17460449973190&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;FA&#47;FAAWildlifeStrikes2015_17460449973190&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1746142263811');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.width='1920px';vizElement.style.height='1107px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.width='1920px';vizElement.style.height='1107px';} else { vizElement.style.width='100%';vizElement.style.height='1327px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>


### Question 1: Which states had the highest number of wildlife strikes? What were costs associated with these strikes?

The top 5 states with the most number of wildlife strikes were:
1. California, $29.7M
2. Texas, $7.1M
3. Florida, $26.5M
4. New York, $50.3M
5. Pennsylvania, $8.3M
   
![image](https://github.com/user-attachments/assets/969aea91-6ca1-4b31-88bd-04d259778407)

### Question 1.5: Based upon the state that incurred the highest costs associated with wildlife strikes, what additional insights can you provide?

New York was the state that incurred the highest costs associated with damages due to wildlife strikes ($50.3M). After including information on the type of aircraft in our analysis, we see that roughly 98% (2,107) strikes occurred between wildlife and airplanes. Of airplanes, 1,862 (88%) strikes were 2-engine planes, which cost New York a total of $47.3M in damages, or roughly 94% of the total cost.


### Question 2: What animal species is responsible for the most strikes? What was the average damage associated with each strike?

![image](https://github.com/user-attachments/assets/d3a6f753-78dc-44e1-9205-fdfb215b2195)

Gulls, Terns, Sandpipers, Plovers, and Skimmers were responsible for the most number of strikes (4,797), which cost roughly $5,356 per strike. However, Ducks, geese, swans, and waterfowls accumulated the most damages associated with strikes at $142.1M- more than 5x the damages of the former group with less than half the number of strikes (1,738), and an average cost per strike of $81,779. Most interestingly, Deer, Elk, and Moose have the largest cost per strike figure of a whopping $130,099. My best guess is due to the sheer size of these animals, they would likely cause the most extensive repairs, damaging critical components versus smaller avian species that are likely sucked into engine components at best. According to the [FAA](https://www.faa.gov/airports/airport_safety/wildlife/faq), for civil aircraft in USA, wings and engines are the components most frequently damaged by bird strikes.


### Question 3: What can you report about the average cost per strike over the years? 

![image](https://github.com/user-attachments/assets/0c20e41e-7d08-4584-af39-88859a6dc1e3)

Since 2000, across all states, the average cost per wildlife strike has decreased. However, since 2013, the average cost per strike has risen, jumping from $3,185 to $10,748- a 237% increase. 


### Question 4: During what time of the year do the most wildlife strikes occur? 

![image](https://github.com/user-attachments/assets/4f439f56-1372-4bc7-a348-a9f22d244534)

Based on the data, the most strikes occur between July and October, which accounts for roughly 51% of all wildlife strikes. According to the [FAA](https://www.faa.gov/airports/airport_safety/wildlife/faq), this is likely due to fall migration and the time period when young birds have recently fledged from their nests.


### Question 5: What can you report on strikes associated with helicopters?

![image](https://github.com/user-attachments/assets/7f007bd5-be53-4c44-b540-d463cfe18455)


Between 2000 and 2015 there were a total of 97 wildlife strikes with helicopters, which represents less than half a percent of all strikes (0.34%). The majority of these strikes occurred in California (18), which amassed roughly $52,609 in damages. However, the state with the largest total cost associated with wildlife strikes during this time period was Utah, which amassed roughly $547K in damages with only 3 strikes ($182K cost per strike). What's interesting, is that a single helicopter crash accounted for 98% of damages ($537K) that involved grebes- a type of waterfowl- and decommissioned the aircraft for over 60 days (62) in 2011.
