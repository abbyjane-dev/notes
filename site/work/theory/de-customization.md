# De-Customization

## Purpose
This framework is intended as a practical tool for registrar leadership teams undertaking SIS modernization, ERP upgrades, or moving to cloud and/or SaaS environments. It offers a structured way to inventory, evaluate, and intentionally retain or retire customizations without flattening legitimate academic complexity.

The goal is not to reduce customization for its own sake, but to make institutional complexity explicit, governable, and sustainable over time.

## Guiding Principle

What is "de-customization":

> Systematically reducing institution-specific logic that increases technical debt, impedes upgrades, and embeds obsolete policy assumptions, while preserving the academic values that motivated the customizations in the first place.

## Framework

<hr />

Questions to guide the process:

1. What customizations do we have?

2. What are the parameters of the customization?

3. What limitations of the baseline SIS made the customization necessary?

4. Is the process for which the customization was built still used; has it materially changed since implementation?

5. For each customization, is it still necessary, is the process simply unable to be incorporated into baseline, if not, what changes can be reasonably made to the process so it can be integrated into baseline?

### 1. Inventory and Visibility

Identify all **non-baseline elements**, including:

- Database-level modifications
- Custom scripts / middleware
- Configuration overrides that behave like code
- Manual workarounds that function as “shadow customizations”

**Document**:

- Owner
- Date implemented
- Triggering requirement (policy, accreditation, faculty demand, historical artifact)

### 2. Define the Scope and Nature of Each Customization

Classify each customization as one of:

- Policy-driven (e.g., grading exceptions, registration priority)
- Pedagogical (tutorial systems, narrative evaluation workflows)
- Compliance-driven (VA, financial aid, visa tracking)
- Historical workaround (baseline once lacked a feature)
- Cultural preference (“we’ve always done it this way”)

This matters because **only some categories deserve preservation pressure**.

### 3. Interrogate the Original Constraint

Was baseline truly incapable, or merely unfamiliar?

Has the vendor since:

- Added baseline support?
- Shifted philosophy (e.g., from transactional to workflow-driven)?

Was the customization compensating for:

- Weak governance
- Policy ambiguity
- Faculty needs that have since changed

_Has the system changed, but the customization hasn't?_

### 4. Assess Process Drift

For each customization, is the underlying academic or administrative process:

- Still in use?
- Materially changed?
- Under active debate?

Has the customization:

- Frozen a process that should have evolved?
- Become _de facto_ policy?

### 5. Decision Matrix: Retire, Refactor, Retain

For each customization:

1. Retire
   - Criteria
	   - If baseline now supports it
	   - If the process no longer exists
	- Requires
		- Policy owner sign-off
		- Data migration or archival plan
		- Communication to affected stakeholders
2. Refactor into configuration
	- Criteria
		- If logic can be expressed via delivered tools
	- Requires
		- Vendor validation
		- Test environment modeling
		- Rollback plan
		- Documentation update
		- Training for users
3. Retain (explicity and defensively)
	- Criteria
	   - If it reflects a core academic value
	   - If eliminating it would materially harm pedagogy
	 - Requires
		 - Named business owner
		 - Justification tied to institutional mission
		 - Upgrade/migration impact assessment
		 - Timeline for periodic review

The guiding principle is that **retention becomes an intentional act**, not simply inertia.

## Keys

<hr />

1. Faculty, student, and staff needs are real and important.
2. Academic exceptionalism is a feature.
3. The staff/faculty own the logic.
4. No one is being replaced.
5. Technical debt is necessary only when it serves a purpose that coincides with the academic, cultural, and social mission of the College.
6. **Systems encode values whether we intend them to or not.**

## Quotes

<hr />

> Many institutions were afraid to touch student systems, especially customizations, because no one remembered why they existed. That’s where the real risk lives.
>
> The goal isn’t to remove what works, but to understand it well enough that we can support it sustainably, upgrade safely, and explain it clearly to the next group of people who inherit it.

> The goal not here to simplify the College. Rather, it is to make its complexity intentional and sustainable.

> The first thing to understand is: what in the system matters most to the College, and what would feel like a loss if we got it wrong?

---
Abby Jane Morton  
Prepared as part of a University Registrar search process  
January 2026

<!--## Avoidances

<hr />

- Best practices
- Industry standard
- Out of the box
- Efficiency gains
- Streamlining
- Modernization
- Words that connote external judgement
-->
<!--
Questions:
What are the metrics for success?
Is zero customization the only success?
-->

