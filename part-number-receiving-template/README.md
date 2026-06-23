# Part Number Receiving Template
A packing list receiving template that allows for seamless scanning of part numbers without having to read them.
## Stack

Google Sheets + Apps Script automation

## Problem

New Company C products arrive with part numbers that are difficult to read and sort manually (10+ digits, one letter difference in the middle of the number). Receiving/picking these products is a big pain and has high room for error.

## Why Can't We use the Serial Number Counter?

This workflow requires a different receiving format because there are no unique serial numbers, so duplication detection is not ideal here. Items of the same model will have the same part number, but we are removing the need to read the part numbers in order to reduce errors involving with these items.

## Purpose

This tool supports scanner-based receiving by checking scanned barcodes against a packing list and tracking receiving progress automatically without having to read a part number.

## Reported Benefits

- Up to 300 percent efficiency gain in some scenarios
- Tasks that once took around 15 minutes may take closer to 5 minutes
- Accuracy improvements of around 80 percent
- Easier backtracking when miscounts happen
- Reduced mental and physical strain from reading part numbers

## How It Helps

- Reduces the need to manually read difficult part numbers
- Uses barcode scans to validate received items against the packing list
- Makes receiving faster and easier to audit
- Supports append-only workflows that preserve scan history

## How It Works
- **Row 1: Col. headers**
- **Col. A-[x]**: Columns reserved for the packing list. Dependent on the format of the list. Our packing lists are in the format as follows
  - **Col. A:** Product number
  - **Col. B:** Product Description
  - **Col. C:** Quantity
- **Col. D: # of times scanned.** A column tracking the number of times we scanned a part #. Updates upon edit in Col. G.
- **Col. E: Difference.** This column calculates (Quantity - # of times scanned) to inform the user of the quantity left over. If difference = 0, the cell will highlight bright green. If difference is negative, indicating an over-scan, the cell will highlight yellow.
- **Col. G: Input column.** Scan barcodes in the cells of this column in an append-only manner (no need to backtrack and delete, just keep scanning). Check corresponding cell in Col. H for result of the scan. 
- **Col. H: Message column**. A corresponding message column that goes shows the result of the scan in Col. G. Our code looks for an exact match between cell in Col. A and cell in Col G. There are four possible results in the form of a message and a highlight of the cell:
  1. **Successfully received**. When scanned part number matches a part number in the packing list. Corresponds to a dark green highlight
  3. **Fully received**. When difference is 0. Corresponds to a bright green highlight.
  4. **Overscanned**. When difference is negative. Corresponds to a yellow highlight.
  5. **Not in packing list**. If no match for the scan. Corresponds to a red highlight.
- **Col. I: Timestamp column.** Indicates when input happened. 

## Workflow

1. Input the packing list (our software allows for exporting to spreadsheet)
2. Scan items into the scan column without manually reading each part number
3. Check the message and difference columns to monitor progress
4. Continue scanning until receiving is complete
5. Use timestamps and scan history for audit and backtracking

## Use Cases

- Receiving items with very similar part numbers
- Faster barcode-driven receiving
- Potential validation support for picking workflows in the future

## Expansion Potential

- Can be used for any vendors
- Works best with barcodes, but can also use scanner text input or voice input where needed
- May be adapted into a picking validation tool if packing lists and location data can be integrated reliably
- Especially useful for onboarding newer workers who are not yet familiar with part numbers
