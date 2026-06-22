# Company B Serial Number Counter Template
A flexible template that allows for categorical tracking of different models by serial number, for any amount of model numbers. 
## Stack

Google Sheets + Apps Script automation

## Problem

Company B ships units that requires tracking by serial number. The current workflow for Company B products often involves receiving a high amount of units, writing serial numbers by hand/typing, counting on paper, and then manually entering the results into Company B's database. This process is slow and introduces multiple opportunities for error at any point in the process.

## Purpose

This template streamlines that process, providing a scanner-based counting workflow for products with serial numbers, with built-in duplicate detection and automatic counting.

## Operational Benefits/Impact

- Increase of roughly **300%** in operational speed
- Significant accuracy improvement when using barcode scans instead of handwritten entry (**almost 100%**)
- Easier identification of missing units
- Reduced money lost from picking errors
- Easier for more people to perform accurately
- Greater independence from Company B's system
- Already in a printer-friendly format for the customer/sales.

## How It Helps

- Eliminates manual handwritten serial number entry
- Reduces duplicate entry mistakes
- Removes the need for separate manual counting
- Makes it easy to copy and paste results into Company B's database

## How It Works
- **Row 1: Count.** No need to edit anything in this row. A count of non-empty cells in the column (not counting row 2) will automatically appear upon input from Row 3 downwards.
- **Row 2: Model** Put the name of the model you are tracking here.
- **Row 3 downards:** Input serial numbers based on part number. For example, you see SN '1234' is from model E. Click on the next empty cell in model E's column, and scan the barcode.
- **Conditional formatting** will highlight duplicates in **red** to alert that you scanned the same SN twice. 

## Features

- Independent columns that each act as their own category
- Automatic counters within each column
- Duplicate detection logic
- Flexible layout that can use as many or as few columns as needed
- Printable format with ready-made categories

### Picking and Receiving Company B Unit sample workflow

- Create categories for different unit types based on the packing list
- Scan serial numbers into the matching columns
- Let the sheet count automatically
- Avoid recounting and duplicate checking
- Check against packing list after scanning.
- A worker can walk a shipment, scan units directly into the sheet from the scanner, and complete the data collection process without having to stop and manually write everything down first.

## Real Run Example
- 56 units
- 7 different models
- Quantities checked, serial numbers recorded exactly, and entered into Company B's system in 19 minutes and 15 seconds

## Expansion Potential

Any vendors with serial numbers can use this template. In the case that some products have serial numbers but no barcode, our scanners have **cameras** that allow for text scanning. The text scanning is seamless with Google Sheets.
