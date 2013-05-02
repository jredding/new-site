---
layout: default
title: Events
published: true
---

<pre>
corr   d8commits totalevents  regevents relevents sprintevents trngevents ugevents virtevents if datenew >= d(1feb2011) & datenew <= d
> (31Mar2013)
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
</pre>

<pre>
. corr  d7commits totalevents  regevents relevents sprintevents trngevents ugevents virtevents if datenew >= d(2feb2008) & datenew <= d(
> 31Jan2011)
(obs=35)
             | d7comm~s totale~s regeve~s releve~s sprint~s trngev~s ugevents
-------------+---------------------------------------------------------------
   d7commits |   1.0000
 totalevents |   0.3880   1.0000
   regevents |   0.2734   0.2747   1.0000
   relevents |  -0.1169   0.5800   0.0292   1.0000
sprintevents |        .        .        .        .        .
  trngevents |   0.3005   0.8912   0.2197   0.4921        .   1.0000
    ugevents |   0.3570   0.9893   0.1727   0.5965        .   0.8446   1.0000
  virtevents |   0.5153   0.5004  -0.0311  -0.0088        .   0.5256   0.4574
             | virtev~s
-------------+---------
  virtevents |   1.0000
</pre>
