# Journal Adaptation Task List

This document tracks the step-by-step adaptation of the thesis to Springer Nature journal requirements.

## Phase 1: General Formatting & Document Class
- [x] Replace document class from `\documentclass[11pt]{article}` to `\documentclass[pdflatex,sn-mathphys-num]{sn-jnl}`
- [x] Update package imports to match sn-jnl template requirements
- [x] Remove custom page layout settings (margins, spacing) - let template handle this
- [x] Update bibliography style from `biblatex` with `ieee` to sn-jnl's built-in citation style
- [x] Ensure all figures use Arabic numerals and are cited consecutively
- [x] Ensure all tables use Arabic numerals and are cited consecutively
- [x] Verify figure captions start with "Fig." in bold - sn-jnl handles automatically
- [x] Verify table captions are properly formatted - sn-jnl handles automatically
- [x] Remove custom line spacing (`\linespread{1.2}`)
- [x] Copy sn-jnl.cls to main directory

## Phase 2: Title Page
- [x] Move title from `\title{}` to sn-jnl format
- [x] Ensure title is concise and informative
- [/] Add author information using `\author{}` with proper sn-jnl syntax
  - [x] Add author name(s)
  - [/] Add affiliation(s) with `\affil{}` - **NEEDS USER INPUT FOR ACTUAL AFFILIATION**
  - [/] Add corresponding author email - **NEEDS USER INPUT FOR ACTUAL EMAIL**
  - [ ] Add ORCID if available
- [x] Move abstract from `kapitel/einleitung.tex` to main document using `\abstract{}`
- [x] Verify abstract is 150-250 words (can extend to 450 if needed)
- [x] Ensure abstract contains no undefined abbreviations or unspecified references
- [x] Add 4-6 keywords using `\keywords{}`

## Phase 3: Table of Contents Decision
- [x] **Decision**: Based on sn-article template, table of contents is NOT typically included in journal articles
- [x] Remove `\tableofcontents` from einleitung.tex

## Phase 4: Section Structure Analysis & Planning
Current sections in thesis:
- Introduction (with abstract, hypotheses)
- Theoretical Background and Related Work
- Methodology
- Results
- Discussion
- Conclusion and Outlook
- Appendix

Required/typical journal article sections:
- Introduction
- Materials and Methods (or Methodology)
- Results
- Discussion (or Results and Discussion combined)
- Conclusion
- Acknowledgments (optional)
- Declarations (REQUIRED)
- References
- Appendix (optional)

### Section Restructuring Plan:
- [x] **Keep**: Introduction section (remove abstract, keep hypotheses)
- [x] **Keep**: "Theoretical Background and Related Work" - appropriate for journal
- [x] **Keep**: Methodology section
- [x] **Keep**: Results section
- [x] **Keep**: Discussion section
- [x] **Keep**: Conclusion section
- [x] **Keep**: Appendix section
- [x] **Add**: Acknowledgments section (template created)
- [x] **Add**: Author Contributions statement (in Declarations)
- [x] **Add**: Declarations section (REQUIRED)

## Phase 5: Content Adaptation - Introduction
- [x] Remove `\begin{abstract}...\end{abstract}` from einleitung.tex (moved to main document)
- [x] Remove `\tableofcontents` from einleitung.tex
- [x] Keep hypotheses in Introduction or move to end of Introduction
- [x] Ensure Introduction has no subheadings (journal requirement) - converted to paragraph
- [x] Verify all citations are properly formatted

## Phase 6: Content Adaptation - Background/Related Work
- [x] Decide: Keep as separate section "Background" or merge key content into Introduction
- [x] Keeping as "Theoretical Background and Related Work" - appropriate for journal
- [x] Ensure proper heading hierarchy (max 3 levels)
- [x] Verify all citations

## Phase 11: New Required Sections - Declarations
- [x] **Add "Declarations" section** before references
- [x] Add **Funding** statement
- [x] Add **Competing Interests** statement
- [x] Add **Data Availability** statement (REQUIRED for original research)
- [x] Add **Author Contributions** statement
- [x] Add **Ethics approval** (if applicable) - marked as N/A in template
- [x] Add **Consent** (if applicable) - marked as N/A in template
- [x] Add **Code availability** (highly relevant for this work!)

## Phase 12: Acknowledgments (Optional)
- [x] Add Acknowledgments section if needed (before Declarations) - template created
- [x] Thank funding sources, collaborators, etc. - template provided, commented out

## ⚠️ REQUIRED USER ACTIONS

### Must Update Before Submission:
1. **Author Information** in `thesis_main.tex` (lines ~73-75):
   - Replace `paul.hornig@example.com` with actual email
   - Replace placeholder affiliation with actual institution
   - Add ORCID if available

2. **Code Repository** in `declarations.tex` (line ~50):
   - Add actual GitHub/GitLab repository URL

3. **Review Declarations** in `declarations.tex`:
   - Verify all statements are accurate

## Phase 13-14: Final Checks
- [x] Compile document and verify it works
- [x] Check PDF output
- [x] Verify all citations render correctly
- [ ] Final proofreading
