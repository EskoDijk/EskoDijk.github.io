---
layout: post
title:  "Non-visual virtual worlds: created with audio, haptics and your imagination"
date:   2011-10-24 09:45:12 +0100
categories: game
---

At first sight, a *non-graphical* or *non-visual* virtual world may sound unusual. However, one could say that well-known media like written novels, radio drama and audio books in fact create a virtual world with clearly non-visual means. But – these worlds are not very interactive in the way that 3D virtual environments and games are.

Today, the early beginnings of complex, interactive non-visual worlds have arrived: there is existing research on how to design interactive audio worlds and audio-only games [1].  However, the full potential of such a technology seems barely exploited at this point in time. One could view a non-graphical virtual environment as a (3D) virtual environment with graphics replaced by other rendering options that together convey a worthwhile experience to the user: think of 3D spatial audio, haptics, motion actuation, colored light, air flows and scents. Obviously, such an environment requires designing new ways of interaction and navigation compared to a graphical environment [1].

An existing product I worked with like AlphaSphere [2] already offers such a multi-sensory experience with light, warmth, audio and tactile stimuli, but is limited in its content and it is not interactive (that is, user-responsive). Software that I've created during my work allows scripting of more complex "experiences" which can be realtime adapted to inputs like button presses or measured sensor values. This was used in creating our ["relaxing at the beach" experience](http://www.geekstijl.nl/tech/tactiele-technologie-reele-virtualiteit/) shown at a public event. Another interesting product for creating audio-haptic experiences, the Feel The Music Suit, is being tested by Sense Company [6].

### Carving out a new research area
We can take the non-graphical world concept and put it to some good use: call it serious gaming if you like. Let’s define this new research area in which three features play a key role, in addition to the key features for interactive audio environments as listed in [1]:

1. Provide a user with pleasant or exciting tactile (haptic) stimuli linked to events in the virtual environment;
2. Use of implicit, low-effort methods for a user to control the virtual experience (e.g. using user body motions, or vocal/bodily reactions, changes in bio-signals and perhaps limited arm/leg gestures);
3. An application context and media content for healthcare and well-being applications.

In short, the aim is to create *interactive audio-haptic virtual environments for healthcare and well-being*.

The intended technology allows a user to experience an entertaining virtual environment while sitting or lying in a comfortable and relaxed positions, even with the eyes closed. Also multi-user experiences would be possible, in principle. Likely, systems built along these lines will serve entirely different markets than current graphics-intensive 3D virtual environments. One potential novel application is in the area of well-being and healthcare as argued in [3], because well-chosen tactile stimuli can relax a user, feel good, induce emotions, relax the muscles, or even reduce pain. The combination of haptics with audio has even more potential [3] for creating compelling feel-good experiences than using haptics or audio alone - as is mostly the case in today's solutions.

### Use case example
An example use case is an interactive relaxation chair situated in a hospital or care institute. A user lies in the chair with the eyes closed and  listens to a combination of nature sounds, music and voice coaching, while enjoying tactile stimulation and perceiving the color and warmth of light through the eyelids. Compare it for example to lying on a quiet beach on a sunny day with your eyes closed. The type of audio a user perceives could be similar to that provided by the company Meditainment [4] which is used for therapy and relaxation purposes, including use in hospitals and airplanes. This content is designed to immerse a user in an imaginary dream-like virtual world with high level of detail. Contrary to Meditainment, in our use case the experience can be guided or controlled by the user. For example, a user could use a gesture of two arms held up to indicate "start flying" or "fly higher". Adding other gestures would allow a user to actually explore the world, dive in virtual water (triggering modified audio, light and tactile effects), or re-visit favorite places.

Optionally, bio-signals such as heart and respiration signal can be sensed as well [3] and the obtained information on a user's level of relaxation can be used as part of the virtual experience narrative. This might even allow subtle new forms of bio-feedback training.

### Design challenges
Being a new and relatively unexplored medium, audio-haptic virtual environments do not yet have an established set of design rules and design patterns. University research is a very suitable means to map this unexplored territory, taking into account existing design knowledge from fields like music composition, tactile effect design, game design, cinema, radio drama or even (medical) interior architecture.

### Relevance
The primary guiding principle in this kind of research work should be to establish its relevance and benefit for specific user groups, for example in the healthcare domain. Although non-graphical virtual environments may not be relevant to the current mainstream gaming/simulation industry, there are compelling use cases in healthcare and well-being niche markets. For example, anxiety reduction in patients prior to examinations or treatment is a potential market. It can also be used as a new form of "relaxation gaming" examples of which already exist commercially (e.g. Wild Divine). In such games, creating a unique experience and escape from daily life is more important than having intensive user control (think about the 20 action keys in your typical 3D shooter!) or getting the high score.

This research topic may build on previous work on user-adaptive relaxation systems that use audio, haptics and light as the rendering means [3][5]. A working hypothesis for a relaxation application using such technology is that long-term treatment effectiveness and user enjoyment can be significantly improved by adding tactile stimuli and easy-to-use interactive elements, compared to a fixed-content audio-only solution like [4] where one linear storyline is played always in the same way.

One possible obstacle for researchers and designers alike is that the required technology (especially the *right* haptic/tactile stimulation), development kits and content authoring kits are not readily available. Time will tell whether such technology will be available on the market. I hope that one day I'm able to de-stress and at the same time explore the virtual worlds of my imagination - in a very real way!

### References
[1] N. Röber, Interaction with Sound – explorations beyond the frontiers of 3d virtual auditory environments, Ph.D. thesis, Univ. Magdeburg, September 2008. [View thesis here](http://www.x3t.net/thesis.html).

[2] AlphaSphere relaxation chair or "Spaceship for the inner journey", Wikipedia article, [link](http://en.wikipedia.org/wiki/AlphaSphere)

[3] E.O. Dijk, A. Nijholt, J.B.F. van Erp, E. Kuyper, G. van Wolferen (2010). Audio-tactile stimuli to improve health and well-being - a preliminary position paper, Special Symposium at EuroHaptics 2010, *Haptic and Audio-Visual Stimuli: Enhancing Experiences and Interaction*, pp. 1-10, Amsterdam, July 7th 2010.  [Link to PDF](http://www.eskodijk.nl/doc/Dijk10_Auditory-tactile.pdf")

[4] Meditainment.com website, [www.meditainment.com](http://www.meditainment.com/)

[5] E.O. Dijk, A. Weffers-Albu (2010). Breathe with the Ocean: a System for Relaxation using Audio, Haptic and Visual Stimuli, Special Symposium at EuroHaptics 2010, *Haptic and Audio-Visual Stimuli: Enhancing Experiences and Interaction*, pp. 47-60, Amsterdam, July 7th 2010. [Link to PDF](http://www.eskodijk.nl/doc/Dijk10_Breathe-with-the-ocean.pdf)

[6] Sense Company, [www.sense-company.com](http://www.sense-company.com/)

![Dream beach (c) by Eddy.H]({{ http://www.flickr.com/photos/eedh/5573466077/ }})


