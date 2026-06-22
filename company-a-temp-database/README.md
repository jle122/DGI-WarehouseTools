# Company A Temporary/Overstock Database

## Stack

Google Sheets + Apps Script automation + Barcode Scanner

## Problem

Our company acts as a distributor for Company A, with onboarding occurring around 2-3 years ago. Company A uses a completely different and separate enterprise software to do their sales orders, inventory control, and warehouse management, leading to our employees to have to learn their system on top of our current system. (For reference, most vendors usually apply through our previously established enterprise software and inventory control is updated through a direct data pipeline). As a subsidary of Company A, we are restricted to the permissions the administrators put on us. This includes no access to adding new locations and changing fixed locations. All updates must be done through requests to Company A. This creates delays and limits flexibility when trying to track overstock or temporary storage locations, especially when waiting for approval or updates in Company A's system.

## Purpose

This tool provides an independent way to track overstocked or temporarily located items outside of Company A's system, giving our warehouse the flexibility to put items where we want. 

## Impact

An estimated 20% efficiency increase in order picking. Workers are now more inclined to find overstocked items as needed by referencing the database. The time + multiple location log also increases capabilities for tracking missing items/pallets. The database removes a bottleneck on knowledge of these overstocked locations, so operations can stay up when workers specializing in overstocked locations are absent.

## How it Works
- **Rows 1-2 (up to Col. E):** Merged together to make a big Title
- **Row 3:** Column headers
- **Rows 4 downwards:** One row represents one item.
- **Col. A: Date/time**. Automatically generated upon edit to Col. B
- **Col. B: Item ID**. Can be typed/scanned in.
- **Col. C: Quantity**. Not updated automatically. Used optionally for our purposes as Company A tracks real-time quantity. 
- **Col. D: Default location**. Where the item is normally stored/fixed location on Company A's database.
- **Col. E onwards**: Space for overstocked locations. No restriction on formatting of location, and code generates a timestamp within the edited cell to let users know when location was inputted. Allows for [x] amount of locations for a specific item.

## Features

- Space for product name and quantity
- Space for as many locations as needed for overstocked items
- Duplicate detection to alert when a product already exists in the database
- Automatic date tracking for database entry
- Automatic time recording for location updates

## Operational Benefits

- Reduces dependency on a third-party inventory process
- Improves access to location knowledge beyond a few experienced workers
- Helps current and new workers find overstock more easily
- Supports continuity when key workers are absent
- Lower risk of losing items due to untracked location changes
- Holding temporary locations while waiting for Company A to add official locations
- Highly flexible use

## Expansion Potential

While designed for Company A, we are starting to implement this database format to other vendors that require overstock locations. It can be adapted anywhere a warehouse needs temporary or unofficial location tracking.
