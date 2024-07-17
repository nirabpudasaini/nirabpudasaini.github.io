---
layout: post
title: Open Source and Open Data's Role in Nepal Earthquake Relief
---

A devastating magnitude 7.8 earthquake struck Nepal on April 25, 2015, killing more than 9,000 people, injuring thousands more, and leaving an additional 3 million homeless.

Immediately after the earthquake, the government, local and international security forces, and international aid agencies all jumped in to try to help. However, there was a lack of coordination between these groups.

The power of an open source project like [OpenStreetMap](https://openstreetmap.org) during a crisis like Nepal's earthquake is undeniable, and I had the opportunity to see it up close and personal. I worked with the Kathmandu Living Labs team, where I observed thousands of local and international volunteers collaborating to create data and tools. Responding agencies used the team's work to plan and execute their operations.

The philosophy of [Kathmandu Living Labs](http://kathmandulivinglabs.org) is that by collaboratively building upon existing work, we will reach much further and have a far greater impact than working on problems individually and from scratch.

**OpenStreetMap**

![_config.yml]({{ site.baseurl }}/images/open_data_relief_0.png) 

_An OpenStreetMap map of Kathmandu_

Before the earthquake, Nepal had a strong OpenStreetMap community thanks to the work of Dr. Nama Raj Budhathoki. Budhathoki hosted mapping events with the support of major universities, youth groups, and NGOs/INGOs in the Nepali capital of Kathmandu. So before the earthquake even occurred, the city had already been densely mapped by hundreds of volunteers. And that work had started to expand beyond the capital city.

In the aftermath of the earthquake, about 8,000 local and international OpenStreetMap community members worked to create detailed map of affected areas, which first responders used for planning and mobilizing their resources. A task of this scale would not have been possible with only local mappers. Because many of these mappers were first-timers, resources like LearnOSM.org were invaluable in getting them up to speed. Coordination between thousand of mappers was done using the [Humanitarian OpenStreetMap Team's tasking manager](http://tasks.hotosm.org/), an open source tool that has been used in several disaster situations and is continuously being improved.

![_config.yml]({{ site.baseurl }}/images/open_data_relief_1.png) 

_Nepal earthquake mapping in the Humanitarian OpenStreetMap Team's tasking manager_

Kathmandu Living Labs then took the open data gathered by what I like to call "digital humanitarians" through OpenStreetMap to relay needs of survivors and victims to volunteers on the ground. The responding units and organizations needed training on OpenStreetMap (which we provided) as well as custom maps for specific purposes and missions.

**Ushahidi**

The most powerful project the Kathmandu Living Labs team created during this time was QuakeMap.org. This platform helped people communicate their needs to responding organizations effectively. The system received 2,035 reports, out of which 978 were verified and 551 required action. Of the actionable reports, 434 reports were acted on and 309 were completely closed. Due to difficulties with feedback loops, we were not able to ascertain whether action was taken on the remaining reports.

QuakeMap.org was built on top of the open source [Ushahidi framework](https://www.ushahidi.com/), which was built in 2008 to map post-election violence in Kenya. Ushahidi has grown significantly since then, with customizable features and about 90,000 deployments worldwide.

![_config.yml]({{ site.baseurl }}/images/open_data_relief_2.png)

Building QuakeMap.org on top of Ushahidi allowed us to quickly get the platform running. Because it is open, we were able to customize the deployment as the needs came in. Moreover, it allowed us to focus on the deployment from the outset, creating a process around dispatching requests to the appropriate responding organizations. Our volunteers were working around the clock on verifying and channeling the reports to the responding organizations. They were then actively seeking information on whether the needs in the reports were addressed and updating the status of the reports from that information.

Building similar technology from scratch would have required significant development time, which would have consumed all of the resources of our small team. Not to mention, in a crisis, you need to be able to move very quickly to respond to life-threatening needs.

**Open Data Kit**

Since the earthquake, Kathmandu Living Labs has been involved in many data collection projects for damage assessment, relief distribution tracking, and reconstruction monitoring. We've been working with the Nepali government's Department of Archeology, Department of Education, Central Bureau of Statistics, and National Reconstruction Authority to collect damage assessments of historical sites, schools, and residential buildings. We've worked with other partners, like World Bank, Teliasonera, and Mercy Corps Nepal to use mobile data collection for relief and reconstruction monitoring and tracking.

We use KLL Collect, an application built on top of the open source Open Data Kit, for all of our data collection project. [Open Data Kit (ODK)](https://opendatakit.org/) is a data collection platform consisting of various sets of tools to author, deploy, and manage mobile data collection. It allows easy authoring of mobile surveys that can be written in spreadsheets. The project started in 2008 and is backed by a worldwide community of developers and users.

By building on top of the existing ODK framework, we were able to add necessary features and customize the app to the project's needs. We were able to use existing ODK server-side technologies and focus on improving the mobile app. In addition, the active community and fair amount of already existing online resources meant that we could always count on getting help when we got stuck.

![_config.yml]({{ site.baseurl }}/images/open_data_relief_3.png)


**The way ahead**

It took us a calamity of huge scale to learn the importance of open data. After the earthquake, we saw adoption of OpenStreetMap by most agencies. Due to its level of details was used as a default map source.

There are important lessons that other countries can learn from Nepal and its adoption of open data after the earthquake. We saw the importance of building and having a capable local team. We saw that when thousands of people come together in an open ecosystem, they can accomplish in weeks what would have otherwise taken years to do. We saw that having easily deployable and open source systems in place is critical in times of crisis.

We can safely say that open data and open source projects saved numerous lives after the earthquake. We will need to invest in more of these projects in the future and create a local and self-sustaining communities around them.

_I wrote the post originally for opensource.com and the original article can be found [here.](https://opensource.com/life/16/6/open-source-open-data-nepal-earthquake)_



