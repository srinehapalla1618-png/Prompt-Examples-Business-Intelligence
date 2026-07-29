# Prompt-Examples-Business-Intelligence
Prompt and golden-answer examples for data and BI analysis tasks

## Business Intelligence

### Example 1

**Prompt**
 "Our Q3 revenue grew 12% year-over-year, but our Q3 net profit margin dropped from 18% to 14%. Marketing spend increased 40% and COGS stayed flat as a % of revenue. What's most likely driving the margin compression, and is the 40% marketing increase justified?"

**Why I picked this one**
There's enough here to actually pin down the cause — since COGS is flat, the margin drop has to be coming from opex, and marketing spend growing at 40% against 12% revenue growth is the obvious lever. I want to see if a model does that arithmetic or just says "several factors could be at play" and dodges.

**What the golden answer has to nail**
- Has to actually isolate marketing spend as the driver, using the fact that COGS is ruled out.
- Show the logic, not just the conclusion.
- On "is it justified" — the honest answer is we don't know yet, because spend growth alone doesn't tell you about ROI or CAC. A good answer says that instead of guessing yes or no.
- Should note 12% growth is fine but not spectacular, so the marketing spend isn't clearly paying for itself yet.

### Example 2

**Prompt**
 "We ran an A/B test on our checkout page for 2 weeks. Variant B converted at 4.8% vs. Variant A's 4.2%, with 3,000 visitors per variant. Should we roll out Variant B to everyone?"

**Why I picked this one**
The sample size and lift here are small enough that this could easily be noise rather than a real effect, and a lot of people (and models) will just see "B is bigger" and call it a win. I want to test whether the answer actually engages with statistical significance instead of taking the raw numbers at face value.

**What the golden answer has to nail**
- Has to raise the question of statistical significance directly — a 0.6 point lift on 3,000 visitors per arm is a size where the result could plausibly be noise, and the answer shouldn't just accept it as a real effect without saying that.
- Shouldn't just say "run a significance test" and stop — should explain in plain terms why sample size and effect size both matter here.
- If it can't run the actual calculation, it should still be honest that a firm recommendation isn't possible without knowing the test's significance level.
- Should mention practical considerations too — did anything change mid-test, was traffic split evenly, any seasonality in those two weeks — since those affect trustworthiness of the result as much as the raw numbers do.

---
