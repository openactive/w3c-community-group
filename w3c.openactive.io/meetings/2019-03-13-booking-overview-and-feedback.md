# 2019-03-13 - Booking: Overview and feedback

## Summary

We ran through the [booking specification](https://www.openactive.io/open-booking-api/EditorsDraft) in more detail, including checking the direction taken on issues raised since the previous call. Everyone was broadly happy, with notable points raised which did not require updates to the spec:

* MLP emphasising for the importance of flexibility of payment provider, including decoupling of payment method from reconciliation.
* After a discussion on the value of having telephone number as a required field it was concluded that it would be best for this not be required at the API level, and for any such constraints to be applied on a contract level if required for specific scenarios.
* The usefulness of Offer overrides for flexibility of business models.
* The spec covers cancellations and refunds before the event has occurred, however it does not explicitly cover cancellations after the event has occurred \(e.g. partial refunds are useful if for example floodlights shut out halfway through the event\). These can be completed out-of-band, as they were considered an edge-case for this version of the specification.

As a result of the call we:

* Have left the [version issue](https://github.com/openactive/open-booking-api/issues/105) open for comment to seek wider feedback.
* Clarified the cancellation of events after they have occurred in the specification.

Additionally Izy requested feedback [her work](https://docs.google.com/document/d/1-z3KkQYch-qY1OKbk-o9WTEabIr-JGcRd55fEtKjQJg/edit) following the [last accessibility call](2018-10-24-accessibility-requirements.md).

## Slides

{% embed url="https://docs.google.com/presentation/d/1b6sbpd0wwGx\_ezWEk\_wmr-ZoRdC04tYexhedsa1viYA/edit?usp=sharing" %}

## Video

{% embed url="https://youtu.be/7Zg4iRWRRj8" %}



