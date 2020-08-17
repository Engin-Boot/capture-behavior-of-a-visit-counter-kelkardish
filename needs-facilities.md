# Visit-counter for a Facilities Manager

A foot-fall counter at door provides the information of the number of people
entering and exiting the hospital facility.

The foot-fall counter counts a person along with a time-stamp.

Scenario: Report visitor trends during a week of operation

  Given the visitor visits the hospital
  When a visitor enters the hospital
  Then the foot-fall counter increments and stores the count with time-stamp
  to get people count and busy timings.

Scenario: Alert when seating capacity is full

  Given a visitor enters the hospital
  When foot-fall exceeds a certain threshold calculated from previous trends
  Then alert the facility manager regarding seating capacity
