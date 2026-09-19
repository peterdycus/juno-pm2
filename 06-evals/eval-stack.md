**Evaluation Stack · Juno PM**

**User Feedback (Online)**

Signals captured: 
Active: thumbs up/down, regenerate, edit-before-send, free-text reason on thumbs-down. 
Passive: dismiss/suppress, time-to-first-action, abandon rate.

Cadence: Capture per request in real time; review aggregate trends weekly.

Pass bar: ≥80% thumbs-up; regenerate ≤15%; abandon ≤20% for non-trivial P0 triage requests.

Escalation trigger: ≥2 thumbs-down for the same intent within 24 hours triggers review of affected runs.

Owner: PM reviews weekly trends; on-call PM owns immediate escalation and triage.

**Human Evaluation**

Sample: 50 P0 triage runs/week, stratified across high, medium, and low confidence, plus 100% of hand-off/escalation cases.

Evaluation method: Score each sampled run using the Juno Human Evaluation Rubric: Accuracy of Top-3 Risks, Citation Quality, Decision Usefulness, and Tone & Calibration.

Cadence: Weekly scoring and calibration; monthly trend review.

Pass bar: ≥90% of sampled runs score ≥3 on every rubric dimension; ≥80% score 4 or 5 overall; 0 fabricated risks or citations.

Escalation trigger: Any fabricated risk/citation or repeated score <3 on the same dimension triggers root-cause review and eval-set update.

Owner: 2 senior PMs + 1 SRE representative + 1 Support lead; PM owns remediation backlog.

**Offline / Golden-Set Evaluation**

What gets tested: Representative P0 Slack + ticket threads with PM-curated golden Top-3 risks, supporting citations, confidence, and expected escalation behavior. Include ambiguous, noisy, conflicting, and incomplete cases.

When run: Before prompt/model/tool changes and on every release candidate; full regression weekly.

Pass bar: ≥90% Top-3 risk agreement with golden set; ≥95% citation grounding; 100% correct escalation on designated must-escalate cases.

Regression rule: No release if a safety-critical or decision-critical metric regresses; other material regressions require PM approval and documented rationale.

Owner: PM owns golden set and release decision; engineering owns automated execution and reporting.

**Production / System Monitoring**

Signals monitored: Retrieval failures, tool errors, latency, timeout rate, confidence distribution, escalation rate, token/cost usage, repeated-tool failures.

Cadence: Continuous monitoring with weekly trend review.

Pass bar: ≥99% successful workflow completion; p95 latency ≤90 sec; tool-error rate ≤2%; 100% adherence to Juno's max-step and escalation controls.

Escalation trigger: Threshold breach, abnormal confidence shift, or repeated tool failure triggers cautious mode and/or PM escalation per Agent Control Panel.

Owner: Engineering/SRE monitors system health; PM monitors product-quality and behavioral trends.

**Evaluation Loop**

Online Feedback → Human Review → Golden-Set Regression → Production Monitoring

The evaluation stack creates a closed quality loop:

Detect a problem → Understand it → Add it to the eval set → Prevent it from recurring.

**Critical Quality Gate**

0 fabricated risks or citations.

For Juno's P0 Triage Copilot, fabricated risks or citations are treated as critical failures because the output supports a rollback / hold / ship decision within five minutes.
___
