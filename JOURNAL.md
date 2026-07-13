## Week 7 — Issue selection

**Issue link:** [https://github.com/jamjamgobambam/pathreview/issues/21]

**Issue title:** [Review generator returns raw JSON string instead of parsed feedback object]

**Tier:** [x] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
The review generator sometimes returns a raw JSON string instead of a parsed feedback object because the output parser expects the LLM response to be wrapped in a JSON code fence. When the model returns valid JSON without the code fence, the parser fails to extract the data and passes the unparsed string to the API and frontend. The fix should update the parser logic to handle both fenced and unfenced JSON responses in the RAG generator output parser.

**Branch name:** fix/21-handle-unfenced-json

**Setup confirmation:** [x] App runs locally at localhost:5173

**Cohort ledger:** [x] Issue added to cohort ledger