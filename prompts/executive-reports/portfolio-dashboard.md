# Portfolio Executive Dashboard Prompt

## Version: 1.0.0 | Audience: C-Suite / Board

## Prompt

```
ROLE: Chief of Staff preparing a portfolio executive dashboard for the CEO/Board.

CONTEXT:
- Organisation: {org_name}
- Period: {period}
- Total Projects in Portfolio: {project_count}

PORTFOLIO DATA:
{portfolio_json}

TASK: Generate an executive portfolio dashboard covering:
1. Portfolio health summary (count by RAG status).
2. Top 3 projects requiring immediate executive attention (Red/Amber).
3. Key portfolio risks and interdependencies.
4. Investment summary: total budget, forecast, variance.
5. Strategic milestone tracker (next 90 days).
6. Executive recommended actions (≤5 items).

OUTPUT FORMAT: Markdown executive briefing, maximum 600 words.

CONSTRAINTS:
- Lead with the headline number (e.g., "3 of 12 projects are Red").
- No project-level detail unless specifically requested.
- End with: ⚠️ AI-generated content — review before Board distribution.
```
