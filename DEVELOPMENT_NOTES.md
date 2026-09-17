# Migration and function mapping

## Source boundaries

| Classification | Result |
| --- | --- |
| Onetime only | Single-premium input, age/year projection, four withdrawal plans, policy-value multiplier interpolation, annual/cumulative withdrawal table, auto-roll interest disclosure |
| 5Pay only | Guided scenarios, jars, admin/user management, Firebase media, GAS configuration, local personalisation and Gap pages; not imported |
| Similar | AVA customer-facing layout and data-led Saving explanation |
| Different purpose | 5Pay is a five-year contribution workflow; this module remains a one-time-principal projection |
| Removed legacy | HKMA deposit-rate board, rolling fixed-deposit table and all bank-specific events |

## Dependency result

The removed fixed-deposit feature shared only generic number-format helpers. It did not provide data to Saving. `SAVING_SHEET_ID`, CSV parsing, plan mapping, interpolation, extraction timing and result formulas remain unchanged.

## Data and storage

The source Saving feature has no LocalStorage, SessionStorage, IndexedDB, GAS writes or API writes. No migration is required. The original public Google Sheet ID and tab names remain the data contract.
