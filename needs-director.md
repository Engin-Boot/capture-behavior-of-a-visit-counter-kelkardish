# Visit-counter for a Director

Entry-card issuer has a feature to track the type of entry-card issued.
This helps to differentiate between the types of visitors. Example, an
OPD patient, visitor or visiting specialists.

The entry-card can also double as a parking pass if parking is availed.
The parking slot is mentioned in the entry-card.

Scenario: Show patient visits during working days and holidays

  Given a visitor enters the hospital.
  When the visitor is issued an entry-card
  Then the type of card issued is tracked (say patient) and a total
  entry-cards issued is tracked.

Scenario: Compute parking slots to reserve for visiting specialists

  Given a visitor enters the hospital.
  When the visitor is issued an entry-card and the visitor has availed parking
  and parking slot is available
  Then a parking slot is given to visitor from the available parking slots after
  reserving any necessary parking slots for the day for any visiting specialists
