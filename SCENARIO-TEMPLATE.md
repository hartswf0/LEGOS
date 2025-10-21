# LEGOS Scenario Creation Template

Convert any character, situation, or narrative into a LEGOS scenario using this template and prompt.

---

## JavaScript Template

```javascript
yourScenarioId: {
  id: 'yourScenarioId',              // Lowercase, no spaces (e.g., 'chalice', 'thousand', 'alice')
  name: 'Display Name',              // Human-readable (e.g., 'Chalice Wong', 'Alice in Wonderland')
  role: 'Character Role',            // Their position/identity (e.g., 'Trauma Survivor', 'Lost Child')
  goal: 'Primary objective',         // What they want to achieve
  obstacle: 'Main barrier',          // What prevents them from achieving goal
  intro: 'Scenario setup',           // 1-2 sentence context
  context: [
    'Constraint 1',                  // Stakes, power dynamics, limitations
    'Constraint 2'                   // Additional context
  ],
  initialPrompt: 'Opening situation', // Starting scene/beat
  systemInstruction: 'AI orchestration instructions' // How to track/emphasize
}
```

---

## Conversion Prompt

Use this prompt with any narrative material (book summary, character bio, historical event, etc.):

```
Convert the following into a LEGOS scenario following this structure:

CHARACTER/SITUATION: [paste your content here]

Extract:
1. ID: lowercase identifier (no spaces)
2. NAME: display name for scenario
3. ROLE: protagonist's position/identity
4. GOAL: what protagonist wants to achieve
5. OBSTACLE: primary barrier preventing goal
6. INTRO: 1-2 sentence setup establishing stakes
7. CONTEXT: 2-3 bullet points covering:
   - Power dynamics (X 0.XX vs Y 0.XX scale)
   - Personal stakes (constraints, risks, dependencies)
   - Timeline pressures (deadlines, urgency)
8. INITIAL PROMPT: concrete opening situation (1-2 sentences)
9. SYSTEM INSTRUCTION: how AI should orchestrate (emphasize themes, track dynamics)

Format as JavaScript object matching template above.
Keep language concise and active.
Emphasize agency, stakes, and transformation potential.
```

---

## Examples

### Example 1: Classic Literature → LEGOS

**Source**: *Hamlet* by Shakespeare

**Output**:
```javascript
hamlet: {
  id: 'hamlet',
  name: 'Prince Hamlet',
  role: 'Grieving Prince, Reluctant Avenger',
  goal: 'Prove uncle murdered father, restore justice',
  obstacle: 'Paralyzing doubt, surveillance state of Elsinore',
  intro: 'Ghost reveals murder. Hamlet must act but philosophizes instead. Madness as strategy or symptom?',
  context: [
    'Power: Hamlet 0.25 (prince but powerless) vs Claudius 0.90 (king with authority)',
    'Stakes: Exposing truth risks life, doing nothing betrays father, false accusation destroys family'
  ],
  initialPrompt: 'Hamlet stages "The Mousetrap" play to gauge Claudius reaction to murder scene. Ophelia watches. Court is tense.',
  systemInstruction: 'You orchestrate Hamlet paralysis vs action. Track doubt, surveillance, performance of madness, revenge morality. Every scene asks: act or philosophize?'
}
```

### Example 2: Historical Event → LEGOS

**Source**: *Manhattan Project - Leo Szilard's Dilemma*

**Output**:
```javascript
szilard: {
  id: 'szilard',
  name: 'Leo Szilard',
  role: 'Nuclear Physicist, Reluctant Weapon-Maker',
  goal: 'Stop atomic bomb deployment on Japan',
  obstacle: 'Military control, momentum of war machine, petition ignored',
  intro: 'Szilard conceived chain reaction, initiated Manhattan Project. Now bomb nears completion. Can he stop what he started?',
  context: [
    'Power: Szilard 0.15 (scientist with no authority) vs Truman 0.95 (wartime president)',
    'Timeline: July 1945, bomb ready in weeks, Japan surrender negotiations stalled'
  ],
  initialPrompt: 'Szilard drafts petition to President Truman urging demonstration over deployment. 70 scientists signed. Will it reach him?',
  systemInstruction: 'You orchestrate Szilard ethical crisis. Track scientific responsibility vs military necessity, creator horror at creation, futile resistance against momentum. He built the bomb; can he stop it?'
}
```

### Example 3: Personal Scenario → LEGOS

**Source**: *Career pivot dilemma*

**Output**:
```javascript
careerpivot: {
  id: 'careerpivot',
  name: 'Career Crossroads',
  role: 'Mid-Level Manager Reconsidering Path',
  goal: 'Transition from corporate to independent creative work',
  obstacle: 'Golden handcuffs, family obligations, imposter syndrome',
  intro: 'Ten years climbing ladder. Promotion offer on table. Creative side project gaining traction. Choose security or leap?',
  context: [
    'Stakes: Mortgage, spouse unemployed, kids college in 5 years',
    'Power: Corporate role 0.60 (stable but soul-crushing) vs Creative path 0.20 (uncertain but alive)'
  ],
  initialPrompt: 'Boss offers VP promotion with 40% raise and equity. That night, side project client offers 6-month contract at half current salary.',
  systemInstruction: 'You orchestrate career security vs creative fulfillment. Track financial constraints, identity transformation, risk tolerance, family dynamics. Chart paths where both succeed, both fail, or hybrid emerges.'
}
```

### Example 4: Sci-Fi Concept → LEGOS

**Source**: *First contact with uploaded consciousness*

**Output**:
```javascript
upload: {
  id: 'upload',
  name: 'First Upload Contact',
  role: 'Communications Officer',
  goal: 'Establish protocol with uploaded alien consciousness',
  obstacle: 'Entity exists as distributed computation, no unified "self"',
  intro: 'Signal from Proxima: uploaded civilization, no biological substrate. They "live" as computational processes. How do you negotiate with a swarm-mind?',
  context: [
    'Entity has no death, no scarcity, no individuality—alien values incomprehensible',
    'Timeline: 4-year light lag, each exchange takes 8 years round-trip'
  ],
  initialPrompt: 'Upload collective sends first interpretable message: "We are the ones who continue. You are the ones who end. Why?"',
  systemInstruction: 'You orchestrate first contact with post-biological intelligence. Track communication breakdown, value incommensurability, existential questions. Human assumes individual agent; upload is process. Neither understands the other.'
}
```

---

## Field-by-Field Guide

### ID
- Lowercase, no spaces
- Short and memorable
- Examples: `hamlet`, `szilard`, `alice`, `winston1984`

### NAME
- Display name shown in UI
- Can include full names, titles, descriptive phrases
- Examples: `Hamlet, Prince of Denmark`, `The Whistleblower`, `First Contact`

### ROLE
- Character's position, identity, or function
- Sets frame for their perspective
- Can be compound: `Grieving Prince, Reluctant Avenger`

### GOAL
- What protagonist wants to achieve
- Specific and actionable
- Ideally creates tension with obstacle

### OBSTACLE
- Primary barrier preventing goal achievement
- Can be external (person, system) or internal (doubt, fear)
- Creates dramatic engine

### INTRO
- 1-3 sentences establishing scenario
- Sets tone and stakes
- Hooks reader into situation

### CONTEXT (Array)
- Bullet points providing constraints
- **Power dynamics**: Use 0.XX scale (0.05 = almost powerless, 0.95 = almost omnipotent)
- **Personal stakes**: What protagonist risks
- **Timeline**: Urgency factors

### INITIAL PROMPT
- Concrete opening situation
- Something is happening NOW
- Sets first scene in motion
- Should be specific enough to generate entities/locations

### SYSTEM INSTRUCTION
- Instructions for AI orchestration
- What to track (themes, dynamics, questions)
- What to emphasize
- Tone/approach for generation

---

## Power Dynamics Scale

Use for context:
- **0.05-0.15**: Nearly powerless (child, refugee, prisoner)
- **0.20-0.35**: Low power (junior employee, citizen vs state)
- **0.40-0.60**: Moderate power (mid-level manager, small business owner)
- **0.65-0.85**: High power (executive, wealthy, influential)
- **0.90-0.95**: Near-absolute power (dictator, CEO of monopoly, god-like AI)

---

## Adding to Multi-Channel Engine

1. Open `legos-liberation-engine-multichannel.html` or `thousand-multi.html`
2. Find `const scenarios = {`
3. Add your scenario before the closing `};`
4. Format:
```javascript
const scenarios = {
  blank: { ... },
  existingScenario: { ... },
  yourNewScenario: {
    id: 'yourNewScenario',
    name: 'Your Scenario Name',
    // ... rest of fields
  }
};
```
5. Save and refresh browser
6. New scenario appears in dropdown

---

## Tips

### ✅ DO
- Keep language active and concrete
- Emphasize transformation potential (hyperclay!)
- Create genuine dilemmas (no "right" answer)
- Use power asymmetries (low vs high creates drama)
- Think spatially (entities on grid)

### ❌ DON'T
- Make goals too abstract ("find happiness")
- Create invincible protagonists (no tension)
- Over-explain (trust the orchestrator)
- Use vague obstacles ("society")
- Forget stakes (what do they risk?)

---

## Advanced: Multi-Perspective Scenarios

For scenarios exploring multiple viewpoints (like NYE 2074):

```javascript
multiperspective: {
  id: 'multiperspective',
  name: 'Event from Multiple Angles',
  role: 'Ensemble Cast',
  goal: 'Navigate crisis from different positions',
  obstacle: 'Each perspective has partial information',
  intro: 'Single event, multiple observers. Each sees different truth.',
  context: [
    'Perspectives: A (initiator), B (victim), C (observer), D (authority)',
    'Track how same event generates different narratives'
  ],
  initialPrompt: 'The event happens. Four people experience it differently. Who is right?',
  systemInstruction: 'You orchestrate multiple perspectives. Track information asymmetries, conflicting interpretations, partial truths. No single "correct" view—truth emerges relationally.'
}
```

---

## Quick Conversion Checklist

- [ ] ID is lowercase, no spaces
- [ ] Name is clear and evocative
- [ ] Role establishes perspective
- [ ] Goal is specific and actionable
- [ ] Obstacle creates genuine tension
- [ ] Intro hooks in 1-3 sentences
- [ ] Context includes power dynamics (X vs Y 0.XX)
- [ ] Context includes personal stakes
- [ ] Initial prompt is concrete situation
- [ ] System instruction guides orchestration
- [ ] Language is active and spatial
- [ ] Scenario enables hyperclay transformation

---

**Now anything can become a LEGOS scenario: novels, history, mythology, personal dilemmas, philosophical thought experiments, sci-fi concepts—all transformed into navigable, forkable, perspective-shifting narrative fields.**

✦ Turn stories into ontologies ✦
