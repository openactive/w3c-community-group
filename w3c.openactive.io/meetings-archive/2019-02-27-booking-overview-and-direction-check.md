# 2019-02-27 - Booking: Overview and direction check

## Summary

We ran through the [booking specification](https://www.openactive.io/open-booking-api/EditorsDraft) at a high level, including checking the direction taken on remaining issues. Everyone was broadly happy, with some comments to raise on GitHub and a suggestion to consolidate cancellations into a single PUT call for the Order \(to allow for atomic cancellation, given the potential for additional cancellation constraints to exist\).

As a result of the call we:

* Clarified the spec regarding the error raised when attempting to book a non-"bookable" opportunity.
* Amended the spec to make cancelling multiple items atomic, with an outstanding question regarding restrictions \([https://github.com/openactive/open-booking-api/issues/102](https://github.com/openactive/open-booking-api/issues/102)\)
* Raised and linked an additional issue: [https://github.com/openactive/open-booking-api/issues/103](https://github.com/openactive/open-booking-api/issues/103)

## Video

{% embed url="https://youtu.be/hz85pUuDgx8" %}



