# DGI-WarehouseTools

DGI-WarehouseTools is the main landing repository for this warehouse tool suite.

## Shared Overview

A suite of software tools built to reduce item discrepancies, improve accuracy and efficiency, and make warehouse workflows easier to learn, use, and scale.

These tools are designed around scanner-friendly workflows and Google-based systems such as Google Sheets, Apps Script, Google Forms, and Google accounts. The goal is to build practical, low-cost tools that work well on mobile scanners and computers while improving accessibility, speed, and accuracy.

## Why This Stack

The suite is built on the Google ecosystem because it is:

- Free and practical for a zero-dollar software budget
- Scalable for small or growing warehouse teams
- Familiar to most users who already know spreadsheets or Google tools
- Accessible across scanners, phones, and computers
- Easy to build on top of existing workflows
- Flexible enough to support independent warehouse processes outside vendor systems

## Repository Purpose

This repository serves as the shared, high-level index for the warehouse tool suite. Each tool has its own README with details about its purpose, workflow, features, benefits, and potential future improvements.

## Tool README Links

- [Company A Temporary/Overstock Database](company-a-temporary-overstock-database/README.md) - Temporary and overstock location tracking outside Company A's system.
- [Company B Counter Template](company-b-counter-template/README.md) - Scanner-based serial number counting and duplicate detection for Company B and similar products.
- [Company C Receiving Template](company-c-receiving-template/README.md) - Packing list based receiving workflow for barcode scanning and part validation.
- [Misc. Receiving Template](misc-receiving-template/README.md) - Lightweight electronic receiving template for manual quantity entry.
- [Automatic Label Maker](automatic-label-maker/README.md) - Form-based label generation for faster and cleaner warehouse label printing.

## Common Themes Across the Tools

- Barcode-first workflows where possible
- Reduced dependence on paper and pencil processes
- Less manual data entry
- Better auditability through timestamps and logs
- More accessible workflows for current and new workers
- Flexible use across scanners, phones, and desktop computers
- Potential expansion into both receiving and picking workflows

## Current Considerations and Future Opportunities

- Picking and receiving are closely related workflows, and some receiving tools may be adapted for picking
- There may be opportunities to bring CloudSuite workflows onto mobile devices
- Packing list import into Sheets can likely be streamlined further
- Bin-location retrieval during receiving is still an open problem
- Scanner hardware has additional untapped features such as scan-text and voice input
- Secure sharing is important so users can benefit from the tools without exposing implementation details
- Full real-time integration with CloudSuite is not currently in place, but may be possible in the future
