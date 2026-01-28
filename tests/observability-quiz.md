# Observability Quiz for PMs

Test your understanding of observability concepts. Answers are at the bottom - no peeking!

---

## Section 1: Core Concepts

### Q1: Monitoring vs Observability

What's the key difference between monitoring and observability?

- A) Monitoring is free, observability costs money
- B) Monitoring answers pre-defined questions, observability lets you ask arbitrary questions
- C) Monitoring is for engineers, observability is for PMs
- D) They're the same thing with different names

---

### Q2: The Three Pillars

Which of these is NOT one of the three pillars of observability?

- A) Logs
- B) Metrics
- C) Dashboards
- D) Traces

---

### Q3: What is a Trace?

A trace is best described as:

- A) A count of errors per minute
- B) The journey of a single request through all services
- C) A text record of an event
- D) A graph showing CPU usage

---

## Section 2: Observability vs Other Tools

### Q4: Database vs Observability

Your database stores `User { id: 123, name: "Jane" }`. What would observability capture about Jane?

- A) Jane's email address
- B) Jane's password (hashed)
- C) "Jane's checkout request took 5s, failed at payment service"
- D) Jane's order history

---

### Q5: Product Analytics vs Observability

PostHog tells you "30% of users abandon checkout." What question does observability answer?

- A) Which features should we build next?
- B) Why are checkout requests failing or slow?
- C) How many users signed up this week?
- D) What's our NPS score?

---

### Q6: When to Use What

A user reports "the app is slow." Which tool helps you find out WHY?

- A) PostHog (product analytics)
- B) Google Analytics
- C) Honeycomb (observability)
- D) Figma

---

## Section 3: PM-Specific Knowledge

### Q7: Asking Engineering

Which question will get you a better answer from engineering?

- A) "Is the app working?"
- B) "What's the P95 latency for checkout this week?"
- C) "Can you fix the bug?"
- D) "Why is everything so slow?"

---

### Q8: Understanding P95

If the P95 latency is 2 seconds, what does that mean?

- A) All requests take exactly 2 seconds
- B) The average request takes 2 seconds
- C) 95% of requests complete in under 2 seconds
- D) 5% of requests complete in under 2 seconds

---

### Q9: Feature Launch Validation

You just launched a new feature. What should you check in observability?

- A) How many people liked your launch tweet
- B) Error rate and latency for the new feature
- C) Competitor feature comparison
- D) Design review feedback

---

### Q10: Incident Response

During an outage, which question is MOST useful to ask?

- A) "Who broke it?"
- B) "What's the blast radius - how many users are affected?"
- C) "When will it be fixed?"
- D) "Why didn't we prevent this?"

---

## Section 4: Tool Selection

### Q11: High Cardinality

A tool that supports "high cardinality" means it can:

- A) Only work with small datasets
- B) Handle millions of unique values (like user IDs)
- C) Display pretty graphs
- D) Send email alerts

---

### Q12: Tool Matching

Match the strength to the tool:

**Scenario:** You need to debug why a specific enterprise user's request failed.

Which tool is best?

- A) Splunk (log aggregation)
- B) Honeycomb (high-cardinality queries)
- C) CloudWatch (AWS monitoring)
- D) Prometheus (metrics)

---

### Q13: When NOT to Add Observability Tools

When should you NOT invest in better observability?

- A) When you have 1 user and can check the logs manually
- B) When you're a large company with production issues
- C) When debugging takes days
- D) When you can't reproduce bugs

---

## Section 5: Scenario-Based

### Q14: The Support Ticket

A user emails: "The app crashed when I tried to checkout."

With good observability, what's your FIRST step?

- A) Ask the user to try again
- B) Ask for their session ID and look up their trace
- C) Tell engineering "there's a bug"
- D) Check the company Twitter for complaints

---

### Q15: Prioritization

Your observability dashboard shows:
- Feature A: 0.1% error rate, 50 daily users
- Feature B: 2% error rate, 5,000 daily users

Which should you prioritize fixing?

- A) Feature A (lower error rate)
- B) Feature B (more users affected)
- C) Neither, 2% is acceptable
- D) Both equally

---

## Section 6: AI-Specific (Bonus)

### Q16: AI Agent Observability

What makes AI agent observability different from traditional web app observability?

- A) AI agents don't need observability
- B) AI outputs are non-deterministic, so you need to track decision quality
- C) AI is always faster so latency doesn't matter
- D) AI systems don't have costs to track

---

### Q17: LLM Cost Tracking

For an AI product, why is tracking token usage important?

- A) Tokens are a security risk
- B) Tokens = money, and costs can grow quickly
- C) Users care about token counts
- D) Tokens affect UI design

---

---

# Answer Key

**Don't scroll down until you've attempted all questions!**

.
.
.
.
.
.
.
.
.
.

## Answers

| Question | Answer | Explanation |
|----------|--------|-------------|
| Q1 | **B** | Monitoring checks known things (is server up?). Observability lets you ask any question about system state. |
| Q2 | **C** | The three pillars are Logs, Metrics, and Traces. Dashboards are a visualization tool, not a data type. |
| Q3 | **B** | A trace follows a single request through all services, showing the full journey. |
| Q4 | **C** | Databases store business data. Observability captures system behavior - how requests performed. |
| Q5 | **B** | Product analytics finds the what (users abandon). Observability finds the why (checkout is failing/slow). |
| Q6 | **C** | Honeycomb and similar observability tools let you trace slow requests to find root causes. |
| Q7 | **B** | Specific, measurable questions ("P95 latency for checkout") get better answers than vague ones. |
| Q8 | **C** | P95 = 95th percentile. 95% of requests are faster than this number. |
| Q9 | **B** | Check error rates and latency to validate the feature is working, not just that it shipped. |
| Q10 | **B** | "Blast radius" (affected users) helps prioritize and communicate impact to stakeholders. |
| Q11 | **B** | High cardinality = many unique values. Important for querying by user ID, session ID, etc. |
| Q12 | **B** | Honeycomb excels at querying specific users/sessions due to high-cardinality support. |
| Q13 | **A** | For tiny scale, manual debugging is fine. Invest in observability when scale makes it necessary. |
| Q14 | **B** | With good observability, you can look up exactly what happened in their session. |
| Q15 | **B** | Feature B affects 100 users/day (5000 × 2%), Feature A affects 0.05 users/day. Prioritize by impact. |
| Q16 | **B** | AI is non-deterministic - same input can give different outputs. Need to track decision quality, not just success/failure. |
| Q17 | **B** | LLM API calls cost money per token. Without tracking, costs can spiral unexpectedly. |

---

## Scoring

| Score | Level |
|-------|-------|
| 15-17 | Expert - You understand observability deeply |
| 12-14 | Proficient - Solid foundation, minor gaps |
| 9-11 | Developing - Review the fundamentals |
| 0-8 | Beginner - Start with [01-Fundamentals.md](../learn-code/observability/01-Fundamentals.md) |

---

## Further Reading

- [Observability Fundamentals](../learn-code/observability/01-Fundamentals.md)
- [Tools Overview](../learn-code/observability/02-Tools-Overview.md)
- [Observability for PMs](../learn-code/observability/04-For-PMs.md)
- [AI Agent Observability](../08-AI-Skills/04-Building-Agents/05-Observability.md)
