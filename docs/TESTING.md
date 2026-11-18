# FreshRoute Prototype — Testing Record

## Test status
The following are test instructions derived from the supplied application and coursework requirements. They are **not completed test results**. Execute them on the actual demonstration browser/device and record actual outcomes before submission.

## Test environment
| Item | Record |
|---|---|
| Operating system | To be completed |
| Browser and version | To be completed |
| Test date | To be completed |
| Tester | To be completed |
| Application version | v1.1 |

## Test cases
| ID | Scenario | Steps | Expected result | Actual result | Status |
|---|---|---|---|---|---|
| FR-T01 | Create order | Enter valid customer/contact/date and one produce item with positive whole-number quantity; save | Success message; new FR reference assigned; order saved | Not executed | Not tested |
| FR-T02 | Required fields | Attempt save with required customer or contact empty | Form prevents incomplete order from being saved | Not executed | Not tested |
| FR-T03 | Produce validation | Enter missing item name or invalid quantity | Invalid produce line is rejected | Not executed | Not tested |
| FR-T04 | Add/remove rows | Add a produce row and remove an additional row | Row is added/removed; at least one row remains | Not executed | Not tested |
| FR-T05 | Exact-reference search | Search for existing sample reference FR-1042 | Matching order appears | Not executed | Not tested |
| FR-T06 | Unknown reference | Search for FR-9999 | `No order found for FR-9999. Check the reference and try again.` appears | Not executed | Not tested |
| FR-T07 | Edit order | Open FR-1042, change permitted fields/items, save | Changes appear and original reference remains unchanged | Not executed | Not tested |
| FR-T08 | Invalid edit line | Enter an item line without a valid `item,quantity` pair | Save is blocked with validation feedback | Not executed | Not tested |
| FR-T09 | Delivery date match | Select a date with scheduled orders | Only orders for that date appear | Not executed | Not tested |
| FR-T10 | Empty schedule | Select a date with no scheduled orders | Empty-schedule message appears | Not executed | Not tested |
| AT-01 | Keyboard-only existing order | With FR-1042 present, use Tab/Enter only to focus reference field, enter FR-1042, submit, navigate to result action and open it | Correct FR-1042 opens without mouse use | Not executed | Not tested |
| AT-02 | Keyboard-only unknown reference | Search FR-9999 using Tab/Enter only and navigate to/read status message | Exact no-match message is visible/readable without mouse use | Not executed | Not tested |

## Defect and retest log
| Defect ID | Test ID | Observed issue | Severity | Action taken | Retest result |
|---|---|---|---|---|---|
| — | — | Complete after test execution | — | — | — |

## Completion note
Do not mark a test **Pass** until it has been executed and its actual result recorded. If a test fails, record the observed behaviour, raise a defect, fix it if in scope, and retest. Classroom acceptance-test specifications do not, by themselves, prove that the prototype passed.
