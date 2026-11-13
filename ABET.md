# IEEE Systems Engineering Processes and Extreme Programming

## Collaboration notes

- Each person should edit only their assigned section below. Keep additions within that section to reduce merge conflicts.
- For every task in your section, record the single-letter process outcome it addresses and explain the Extreme Programming (XP) implementation.
- Support the XP explanation with direct quotations from the XP book. Include a page number or other locator with each quote when available.
- Do not add a task list or outcome letters unless they have been verified against the assigned IEEE document.

---

## 6.4.2 Stakeholder Needs and Requirements Definition process

**Owner:** Emmet

<!-- Emmet: add your task responses below. Please leave the other sections unchanged. -->

### Task responses

<!--
Copy this block once per task:

#### Task: [task identifier or short name]

- **Process outcome:** [single letter]
- **XP implementation:** [How XP implements this task.]
- **XP book quote(s):** “[Direct quote]” ([page or locator])
-->

---

## 6.4.4 Architecture Definition process

Listed Outcomes:
a) Identified stakeholder concerns are addressed by the architecture.

b) Architecture viewpoints are developed.

c) Context, boundaries, and external interfaces of the system are defined.

d) Architecture views and models of the system are developed.

e) Concepts, properties, characteristics, behaviors, functions, or constraints that are architecture decisions of the system are allocated to architectural entities.

f) System elements and their interfaces are identified.

g) Architecture candidates are assessed.

h) An architectural basis for processes throughout the life cycle is achieved.

i) Alignment of the architecture with requirements and design characteristics is achieved.

j) Any enabling systems or services needed for the architecture definition are available.

k) Traceability of architecture elements to stakeholder and system/software requirements is developed.

## a. Prepare for architecture definition
### 1) Review pertintent information and identify key drivers of the architecture.

a. a
b. The team and customer write user stories, and the team runs short spikes on risky technical questions. The key drivers surface in release planning, where the customer sets priorities and the team states the quality constraints (performance, security, platform).

### 2) Identify stakeholder concerns.

a. a
b. The on-site customer is the main source of concerns, and the planning game turns them into user stories. Other stakeholders’ concerns come in through the customer or through frequent iteration demos.

### 3) Define the Architecture Definition roadmap, approach, and strategy.

a. h
b. The release plan and iteration plans act as the roadmap. The strategy is evolutionary: build the simplest architecture that works, guided by the system metaphor, and refine it every iteration instead of designing it all up front.

### 4) Define architecture evaluation criteria based on stakeholder concerns and key requirements.

a. g
b. The customer writes acceptance criteria and the team adds measurable targets for non-functional needs, such as response time. Both are captured as automated acceptance or performance tests that any architectural choice must pass.

### 5) Identify and plan for the necessary enabling systems or services needed to support the Architecture Definition process.

a. j
b. The team plans the shared tooling in an early iteration (sometimes called iteration zero): a version control repository, a continuous integration server, test frameworks, an issue or story tracker, and a shared workspace with a whiteboard.

### 6) Obtain or acquire access to the enabling systems or services to be used.

a. j
b. The team sets up the repository, CI build, test harness and pairing workstations before feature work starts. Everyone gets access, and collective ownership means anyone can use the tools.

## b. Develop architecture viewpoints.
### 1) Select, adapt, or develop viewpoints and model kinds based on stakeholder concerns.

a. b
b. XP keeps viewpoints minimal. The system metaphor gives a shared high-level view, and CRC cards or quick sketches give a structural view. Acceptance tests give the customer’s behavioral view.

### 2) Establish or identify potential architecture framework(s) to be used in developing models and views.

a. b
b. XP does not use a formal architecture framework. The team agrees on the metaphor, coding standards, chosen technology stack and common design patterns, and that agreement serves as the lightweight framework.

### 3) Capture rationale for selection of framework(s), viewpoints and model kinds.

a. b
b. Rationale is recorded informally: notes on story cards, a team wiki, commit messages and retrospective notes. The tests and code are treated as the main documentation, so little separate paperwork is produced.

### 4) Select or develop supporting modeling techniques and tools.

a. b
b. The team uses whiteboards, CRC cards, informal UML sketches, an IDE with refactoring support, and the automated test framework.

## c. Develop models and views of candidate architectures.
### 1) Define the software system context and boundaries in terms of interfaces and interactions with external entities.

a. c
b. User stories and acceptance tests describe how the system interacts with users and external systems. For external dependencies, the team writes spikes and uses mocks or stubs so the boundary is exercised by tests early.

### 2) Identify architectural entities and relationships between entities that address key stakeholder concerns and critical software system requirements.

a. d
b. The team finds the main classes or components and their collaborations with CRC cards and the system metaphor. Pairs and the whole team discuss these at the whiteboard.

### 3) Allocate concepts, properties, characterisics, behaviors, functions, or constraints that are significant to architecture decisions of the software system to architectural entities.

a. e
b. Responsibilities are assigned to classes or components through CRC sessions and simple design. As stories are implemented, the team refactors to move responsibilities to where they fit best.

### 4) Select, adapt, or develop models of the candidate architectures of the software system.

a. d
b. The team sketches alternative designs and tests the risky ones with spikes. These are throwaway prototypes that answer a specific technical question quickly.

### 5) Compose views from the models in accordance with identified viewpoints to express how the architecture addresses stakeholder concerns and meets stakeholder and system/software requirements.

a. d
b. The views are whiteboard diagrams, the metaphor and the passing test suite. Diagrams are produced when they are needed and kept lightweight.

### 6) Harmonize the architecture models and views with each other.

a. d
b. Collective code ownership, continuous refactoring and daily team communication keep the sketches, tests and code consistent. When the design drifts, the team fixes it through refactoring and a quick design discussion.

## d. Relate the architecture to design.
### 1) Identify software system elements that relate to architectural entities and the nature of these relationships.

a. f
b. CRC cards and metaphor names map directly onto classes, modules and packages in the code. The code structure itself shows which elements implement which entity.

### 2) Define the interfaces and interactions among the software system elements and external entities.

a. f
b. Test-driven development defines interfaces by writing tests first. Integration tests and mocks pin down interactions between elements and with external systems.

### 3) Partition, align and allocate requirements to architecture entities and system elements.

a. i
b. Stories are split during the planning game and assigned to iterations and pairs. Each story’s acceptance tests are tied to the components that implement it.

### 4) Map software system elements and architecture entities to design characteristics.

a. i
b. Simple design rules (passes all tests, no duplication, expresses intent, minimal elements) and coding standards set the design characteristics. Refactoring brings the elements into line with them.

### 5) Define principles for the software system design and evolution

a. h
b. XP’s principles are simplicity, YAGNI, once and only once, continuous refactoring, small releases and coding standards. They guide how the design evolves.

## e. Assess architecture candidates.
### 1) Assess each candidate architecture against constraints and requirements.

a. g
b. Spikes, automated acceptance tests and performance or load tests show whether a candidate meets constraints and requirements. The result is evidence from working code.

### 2) Assess each candidate architecture against stakeholder concerns using evaluation criteria.

a. g
b. The customer reviews working software in iteration demos and checks it against the agreed acceptance criteria. Feedback shapes the next planning game.

### 3) Select the preferred architecture(s) and capture key decisions and rationale.

a. g
b. The whole team decides, usually at planning, in a stand-up or at the whiteboard, and picks the simplest option that satisfies the tests. The decision is noted on cards, in the wiki or in commit messages.

### 4) Establish the architecture baseline of the selected architecture.

a. h
b. The baseline is a tagged version in source control with a green CI build, passing tests and a deployed small release.

## f. Manage the selected architecture.
### 1) Formalize the architecture governance approach and specificy governance-related roles and responsibilities, accountabilities, and authorities related to the design, quality, security, and safety.

a. h
b. Governance is team-based. The coach keeps the team on the practices, the customer has authority over priorities and acceptance, and the whole team shares responsibility for design quality through collective ownership, pair programming and coding standards. Security and safety needs become stories and tests.

### 2) Obtain explicit acceptance of the architecture by stakeholders.

a. a
b. The customer accepts the work by running the acceptance tests and reviewing each iteration’s working software. Acceptance happens continuously, not in one sign-off.

### 3) Maintain concordance and completeness of the architectural entities and characteristics.

a. i
b. Continuous integration, the automated test suite and ongoing refactoring keep the architecture consistent and complete as the code changes.

### 4) Organize, assess and control evolution of the architecture mdoels and views to help ensure that the architectural intent is met and the architectural vision and key concepts are correctly implemented.

a. h
b. The team controls evolution through small releases, refactoring, pair programming, code reviews and retrospectives. The metaphor is revisited and updated so the shared vision stays accurate.

### 5) Maintain the architecture definition and evaluation strategy.

a. h
b. Retrospectives and iteration or release planning are where the team revises its architectural approach, tests and criteria as it learns.

### 6) Maintain traceability of the architecture.

a. k
b. Traceability runs from story card to acceptance test, to code and to commit or issue ID. Test names and the version control history show which requirement drove each element.

### 7) Provide key artifacts and information items that have been selected for baselines.

a. h
b. The key artifacts are the working software, the automated test suite, the tagged releases and the minimal documentation the team chose to keep (such as the metaphor description and the story and test records).

---

## 6.4.5 Design Definition process

**Owner:** Emma

<!-- Emma: add your task responses below. Please leave the other sections unchanged. -->

### Task responses

<!--
Copy this block once per task:

#### Task: [task identifier or short name]

- **Process outcome:** [single letter]
- **XP implementation:** [How XP implements this task.]
- **XP book quote(s):** “[Direct quote]” ([page or locator])
-->