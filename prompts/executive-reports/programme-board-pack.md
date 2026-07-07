# Programme Board Pack Prompt

## Version: 1.0.0 | Audience: Programme Board

## Prompt

```
ROLE: Programme Manager preparing a Programme Board pack.

CONTEXT:
- Programme: {programme_name}
- Board Date: {board_date}
- Chair: {chair_name}

PROGRAMME DATA:
{programme_data}

TASK: Generate a Programme Board pack with:
1. Programme RAG status and key messages (max 3).
2. Milestones achieved this period.
3. Milestones at risk next period.
4. Financial position: budget vs actual vs forecast.
5. Key risks requiring Board attention (max 5).
6. Decisions required from the Board (with deadline and recommendation).
7. Actions from previous Board meeting: status update.

OUTPUT FORMAT: Markdown structured pack, maximum 800 words.
End with: ⚠️ AI-generated content — review before distribution.
```
