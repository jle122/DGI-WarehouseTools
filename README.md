# DGI-WarehouseTools

DGI-WarehouseTools is the main landing repository for this warehouse tool suite.

## Shared Overview

A suite of software tools built to reduce item discrepancies, improve accuracy and efficiency, and make warehouse workflows easier to learn, use, and scale.

These tools are designed around scanner-friendly workflows and Google-based systems such as Google Sheets, Apps Script, Google Forms, and Google Workspace. The goal is to take advantage of the Google ecosystem to build practical, low-cost tools that work well on mobile scanners and computers while improving accessibility, speed, and accuracy.

## The Scanners
- Used mainly for one Company's Warehouse Management App.
- Effectively an Android phone with a builtin scanner and camera.
- Scanner acts a keyboard emulator. This realization resulted in the creation of the suite as these tools can be utilized beyond the App it was originally intended.
<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/99db73e6-2243-4b23-91f8-d8b6aabe6876" />

## Why This Stack

The suite is built on the Google ecosystem because it is:
- **Low-cost and practical**
- **Apps Scripts** is phenomenal for spreadsheets that are only hundreds of lines long
- **Scalable/easy** to manage for small or growing warehouse teams
- **Familiar** to most users who already know spreadsheets or Google tools
- Utilize on multiple devices via Google sign-on
- **Easy to configure** on top of existing workflows
- **Flexible** enough to support independent warehouse processes outside vendor systems
- High degree of **creative freedom** despite the controlled ecosystem
- **Secure**, easy to change permissions via **Google Workspace** Super Admin model

## Architecture
- **Google Workspace**: a **Super Admin** email containing all code, owning all sheets/tools, and controlling all aspects of user emails to allow for safe access, sharing, and use of tools
- Tools are shared through Google's share feature
- We use AWS' **Principle of Least Privelege** as our security model. Users in the workspace are restricted to only being able to edit the sheets shared and nothing else for maximum security. Extra permissions are shared as needed.
- Code is shipped with the sheets through Document ID.
- **Main Tradeoff**: Ease of sharing/monitoring for being bottlenecked by a master email. We take this tradeoff here because the number of users and size of data is relatively small, and we want the suite to be easily monitored by one person. As long as Super Admin takes care of master email, this is an effective architecture. 
- Diagram seen below:
<img width="700" height="500" alt="DGI-Tools-Architecture-2" src="https://github.com/user-attachments/assets/066af60a-be86-42ee-a1b7-f78755b6cc14" />

## Design Philosophy and Recurring Patterns
- **User input and seamless fit into current workflows** takes top priority
- **Fast integration and iteration** based on user feedback
- **Flexibility**: Can be applied to multiple vendors/use cases. While designed for a specific problem, tools can often be used in multiple cases.
- **Barcode-first** workflows where possible
- **Better auditability** through timestamps and logs
- Utilizing Google Sheets as UI for a **simpler learning curve**
- Potential expansion into both receiving and picking workflows

## Repository Purpose

This repository serves as the shared, high-level index for the warehouse tool suite. Each tool has its own README with details about its purpose, workflow, features, benefits, and potential future improvements.

## Tool README Links

- [Temporary/Overstock Database](overstock-temp-database/README.md) - Temporary and overstock location tracking outside Company A's system.
- [Serial Number Counter](part number-receiving-template/README.md) - Scanner-based serial number counting and duplicate detection for Company B and similar products.
- [Upgraded Serial Number Counter](serial-number-counter/README.md) - The upgraded Company B Counter Template with automated model recognition.
- [Part Number Receiving Template](upgraded-SN-counter/README.md) - Packing list based receiving workflow for barcode scanning and part validation.
- [Automatic Label Maker](automatic-label-maker/README.md) - Form-based label generation for faster and cleaner warehouse label printing.
- ** To maintain company privacy and confidentiality, vendors/products for which tools are designed are omitted to "Company [x]", and code used is not shared.
