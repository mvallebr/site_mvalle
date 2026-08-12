---
layout: post
title:  "The Myth of the Leaderless Team: When Consensus Becomes Control"
date:   2026-08-12 07:00:00 +0100
categories: software management leadership
description: "Good leadership is not the absence of authority. It is creating the conditions for ownership, resilient systems, and more capable leaders."
image:
    path: /assets/img/the-myth-of-the-leaderless-team.png
    width: 1734
    height: 907
---

Imagine that you lead a team of capable people. They own different projects, make design decisions, and are expected to improve the systems they work on.

One day, someone proposes a change that could significantly improve the system. It could also cause a serious production incident if the assumptions behind it are wrong.

<div class="dilemma">
<p class="dilemma-label">The dilemma</p>
<p>What do you do?</p>
<ol>
<li>Review every detail before allowing the work to continue.</li>
<li>Make the design decision yourself and ask the team to implement it.</li>
<li>Let the person decide and create conditions in which a mistake is safe.</li>
</ol>
</div>

The first option feels responsible. The second feels efficient. The third feels dangerous.

But there is another possibility: instead of choosing between control and recklessness, you can build a system in which people are free to make decisions and mistakes are difficult to turn into disasters.

That is one of the central responsibilities of leadership.

## Does freedom increase risk?

The honest answer is yes. Freedom can increase the risk of a bad decision. A person with ownership can make a mistake, choose the wrong design, or underestimate a consequence.

But control also creates risk. When one person reviews or decides everything:

- the team becomes dependent on that person;
- decisions become slower;
- people stop developing their judgment;
- the leader becomes a bottleneck and a single point of failure;
- responsibility and authority become separated.

The goal is not to eliminate risk. That is impossible. The goal is to decide where risk should be handled.

Should it be handled by one person trying to supervise every decision, or by the design of the system in which decisions are made?

<div class="principle">
<p>Freedom without safety mechanisms is reckless. Control without ownership is fragile.</p>
</div>

## What should a leader do?

The next dilemma is more specific. What should a leader do when someone is not ready to own a highly ambiguous problem? And what should the leader do when that person is ready?

The answer is not to give everyone the same level of freedom. Leadership should calibrate the level of delegation to capability, while helping people expand their capability.

<div class="leadership-calibration" aria-label="A progression from supervision to ownership">
<div class="calibration-step">
<span>Not ready yet</span>
<strong>Learn the system</strong>
<p>Clearer constraints, narrower scope, more context, and feedback on both decisions and consequences.</p>
</div>
<div class="calibration-arrow" aria-hidden="true">-&gt;</div>
<div class="calibration-step">
<span>Growing capability</span>
<strong>Improve the system</strong>
<p>Take on more ambiguity while making failures safer through tests, observability, and better boundaries.</p>
</div>
<div class="calibration-arrow" aria-hidden="true">-&gt;</div>
<div class="calibration-step">
<span>Ready to own</span>
<strong>Build tolerance</strong>
<p>Own the outcome, the decisions, and the mechanisms that help the next person succeed.</p>
</div>
</div>

<div class="leadership-contrast">
<div>
<p class="contrast-label">Less mature model</p>
<p class="contrast-line">A mistake is treated as a personal failure.</p>
<p class="contrast-line">The response is more supervision.</p>
<p class="contrast-result">The system remains error-prone.</p>
</div>
<div>
<p class="contrast-label">More mature model</p>
<p class="contrast-line">A mistake is investigated as a system signal.</p>
<p class="contrast-line">The response is a more resilient system.</p>
<p class="contrast-result">The system becomes more tolerant.</p>
</div>
</div>

A person who is not ready should not be left alone in the name of empowerment. They should receive support and a deliberate path toward greater ownership. But a person who is ready should not remain under the same level of supervision forever.

The difference between a junior and a more capable person is not simply that the latter can be trusted with a more ambiguous problem. More capable people also understand that errors will happen even when people are competent. They think about how to make errors tolerable, how to detect them early, how to avoid error-prone designs, and how to make sure the same failure is less likely to happen again.

Less mature environments often reward the person who did not make a visible mistake. Better environments reward the person who makes the system safer for everyone, including when their own experiment fails.

Limiting someone's freedom while they learn can be good leadership. Turning that temporary limitation into the permanent operating model for the whole team is not. The goal is not to let the team decide everything immediately. The goal is to use each decision as an opportunity to increase people's ability to own the next one. A good leader calibrates delegation today while deliberately moving the team toward greater ownership over time.

## If there is no resilience, should failure be surprising?

Suppose a team is changing a system without enough tests, observability, rollback mechanisms, or clear ownership. The team is told to be careful, but the system provides little protection when care is not enough.

Should we be surprised when something breaks in production?

The incident may have been triggered by a person's decision, but the absence of resilience is also part of the explanation. The system was allowed to operate without enough ability to prevent, detect, contain, or recover from failure.

This does not mean that every mistake is automatically somebody else's fault. People remain responsible for their decisions. It means that accountability should include the conditions in which those decisions were made.

<div class="resilience-cycle" aria-label="The failure resilience cycle">
<div><span>Prevent</span><small>Tests, validation, safe defaults</small></div>
<span class="resilience-arrow" aria-hidden="true">-&gt;</span>
<div><span>Detect</span><small>Observability, alarms, monitoring</small></div>
<span class="resilience-arrow" aria-hidden="true">-&gt;</span>
<div><span>Contain</span><small>Idempotency, isolation, small blast radius</small></div>
<span class="resilience-arrow" aria-hidden="true">-&gt;</span>
<div><span>Recover</span><small>Rollback, playbooks, automation</small></div>
<span class="resilience-arrow" aria-hidden="true">-&gt;</span>
<div><span>Learn</span><small>Better designs and new protections</small></div>
</div>

This is broader than boundaries around individual decisions. It includes non-functional requirements such as failure tolerance and idempotency, as well as the practical systems around the software: alarms, playbooks, infrastructure as code, deployment automation, and clear ownership.

Mature people do not merely try harder to avoid mistakes. They design systems that make mistakes less damaging, easier to detect, and faster to recover from. They also look for error-prone designs and remove them when they find them.

<div class="principle">
<p>"Be more careful next time" is not a system improvement.</p>
</div>

Care matters, but care is not a mechanism. If the failure was predictable because there were no tests, rollback, alarms, or recovery procedures, asking for more attention does not address the cause.

## What about legacy systems?

Most teams do not start with a clean system and unlimited time. They inherit software that is difficult to test, difficult to observe, and dangerous to change. Safety mechanisms and resilience cannot always be created overnight.

That creates another dilemma. Should the team remain under permanent centralized control until the legacy system is safe?

The answer should be no, but the alternative is not pretending that the system is safe. The alternative is to make the risk explicit, reduce the radius of possible damage, and improve the system's resilience incrementally.

Not having every protection yet can be a legitimate constraint. Failing to recognize that absence as a risk is a leadership failure. Refusing to prioritize resilience is an organizational choice.

The most dangerous situation is when the lack of safety mechanisms becomes a permanent excuse for keeping all decisions centralized.

<div class="dilemma exit-path">
<p class="dilemma-label">Ask this</p>
<p>If control is described as temporary, what is the concrete path for removing it?</p>
<div class="exit-path-rule" aria-hidden="true"></div>
<p class="exit-path-conclusion">If there is no path, it is not temporary control.<br><strong>It is the operating model.</strong></p>
</div>

## How control becomes permanent

Centralized control often creates the conditions that appear to justify more centralized control.

<div class="cycle" aria-label="The control bottleneck cycle">
<div>Centralized<br>control</div>
<span aria-hidden="true">-&gt;</span>
<div>Leader becomes<br>bottleneck</div>
<span aria-hidden="true">-&gt;</span>
<div>Team improves<br>the system less</div>
<span aria-hidden="true">-&gt;</span>
<div>System protections<br>remain missing</div>
<span aria-hidden="true">-&gt;</span>
<div>More control<br>seems necessary</div>
<div class="cycle-return" aria-hidden="true">↩ back to centralized control</div>
</div>

The team has less capacity to improve the system because so much of its energy is spent waiting for decisions or implementing decisions made elsewhere. New needs arrive faster than the team can improve its safety mechanisms. The system never reaches the promised future state in which control will no longer be necessary.

The leader is not simply responding to the problem anymore. The control model is helping to preserve it.

## Is freedom the absence of authority?

There is a mistake on the opposite side. A leader may decide not to control every decision, but also avoid using authority to create a functional environment. That does not create freedom. It creates a vacuum.

Someone will fill that vacuum: the loudest person in the room, the most political person in the organization, or an informal group whose decisions are difficult to challenge. The result is often consensus by exhaustion, not ownership.

The leader must use authority to stop the cycle of permanent control. They must set boundaries, establish priorities, clarify ownership, protect the team from unreasonable demands, and require the work needed to make the system safer.

<div class="leadership-order">
<p class="dilemma-label">An order worth giving</p>
<p>More ownership.<br><strong>Less control.</strong></p>
<small>Build the conditions that make this possible.</small>
</div>

A good manager sometimes needs to impose things. Authority is not the opposite of freedom when it is used to protect the boundaries within which freedom can exist.

This is why strong institutions can sometimes create more freedom rather than less. Rules and enforcement can make fair competition possible. The same pattern can be seen in China's model: strong central authority has created a framework in which companies and individuals can compete aggressively within boundaries set by the state. The political model is not the point here. The point is that freedom in an area often depends on authority defining and enforcing the boundaries around it.

Good leadership is not the absence of hierarchy. It is clarity about who can decide, who must be consulted, who will be informed, and who deals with the consequences. I explored this broader idea in [The problem is not hierarchy, but lack of accountability]({{ "/personal/politics/management/2023/09/19/the-problem-is-not-hierarchy-but-lack-of-accountability.html" | relative_url }}), including the role that clear delegation and delegation levels can play in making hierarchy work.

The leader's authority should be aimed at making the team less dependent on the leader over time.

## What does good delegation look like?

Good delegation is not asking a group to reach consensus on every decision. Consensus sounds collaborative, but it often turns decisions into religious discussions: everyone defends a preferred belief, the discussion becomes a bottleneck, and nobody clearly owns the result.

In a team with ownership, people are responsible for projects. They lead them, make decisions within their delegation level, report progress, demonstrate results, and share knowledge periodically. They ask for opinions when they believe another perspective will improve the decision, not because every decision requires permission from the whole team.

<div class="delegation-model">
<div class="delegation-column delegation-consensus">
<p class="contrast-label">Consensus by default</p>
<strong>Everyone discusses</strong>
<span>Decision waits for agreement</span>
<span>Knowledge stays in the room</span>
<span>Ownership is blurred</span>
</div>
<div class="delegation-column delegation-ownership">
<p class="contrast-label">Ownership by default</p>
<strong>One person leads</strong>
<span>Others advise when useful</span>
<span>Knowledge is shared periodically</span>
<span>Tools and AI amplify judgment</span>
<span>Resilient systems contain mistakes</span>
</div>
</div>

<div class="ownership-illustration">
<img src="{{ "/assets/img/ownership-by-default.png" | relative_url }}" alt="A visual contrast between a quiet person in a consensus-driven meeting and the same person building a rocket with engineering tools and safety mechanisms." />
</div>

Ownership does not mean working alone. It means combining autonomous leadership with collaboration, expertise, AI, and other tools. The person who owns the work remains responsible for moving it forward, while the team contributes the best knowledge available when it is useful.

This model depends on the same premise as autonomy itself: systems must be resilient enough that a decision does not become a catastrophe merely because one person was wrong.

Before work begins, the leader and the person doing the work should agree on what success means. The task can have more or less ambiguity depending on experience and trust, but the destination should not be invented after arrival.

Good delegation defines the outcome, the decision level, and the ownership without prescribing every step of the journey.

## What do we learn when something fails?

Good teams will fail. The goal is not to create a team where failure is impossible. The goal is to create a team where failure is survivable and useful.

When something fails because a safety mechanism was missing, the first questions should be about the system:

- Which protection or mechanism was missing?
- Why was it missing?
- Was the risk understood?
- Was the work prioritized correctly?
- What can we change so the next person can make a similar decision more safely?

<div class="principle">
<p>"Be more careful next time" is not a system improvement.</p>
</div>

Care matters, but care is not a mechanism. If the failure was predictable because there were no tests, rollback, or observability, asking for more attention does not address the cause.

Accountability is also not the same as control. Accountability means dealing with the consequences of a decision or outcome. Control means having the authority to direct or approve decisions.

When a leader controls the decisions but gives ownership of the result to someone else, authority and accountability become disconnected. I have written more about this distinction in [Culture of blame vs culture of accountability]({{ "/software/management/leadership/2024/01/20/culture_of_blame_vs_culture_of_accountability.html" | relative_url }}).

## Why this matters even more with AI

The need for resilient systems and explicit boundaries becomes even more important as teams adopt AI.

AI increases the speed at which people can explore solutions, write code, and produce changes. That speed is valuable only if the team can distinguish useful experiments from dangerous changes.

If a team cannot distribute ownership among people, it will not be able to distribute the use of AI effectively. Leaders will respond to the new technology by trying to approve every prompt, every generated change, and every experiment. The technology will be available, but the organization will be unable to use it at the speed it promises.

The better response is to invest in the capabilities that allow responsible experimentation: automated verification, clear data and security boundaries, review practices appropriate to the risk, and a culture where people share what they learn.

AI will not make centralized control scalable. It will make the need for resilient systems and clear boundaries impossible to ignore.

## Good leaders create more leaders

The measure of a leader is not how many decisions they personally make. It is how many people become capable of making good decisions because of the environment they created.

Good leaders do not disappear. They set direction, define success, build resilient systems, resolve conflicts, and use authority to protect the boundaries within which the team can own its work.

They create more leaders by allowing people to practice leadership before they have perfect certainty. They make failure survivable. They make accountability clear. They keep improving the system instead of demanding that individuals compensate for its weaknesses.

The best leaders are not the people who remain necessary for every decision.

They are the people who make more decisions possible without them.
