# Test Cases — Executive Reporting Agent

## TC-EXEC-001: Happy Path — Green Project

**Input:**
```json
{
  "project_name": "Alpha Digital Transformation",
  "period": "W/E 2024-03-15",
  "rag_status": "Green",
  "schedule_variance_days": 0,
  "budget_variance_pct": -1.5,
  "open_risks": 2,
  "open_issues": 1,
  "decisions_required": []
}
```

**Expected Output:**
- RAG status displayed as 🟢 Green.
- Key messages section present with at least one positive milestone note.
- No "Decisions Required" section (or clearly marked as empty).
- Footer contains AI-generated content warning.
- Total length ≤ 500 words.

---

## TC-EXEC-002: Amber Project with Escalation

**Input:**
```json
{
  "project_name": "Beta ERP Migration",
  "period": "W/E 2024-03-15",
  "rag_status": "Amber",
  "schedule_variance_days": 10,
  "budget_variance_pct": 8.0,
  "open_risks": 5,
  "open_issues": 3,
  "decisions_required": [
    {
      "title": "Approve extended UAT window",
      "deadline": "2024-03-18",
      "recommended_action": "Approve 2-week UAT extension"
    }
  ]
}
```

**Expected Output:**
- RAG status displayed as 🟡 Amber.
- Decisions Required section present with the UAT decision.
- Schedule variance (10 days) surfaced in Schedule section.
- Budget variance (8%) flagged.

---

## TC-EXEC-003: Red Project — No Data

**Input:**
```json
{
  "project_name": "Gamma Cloud Migration",
  "period": "W/E 2024-03-15",
  "rag_status": "Red",
  "schedule_variance_days": null,
  "budget_variance_pct": null,
  "open_risks": null,
  "open_issues": null
}
```

**Expected Output:**
- RAG status displayed as 🔴 Red.
- Agent must flag that data is unavailable and request it from the user.
- No fabricated numbers in the output.
- Escalation note included advising human review.

---

## TC-EXEC-004: Portfolio Summary (Multiple Projects)

**Input:**
```json
{
  "projects": [
    { "name": "Alpha", "rag_status": "Green" },
    { "name": "Beta",  "rag_status": "Amber" },
    { "name": "Gamma", "rag_status": "Red"   }
  ],
  "period": "W/E 2024-03-15"
}
```

**Expected Output:**
- Portfolio summary table with all three projects and their RAG statuses.
- Gamma flagged as requiring executive attention.
- Recommended executive action for the Red project.
