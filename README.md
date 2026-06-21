# aitools-service

- Track your ai usage, tokens, costs and more
- check past and present data, analyze future prediction

---

- This is for
  - individual users
  - Mid sized
  - Enterprise companies

- This will help user by giving
  - Visibility
  - control
  - Action
  - Get insights
  - Integration
  - Relevant data or analytics, plan spend, usage

- This backend app will be
  - multi-user
  - analytics-heavy
  - scheduled-job-heavy
  - integration-heavy

- Technologies using currently
  - SpringBoot for main backend
  - FastAPI for analytics and future prediction
  - Different AI APIs - OpenAI API, Claude, Gemini, GitHub Copilot, and more
  - PostgreSQL TimescaleDB
  - AWS ECS for hosting

---

### User Flow

1. User saves API key
2. System validates key
3. Background job fetches usage/costs
4. Store snapshots in DB
5. Dashboard reads from DB

---

## Example AI tool
### OpenAI

I have two types of openai api key -

- sk-proj-...
- sk-admin-...

### Api key Architecture

Platform users/companies will:

- Create account
- Create organization
- Add:
  - sk-proj
  - sk-admin
- backend encrypts them
- Store them dynamically in the database
- Store encrypted keys in PostgreSQL
- Scheduler fetches usage/costs periodically

### Potential Analytics Dimensions

- Total tokens
- Input tokens
- Output tokens
- Cached tokens
- Cost
- Daily spend
- Weekly spend
- Monthly spend
- Requests count
- Model breakdown
- Usage trends
- Cost trends
- Growth rate
- Forecasting
- Burn rate
- Budget prediction
- Cost anomaly detection
- Usage anomaly detection
- Team/org analytics

### For MVP

- Total Cost
- Total Requests
- Total Tokens
- Input vs Output Tokens
- Daily Usage Graph
- Daily Cost Graph
- Model Breakdown
- 30-Day Forecast
- Budget Burn Rate
- Cost Anomaly Alerts
