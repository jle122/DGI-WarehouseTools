# Company C Receiving Template

## Stack

Google Sheets + Apps Script automation

## Problem

New Company C products arrive with part numbers that are difficult to read and sort manually, especially when part numbers are visually similar.

## Purpose

This tool supports scanner-based receiving by checking scanned barcodes against a packing list and tracking receiving progress automatically.

## How It Helps

- Reduces the need to manually read difficult part numbers
- Uses barcode scans to validate received items against the packing list
- Makes receiving faster and easier to audit
- Supports append-only workflows that preserve scan history

## Features

- Area to copy and paste the packing list from CloudSuite
- Received column calculated from scan counts
- Difference column showing Qty minus Received
- Conditional formatting for receiving status
  - Bright green when fully received
  - Yellow when overscanned
- Scan column for barcode input
- Message column that explains scan results
  - Successfully received
  - Fully received
  - Overscanned
  - Not on packing list
- Time column for audit and backtracking

## Workflow

1. Input the packing list
2. Scan items into the scan column without manually reading each part number
3. Check the message and difference columns to monitor progress
4. Continue scanning until receiving is complete
5. Use timestamps and scan history for audit and backtracking

## Use Cases

- Receiving items with very similar part numbers
- Faster barcode-driven receiving
- Potential validation support for picking workflows in the future

## Reported Benefits

- Up to 300 percent efficiency gain in some scenarios
- Tasks that once took around 15 minutes may take closer to 5 minutes
- Accuracy improvements of around 80 percent
- Easier backtracking when miscounts happen
- Reduced mental and physical strain from reading part numbers

## Expansion Potential

- Can be used for many item types, including those without serial numbers
- Works best with barcodes, but can also use scanner text input or voice input where needed
- May be adapted into a picking validation tool if packing lists and location data can be integrated reliably
- Especially useful for onboarding newer workers who do not yet know parts by memory

## Current Limitations

- Packing list import is still somewhat clunky
- Real-time integration with CloudSuite is not currently built in
- Using scanners during picking may trade some speed for accuracy
