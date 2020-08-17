# Visit-counter for a Director

Entry-card issuer has a feature to track the type of entry-card issued.
This helps to differentiate between the types of visitors. Example, an
OPD patient, visitor or visiting specialists.

The entry-card can also double as a parking pass.
Entry-card mentions usage of a parking spot.

Scenario: Show patient visits during working days and holidays

  Given a visitor enters the hospital.
  When the entry-card issuer gives the visitor an entry-card
  Then the count of entry-card issued (by type) gives the number of patients
  visiting during any day.

Scenario: Compute parking slots to reserve for visiting specialists

  Given a visitor enters the hospital.
  When the entry-card issuer gives the visitor an entry-card and the visitor
  has availed parking and parking slot is available
  Then the visitor gets a parking spot from the available parking slots after
  reserving any necessary parking slots for the day for any visiting specialists
