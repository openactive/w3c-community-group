# 2019-04-10 - Booking: Workshop followup

## Summary

We discussed feedback received at the Open Booking Finalisation Workshop, and covered some of the common followup questions that we did not have time to address during the event:

* **Opportunity & Offer** - both an Opportunity \("Yoga Tuesday 14th 7pm"\) and an Offer \("Junior \(8-18\)"\) are required to start the booking flow. This explains how a booking system knows which price is applicable without attendee data such as date of birth.
* **Trust and Control** - The specification does not currently include fine-grain control of opportunity bookability e.g. it does not allow "bookability by broker" to be advertised or elegantly controlled. This is simply because of the scale of the controls required and the cost of these e.g. if a Seller partnered with 100 brokers, they would need to administer "Bookable via Broker 1" though to  "Bookable via Broker 100" on a per-activity basis, which would be an enormous administrative burden \(and increased development cost for booking systems\). Especially when we consider that it's likely that the constraints will be more nuanced than just per-activity. For example one might want "Bookable via Broker 1 only off-peak and on a Wednesday", and "Bookable via Broker 5 for junior Offers only". If we went down the route of constraining booking at an API level it would get extremely complicated and the cost of administration would likely not outweigh the risk of bad partners \(keeping in mind that a Seller can instantly terminate their connection with any rogue partner Broker with zero notice if they wish, in the case that they violate the agreement\). The trust relationship discussed at the workshop between Sellers and their partner Brokers is the key. A Seller's contract with each Broker will likely include restrictions on what they can and cannot book and under what circumstances,  which can then be audited during reconciliation if needed. So the Brokers that Sellers partner with will have the technical ability to book anything, but will have to follow the terms of any agreement with them. This has been added to the "out of scope" list in the specification for clarity.
* **Attendee detail capture** - We talked through the Attendee Details Capture [GitHub issue](https://github.com/openactive/open-booking-api/issues/107) \(a.k.a. "date of birth"\) in detail. We are actively seeking feedback on this issue - which is fairly complex - and propose to delay this for a future version of the specification. Izy from Sport England was keen to point out that Sport England are supportive of minimal data capture during booking, and that any activity providers being pressured by Sport England to provide reporting of detailed demographics based on details captured during booking should contact her for assistance.

The [Open Booking specification](https://www.openactive.io/open-booking-api/EditorsDraft) release has been delayed until 17 April to allow for minor technical refinements to be made \(such as REST conformance and model consistency\), and is now scheduled for ratification on 1 May.

The [OpenActive model validator](http://validator.openactive.io) will be updated to include the models in the Open Booking specification as soon as it is published, to aid implementation work.

## Slides

{% embed url="https://docs.google.com/presentation/d/14gm\_ms8hZzbaHIYwjHE0Qa55JlY7fVcMlJ2wPdQMiVs/edit\#slide=id.g3de11654c2\_0\_98" %}

## Video

{% embed url="https://youtu.be/tYFVM2TSb8Q" %}

