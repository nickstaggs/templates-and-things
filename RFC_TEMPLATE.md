---
authors: Nick Staggs (nick.c.staggs@gmail.com)
state: <draft || in-progress || complete>
---

<!-- Feel free to remove any sections that are not relevant for the feature/application being developed -->

# RFC <NUM> - <TITLE>

## Summary

<!-- One paragraph overview of the problem and proposed solution -->
<!--
If I had 60 seconds with a stakeholder, what would I say this RFC is about?
What will be different for users after this ships?
-->

### Problem Statement

<!-- 
What is broken / missing today?  
Who is affected?  
What pain are we removing? 
What concrete behavior do we see today that proves this is a problem?
What happens if we do nothing for 6 months?
Is this a user problem, a business problem, or a technical debt problem?
-->

### Goals

<!--
How will we know this is successful?
What measurable outcome changes after this ships?
What are the metrics that proved the needle was moved?
What does “done” look like?
-->

### Non-Goals

<!--
What tempting scope are we explicitly refusing to take on?
What problems are adjacent but intentionally postponed?
-->

## Key Decisions

| Decision | Options Considered | Chosen | Rationale |
|----------|-------------------|--------|-----------|
<!-- | Auth mechanism | JWT, session cookies | JWT | Needed for cross-service auth |
| API style | REST, GraphQL | REST | Simpler for current clients | -->

<!--
Which choices here are hard to reverse later?
Which decisions would future engineers want to understand?
-->

<!--
For each row:
What would break if we chose a different option?
What constraints forced this decision?
-->

## Architecture

<!--
Where does this fit in the existing system?
What existing components does this depend on?
What new coupling does this introduce?
What part of this is most likely to become slow or brittle over time?
Is this in a critical path?
-->

### High-Level Flow

## Data Model

### Entities

<!-- #### User
```json
{
  "id": "uuid",
  "email": "string",
  "createdAt": "timestamp"
} -->
<!-- ##### Relationships
Users -> Orders (1:N) 
-->

<!--
For entities:
What data must exist for this feature to work?
What data is source-of-truth vs derived?
What data has privacy or compliance implications?
-->

<!--
For relationships:
What invariants must always hold?
What happens if these relationships are violated?
-->

## UI

<!-- A brief description of the UI -->
<!--
What user journey does this enable?
What is the happy path?
What is the most likely confusion point?
-->

### Wireframes

<!-- Create some basic figmas and include them here -->

### Reusable components


### Site url paths


### Error States

<!-- This should be done per page/url path and it should detail the API response codes that cause them and what it means as well as what should be shown -->
<!--
What errors are user-actionable vs system-actionable?
What should the user do next when this happens?
-->

## API

<!-- Details endpoints including path, description, payload, response codes, and response structure -->

<!-- * POST /api/login
    * Payload
        ```json
        {
            "username": "<username>",
            "password": "<password>"
        }
        ```
    * Responses
        * 200 
        * 401 -->

<!--
Who is the primary consumer of this API?
Is this API designed for humans, machines, or both?
What backward-compatibility guarantees are we making?
-->

<!--
For each endpoint:
Is this idempotent?
Is this safe to retry?
-->

## Security

<!--
Where are the security boundaries?
Where does trust begin and end?
Where do we rely on trust rather than verification?
-->

### Authentication/Authorization
<!--
Who can do this?
Who must never be able to do this?
What is the blast radius if auth fails?
-->

#### User Management

### Concerns

<!-- 
What are common threats for this application/feature and how are they going to be mitigated? 
What would an attacker most want from this system?
What would be the worst-case abuse scenario?
-->

## Testing

<!-- 
What kind of testing makes sense? Think of the testing pyramid and what are the most critical components 
What would be catastrophic to get wrong?
What is cheap to test vs expensive to test?
Where do we want fast feedback vs high confidence?
-->

## Observability

### Logging

<!-- 
What should be logged?
What should be redacted? 
What would I want to see in logs during a 2am incident?
What must never appear in logs?
-->

### Metrics

<!-- Key SLIs / SLOs -->
<!--
What tells us this is healthy?
What tells us users are unhappy before they complain?
-->

### Tracing

<!-- 
Which requests must be traceable end-to-end? 
If this breaks in prod, which span will I wish I had?
-->

## Failure Modes

| Failure Scenario | Likely Cause | User Impact | System Impact | Mitigation |
|------------------|--------------|-------------|---------------|------------|
<!-- | Auth service timeout | Downstream outage | Login fails | Request backlog | Timeout + circuit breaker |
| DB connection pool exhausted | Traffic spike | Slow responses | Thread starvation | Rate limiting + autoscale |
| Third-party API returns 500 | Vendor incident | Feature degraded | Retry storms | Bulkhead + fallback | -->

<!--
What are the dependencies and their failure modes?
What is the most likely thing to go wrong?
What is the worst thing that could go wrong?
What failure would page someone at 2am?
What dependency do we trust the most and should we?
-->

## Deployment

<!-- 
Does this need a rollout plan? 
Is there any kind of data migration needed?
Can we roll it back without data loss?
What needs to be true before rollout?
-->

## Assumptions

<!--
What am I assuming about users, traffic, or infrastructure?
What assumptions would hurt the most if wrong?
-->

## Open Questions

<!--
What do I not know yet that could change the design?
What decisions am I deferring because they aren’t urgent today, even though I could make a reasonable call now?
-->

## Risks

<!--
What could go wrong even if we execute perfectly?
What is the plan if this risk materializes?
Are there any projects that rely on this one?
What happens if we go over time?
What happens if we go over budget?
What happens if the amount of traffic explodes?
-->