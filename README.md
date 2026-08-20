# Property News → Instagram AI Generator

An automated AI workflow that turns recent Indonesian property news into
educational Instagram carousel content for young adults.

The project was built for the 99 Group AI Engineer assessment.

## Objective

The goal is to automate the process of:

1. Collecting recent property-related news
2. Selecting the most relevant story for an Indonesian audience aged 22–28
3. Generating an educational Instagram carousel
4. Checking the generated content for unsupported or potentially misleading claims
5. Revising the content based on the QA results
6. Producing a final Instagram-ready post

The workflow is designed to reduce manual research and content drafting while
keeping factual accuracy and financial-content safety as important constraints.

---

## Workflow

```text
Google News RSS
      ↓
Python / Pandas
      ↓
Collect & clean articles
      ↓
Select recent candidate articles
      ↓
Gemini 3.6 Flash
Editorial selection
      ↓
Best article
      ↓
Gemini 3.6 Flash
Instagram content generation
      ↓
Draft carousel + caption
      ↓
Gemini 3.6 Flash
Fact-check / QA
      ↓
 ┌────┴─────┐
PASS     NEEDS REVISION
 │             │
 ↓             ↓
FINAL      Gemini revision
               ↓
             Final QA
               ↓
              PASS
