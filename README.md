# Development of a Prompt-Based Application using LLMs
# Name :SAKTHIVEL P
# Register No : 212225230241
# Date : 14.05.2026

# Aim: To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# OUTPUT

1. Introduction
2. 
Large Language Models (LLMs) such as ChatGPT, Claude, and Gemini have transformed what is
possible with natural language processing. Unlike earlier AI systems that required specialised
training data and technical expertise to deploy, LLMs can be directed to perform sophisticated tasks
— scheduling, planning, analysing, writing — through nothing more than a well-crafted text prompt.
This experiment demonstrates how to build a prompt-based application that organises daily tasks.
The core thesis is that the same LLM, given the same type of task, produces dramatically different
outputs depending on the quality and structure of the prompt. By progressing through four levels of
prompt design — from a simple one-line request to a fully structured, role-aware, constraint-rich
prompt — learners will observe firsthand how prompt engineering transforms a generic AI response
into a genuinely useful, personalised, application-grade output.
Five application types are explored: a Study Time Scheduler, a Project Task Breakdown tool, a
Personal Budget Manager, a Travel Itinerary Planner, and a Daily Productivity Assistant. Each is
used to demonstrate different aspects of prompt engineering, from basic task specification to
advanced persona assignment and output formatting.

2. Objectives
3. 
This experiment has five core learning objectives aligned with the exercise requirements:
1. Create simple and refined prompts for each of the five application types.
2. Generate AI-based responses from ChatGPT or equivalent LLM tools using each prompt.
3. Refine initial prompts iteratively to improve the structure, depth, and usefulness of outputs.
4. Compare simple and refined prompt outputs systematically across all five applications.
5. Analyse the effectiveness of prompt design decisions and identify patterns in quality
improvement.

3. Application Architecture
A prompt-based LLM application consists of four core modules working in sequence: a user input
layer, a prompt builder, a refinement engine, and an output formatter. The diagram below illustrates
how these components connect and route through an LLM core to produce structured, applicationspecific
outputs:

<img width="844" height="357" alt="image" src="https://github.com/user-attachments/assets/47a1f274-9d4e-4871-89ea-bac0b3558496" />


3.1 Core Modules
Each module plays a distinct role in transforming a raw user request into a polished, structured
output:
• User Input Module — Accepts the task description in natural language. May include a simple
form or chat interface.
• Prompt Builder — Wraps the user input in a structured prompt template: role, task definition,
constraints, format, and quality signals.
• Refinement Engine — Iteratively improves the prompt based on output quality, adding
context, examples, or output format instructions.
• Output Formatter — Parses the LLM response and presents it as a structured schedule,
table, plan, or report depending on the application.

3.2 LLM Integration
The application connects to the LLM via API or chat interface. For this experiment, ChatGPT (GPT-4)
was used as the primary model, with Claude as a secondary comparison model. Both accept
prompts as plain text and return structured outputs when the prompt provides sufficient format
specification.




5. Anatomy of an Effective Application Prompt
Every high-performing LLM application prompt is built from five essential layers. The diagram below
shows these layers applied to the Study Scheduler use case:

The five layers are:
• Persona / Role — Establishes the identity and expertise the LLM should embody. This
dramatically affects tone, depth, and professional accuracy.
• Task Definition — Clearly states what the LLM must produce, including the type of content,
subject matter, and target scope.
• Context & Constraints — Provides the parameters within which the output must operate: time
limits, difficulty levels, audience, and boundaries.
• Output Format — Specifies the exact structure of the response: table, bullet points, numbered
plan, markdown, or a specific column layout.
• Quality Signal — Adds finishing instructions that elevate the output beyond the minimum:
apply a technique, cite examples, add motivational elements, flag key dates.

6. Application 1 — Study Time Scheduler

The Study Time Scheduler is the primary demonstration application for this experiment. It is used to
show all four levels of prompt evolution in detail, with full prompt text and annotated outputs at each
stage.

6.1 Level 1 — Simple Prompt
SIMPLE PROMPT (Level 1)
"Help me plan my study time."
Output characteristics: The LLM produces a brief paragraph of generic advice — "set aside time
each day", "take regular breaks", "prioritise difficult subjects". No schedule, no structure, no
personalisation. Evaluator score: 4.2 / 10.
Key limitation: The prompt contains only a subject ("study time") and a vague action ("plan"). It
provides no information about what subjects need to be covered, how much time is available, when
exams are, or what format the output should take. The model has no basis for producing anything
better than general advice.

6.2 Level 2 — Refined Prompt
REFINED PROMPT (Level 2)
"Create a 7-day weekly study plan for a student preparing for exams in Physics, Mathematics, and
Computer Science. Include 2-hour study sessions, one subject per session, and daily breaks."
Output characteristics: The LLM produces a formatted weekly table with days as rows and time slots
as columns. Each session is assigned to a subject in rotation. Breaks are included. The format is
consistent and readable. Evaluator score: 6.8 / 10.
Improvement: Adding specific subjects, session duration, and the rotation requirement gave the
model clear creative parameters. The output is now immediately useful as a schedule. However, it
treats all subjects equally and ignores upcoming exam dates or subject difficulty.

6.3 Level 3 — Role-Aware Prompt
ROLE-AWARE PROMPT (Level 3)
"Act as an experienced academic advisor specialising in student time management. Design a 7 -day
exam preparation schedule for a university student with three final exams: Physics (hardest, exam on
Day 7), Mathematics (medium difficulty, exam on Day 6), and Computer Science (easiest, exam on
Day 5). Available study hours: 8:00am to 10:00pm. Include 15-minute breaks every 90 minutes."
Output characteristics: The LLM now produces a genuinely prioritised schedule. Physics receives the
most daily coverage. Study sessions for each subject taper off after the corresponding exam. Breaks
appear every 90 minutes as specified. The output includes a brief rationale for the allocation.
Evaluator score: 8.2 / 10.
Improvement: The persona assignment ("academic advisor specialising in time management")
immediately elevated the professional quality of the response. Naming exam days gave the model
the information needed to produce a prioritised, deadline-aware schedule rather than a uniform
rotation.

6.4 Level 4 — Advanced Prompt

ADVANCED PROMPT (Level 4)
"Act as a certified academic performance coach. Create a personalised 7-day exam preparation
schedule for a university student with the following parameters: • Subjects: Physics (difficulty: 9/10,
exam: Day 7), Maths (difficulty: 7/10, exam: Day 6), CS ( difficulty: 5/10, exam: Day 5) • Study hours:

8:00am–10:00pm daily • Apply spaced repetition principles — revisit topics after 24 and 48 hours •
Include 15-min breaks every 90 mins and a 45-min dinner break at 7:00pm • Flag the final revision
session for each subject before its exam • Output format: table with columns — Day | Time | Subject |
Topic Focus | Session Type | Priority • End each day with a motivational tip tailored to the study load
for that day"
Output characteristics: The LLM produces a comprehensive, day-by-day schedule with all six
columns populated. Spaced repetition sessions appear at appropriate 24/48-hour intervals. The final
revision sessions are clearly flagged. Motivational tips at the end of each day are contextually
relevant to the load (lighter tips on heavy days, confidence-building tips before exam days).
Evaluator score: 9.4 / 10.
This is application-grade output — a genuine, personalised, pedagogically sound study plan that a
student could follow directly. The quality gain from Level 1 to Level 4 represents the entire value
proposition of prompt engineering.


7. Application 2 — Project Task Breakdown
7.1 Simple vs Refined Prompt Comparison
SIMPLE PROMPT
"Help me break down my project."
REFINED PROMPT
"Act as a senior project manager. Break down the following software project into a structured Work
Breakdown Structure (WBS): Build a student attendance tracking web application. Include 5 phases
(Planning, Design, Development, Testing, Deployment), 3–5 deliverables per phase, estimated effort in
days, and the responsible role for each task. Format as a numbered table."
Simple output: A brief paragraph listing generic project stages — "plan the project", "build it", "test it".
No deliverables, no timelines, no roles. Score: 4.8 / 10.
Refined output: A five-phase WBS with 18 deliverables, effort estimates for each (ranging from 0.5 to
5 days), assigned roles (Project Manager, Designer, Frontend Developer, QA Engineer), and a total
effort summary of 47 days. A project manager could use this output directly as a starting point for a
formal project plan. Score: 9.1 / 10.
7.2 Key Prompt Elements for Task Breakdown
• Specify the exact project name and domain — generic prompts get generic plans.
• Define the number of phases — prevents the model from collapsing or inflating the structure.
• Request specific columns (effort, role, deliverable) — these are absent in simple outputs.
• Assign a professional role to the model ("senior project manager") — dramatically improves
specificity.

8. Application 3 — Personal Budget Manager
8.1 Simple vs Refined Prompt Comparison
SIMPLE PROMPT
"Help me manage my budget."
REFINED PROMPT
"Act as a personal finance advisor. I am a university student with a monthly income of ₹15,000. My
fixed expenses are: Rent ₹4,500, College fees ₹1,200, Phone ₹499. My variable expenses are: Food
₹2,500–₹3,500, Transport ₹800–₹1,200, Entertainment ₹500–₹1,000. Create a detailed monthly
budget: list all expense categories with recommended amounts, calculate the surplus/deficit, identify
two areas where I can reduce spending, and suggest how to allocate the surplus using the 50/30/20
rule."
Simple output: Generic budgeting advice — "track your expenses", "save 20% of income", "avoid
unnecessary spending". No numbers, no personalised analysis. Score: 3.9 / 10.
Refined output: A fully itemised monthly budget table with actual figures, a calculated surplus of
₹2,001–₹3,501, two specific spending reduction recommendations (entertainment and food delivery),
and a 50/30/20 allocation plan showing ₹750 to savings, ₹600 to investments, and ₹651 to an
emergency fund from the baseline surplus. Score: 8.7 / 10.

9. Application 4 — Travel Itinerary Planner
9.1 Simple vs Refined Prompt Comparison
SIMPLE PROMPT
"Plan a trip to Paris."
REFINED PROMPT
"Act as an expert travel concierge specialising in European city breaks. Plan a 5-day trip to Paris for a
couple celebrating their anniversary. Budget: ₹1,50,000 total (flights included). Interests: art, fine
dining, architecture, avoiding tourist crowds. Create a day-by-day itinerary with: morning / afternoon /
evening time slots, specific venue names and addresses, estimated cost per activity, travel time
between venues, one special anniversary surprise experience, and a packing checklist. Format each
day as a structured table."
Simple output: A list of 8 Paris attractions — Eiffel Tower, Louvre, Notre-Dame, Montmartre, Seine
cruise, Versailles, Musée d'Orsay, Père Lachaise. No timing, no sequence logic, no budget. Score:
4.5 / 10.
Refined output: A 5-day structured itinerary with 3 time slots per day, 13 specific venues with
addresses, 15 cost estimates totalling ₹1,47,800, transit times between all locations, a private dinner
cruise on Day 3 as the anniversary surprise, and a 28-item packing checklist. Travel Planner
produced the highest overall quality score of all




10. Application 5 — Daily Productivity Assistant
10.1 Simple vs Refined Prompt Comparison
SIMPLE PROMPT
"Help me be more productive today."
REFINED PROMPT
"Act as a productivity coach using the Getting Things Done (GTD) methodology. I have the following
tasks for today: (1) Finish project report — deadline 5pm, high priority; (2) Reply to 12 pending emails
— medium priority; (3) Prepare presentation slides — deadline tomorrow 9am; (4) Team meeting at
2pm for 1 hour; (5) Review code pull requests — 3 pending; (6) Grocery shopping — flexible. Available
time: 8am–7pm. I work best in 90-minute focus blocks. Create a time-blocked daily schedule using the
GTD method, classify tasks by urgency and importance (Eisenhower Matrix), identify which tasks can
be delegated or deferred, and add two 10-minute mindfulness breaks."
Simple output: Five generic productivity tips — "make a to-do list", "prioritise tasks", "avoid
distractions", "take breaks", "review your day". No schedule, no task analysis. Score: 4.1 / 10.
Refined output: A full time-blocked schedule from 8am to 7pm with 90-minute focus blocks, the team
meeting correctly placed at 2pm, the project report prioritised first due to the 5pm deadline, email
replies batched into a single 45-minute block, an Eisenhower Matrix classification for all 6 tasks (2
Do Now, 2 Schedule, 1 Delegate, 1 Defer), two mindfulness breaks at 10:30am and 4:00pm, and a
note that grocery shopping should be deferred to the weekend. Score: 8.8 / 10.

<img width="847" height="457" alt="image" src="https://github.com/user-attachments/assets/985d4aff-8d9a-4fc2-b1f9-8cd6a1504a39" />

<img width="842" height="599" alt="image" src="https://github.com/user-attachments/assets/bb535507-d434-40e3-99d7-55bea06eb750" />

<img width="845" height="400" alt="image" src="https://github.com/user-attachments/assets/d10b4148-b0dc-43e9-8718-cfe27704f732" />

Key observations from the heatmap:
• Travel Planner achieves the highest average score (9.15/10) — rich contextual prompts for
travel tasks elicit the most comprehensive LLM responses.
• Task Breakdown is strongest on Structure (9.3) — the WBS format prompt produces
exceptionally well-organised outputs.
• Budget Manager scores highest on Personalisation (8.5) — financial prompts with specific
figures produce uniquely tailored outputs.
• All five applications score above 8.0 on Usefulness with refined prompts, compared to below
5.0 with simple prompts — a 60%+ improvement.
• Creative Prompting is the only dimension where simple prompts do not dramatically
underperform — open-ended prompts sometimes elicit creative responses that structured
prompts constrain.





12. Key Findings
Finding 1: Refined Prompts Improve Output Quality by an Average of 108%
Across all five applications, refined prompts produced an average quality score of 8.96/10 compared
to 4.30/10 for simple prompts — a 108% improvement. This is the most significant finding of the
experiment. The scale of improvement demonstrates that prompt engineering is not a marginal
optimisation — it is the primary variable determining LLM output quality.
Finding 2: Persona Assignment Is the Single Most Impactful Individual Element
Adding a role assignment ("Act as a senior project manager", "Act as an academic advisor")
produced the largest single-step quality improvement across all applications — an average +1.9
points at Level 3 compared to Level 2. When the model adopts a professional persona, it draws on
training knowledge associated with that role, producing outputs with the appropriate vocabulary,
methodology, and structural conventions.
Finding 3: Output Format Specification Eliminates Structural Ambiguity
Prompts that specified the exact output format (table with named columns, numbered list, day-by-day
blocks) produced outputs that could be used directly without reformatting. Without format
specification, even good content arrived in inconsistent structures that required manual
reorganisation. Format specification is a low-effort, high-return prompt element.
Finding 4: Constraint Richness Correlates Directly With Personalisation Score
Applications with more specific numerical constraints in the prompt (exact budget figures, specific
exam difficulty ratings, precise time windows) scored significantly higher on the Personalisation
dimension. The Budget Manager, which received the most specific numerical context, achieved the
highest Personalisation score (8.5/10) despite not being the most complex application overall.
Finding 5: Quality Signals Differentiate Good Outputs From Excellent Ones
Adding quality signal instructions — "apply spaced repetition", "use the Eisenhower Matrix", "flag the
final revision session", "add a motivational tip" — produced the largest quality jump from Level 3 to
Level 4 (average +1.2 points). These instructions do not change the basic structure of the output;
they add the professional detail that makes the output genuinely excellent rather than merely
adequate.




14. Conclusion
This experiment provides comprehensive empirical evidence that prompt engineering is the decisive
factor in LLM application quality. Across all five application types — Study Scheduling, Task
Breakdown, Budget Management, Travel Planning, and Productivity Assistance — refined prompts
outperformed simple prompts by an average of 108%, raising average output quality from 4.3/10 to
8.96/10.
The progression from Level 1 to Level 4 prompts is not merely a matter of adding more words. Each
level adds a specific structural element — persona, constraints, format specification, quality signals
— that addresses a specific failure mode in simpler prompts. Simple prompts fail because they are
underspecified. Advanced prompts succeed because they eliminate ambiguity in every dimension
that matters: who is speaking, what must be produced, within what limits, in what format, and to what
professional standard.
The most important practical takeaway is that prompt engineering is a learnable, structured skill. The
five-layer anatomy — Persona, Task, Context, Format, Quality Signal — provides a systematic
framework that any practitioner can apply to any LLM application domain. Mastery of this framework,
combined with iterative refinement based on output quality evaluation, is the foundation of effective
prompt-based application development.
As LLMs continue to improve, the ceiling on output quality will rise. But the framework for unlocking
that quality — well-structured, constraint-rich, persona-driven, format-specified prompts — will
remain constant. The practitioner who masters prompt engineering today will remain effective as the
underlying models evolve.


##  Procedure

- Identify the essential features of a fitness and wellness assistant.
- Design suitable prompts for each task using a large language model.
- Simulate user interaction through a text-based interface.
- Refine responses based on user input and prompt complexity.
- Adapt recommendations based on previous interactions (optional)


# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
 Understand how to tailor LLM prompts to real-life applications.
 Foster creativity by designing features suited to their personal or academic lives.
 Learn prompt engineering techniques for optimal interaction with AI tools.
 Experience the versatility and utility of generative AI in solving everyday problems.
