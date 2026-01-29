# Contributing to Open Piano Skills

Thank you for your interest in contributing! This project thrives on community input from piano teachers, students, and enthusiasts.

---

## Ways to Contribute

### 1. Report Issues or Suggestions (No technical skills needed!)

The easiest way to contribute:

1. Go to [Issues](../../issues)
2. Click "New Issue"
3. Describe your suggestion or problem

**Examples:**
- "The exercise for swing_feel level 5 could be improved by..."
- "I think chord_playing should require interval_theory first"
- "There's a typo in the blues scale exercise"

We'll take care of the technical implementation!

---

### 2. Edit Files Directly on GitHub (Easy)

You can edit files directly in your browser:

1. Navigate to the file you want to edit
2. Click the **pencil icon** (Edit this file)
3. Make your changes
4. Scroll down and click **"Propose changes"**
5. Click **"Create pull request"**

That's it! We'll review your changes and merge them.

---

### 3. Fork and Submit Pull Requests (For developers)

1. Fork the repository
2. Create a branch: `git checkout -b my-improvement`
3. Make your changes
4. Commit: `git commit -m "Add exercise for X"`
5. Push: `git push origin my-improvement`
6. Open a Pull Request

---

## What Can You Contribute?

### Exercises
Add or improve exercises in `/exercises/`. Each skill needs exercises for levels 2-10.

```yaml
# Format
skill_name:
  2: "Exercise to reach level 2 from level 1"
  3: "Exercise to reach level 3 from level 2"
  # ... up to 10
```

**Good exercises are:**
- Specific and actionable
- Progressive (each level builds on the previous)
- Genre-aware when relevant (use default/gospel/jazz variants)

### Skills
Suggest new skills or improvements in `/catalog/`.

**Before adding a new skill, consider:**
- Does it fit an existing skill as a variant?
- What are its prerequisites (`requires`)?
- What type is it? (MECHANICAL, THEORETICAL, AUDITORY, COGNITIVE, EXPRESSIVE, META)

### Learning Paths
Improve checkpoints in `/paths/`. A checkpoint bundles skills that together enable a musical capability.

### Genre Content
Add genre-specific exercises or skill weightings in `/genres/`.

---

## File Format Guidelines

### YAML Structure

```yaml
# Use 2-space indentation
skills:
  skill_name:
    name: "Human Readable Name"
    type: MECHANICAL  # or THEORETICAL, AUDITORY, COGNITIVE, EXPRESSIVE, META
    requires:
      - prerequisite_skill_1
      - prerequisite_skill_2
    mastery:
      1: "Level 1 description"
      10: "Level 10 description"
```

### Writing Style

- **Exercises**: Start with a verb ("Play...", "Practice...", "Listen to...")
- **Mastery descriptions**: Describe the ability, not the exercise
- **Be concise**: One clear sentence per level when possible
- **Be specific**: "Play C major scale, 2 octaves" not "Play scales well"

### Genre Variants

For genre-specific content, use this format:

```yaml
skill_name:
  5:
    default: "General exercise for level 5"
    gospel: "Gospel-specific exercise for level 5"
    jazz: "Jazz-specific exercise for level 5"
```

---

## Review Process

1. All contributions are reviewed before merging
2. We may suggest changes or ask questions
3. Please be patient - we're volunteers!
4. Constructive feedback is always welcome

---

## Code of Conduct

- Be respectful and constructive
- Focus on the content, not the person
- Welcome newcomers
- Assume good intentions

---

## Questions?

- Open an [Issue](../../issues) with your question
- Join the discussion in [Discussions](../../discussions)

---

## License

By contributing, you agree that your contributions will be licensed under [CC-BY-SA 4.0](LICENSE), the same license as the project.

---

Thank you for helping make piano education more accessible!
