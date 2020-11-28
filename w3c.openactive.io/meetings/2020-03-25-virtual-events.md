# 2020-03-25 - Virtual Events and other COVID-19 proposals

## Summary

Given the urgency of the topic in light of the UK-wide 'lockdown', we aimed to finalise approval on all topics on the agenda in the course of the call.

**Virtual Locations \(**[\#224](https://github.com/openactive/modelling-opportunity-data/issues/224)**\)**

* After discussion about the merits of supporting multiple broadcast platforms, the consensus was to keep `beta:virtualLocation` as a singular not array, as multiple broadcast platforms are likely an edgecase in this sector. We agreed to re-evaluate this before moving the property out of beta.

**VideoObjects and/or OnDemandEvents** \([\#228](https://github.com/openactive/modelling-opportunity-data/issues/228)\)

* Use `OnDemandEvent`, to easily make use of all the existing properties of Events.
* Use `workFeatured` to embed any video or other media \(e.g. a `VideoObject`\)

**Describing required equipment** \([\#229](https://github.com/openactive/modelling-opportunity-data/issues/229)\)

* There was a proposal that this should be triple-valued \(roughly `required`, `optional`, `none`\) - to account for events where equipment is optional \(an alternative is provided for those without\). Consensus was that context would indicate the meaning of the attribute, with additional guidance being provided in `attendeeInstructions` if required.

**Describing participantInteraction** \([\#230](https://github.com/openactive/modelling-opportunity-data/issues/230)\)

* Use `beta:isInteractivityPreferred` boolean for now, as interaction being strictly “Required” is probably an edge case
* Consider repurposing [`https://schema.org/interactivityType`](https://schema.org/interactivityType) for this in future
* `attendeeInstruction` should be used to provide further detail if required.

**eventAttendanceMode** \([\#225](https://github.com/openactive/modelling-opportunity-data/issues/225)\)

* No changes

**maximumVirtualAttendeeCapacity and related properties** \([\#226](https://github.com/openactive/modelling-opportunity-data/issues/226)\)

* This has the potential to create a large amount of complexity and confusion, especially given the `maximumAttendeeCapacity` property still exists and is used widely, and `remainingAttendeeCapacity` is used heavily by the [Open Booking API](https://www.openactive.io/open-booking-api/EditorsDraft/).
* For now just add `beta:maximumVirtualAttendeeCapacity` to `VirtualLocation`, so as not confuse any logic around booking \(keeping booking separate for now, and readdressing this with any additions to Open Booking API to handle virtual classes in future\)
* Note that this is the capacity of the specific `VirtualLocation` \(e.g. that specific Zoom room\), not the entire event.

**EventMovedOnline Event status** \([\#227](https://github.com/openactive/modelling-opportunity-data/issues/227)\)

* Add a new property `beta:affiliatedLocation` was proposed for the original locations of an online-only event, to ensure that the existing data users’ implementations would be intentionally broken by the lack of a `location` field in all cases, and hence they would not misrepresent virtual classes as physical ones.
* This replaces the need for `EventMovedOnline`, which can therefore be removed.
* Hence, for virtual events where `eventAttendanceMode` is set to `https://schema.org/OnlineEventAttendanceMode`,  `location` MUST NOT be included.

**Guidance \(**[\#231](https://github.com/openactive/modelling-opportunity-data/issues/231)**\)**

* Put `beta:maximumVirtualAttendeeCapacity` into `VirtualLocation` as a beta field, but keep this RECOMMENDED
* Offer is required either in `SessionSeries` or in `ScheduledSession` update to match current spec
* `beta:affiliatedLocation` is RECOMMENDED
* `workFeatured` is RECOMMENDED

**Levels \(**[\#82](https://github.com/openactive/modelling-opportunity-data/issues/82)**\)**

* Standardise only the string “`Beginner`” for now, as a short term solution to save trying to solve the larger levels problem.

## Slides

{% embed url="https://docs.google.com/presentation/d/1srA7SyfDBqCHwFTT7oVxyu4-Hl\_3NBkSlpCDMKqj4HE/edit" %}

## Video

{% embed url="https://www.youtube.com/watch?v=IR6EDwUvAsA" %}



