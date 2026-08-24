# Creo CAD Design & 3D Printing
> *A hands-on Creo CAD project where I designed an airplane model and a personalised stand featuring my name, learning through failed iterations, dimension changes and repeated design improvements before producing the final 3D-printed result.*

---

## Table of Contents
1. [Project Overview](#1-project-overview)
2. [Objectives](#2-objectives)
3. [Project Scope & Tools](#3-project-scope--tools)
4. [Data Workflow](#5-data-workflow)
5. [Analysis & Metrics](#8-analysis--metrics)
6. [Key Insights](#9-key-insights)
7. [Assumptions & Limitations](#11-assumptions--limitations)
8. [Future Enhancements](#12-future-enhancements)
9. [Author](#14-author)

---

## 1. Project Overview

<!--
  Write 3–5 sentences in plain language.
  Cover: context → problem → approach → outcome.
  Read it out loud. If it sounds like a form - rewrite it.

  WHAT GOOD LOOKS LIKE:
  "A mid-size retail business was seeing inconsistent revenue across
  its regional stores but couldn't identify the root cause. This project
  explored 18 months of transaction data across five regions to determine
  whether underperformance was driven by sales volume, pricing, or return
  rates. The analysis revealed that one region's gap was almost entirely
  explained by an unusually high return rate on a single product category -
  a finding invisible in the company's top-level reporting."

  WHAT TO AVOID:
  "This project analyzes sales data to find trends and insights."
  (Too vague. Could describe 10,000 projects. Describes none of them.)
-->

**Context:** I used Creo CAD to design a detailed 3D airplane model and a personalised display stand featuring my name, which was then developed into a 3D-printed prototype.

**Problem Statement:** The challenge was to create accurate proportions and dimensions while learning from failed design attempts and improving the model through repeated iterations.

**Approach:** I developed the designs step-by-step in Creo CAD, changing dimensions and features where needed. I also used basic statistical comparisons between design iterations to assess changes in dimensions and improve consistency before printing.

**Outcome:** The final result was a refined Creo CAD airplane and personalised stand, followed by a physical 3D print. The project developed my skills in CAD modelling, dimensional analysis, basic statistics, problem-solving and iterative engineering design.

---

## 2. Objectives

<!--
  Write objectives that are specific enough to succeed or fail.
  Use action-oriented verbs: Identify, Determine, Quantify, Build, Evaluate.

  WHAT GOOD LOOKS LIKE:
  ✅ "Determine whether customer churn rate correlates with support ticket volume."
  ✅ "Identify the top three revenue-driving product categories across all regions."
  ✅ "Build a reproducible pipeline that ingests and cleans daily sales exports."

  WHAT TO AVOID:
  ❌ "Explore the data."
  ❌ "Gain insights."
  ❌ "Understand trends."
  (These can't fail - which means they can't succeed either.)
-->

- **Primary Objective:** Design and develop a detailed airplane model and personalised name stand in Creo CAD, taking the concept through multiple design iterations to a final printable version.
- **Secondary Objective 1:** Evaluate and refine dimensions, proportions and features by identifying failed designs and making controlled changes between iterations.
- **Secondary Objective 2:** Apply basic statistical comparison to review dimensional changes between iterations and support more consistent design decisions.
- **Secondary Objective 3:** Produce and evaluate a physical 3D-printed prototype, comparing the final printed result with the original CAD design.

> 💡 *Every analysis decision in this project traces back to one of these objectives.*

---

## 3. Project Scope & Tools

### Scope

<!--
  WHAT GOOD LOOKS LIKE:
  In Scope: "Transaction-level data for Regions A–E, Jan 2023–Jun 2024.
             Analysis covers revenue, return rates, and product category performance."
  Out of Scope: "Customer demographics and marketing spend data were excluded -
                 demographic data was incomplete for two regions, and marketing
                 data sits in a separate system outside this engagement."

  WHAT TO AVOID:
  ❌ Leaving Out of Scope blank. This is the section that protects your credibility.
     If you don't define the fence, reviewers assume you missed things.
-->

| Dimension | Details |
|-----------|---------|
| **In Scope** | Designing a 3D airplane and personalised name stand in Creo CAD, refining dimensions through multiple iterations, and producing the final designs using 3D printing. |
| **Out of Scope** |Advanced aerodynamic simulation, CFD, FEA and industrial-scale manufacturing, as the project focused on CAD development, iteration and prototyping. |
| **Time Period** | CAD design, testing, refinement and 3D-printing stage of the project. |
| **Granularity** |Individual CAD features, dimensions and design iterations, followed by comparison of the final CAD model with the 3D-printed prototype. |

### Tools & Technologies

<!--
  List only what you actually used on this project.
  This is not your skills section - it's the project's technical context.
-->

| Category | Tool(s) Used |
|----------|-------------|
| CAD Design | Creo CAD |
| Analysis | Dimensional measurements & statistics |
| Manufacturing| 3D Printer |
| Documentation | Markdown / GitHub |
| Version Control |Git / GitHub |

---

## 4. Data Workflow

<!--
  Show how data moved through your project - from source to output.
  Every transformation decision should be traceable here.

  WHAT GOOD LOOKS LIKE:
  1. Source: "Monthly CSV exports pulled from the internal POS system.
              Five files, one per region, covering Jan 2023–Jun 2024."
  2. Ingestion: "Loaded into Python using pandas. Files concatenated into
                 a single dataframe (approx. 340,000 rows)."
  3. Cleaning: "Removed 1.2% of rows with null transaction IDs.
                Standardised date formats across regional files.
                Resolved product category naming inconsistencies (3 variants → 1)."
  4. Transformation: "Created a returns_rate field at product-category level.
                      Aggregated to weekly and regional grain for trend analysis."
  5. Analysis: "Descriptive statistics, regional comparison, return rate
                segmentation by product category."
  6. Output: "Summary report (PDF), annotated notebook, processed CSV."

  WHAT TO AVOID:
  ❌ "Data was cleaned and analysed." (No chain. No decisions. No trust.)
-->

```
[Creo CAD Model]
       ↓
[Record Key Dimensions]
       ↓
[Modify & Iterate Design]
       ↓
[Compare Measurements]
       ↓
[3D Print Prototype]
       ↓
[Compare CAD vs Physical Model]
```

1. **Source:** Dimensions and geometry were taken directly from the Creo CAD airplane and personalised stand.
2. **Ingestion:** Key measurements were recorded from each design iteration for comparison.
3. **Cleaning:** Incorrect or inconsistent dimensions were identified and corrected during the CAD refinement process.
4. **Transformation:** Dimensions were organised by model feature and iteration, with changes calculated using absolute and percentage differences.
5. **Analysis:** Descriptive statistics such as mean, minimum, maximum, range and percentage change were used where multiple measurements were available.
6. **Output:** The final Creo CAD models were converted into 3D-printed prototypes, allowing the digital dimensions and physical result to be compared.

---



## 5. Analysis & Metrics

<!--
  Explain what you measured and how - before you share what you found.

  WHAT GOOD LOOKS LIKE:
  Metric: "Customer Return Rate"
  Definition: "Number of transactions flagged as returns divided by total
               transactions, calculated at product-category and regional grain."
  Why It Matters: "Return rate - not sales volume - was hypothesised to
                  explain regional revenue gaps. This metric tests that hypothesis."

  WHAT TO AVOID:
  ❌ Defining a metric only in code: SUM(returns) / COUNT(transaction_id)
     That's an implementation. Write the plain-language definition here.
     Both belong in your project - the definition in the README,
     the implementation in the code.
-->

### Analytical Approach

The project used an iterative CAD and manufacturing analysis. Key dimensions were measured in Creo and SolidWorks, then compared across design iterations and against measurements taken from the 3D-printed prototypes. This allowed design changes and manufacturing accuracy to be evaluated using numerical evidence.

### Key Metrics Defined

| Metric | Plain-Language Definition | Why It Matters |
|--------|--------------------------|----------------|
| CAD Dimension | Intended measurement from the digital model. | Defines the target size. |
| Physical Dimension | Measurement taken from the 3D-printed model. | Shows the actual manufactured size. |
| Absolute Difference | Difference between CAD and physical measurements. | Shows the dimensional error in mm.|
| Percentage Difference | Difference expressed as a percentage of the CAD dimension. | Makes accuracy easier to compare. |
| Percentage Change | Change between two design iterations.| Shows how much the design was modified. |
| Mean | Average of multiple measurements. | Shows the typical measurement. |
| Range | Maximum − minimum measurement.| Shows measurement variation. |
| Standard Deviation | Measures spread around the mean. | Indicates consistency when enough measurements exist. |

### Calculations

- Absolute Change
New Dimension − Previous Dimension

- Percentage Change
((New − Previous) / Previous) × 100

- CAD-to-Print Difference
Physical Measurement − CAD Measurement

- CAD-to-Print Percentage Difference
((Physical − CAD) / CAD) × 100

- Mean
Σ Measurements / Number of Measurements

- Range
Maximum − Minimum

### Methods Used

- Dimensional measurement
- Design iteration comparison
- Descriptive statistics
- CAD-to-print comparison
- Percentage difference analysis
- Visual inspection of prototypes
- Iterative CAD refinement
- 3D-print validation

---

## 6. Key Insights

<!--
  Findings + implications. Not just what happened - what it means.

  WHAT GOOD LOOKS LIKE:
  ✅ "Return rates, not sales volume, explain Region A's underperformance.
      Region A's return rate on home goods was 34% - more than double the
      company average. Revenue was not lost at the point of sale; it was
      lost post-sale through refunds. This points to a fulfilment or
      product quality issue specific to that region, not a demand problem."

  WHAT TO AVOID:
  ❌ "Region A had lower revenue than other regions in Q4."
     (That's an observation. It describes what happened.
      An insight says what it means and where to look next.)

  Aim for 3–6 insights. Quality over quantity.
-->

**Insight 1: Iterative CAD Refinement Improved the Final Design**
Multiple CAD iterations allowed dimensions and geometry to be refined before manufacturing. This reduced the risk of producing a final prototype with obvious design or proportion issues.

**Insight 2: Digital Design and Physical Manufacturing Are Not Identical**
Comparing the Creo CAD dimensions with the 3D-printed prototype showed that physical manufacturing can introduce small dimensional differences. This demonstrates the importance of validating CAD designs through physical prototypes rather than relying solely on the digital model.

**Insight 3: Dimensional Measurements Supported Design Decisions**
Recording dimensions such as overall length, width, height, wing size and stand dimensions provided measurable evidence for design changes. Percentage change and CAD-to-print difference calculations made these changes easier to evaluate.


---

## 7. Assumptions & Limitations

<!--
  WHAT GOOD LOOKS LIKE:
  Assumption: "Transaction records were assumed to be complete for all five regions.
               No validation was performed against source system record counts."
  Limitation: "The analysis cannot distinguish between returns initiated by
               the customer vs. returns initiated by the business (e.g., recalls).
               If business-initiated returns are concentrated in Region A, the
               return rate finding may reflect a policy decision, not a quality issue."

  WHAT TO AVOID:
  ❌ Leaving this section blank or writing "None known."
     Every project has limitations. Documenting them is a sign of
     analytical maturity - not a confession of failure.
-->

### Assumptions
- CAD dimensions were assumed to represent the intended final design dimensions.
- Measurements taken from the physical prototypes were assumed to be sufficiently accurate for project-level comparison.
- The 3D printer was assumed to be operating correctly and within its normal manufacturing capabilities.
- Design decisions were based primarily on dimensional accuracy, appearance, fit and printability rather than full industrial engineering validation.

### Limitations
- The project did not include FEA, CFD or advanced aerodynamic simulation.
- The number of physical measurements may be limited, reducing the reliability of statistical measures such as standard deviation.
- 3D-printing variables such as layer height, material behaviour, printer calibration and shrinkage can affect physical dimensions.
- CAD-to-print comparisons were limited to the features that could be practically measured.
- The project was developed as a prototype rather than an industrial manufacturing study, so the results should not be treated as full production tolerancing data.

> The project demonstrates the CAD-to-prototype workflow effectively, but a more rigorous engineering validation would require controlled manufacturing conditions, larger measurement samples and formal tolerance, material, stress and performance testing.
---

## 8. Future Enhancements

<!--
  WHAT GOOD LOOKS LIKE:
  ✅ "Automate the monthly data pull from the POS export folder using
      a scheduled Python script, replacing the current manual process."
  ✅ "Expand the return rate analysis to include carrier-level data,
      which was unavailable in this dataset but exists in the logistics system."

  WHAT TO AVOID:
  ❌ "Add a machine learning model."
     (Vague, and disconnected from the actual findings of this project.)
  ❌ Listing aspirational features that don't follow logically from the work.
-->

Add tolerance analysis — define acceptable manufacturing tolerances for important CAD features and compare printed results against them.

Improve prototype validation — investigate the effect of print settings, material and layer height on dimensional accuracy.

Expand engineering analysis — introduce FEA for structural components and CFD/aerodynamic analysis for the airplane design where appropriate.

Develop the opposed-piston engine further — add more detailed moving components and investigate the mechanical motion of the assembly.

Increase dimensional testing — take repeated measurements from multiple printed prototypes to improve statistical reliability.

Automate measurement analysis — use a spreadsheet or Python workflow to automatically calculate mean, range, standard deviation and CAD-to-print percentage differences.

---

## 14. Author

**Aaiza Sohail**
Aerospace Engineering Student

- 🔗 www.linkedin.com/in/aaiza-sohail07
- 📧 as1780@student.le.ac.uk

---

