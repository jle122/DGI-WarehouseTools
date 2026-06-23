# Company B Serial Number Counter 2.0
An upgraded version of our Serial Number Counter that allows for smart recognition of model numbers without manual input into the columns. Created for Company B.
## Stack

Google Sheets + Apps Script automation

## Reported Benefits

- Build on benefits of original template, but even faster efficiciency (**20% increase on the original template**).

## How It Works
- Essentially the same as our Serial Number Counter, except we do not edit any other column except Column A.
- Our code utilizes a **hash map** to recognize a prefix in the Serial Number, and automatically create new columns and sort into existing columns based on the corresponding part number.
- If unknown, automatically creates and sorts into an UNKNOWN column


### Mobile Scanner Workflow Example

A worker can walk a shipment, scan units directly into the sheet from the scanner, and complete the data collection process without having to stop and manually write everything down first.

## Expansion Potential

Any vendors with serial numbers that have a predictable pattern can potentially use this template.
