# Open Piano Skills

**A comprehensive, open-source framework for piano skill development**

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

---

> **Note: This is an early release.** We're sharing this framework to gather feedback and invite collaboration. If you know of similar existing systems (skill taxonomies, piano curricula, learning frameworks), please let us know - we'd love to learn from them and potentially integrate proven approaches.
>
> **How this was created:** The initial version was generated with significant AI assistance, then refined through manual iterations. We see this as a starting point for community collaboration - not a finished product. Expert review and real-world testing are needed to validate and improve the skill definitions, dependencies, and exercises.
>
> **What's working:** The skill catalog and exercises are usable as reference material.
>
> **What's planned:**
> - Interactive skill graph explorer (visual navigation)
> - Personalized learning path generation
> - Assessment tools to identify skill gaps
> - More genre-specific content
>
> We believe in building this openly with the community rather than in isolation. Your feedback, corrections, and contributions are genuinely welcome!

---

## What is this?

Open Piano Skills is a structured catalog of piano skills, exercises, and learning paths. It provides:

- **131 Skills** organized in 18 categories
- **Mastery Levels 1-10** with clear progression criteria
- **Skill Dependencies** showing what to learn first
- **Genre-specific Exercises** (Gospel, Jazz, Classical, etc.)
- **Learning Paths** with checkpoints and assessments
- **Curriculum Mappings** (customizable for different standards)

Think of it as a "skill tree" for piano - like in video games, but for real musical development.

---

## Who is this for?

- **Piano Teachers** - Structure your curriculum, track student progress
- **Self-learners** - Know exactly what to practice next
- **App Developers** - Build learning apps on a solid pedagogical foundation
- **Researchers** - Study skill acquisition and music education

---

## Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Ways to contribute:**
- Add or improve exercises
- Suggest new skills or corrections
- Add genre-specific content
- Report issues or inconsistencies

---

## Structure

```
open-piano-skills/
├── catalog/           # Skill definitions with dependencies
│   ├── _index.yaml    # Master index with categories and skill types
│   ├── scales.yaml    # Scale skills (major, minor, modes, etc.)
│   ├── chords.yaml    # Chord skills (triads, 7ths, extensions)
│   ├── harmony.yaml   # Harmony theory (functions, cadences)
│   └── ...            # 18 categories total
├── exercises/         # Exercises per skill and level
├── paths/             # Learning paths and checkpoints
│   ├── generic.yaml   # Universal piano checkpoints
│   └── gospel.yaml    # Gospel-specific path
├── genres/            # Genre-specific skill weights and exercises
└── prompts/           # AI goal-mapping templates
```

---

## Skill Types

| Type | Description | Example |
|------|-------------|---------|
| **MECHANICAL** | Physical technique | Scale fingering, hand position |
| **THEORETICAL** | Knowledge & understanding | Chord structure, key signatures |
| **AUDITORY** | Listening & recognition | Interval recognition, chord quality |
| **COGNITIVE** | Mental processing | Sight reading, transposition |
| **EXPRESSIVE** | Musical expression | Dynamics, phrasing |
| **META** | Combines multiple skills | Improvisation, accompaniment |

---

## Mastery Levels

| Level | Description |
|-------|-------------|
| 1-2 | **Beginner** - One key, slow, with conscious effort |
| 3-4 | **Elementary** - Several keys, basic application |
| 5-6 | **Intermediate** - All keys, fluent tempo |
| 7-8 | **Advanced** - Creative application, variations |
| 9-10 | **Professional** - Virtuosity, innovation, under pressure |

---

## Example: A Skill Definition

```yaml
scale_playing:
  name: Scale Playing
  type: MECHANICAL
  requires:
    - scale_fingering_standard
    - keyboard_note_location
  variants:
    major:
      name: Major Scale
      mastery:
        1: "Play C major with correct fingering, one octave"
        5: "Play major scales in all 12 keys, 2 octaves, fluent"
        10: "Virtuosic scales at any tempo, any key, musical expression"
    minor_natural:
      name: Natural Minor Scale
      # ...
```

---

## How to Use

### For Teachers/Learners
Browse the catalog to understand skill progressions. Use the exercises as practice guides.

### For Developers
Parse the YAML files to build apps, progress trackers, or curriculum planners.

```python
import yaml

with open('catalog/scales.yaml') as f:
    scales = yaml.safe_load(f)

# Access skill definitions
major_scale = scales['skills']['scale_playing']['variants']['major']
print(major_scale['mastery'][5])
# → "Play major scales in all 12 keys, 2 octaves, fluent"
```

---

## Attribution

When using this work, please include:

> **"Open Piano Skills"** - [https://the-ultimate-piano.com](https://the-ultimate-piano.com)
> Licensed under [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)

---

## License

This work is licensed under [Creative Commons Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/).

You are free to share and adapt this work, even commercially, as long as you:
1. Give appropriate credit with a link to https://the-ultimate-piano.com
2. License your adaptations under the same terms

---

## Acknowledgments

Created and maintained by the community at [the-ultimate-piano.com](https://the-ultimate-piano.com).

Special thanks to all contributors who help make piano education more accessible.
