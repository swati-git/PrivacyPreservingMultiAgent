## Privacy Filter Agent(Entry Point)
- Purpose: First line of defense - detects and blocks sensitive information
Responsibilities:
- Scan incoming queries for PII (names, emails, SSNs, credit cards)
- Detect confidential markers ("confidential", "internal only", client names)
- Check against company's sensitive entity list
- Flag queries that might contain proprietary information

Decision Logic:
IF query contains PII/sensitive data:
  → Route to Anonymization Agent
ELSE IF query is safe:
  → Route to Query Router Agent
ELSE IF unclear:
  → Route to Human-in-the-Loop for approval