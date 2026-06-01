# AI Audit Report

## 1. Student Information

| Field | Value |
| :--- | :--- |
| Student name (printed) | Nguyen Nhat Nam |
| Student ID | 23127092 |
| Class / Cohort | 23KTPM2 |
| Assignment ID | HW01-AI |
| Assignment date | 01/06/2026 |
| AI tool(s) used | ChatGPT GPT 5.5 Thinking |
| AI tool(s) used? | Yes |

## 2. Audit Table - One Row per Artifact

### Artifact #1 - AI Impact Analysis for QA/QC Job Postings

| Field | Value |
| :--- | :--- |
| Prompt + Tool | **Tool:** ChatGPT GPT 5.5 Thinking<br>**Time:** 21:02 27/05/2026 to 14:56 28/05/2026<br>**Prompt:** Prompts 01-10 in `prompt_log.md`. I provided each QA/QC job description and asked: "For this JD, can you help me talk about the AI Impact for this job in 1-2 sentence?" |
| AI Output | AI generated 1-2 sentence AI Impact Analysis for 10 QA/QC job postings. The outputs explained how AI can assist QA/QC roles through test case generation, automation support, defect analysis, API testing support, AI-assisted testing tools, and human review. Full outputs are recorded in Appendix A: `prompt_log.md`. |
| Verdict | VALID |
| Reasoning | The AI outputs were relevant to the job descriptions and helped explain how AI can assist, replace, or not replace QA/QC work. The outputs matched the Requirement 1 task of writing AI Impact Analysis for each job posting. |
| Student Fix | I reviewed the AI-generated text against each real job description, checked whether the job actually involved AI/LLM/automation-AI skills, and used the corrected versions in Section 1 of the report. |

### Artifact #2 - QA/QC Role Mindmap

| Field | Value |
| :--- | :--- |
| Prompt + Tool | **Tool:** ChatGPT GPT 5.5 Thinking<br>**Time:** 15:18 28/05/2026<br>**Prompt:** "Create a mindmap for QA/QC ISTQB based on the 10 jobs above, covering key concepts, tools, and practices in software testing and quality assurance." |
| AI Output | AI generated a QA/QC role mindmap image covering QA/QC skills, ISTQB concepts, test levels, testing tools, automation, and AI-augmented QA topics. |
| Verdict | INCOMPLETE |
| Reasoning | The mindmap was useful as a first draft, but it contained mistakes. It misspelled "Test Management", confused ISTQB core principles with general testing ideas, and incorrectly listed "Production" as a test level. The assignment requires students to ask AI for a QA/QC role mindmap and find at least 3 mistakes. |
| Student Fix | I identified and documented 4 issues in Section 1.11 of the report: spelling error, incorrect ISTQB principles, incorrect test level categorization, and image formatting/cropping issue. |

### Artifact #3 - Software Defect Source Suggestions

| Field | Value |
| :--- | :--- |
| Prompt + Tool | **Tool:** ChatGPT GPT 5.5 Thinking<br>**Time:** 15:42 28/05/2026<br>**Prompt:** "Suggest me some websites where the software defects reported on." |
| AI Output | AI suggested websites for finding reported software defects, such as GitHub Issues, Mozilla Bugzilla, Chromium Issue Tracker, HackerOne, Bugcrowd, CVE/NVD Database, GitLab Issues, and Launchpad Bugs. |
| Verdict | INCOMPLETE |
| Reasoning | The output was useful for brainstorming possible defect sources, but it did not directly produce the final 20 defects required by the assignment. Some suggested sources were general bug-reporting platforms, while the final report needed verified defects from 2022-2026 with source links, severity, consequences, and solutions. |
| Student Fix | I used the suggestion as a starting point, then selected and verified defects mainly from OpenAI Community, AI Incident Database, Snyk, and NVD. I added source links and wrote the final 20-defect analysis in Section 2. |

### Artifact #4 - AI Hallucination / Bias Finding for RAG Chatbot Defect

| Field | Value |
| :--- | :--- |
| Prompt + Tool | **Tool:** ChatGPT GPT 5.5 Thinking<br>**Time:** 20:53 30/05/2026<br>**Prompt:** "Explain the RAG chatbot defect where a vector database is not always queried and the chatbot sometimes hallucinates despite an attached dataset. Include the root cause, consequences, and solution." |
| AI Output | AI explained that the RAG chatbot defect occurs when the retrieval step is not enforced, causing the chatbot to answer from general model knowledge instead of the attached dataset. It also suggested general RAG solutions such as enforcing retrieval, adding citations, improving chunking, embeddings, similarity thresholds, retrieval monitoring, and RAG test cases. |
| Verdict | INCOMPLETE |
| Reasoning | The answer was partly correct but too generic. It did not fully address the specific OpenAI API context from the verified forum source. The AI gave general RAG advice, but the actual issue in the report was more specifically related to API configuration, especially whether the system forces file/vector search or allows the model to decide automatically. |
| Student Fix | I corrected the explanation in Section 2.4. I identified this as generalization bias because the AI gave a plausible generic RAG explanation instead of focusing on the specific OpenAI API issue. I corrected the root cause and solution by emphasizing `tool_choice = "required"` and stronger grounding instructions. |

### Artifact #5 - Physical Product Test Cases for Air Conditioner Remote

| Field | Value |
| :--- | :--- |
| Prompt + Tool | **Tool:** ChatGPT GPT 5.5 Thinking<br>**Time:** 13:16 01/06/2026<br>**Prompt:** "For this model of the air conditioner and this remote, create for me 12 test cases and description, expected output to test this air conditioner remote in English." |
| AI Output | AI generated 12 test cases for a Panasonic air conditioner remote, including Power ON/OFF, COOL mode, DRY mode, AUTO mode, temperature increase/decrease, minimum/maximum temperature limit, fan speed, air swing, Powerful/Quiet mode, and Timer ON/OFF setting. |
| Verdict | INCOMPLETE |
| Reasoning | The generated test cases covered normal functional behavior, but the assignment requires 15 test cases and at least 3 edge cases that AI missed. The AI did not include enough abnormal or real-world edge cases such as unstable signals, blocked remote signal, or rapid repeated button pressing. |
| Student Fix | I expanded the set from 12 to 15 test cases by adding TC13, TC14, and TC15. These student-added edge cases cover rapid temperature button pressing, blocked remote signal, and weak battery/unstable signal behavior. |

## 3. Summary of AI Accuracy

| Metric | Count | Percentage |
| :--- | :--- | :--- |
| Total AI-generated artifacts audited | 5 | 100% |
| VALID | 2 | 40% |
| INVALID | 0 | 0% |
| INCOMPLETE | 3 | 60% |

## 4. Conclusion - When should AI be used or not?

AI should be used for brainstorming, drafting, organizing information, and generating first versions of test cases or report sections. In this homework, AI was helpful for writing AI Impact Analysis, creating a QA/QC mindmap draft, suggesting defect sources, explaining an AI-related defect, and generating initial test cases for the air conditioner remote.

However, AI should not be treated as the final authority. It missed edge cases, produced incomplete or overly general explanations, and required source verification. For software testing work, AI should be used as a support tool, while the student must verify sources, check correctness, execute tests, and add missing boundary or edge cases.

## 5. Mandatory Disclosure

[Test cases / defect analysis / QA-QC mindmap / report structure] was initially generated by ChatGPT GPT 5.5 Thinking; I reviewed and modified the QA/QC job analysis, verified and corrected the software defect source links, added edge cases TC13, TC14, and TC15 for the physical product testing section, and wrote the final evidence collection and self-assessment by myself. The detailed AI Audit Report is attached as Appendix A. I confirm I did not use AI to generate any artifact listed in the prohibited category.

## Signature

| Field | Value |
| :--- | :--- |
| Student name (printed) | Nguyen Nhat Nam |
| Student ID | 23127092 |
| Class | 23KTPM2 |
| Course | CSC13003 - Software Testing |
| Instructor | Dr. Lam Quang Vu / Dr. Tran Duy Hoang / MSc. Tran Thi Bich Hanh / MSc. Truong Phuoc Loc / MSc. Ho Tuan Thanh |
| Date | 01/06/2026 |
| Signature | Nguyen Nhat Nam |
