# Article Title

- **Source:** https://en.wikipedia.org/wiki/Ironies_of_Automation
- **Author:**
- **Published:**
- **Read:**
- **Status:** Unreviewed / Reviewed

## Summary

New, severe problems are caused by automating most of the work, while the human operator is responsible for tasks that can not be automated. Thus, operators will not practice skills as part of their ongoing work. Their work now also includes exhausting monitoring tasks. Thus, rather than needing less training, operators need to be trained more to be ready for the rare but crucial interventions.



## Key Claims

A. **Automation removes the practice that builds expertise.**. 
An AI coding agent can implement features, write tests, debug errors, and modify configuration files. If a developer delegates most of that work, they may gradually lose familiarity with the codebase's details.
When the agent makes a subtle architectural mistake, the developer is expected to catch it. But reviewing unfamiliar code may be harder than writing and understanding it in the first place.

B. **Supervising automation is harder than it looks.**. 
An agent might execute dozens of tool calls, inspect files, change code, run tests, and retry failed operations. A human reviewing the final summary may not see the intermediate decisions or recognize an incorrect assumption.
The supervisor is nominally in control but may lack the information needed to exercise that control effectively.

C. **Automation handles the normal cases, leaving humans the exceptions.**. 
Agents can be effective when tasks resemble their training examples or when tools behave as expected. Failures often arise at the boundaries: unexpected permissions, inconsistent data, unusual system states, ambiguous requirements, or interactions between components.
These are precisely the cases where understanding the underlying system matters most.

D. **Successful automation can conceal deteriorating capability.**  
An agent may complete hundreds of tasks successfully, creating confidence in the workflow. Meanwhile, the human operator gets less practice diagnosing failures and may become less able to judge whether the agent's output is plausible.
The problem becomes visible only when an unusual failure occurs.

## My Assessment

What this implies for designing agentic AI workflows. 
The practical lesson is not to avoid automation. It is to design workflows that preserve the ability to detect and recover from failure.

| Design choice | Why it matters |
|---|---|
| Keep humans involved in selected substantive tasks | Maintains practical expertise instead of relegating people entirely to supervision. |
| Require review of consequential changes | Directs attention to decisions where errors matter most. |
| Preserve logs, diffs, and intermediate results | Lets reviewers reconstruct what the agent did. |
| Use independent validation | Checks results against scientific or operational requirements, not merely the agent's own claims of success. |
| Limit permissions and provide rollback | Prevents an agent from turning an incorrect decision into a larger incident. |
| Exercise manual recovery procedures | Ensures humans can still respond when automation fails. |
## Connections

Related concepts, notes, or prior observations.

## Open Questions

What would I like to verify or investigate further?
