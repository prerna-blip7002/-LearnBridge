# -LearnBridge
LearnBridge

Personalized learning support for stronger foundations.

LearnBridge is a working prototype under the Education & Skill Development theme. It helps teachers and NGO volunteers identify learning gaps, suggest focused practice and maintain continuity between teaching sessions.

Problem

Students in the same class may have different gaps in reading, English and numeracy. Teachers and volunteers need a practical way to identify these gaps, plan suitable activities and track progress within limited teaching time.

Features

* Six-question assessment covering reading, English and numeracy.
* English or Tamil-English question prompts.
* Rule-based skill scores and learning-gap identification.
* Personalized four-session weekly practice plans.
* Session completion tracking.
* Tutor handover notes.
* Assessment history using the same learner alias.
* JSON data export and printable learning plans.

Technology Stack

* HTML5
* CSS3
* Vanilla JavaScript
* Browser localStorage

No backend, external libraries, AI models or paid services are required.

Setup and Environment Variables

1. Download the repository and extract its files.
2. Open index.html in a modern desktop browser.
3. Start using the prototype.

No installation, environment variables, API keys or build commands are required.

For an interactive iPhone demo, host the files using GitHub Pages and open the published website in Safari. The iPhone Files preview may not execute JavaScript.

How to Use

1. Open Assessment.
2. Enter a fictional learner name or alias.
3. Choose the question language and answer all six questions.
4. Generate and review the suggested learning plan.
5. Mark practice sessions as completed.
6. Open Progress & handover to save tutor notes.
7. Repeat the assessment using the same alias to view assessment history.

The overview includes one fictional demonstration learner.

Scoring and Personalization

Each skill has two questions. Each correct answer contributes 50 percentage points to that skill’s score.

Scores below 75% are flagged for targeted support. The system prioritizes the weakest skills and distributes practice across four sessions. Learners without flagged gaps receive extension practice.

Suggestions are generated using predefined rules and activities. Educators should review them before use.

Architecture

flowchart TD
    A[Assessment answers] --> B[Rule-based scoring]
    B --> C[Learning-gap identification]
    C --> D[Weekly practice plan]
    D --> E[Session tracking and tutor notes]
    E --> F[Browser localStorage]
    F --> G[Progress view and JSON export]

Further implementation details are available in DESIGN.md.

Repository Files

File	Purpose
index.html	Complete working prototype
README.md	Overview, setup and usage
DESIGN.md	Technical design and architecture
sample-data.json	Fictional demonstration data
tests.js	Automated scoring and priority tests
TEST_CASES.md	Test cases and manual verification steps
LICENSE	MIT open-source license

Testing

With Node.js installed, run:

node tests.js

Six automated tests cover correct, incorrect and mixed answers, priority ordering and the scoring threshold.

Manual verification steps are provided in TEST_CASES.md, including assessment submission, completion tracking, saved notes, data export and mobile layout.

Data and Offline Use

Records are stored locally in the current browser. There is no cloud synchronization.

The downloaded application can operate without internet in a compatible browser. A hosted page is not guaranteed to reopen offline because this prototype has no service worker.

Use fictional learner aliases and sample data for demonstrations.

Expected Impact

LearnBridge aims to support targeted teaching and smoother tutor handovers. A future pilot would measure:

* Changes in reassessment scores.
* Practice-session completion.
* Time spent preparing learning plans.

No measured educational outcomes are claimed for this prototype.

UN SDG Alignment

* SDG 4 — Quality Education: Supporting foundational learning and educator-guided practice.
* SDG 10 — Reduced Inequalities: Designing accessible learning support for underserved learners.

Sustainability

The proposed model uses reusable, educator-reviewed activities and future school or NGO partnerships to keep costs low. No existing partnerships are claimed.

Limitations and Future Development

The six-question screening is not a validated educational assessment. Repeated questions may inflate reassessment scores. Tamil support currently covers question prompts; answer options and practice activities remain in English.

Future development could include larger validated question banks, complete Tamil activities, reliable offline caching and secure multi-user access.

License

Released under the MIT License. See LICENSE.