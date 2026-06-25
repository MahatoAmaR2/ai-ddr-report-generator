# AI DDR Report Generator - Solution Architecture

## High-Level Architecture

```text
                    +------------------------+
                    |    User Uploads PDFs   |
                    |------------------------|
                    | • Inspection Report    |
                    | • Thermal Report       |
                    +-----------+------------+
                                |
                                v
                    +------------------------+
                    |  Document Processing   |
                    |------------------------|
                    | • PDF Text Extraction  |
                    | • Image Extraction     |
                    | • Metadata Extraction  |
                    +-----------+------------+
                                |
                                v
                    +------------------------+
                    |   AI Processing Layer  |
                    |------------------------|
                    | • Observation Extractor|
                    | • Thermal Analyzer     |
                    | • Duplicate Removal    |
                    | • Conflict Detection   |
                    | • Root Cause Analysis  |
                    | • Severity Assessment  |
                    +-----------+------------+
                                |
                                v
                    +------------------------+
                    |  Data Structuring      |
                    |------------------------|
                    | • Merge Findings       |
                    | • Attach Images        |
                    | • Handle Missing Data  |
                    | • Validate Output      |
                    +-----------+------------+
                                |
                                v
                    +------------------------+
                    |   DDR Report Generator |
                    |------------------------|
                    | • Client-Friendly Text |
                    | • Embedded Images      |
                    | • Structured Sections  |
                    | • PDF Generation       |
                    +-----------+------------+
                                |
                                v
                    +------------------------+
                    |      Final Output      |
                    |------------------------|
                    | • Detailed DDR Report  |
                    | • Downloadable PDF     |
                    +------------------------+
```

---

# Component Overview

## 1. Document Upload
The user uploads two PDF documents:

- Inspection Report
- Thermal Report

---

## 2. Document Processing

The system extracts:

- Text content
- Images
- Page numbers
- Metadata

### Technologies

- pdfplumber

---

## 3. AI Processing Layer

The extracted content is analyzed using an LLM.

Responsibilities:

- Extract observations
- Extract thermal findings
- Detect duplicate observations
- Detect conflicting information
- Generate probable root causes
- Assess issue severity
- Produce client-friendly explanations

---

## 4. Data Structuring

The processed information is merged into a structured JSON format.

Example:

```json
{
  "propertySummary": {},
  "observations": [],
  "rootCause": {},
  "severity": {},
  "recommendations": [],
  "missingInformation": []
}
```

This intermediate layer improves consistency and makes the system reusable.

---

## 5. DDR Report Generator

The final report is generated with the following sections:

1. Property Issue Summary
2. Area-wise Observations
3. Probable Root Cause
4. Severity Assessment
5. Recommended Actions
6. Additional Notes
7. Missing or Unclear Information

Relevant extracted images are inserted under their corresponding observations.

---

# System Workflow

```text
Upload PDFs
      │
      ▼
Extract Text & Images
      │
      ▼
AI Analysis
      │
      ├── Extract Observations
      ├── Extract Thermal Findings
      ├── Detect Conflicts
      ├── Remove Duplicates
      ├── Assess Severity
      └── Generate Root Causes
      │
      ▼
Merge Structured Data
      │
      ▼
Generate DDR Report
      │
      ▼
Download Final PDF
```

---

# Key Features

- AI-powered document understanding
- Multi-document information merging
- Duplicate detection
- Conflict detection
- Missing information handling
- Image extraction and placement
- Structured JSON intermediate representation
- Client-friendly report generation
- Generalizable workflow for similar inspection reports

---

