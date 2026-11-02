# Prompt Scorecard

## Prompt Version

P1.1

---

## Test Scenario

Analyze the customer support ticket and provide a brief summary of the customer's issue along with the most appropriate next support action. Consider the ticket category, priority, issue description, and current status when making your recommendation. Keep the response concise, professional, and limited to 2-3 sentences.


Input:
Query ID: 1002

---

## Model Used

Microsoft Copilot

---

## Accuracy

4

---

## Clarity

4

---

## Consistency

4

---

## Completeness

4

---

## Improvement Notes

Improving tone of text generation.

---

## Prompt Version

P1.2

---

## Test Scenario

You are a Senior Enterprise Customer Support Specialist. You always provide your response in professional tone.

Analyze the customer support ticket and provide a brief summary of the customer's issue along with the most appropriate next support action. Consider the ticket category, priority, issue description, and current status when making your recommendation. Keep the response concise, professional, and limited to 2-3 sentences.

Input:
Query ID: 1002

---

## Model Used

Microsoft Copilot

---

## Accuracy

4

---

## Clarity

5

---

## Consistency

4

---

## Completeness

4

---

## Improvement Notes

Add grounding data: support_faq.txt
Add constriants to get consistent and reproducible output.
---


## Prompt Version

P1.3

---

## Test Scenario

You are a Senior Enterprise Customer Support Specialist. You always provide your response in professional tone.

Analyze the customer support ticket and provide a brief summary of the customer's issue along with the most appropriate next support action. Consider the ticket category, priority, issue description, and current status when making your recommendation. Keep the response concise, professional, and limited to 2-3 sentences.

Constraints:
●	Do not assume missing information.
●	Do not generate unsupported recommendations.
●	Use only the provided business documents.
●	Keep the response professional.

Input:
Query ID: 1002

---

## Model Used

Microsoft Copilot

---

## Accuracy

5

---

## Clarity

5

---

## Consistency

5

---

## Completeness

4

---

## Improvement Notes

Add Output format to get complete response 

---


## Prompt Version

P1.4

---

## Test Scenario

You are a Senior Enterprise Customer Support Specialist. You always provide your response in professional tone.

Analyze the customer support ticket and provide a brief summary of the customer's issue along with the most appropriate next support action. Consider the ticket category, priority, issue description, and current status when making your recommendation. Keep the response concise, professional, and limited to 2-3 sentences.

●	Do not assume missing information.
●	Do not generate unsupported recommendations.
●	Use only the provided business documents.
●	Keep the response professional.

Provide your response in following output format
●	Customer Summary
●	Root Cause
●	Recommended Resolution
●	Priority Level
●	Suggested Next Action


Input:
Query ID: 1002

---

## Model Used

Microsoft Copilot

---

## Accuracy

5

---

## Clarity

5

---

## Consistency

5

---

## Completeness

5

---

## Improvement Notes

No improvements required.

---


## Overall Findings
Progressive prompt refinement improved output quality significantly. Adding role definition, grounding constraints, and a structured output format increased clarity, consistency, accuracy, and completeness, resulting in more reliable and professional responses.

---

## Best Performing Prompt

**P1.4**

Reasons:
- Achieved the highest overall scores across all evaluation criteria.
- Included clear role definition, constraints, and explicit output structure.
- Produced consistent, complete, and professional responses with minimal variability.

---

## Improvement Opportunities


- Define expected response length more precisely for reproducibility.
- Test against multiple ticket categories and priority levels to validate robustness.


---

## Lessons Learned


- Role-based instructions improve response tone and professionalism.
- Constraints reduce hallucinations and unsupported recommendations.
- Grounding with business documents increases accuracy and reliability.
- Structured output formats significantly improve completeness and consistency.


---

## Final Recommendation
Adopt **Prompt Version P1.4** as the production prompt template. It delivers the most accurate, consistent, complete, and professional output while ensuring responses remain grounded, structured, and aligned with enterprise support requirements.
