# Automatic Label Maker

## Stack

Google Forms + Google Docs + Apps Script

## Purpose

A lightweight label generation workflow that replaces handwritten labels and manual copying with form-based on-demand printing.

## Benefits

- Supports on-demand label printing that is cleaner and more legible,
- Easy to use
- Improves efficiency by an estimated 20%.

## Features

- Accessible form-based interface
- Optional fields for flexible inputs
- Adjustable formatting
- Ability to print as many copies as needed depending on skid count
- Fast generation of print-ready labels

## Architecture:
- Google Docs: We utilize 2 docs here. One called Template and one called Live Label. Upon Form Submission, our code copies from Template, pastes to Live Label, and updates arguments.
- Google Forms: The UI of our label maker. Input information and number of skids here. A link to Live Label is provided after form submission to get to the Google Doc.

## Current Workflow

1. Write the label by hand
2. Copy it using the copier
3. Write skid numbers manually when needed

## Updated Workflow

1. Fill out the form
2. Wait a few seconds
3. Open the generated document
4. Print the labels like any normal document
5. Skid numbers automatically generated

## Expansion Potential

This tool could be extended further by standardizing more label formats and integrating more warehouse printing workflows.
