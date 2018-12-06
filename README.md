# MetOceanAPI-Workshop
Working area for MetOcean API Workshop 05 - 07 December at ESRI in Tysons Corner, VA, USA

## Background
The MetOcean community is required to make more data available and the initiative “Weather on the Web” will be an important part of the solution.  The design of a REST based API (cf WFS 3.0) should make life as easy as possible for our current and prospective customers.  An initial design and prototype based on a version on an implementation of the WCS2.1 MetOcean profile is nearly completed and under test.  The purpose of this work is to demonstrate and evaluate the design of the RESTful API, involving industry users.  For now we call this API the WOW API (Weather on the Web), although this may well change in the light of our experience.

## The WOW API (Formerly known as the Restful API)

The WOW API facilitates the extraction of metadata and data using the underlying MetOcean profile of WCS 2.1.  A prototype WCS 2.1 was implemented by IBLsoft’s VisWX over two years ago and will be used, at least initially to provide the base on which the prototype WOW API will be built, although there is no reason why the WOW API may not be built separately.  The only prerequisite is that the underpinning database supports multi-dimensional queries.  It is hoped that other vendors will soon implement the MetOcean profile of WCS 2.1.

The work on the "WOW" API, based on the OGC's WFS 3.0 specification, explores how the WFS 3.0 pattern might be adapted to provide a variety of APIs required for MetOcean data.  This work has reached a prototype stage using the prototype WCS 2.1 already implemented on VisWX (IBLsoft). One of the key design principles is to create a family of APIs to reflect the varying complexity of the available extraction patterns.  An API to extract data on a 4D aircraft trajectory is necessarily more complicated than an API used to extract a simple point. The WCS 2.1 API would be able to support both queries, but at the cost of being overly complex for simple queries.  A "family" of simpler REST style APIs sitting atop of WCS 2.1 are easier to design and use.  A “top level” API exposes these API patterns for each query style and documented using the "Open API 3.0" specification.

## The OGC and proposed Workshop

The OGC's WFS working group is supportive of this work and keen to be involved. A number of organizations (UKMO, NOAA/NWS, ECCC/MSC, USAF) and GIS vendors (e.g. ESRI, GeoServer, NWS) are also very interested in this work and by trialing, the prototype APIs hopefully provide feedback.  The workshop, kindly hosted by ESRI, is open to anyone who would like to access MetOcean data using either the WOW or WCS APIs. The purpose of the workshop is to provide engineering feedback to help with the evaluation of both APIs and therefore understand any issues with adoption or their suitability.  The intention is to provide feedback to the various interested OGC working groups our findings and of course future actions.

ESRI have offered to host a two-day workshop (Dec. 5: Setup and Dec 6-7: workshop) in their Crystal City, Virginia location the week before the next OGC meeting in Charlotte North Carolina (Dec 10th to 14th).  Remote participation will be supported.  The work will take the form of a hackathon and be open to all interested parties and the provisional results presented at the OGC meeting held the following week. 

## Proposed Schedule and topics for the workshop

Dec 5th Schedule

- 8am - 12 noon → Setup of prototypes and material for presentation
- 12 noon - 1pm → Lunch break
- 1pm - 6 pm → APIs in MetOcean Community
  - Orientation/Context (Set of presentations)
  - WOTW API
    - Live Demonstration of WOTW
    - Evaluation and feedback on the WOTW API
    - How easy is to create a client software using this API
    - What “Use Cases” are not included?
    - A brief presentation to outline the scope and purpose of the WOTW API
    - Where does the WOTW API fit in with WFS3.0
    - Hackathon on WOTW
  - WCS 2.1/CIS1.1 with MetOcean Profile
    - Live Demonstration of IBL implementation of WCS2.1/CIS 1.1
    - A brief overview of the design and purpose of WCS2.1 metOcean profile.
    - A live demonstration using the IBL implementation
    - How easy is to create a client software using this API
    - Broader discussion on mind set for moving to multi-dimensionality (4D WCS space).  Has anyone has implemented this outside of IBL?  How do we alleviate concerns with implementation?  Should we create a “recipe” for implementation?  Should we put out cloud instance as prototype design for folks to follow?

Dec 6th schedule
- 8am - noon → Hackathon sessions on WOTW API and WCS2.1/CIS1.1
  - Build teams and set goals
- 12 noon - 1pm → Lunch break
- 1pm - 5pm → Continued Hackathon sessions
- 5pm - 6pm → Report out on hackathon findings

Dec 7th schedule
- 8 - 12 noon → Continued Hackathon sessions and final report outs
- 12 noon - 1pm → Lunch break
- 1pm - 4pm → General discussion on two topics:
  - Discussion on the applicability of each API to various uses e.g. interoperability with other WCS servers
  - The OGC appetite for this approach?
