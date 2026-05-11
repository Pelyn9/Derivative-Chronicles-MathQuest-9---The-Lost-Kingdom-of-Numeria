# GAME DESIGN DOCUMENT (GDD)
## Derivative Chronicles: MathQuest 9 – The Lost Kingdom of Numeria

---

## 1. GAME OVERVIEW

| Field | Details |
|-------|---------|
| **Genre** | Educational RPG + Puzzle + Quiz-Based Adventure |
| **Platform** | Mobile (Android) – Built with React Native / Expo |
| **Target Users** | Grade 9 Students (Philippines – MATATAG Curriculum) |
| **Deployment** | Offline-capable Android APK |

**Game Description:**

MathQuest 9 is a gamified mobile learning application designed to enhance students' mathematical literacy, performance, attitude, and reduce math anxiety. Players journey through the fictional kingdom of Numeria, where solving math problems restores balance to the land. The game combines RPG exploration, puzzle mechanics, and quiz-based challenges aligned with the Grade 9 MATATAG Curriculum.

---

## 2. LEARNING OBJECTIVES

The game aligns with the Grade 9 MATATAG Curriculum, focusing on four core domains:

| Domain | Topics Covered |
|--------|----------------|
| **Arithmetic & Math Literacy** | Real-number operations, percentages, ratios, data interpretation |
| **Geometry** | Lines, angles, angle pairs, parallel lines cut by a transversal |
| **Relations and Functions** | Ordered pairs, domain and range, function notation, mapping diagrams |
| **Linear Functions** | Slope, graphing linear equations, slope-intercept form, real-world modeling |

**Learning Outcomes:**

- Improve problem-solving skills through contextualized math challenges
- Develop conceptual understanding via interactive simulations
- Increase confidence in mathematics through mastery-based progression
- Reduce math anxiety through low-stakes, self-paced gameplay
- Foster positive attitude toward mathematics via gamified reward systems

---

## 3. GAMEPLAY

### Core Premise
Players take the role of a **Math Hero** tasked with saving the kingdom of Numeria from mathematical chaos.

### Structure
- **Each Module** = a world/kingdom with a unique theme
- **Each Lesson** = a level/mission within that world
- **Each Level** = a series of math challenges to complete

### Core Gameplay Loop

```
┌─────────────┐
│ Explore Area │
└──────┬──────┘
       ↓
┌──────────────────┐
│ Encounter Challenge│
└──────┬───────────┘
       ↓
┌──────────────────┐
│ Solve Math Problem │
└──────┬───────────┘
       ↓
┌──────────────────┐
│  Receive Feedback  │
└──────┬───────────┘
       ↓
┌──────────────────┐
│   Earn Rewards     │
└──────┬───────────┘
       ↓
┌──────────────────┐
│ Unlock Next Level  │
└──────────────────┘
```

### Player Actions
- Tap to navigate areas and select levels
- Solve math problems (multiple-choice, open-ended, drag-and-drop)
- Interact with NPCs (Non-Player Characters) for story and hints
- Collect coins, badges, and unlockable avatars
- Manage lives and use lifelines strategically

---

## 4. GAME MECHANICS

### Core Mechanics

| Mechanic | Description |
|----------|-------------|
| **Problem-Solving Quests** | Each level presents a themed quest requiring math solutions |
| **Multiple-Choice Questions** | Standard quiz format with 4 options |
| **Open-Ended Questions** | Numerical/text input for constructed responses |
| **Timed Challenges** | Optional speed rounds for bonus rewards |
| **Interactive Simulations** | Drag-to-graph, tap-to-select-angle, slider-based exploration |

### Lives System

```
❤️ ❤️ ❤️  = Full lives (3 total)
💔 ❤️ ❤️  = 1 life lost
```

- Players start each session with **3 lives**
- Each incorrect answer costs **1 life**
- Lives regenerate at a rate of **1 life per 30 minutes** (offline-capable timer)
- When all lives are depleted, players must wait or watch an optional ad to restore
- Lives are never lost on tutorial or practice levels

### Lifelines

| Lifeline | Effect | Cooldown |
|----------|--------|----------|
| **50/50** | Eliminates two incorrect answers | 1 per level |
| **Hint** | Reveals a helpful clue or formula | 1 per level |
| **Call a Friend** | AI-powered hint system that breaks down the problem step-by-step | 1 per 3 levels |

### Reward System

| Reward Type | How to Earn | Usage |
|-------------|-------------|-------|
| **Coins** | Correct answers, streak bonuses, level completion | Buy hints, avatar unlocks, power-ups |
| **Badges** | Achievement milestones (e.g., "Perfect Score," "Speed Demon") | Profile display, bragging rights |
| **Unlockable Avatars** | Complete modules, reach score thresholds | Customize player character |
| **Level Progression** | Clear all challenges in a level | Access next level/module |

### Scoring Formula

```
Score = Base Points × Difficulty Multiplier × Streak Bonus
       + Time Bonus (if applicable)
```

| Factor | Value |
|--------|-------|
| Base Points | 100 per correct answer |
| Difficulty Multiplier | Easy: 1.0 / Medium: 1.5 / Hard: 2.0 |
| Streak Bonus | ×1.0 (base), +0.1 per consecutive correct (max ×2.0) |
| Time Bonus | Up to +50 points for speed (timed challenges only) |

---

## 5. STORYLINE

### Backstory

The kingdom of **Numeria** was once a land where mathematics kept the world in perfect balance. Rivers flowed at precise angles, bridges stood strong through geometric integrity, and trade flourished through accurate calculation.

But then came the **Chaos of Miscalculation**.

The evil **Null Master** — a being born from forgotten formulas and corrupted equations — spread mathematical decay across the land. Numbers no longer add up. Angles are warped. Functions behave unpredictably.

### Player's Mission

You are the **Math Hero**, the last hope of Numeria. Guided by the wise elder **Sage Digit**, you must:

1. **Restore lost concepts** — Recover scattered mathematical knowledge
2. **Defeat math-based enemies** — Overcome corrupted numbers and geometric monstrosities
3. **Solve real-world problems** — Help Numerians rebuild their city, market, and lives
4. **Defeat the Null Master** — Restore balance once and for all

### Narrative Progression

| Module | Story Chapter | Villain / Boss |
|--------|---------------|----------------|
| 1: Arithmetic | The Village of Traders | The Interest Goblin |
| 2: Geometry | The City of Architects | The Angle Wraith |
| 3: Relations & Functions | The Data Kingdom | The Function Phantom |
| 4: Linear Functions | The City of Motion | The Slope Shadow |
| Final | The Null Tower | The Null Master |

---

## 6. EDUCATIONAL DESIGN (THEORY-BASED)

The game is grounded in four established learning theories:

### Constructivism

| Principle | Application in Game |
|-----------|-------------------|
| Active problem-solving | Players construct knowledge by solving contextualized problems |
| Inquiry-based learning | Exploration zones encourage discovery before direct instruction |
| Scaffolding | Difficulty gradually increases; hints provide just-in-time support |

### Cognitive Theory of Multimedia Learning (CTML) sdasd

| Principle | Application in Game |
|-----------|-------------------|
| Visual + audio explanations | Animated tutorials with narration |
| Interactive animations | Graph builders, angle explorers, function machines |
| Segmenting | Content broken into bite-sized levels |
| Signaling | Key information highlighted in problems |

### Math Anxiety Reduction Strategies

| Strategy | Implementation |
|----------|----------------|
| Immediate feedback | Correct/incorrect shown instantly with explanation |
| No public failure | All results are private to the player |
| Self-paced learning | No time limits on standard levels |
| Mastery orientation | Players can retry levels to improve scores |
| Encouraging language | "Great effort!" / "Almost there!" / "You're improving!" |

### Technology Acceptance Model (TAM)

| Factor | Design Consideration |
|--------|---------------------|
| Perceived Ease of Use | Simple navigation, large touch targets, consistent UI |
| Perceived Usefulness | Clear alignment with curriculum, real-world applications |
| Attitude Toward Using | Engaging visuals, story-driven, rewarding progression |

---

## 7. GAME STRUCTURE (MODULES)

### MODULE 1: Arithmetic & Math Literacy — Village of Traders

| Level | Activity | Math Focus |
|-------|----------|------------|
| 1.1 | **Palengke Math** — Help vendors calculate totals, change, and discounts | Percentages, decimals, money operations |
| 1.2 | **Budget Simulator** — Plan a weekly budget for a Numerian family | Addition, subtraction, budgeting |
| 1.3 | **Graph Interpretation** — Read sales charts and predict trends | Data interpretation, line graphs, bar charts |
| 1.4 | **Boss: The Interest Goblin** — Solve compound interest and markup problems | Percentage increase, interest |

### MODULE 2: Geometry — City of Architects

| Level | Activity | Math Focus |
|-------|----------|------------|
| 2.1 | **Angle Explorer** — Identify and measure angles in buildings | Acute, obtuse, right, straight angles |
| 2.2 | **Construction Simulator** — Build stable structures using correct angle pairs | Complementary, supplementary, adjacent angles |
| 2.3 | **Transversal Puzzle** — Solve parallel lines cut by a transversal | Corresponding, alternate interior/exterior, same-side interior |
| 2.4 | **Boss: The Angle Wraith** — Repair a warped bridge using angle relationships | All angle pair types |

### MODULE 3: Relations & Functions — Data Kingdom

| Level | Activity | Math Focus |
|-------|----------|------------|
| 3.1 | **Function Machine** — Input-output exploration | Function as a rule, function notation f(x) |
| 3.2 | **Mapping Game** — Connect inputs to correct outputs | Ordered pairs, mapping diagrams |
| 3.3 | **Domain & Range Challenge** — Identify valid domains and ranges | Domain, range, vertical line test |
| 3.4 | **Boss: The Function Phantom** — Classify relations as functions or not | Function vs. relation identification |

### MODULE 4: Linear Functions — City of Motion

| Level | Activity | Math Focus |
|-------|----------|------------|
| 4.1 | **Graph Builder** — Plot points and draw lines | Coordinate plane, plotting, graphing linear equations |
| 4.2 | **Slope Simulator** — Explore slope through ramps and hills | Slope = rise/run, positive/negative/zero/undefined |
| 4.3 | **Real-Life Modeling** — Model speed, cost, and growth scenarios | y = mx + b, slope-intercept form, word problems |
| 4.4 | **Boss: The Slope Shadow** — Race to graph the correct line | Graphing linear functions under time pressure |

---

## 8. USER INTERFACE (UI)

### Key Screens

| Screen | Purpose |
|--------|---------|
| **Home Dashboard** | Welcome, player stats, quick-access to modules |
| **Map Navigation** | World map showing module locations and progress |
| **Level Select** | Levels within a module with lock/unlock states |
| **Lesson Screen** | Instructional content with animations and examples |
| **Quiz Interface** | Question display, answer options, timer, lifelines |
| **Results & Feedback** | Score summary, correct/incorrect review, encouragement |
| **Profile** | Avatar, badges, coins, achievement progress |
| **Settings** | Sound, music, reset progress, about |

### Design Principles

- **Simple and clean**: Minimalist layout to avoid cognitive overload
- **Color-coded modules**:
  - Module 1: Green (🟢 Village of Traders)
  - Module 2: Blue (🔵 City of Architects)
  - Module 3: Purple (🟣 Data Kingdom)
  - Module 4: Red (🔴 City of Motion)
- **Touch-friendly**: Minimum 48x48dp touch targets
- **Consistent navigation**: Bottom tab bar + back button
- **Readable typography**: Sans-serif fonts, minimum 16sp body text
- **High contrast**: Dark text on light backgrounds for readability

### Wireframe Layout (Quiz Screen)

```
┌─────────────────────────────────────┐
│  [< Back]  Level 1.3   ❤️❤️❤️  🪙 150 │
├─────────────────────────────────────┤
│                                     │
│   ┌─────────────────────────────┐   │
│   │                             │   │
│   │  Question / Problem Text    │   │
│   │                             │   │
│   │  [Interactive Element]      │   │
│   │                             │   │
│   └─────────────────────────────┘   │
│                                     │
│   ┌─────────────────────────────┐   │
│   │  ○ Option A                 │   │
│   ├─────────────────────────────┤   │
│   │  ○ Option B                 │   │
│   ├─────────────────────────────┤   │
│   │  ○ Option C                 │   │
│   ├─────────────────────────────┤   │
│   │  ○ Option D                 │   │
│   └─────────────────────────────┘   │
│                                     │
│   [💡 Hint]  [50/50]  [📞 Friend]   │
│                                     │
│          [Submit Answer]            │
└─────────────────────────────────────┘
```

---

## 9. ASSESSMENT SYSTEM

### Pre-Test / Post-Test

- **Pre-Test**: Administered before Module 1 to establish baseline
- **Post-Test**: Administered after Module 4 to measure improvement
- Both tests contain 20 items covering all four domains
- Results are stored locally and displayed as growth metrics

### In-Game Assessment

| Metric | Tracking Method |
|--------|-----------------|
| **Score per level** | Points accumulated from correct answers |
| **Accuracy** | Percentage of correct answers per level/module |
| **Time performance** | Average time per question |
| **Streak records** | Longest consecutive correct streak |
| **Lives used** | Total lives lost per session |

### Learning Analytics Dashboard

- Progress bar per module showing completion percentage
- Radar chart comparing performance across four domains
- Weak topic identification (topics with < 70% accuracy)
- Historical performance trends across sessions
- All data stored locally using SQLite/AsyncStorage

---

## 10. FEEDBACK SYSTEM

### Immediate Feedback

| Response | Visual | Audio |
|----------|--------|-------|
| **Correct** | Green glow, checkmark animation | Positive chime |
| **Incorrect** | Red highlight, X mark | Gentle buzz |
| **Partial Credit** | Yellow glow, half-check | Neutral tone |

### Step-by-Step Solutions

- After each incorrect answer, a detailed solution is shown
- Solutions break down the problem into 3-5 steps
- Key formulas and concepts are highlighted
- Players can bookmark solutions for review

### Encouraging Messages

| Context | Message Examples |
|---------|-----------------|
| Correct answer | "Great work!" / "You're on fire!" / "Brilliant!" |
| Streak milestone | "5 in a row! Amazing!" / "Unstoppable!" |
| Incorrect answer | "Nice try! Let's see how to solve it." / "Almost! Here's the trick." |
| Level complete | "Level cleared! You're a Math Hero!" |
| Module complete | "You've saved this kingdom! Onward!" |

---

## 11. BENEFITS & CHALLENGES

### Benefits

| Benefit | Description |
|---------|-------------|
| **Increased engagement** | Gamification motivates repeated practice |
| **Reduced math anxiety** | Private, self-paced, encouraging environment |
| **Real-life application** | Contextualized problems show math relevance |
| **Mastery learning** | Retry mechanics ensure concept mastery |
| **Curriculum alignment** | Directly supports Grade 9 MATATAG competencies |
| **Offline accessibility** | No internet required after installation |

### Challenges & Mitigations

| Challenge | Mitigation |
|-----------|------------|
| **Device availability** | Lightweight app works on budget Android devices |
| **Internet dependency** | Fully offline after initial install |
| **Learning curve for teachers** | Teacher guide included; simple integration |
| **Student motivation over time** | New content, badges, and story updates |
| **Screen time concerns** | Levels designed to be 10-15 minutes each |

---

## 12. DEVELOPMENT MODEL

### ADDIE Model

| Phase | Activities |
|-------|-----------|
| **Analysis** | Needs assessment, curriculum mapping, learner analysis |
| **Design** | GDD creation, wireframing, question bank development |
| **Development** | React Native coding, asset creation, database setup |
| **Implementation** | Beta testing, teacher training, deployment to Play Store |
| **Evaluation** | Pre/post-test analysis, user feedback, iteration |

### Technology Stack

| Layer | Technology |
|-------|-----------|
| **Framework** | React Native (Expo managed workflow) |
| **Navigation** | @react-navigation/native (stack + bottom tabs) |
| **State Management** | React Context API + useReducer |
| **Local Storage** | @react-native-async-storage/async-storage |
| **Icons** | @expo/vector-icons |
| **Animations** | React Native Animated API + react-native-reanimated |
| **Build** | Expo EAS Build (APK/AAB) |

---

## 13. TECHNICAL REQUIREMENTS

### Minimum Specifications

| Requirement | Specification |
|-------------|---------------|
| **Operating System** | Android 7.0 (API 24) or higher |
| **RAM** | 2 GB minimum |
| **Storage** | 100 MB free space |
| **Processor** | 1.5 GHz quad-core |
| **Internet** | Not required (fully offline) |
| **Display** | 720p or higher |

### Performance Targets

- App bundle size: < 60 MB
- Load time: < 3 seconds on cold start
- Frame rate: 60 FPS on target devices
- Battery usage: Minimal (no background services)

---

## 14. SUCCESS METRICS

| Metric | Measurement Method | Target |
|--------|-------------------|--------|
| **Improved test scores** | Pre-test vs. post-test comparison | ≥ 20% improvement |
| **Reduced anxiety levels** | Pre/post Math Anxiety Scale survey | ≥ 15% reduction |
| **Positive student feedback** | In-app ratings and survey | ≥ 4.0 / 5.0 average |
| **Increased engagement time** | Total play time per student | ≥ 60 minutes/week |
| **Module completion rate** | % of players completing all modules | ≥ 70% |
| **Accuracy improvement** | Accuracy trend across levels | ≥ 10% increase |

---

## 15. FUTURE ENHANCEMENTS

| Enhancement | Description | Priority |
|-------------|-------------|----------|
| **Multiplayer mode** | Real-time quiz battles between classmates | Medium |
| **Leaderboards** | Class-level and school-level rankings | Medium |
| **AI Tutor** | Adaptive difficulty based on player performance | High |
| **Expanded topics** | Grade 10+ content (polynomials, trigonometry, statistics) | Low |
| **Teacher Dashboard** | Web-based analytics for teachers to monitor classes | High |
| **iOS Support** | Expand to iPhone and iPad | Medium |
| **Cloud Sync** | Sync progress across devices | Low |
| **AR Math** | Augmented reality geometry exploration | Low |

---

## APPENDIX A: Sample Question Bank

### Module 1 — Arithmetic
```
Q: Aling Maria sold 15 kilograms of rice at Php 52 per kilo.
   How much did she earn in total?
A) Php 670
B) Php 780 ←
C) Php 800
D) Php 750
```

### Module 2 — Geometry
```
Q: Two angles are complementary. One measures 35°.
   What is the measure of the other angle?
A) 45°
B) 55° ←
C) 65°
D) 145°
```

### Module 3 — Relations & Functions
```
Q: If f(x) = 2x + 3, what is f(4)?
A) 8
B) 9
C) 11 ←
D) 12
```

### Module 4 — Linear Functions
```
Q: What is the slope of the line passing through (1,2) and (3,6)?
A) 1
B) 2 ←
C) 3
D) 4
```

---

## APPENDIX B: Badge Catalog

| Badge | Requirement |
|-------|-------------|
| 🏅 **First Steps** | Complete your first level |
| 🔥 **On Fire** | Get 5 consecutive correct answers |
| 💯 **Perfect Score** | Complete a level with 100% accuracy |
| ⚡ **Speed Demon** | Complete a timed challenge with full marks |
| 🛡️ **Module Master** | Complete all levels in a module |
| 👑 **Numeria's Savior** | Complete the entire game |
| 💰 **Trader Tycoon** | Collect 1000 coins |
| 📚 **Bookworm** | View 10 solution explanations |
| 🔁 **Comeback King** | Complete a level without losing any lives |

---

## APPENDIX C: Localization Notes

- All text content uses **English** for math instruction
- Story and NPC dialogue uses **English with Filipino expressions**
- Currency references use **Philippine Peso (Php)**
- Real-world contexts are Philippines-specific (palengke, jeepney, etc.)

---

*Document Version 1.0 — Prepared for MathQuest 9 Development*
