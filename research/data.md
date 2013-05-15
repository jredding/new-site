---
layout: default
title: Examination of Data
published: true
---
last update: {{ page.date }}
As research progresses this page will serve as a dumping ground for the foundational information and data we derived from the data analysis/mining. The information or data may not make sense and it will not serve as a conclusive definition or direction of the overall research. What you can derive from this page is the direction of the research and draw your own conclusions from the information or data provided. Opinions, comments, and suggestions are [always welcome](/contact "always welcome"). 

Please keep in mind that this research only looks at contributions to the core of Drupal and Joomla!.

Our approach
------------------
Our approach to understanding how intrinsic and extrinsic motivations influence innovation in a community setting is to examine specific defining events within the Joomla! and Drupal communities that had meaningful impact on the source code. The underlying notion is that these events either reinforced or challenged the (implicit) social contracts held between the developers in their respective communities. By characterizing the events as either supporting intrinsic or extrinsic motivations and then assessing who—either the community or the individual—captured the majority of the benefits of the resulting innovation, we can shed light on how developer motivation to create value is associated with value capture. One of the defining events in each community was the creation of their anchor boundary organization— Open Source Matters in the case of Joomla! and the Drupal Association in the case of Drupal. We consider how they have contributed to defining events in source code evolution and how their respective governance structures influence the resiliency of the innovations core to the health of the ecosystem.

### Eh? What?
In other words we think there is something behind-the-scenes of each project that bubbles up through organizations such as the Drupal Association (Drupal) and Open Source Matters (Joomla!) that helps to indirectly or directly keep pushing the projects forward. We're looking to prove that with data by, for example, showing a direct correlation between conferences and new contributions or an increase in 

Our research is focusing on many data points including the following
* Total contributions to core by version, date, and individuals
* Total number of events in each ecosystems (usergroup meetings, sprints, trainings, conferences, etc.)
* Core developer time in the project,  
* Core developer 


Laura crunched some great numbers for the work today. We looked at correlations between the number of events that occured every month to the number of contributions that occurred. This preliminary set of correlations is done on a month by month basis without a lag but in subsequent analysis she looked at lag times (ex. event in January but contributions in March, April, or May). The goal is to determine if there are any trends in encouraging contributions. 

Analysis was done with STATA. 

    corr  d7commits totalevents  regevents relevents sprintevents trngevents ugevents virtevents if datenew >= d(2feb2008) & datenew <= d(> 31Jan2011)
(obs=35)

                 | d7comm~s totale~s regeve~s releve~s sprint~s trngev~s ugevents
    -------------+---------------------------------------------------------------
       d7commits |   1.0000
     totalevents |   0.3880   1.0000
       regevents |   0.2734   0.2747   1.0000
    sprintevents |        .        .        .        .        .
      trngevents |   0.3005   0.8912   0.2197   0.4921        .   1.0000
        ugevents |   0.3570   0.9893   0.1727   0.5965        .   0.8446   1.0000
      virtevents |   0.5153   0.5004  -0.0311  -0.0088        .   0.5256   0.4574
                 | virtev~s
    -------------+---------
      virtevents |   1.0000


And the Drupal 8 correlations 

    . corr   d8commits totalevents  regevents relevents sprintevents trngevents ugevents virtevents if datenew >= d(1feb2011) & datenew <= d(>31Mar2013)

(obs=26)

                 | d8comm~s totale~s regeve~s releve~s sprint~s trngev~s ugevents
    -------------+---------------------------------------------------------------
       d8commits |   1.0000
     totalevents |   0.4942   1.0000
       regevents |   0.1279   0.4159   1.0000
       relevents |   0.2080   0.5356   0.2026   1.0000
    sprintevents |   0.6815   0.2339   0.1136  -0.0446   1.0000
      trngevents |   0.2339   0.5274   0.1135   0.0014   0.2053   1.0000
        ugevents |   0.3134   0.9304   0.2721   0.5226  -0.0394   0.3540   1.0000
      virtevents |   0.6111   0.6727   0.2568   0.3955   0.4434   0.3417   0.4638
                 | virtev~s
    -------------+---------
      virtevents |   1.0000


