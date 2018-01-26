---
layout: post
title:  "Interaction with a virtual world of infinite (unlimited) detail"
date:   2011-06-26 20:58:10 +0100
categories: game
---

In past years I have spent time in virtual worlds,  more time reading about them, and even more time in virtual world projects. So that should be a good topic to write about.

Current 3D games and virtual worlds, although sometimes amazingly detailed, still have only a limited level of detail in the graphical models and textures – compared to reality! Also virtual worlds often cover only a relatively small space for players to explore. This means that inevitably a player’s feel of realism is compromised.

# Limitations

First let’s list here the main reasons for these limitations in world detail:

1. Graphics hardware performance is limited;      e.g. polygon throughput or texture memory limits.
2. Design resources are limited; creating highly      detailed worlds manually is not feasible (e.g. think of designing all the      leaves on a tree or all individual stones in a river bedding – approaches      that do not scale).
3. Memory/storage/network resources are      limited; for example a building in a virtual world that requires many      terabytes of geometry data is not feasible on today\'s gaming platforms.
4. Computational resources are limited;      simulating many millions of entities in real-time (including AI and      physics) on current platforms is infeasible. For example, simulating      millions of individual insects that inhabit a forest seems impossible.

Despite of these four limiting factors, having virtual worlds with near-infinite detail is not necessarily impossible, using some compromises and clever solutions.  The key is to realize the *feeling* of a highly detailed reality without necessarily simulating it all.

# Relevance

Having detailed virtual worlds could enable a deeper gaming experience and also new ways of gameplay. For example, in a hunting type of game the hunter could inspect the grass in detail, looking for traces and footsteps that help to track prey that has recently passed. Or in a simulated forest, a player could mark some leaves on a specific tree as a way to communicate a secret message to a guild member. In serious-gaming applications, more detail may help to increase immersion in the world. It seems worth investigating how such \"unlimited\" detail could be obtained in a practical way.


# Overcoming the limitations?

The company [Unlimited Detail](http://unlimiteddetailtechnology.com) claims to have a solution for limitation #1 above (graphics hardware limits), by using a novel algorithm for rendering point cloud geometry models instead of using polygon geometry. Such a solution may help, but still – don’t the other limitations remain? For the classical polygon models, the technique of model-swapping may also get us some way towards overcoming limitation #1.

One approach to overcome limitation #2, limited availability of design resources, is to use algorithms for procedural generation of world content. Do (AI) methods exist to extract world design rules automatically from examples of worlds designed by people? This could certainly be an interesting research field.

Limitation #3 (memory availability) could be tackled by using pseudo-random number generators to generate parameters, which are then used as input to procedural content generators. Taken to the extreme, with this approach a single random seed number could effectively represent an entire world, so it can be generated on the fly at the user\'s machine without requiring any storage – if the content generation algorithms are good enough!

Finally, limitation #4 (limited computational resources) could be overcome by abandoning simulation realism and striving only for believability or the feel of immersion. For example, using a multi-step simulation level-of-detail (LoD) approach with low detail used for entities (like NPCs) that do not have a main role in the simulation or which are not close to any one of the human controlled characters.


# Problems (a.k.a. research topics)

In applying the above techniques to overcome the limitations, some problems remain, especially in multi-player simulations:

1. How can interaction events of players with      the world be recorded, represented and shared with the simulation      platforms of other players? Take the example of a player picking a random      leaf from a tree. Can another player later see that the leaf was picked? Can      this change event be represented as a data object describing a      \"delta\" onto the procedurally generated tree-with-leaves, and be      shared to other players on demand? Ideally the \"delta\" data is      only shared to other players that come close to the specific tree and      start to look at it in detail.
2. How to deal with the flood of      \"delta\" events that accumulate over time while playing? Should      there be a \"forgetting\" mechanism so that after some time the      game world resets back to its initial (procedurally generated) state? For      example the picked leaves of a tree will grow back after 5 simulated days.
3. How to treat relatively unimportant      entities (NPCs) that were in some way persistently affected or modified through      interaction with a player? Should they be simulated (AI/motion) with a higher      level of detail from the point in time of interaction onwards? Is this      feasible and scalable over time, or do we need a \"forgetting\"      mechanism as well to avoid that over time numerous entities have to be      simulated all the time in a high level of detail?

Although we have only scratched the surface of this topic, the problems that appear by this scratching are abundant. Sounds like a great topic for virtual worlds / game research!

