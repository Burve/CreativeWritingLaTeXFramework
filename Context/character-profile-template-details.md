# Character Profile Template

## LaTeX Commands
```latex
% Character's Primary Name
\NewDocumentCommand{\character}{}{Full Character Name} 
% The LaTeX command must be easy to remember and associated with the character. For example,
% Main character of the story gets command \character. If there is a king or a princess they got a simple to remember command \king or \princess. 
% In some cases command goes with a simple visual description by one or two words or by job description\dots
% the point of the command is to have an easy to remember command while actual fancy name is saved in it and replaced during compilation.
\NewDocumentCommand{\characterShort}{}{Short Name/Nickname}
\NewDocumentCommand{\characterTitle}{}{Character's Title (if applicable)}

% Additional Character-Specific Commands (if needed)
\NewDocumentCommand{\characterSpecial}{}{Special Designation}
```

## Basic Information
- **Full Name:** [Character's complete name, including any titles]
- **Age:** [Character's age and any relevant age-related context]
- **Birthday:** [Character's birthday in age-related context]
- **Gender:** [Character's Gender]
- **Species/Origin:** [Character's species, race, or origin]
- **Position/Role:** [Character's primary role or occupation]
- **Location:** [Primary location/base of operations]

## Physical Characteristics
- **Height:** [Character's Height]
- **Weight:** [Character's Weight]
- **Hair Color:** [Character's hair Color]
- **Eye Color:** [Character's eye Color]
- **Blood Type:** [Character's blood type - can be medically relevant or culturally significant for personality references]
- **Notable Features:** [Distinctive physical characteristics: scars, tattoos, birthmarks, prosthetics, etc.]

### Body Measurements (for visual depiction)
**Female Characters (mandatory):**
- **Bust:** [Measurement]
- **Waist:** [Measurement]
- **Hips:** [Measurement]

**Male Characters (recommended):**
- **Chest:** [Measurement]
- **Waist:** [Measurement]
- **Shoulders:** [Measurement]

## Background
### Personal History
- Key events that shaped the character
- Important achievements or milestones
- Significant relationships or connections

### Current Role/Status
- Present responsibilities
- Recent developments
- Ongoing projects or missions

## Motivations & Goals
### Primary Motivation
- What drives this character fundamentally?
- Core desires or needs

### Short-term Goals
- Immediate objectives
- Current chapter/arc goals

### Long-term Goals
- Story-spanning ambitions
- Ultimate desires or fears

### Internal Conflict
- Contradictions in desires
- Moral dilemmas

## Personality Traits
### Strengths
- List key positive attributes
- Notable skills or abilities
- Special talents

### Weaknesses/Flaws
- Character flaws that create conflict
- Vulnerabilities (emotional, physical, social)
- Blind spots or biases

### Quirks
- Distinctive behavioral patterns
- Unique habits or mannerisms
- Personal peculiarities

## Speech Pattern
### General Characteristics
- Overall speaking style
- Accent or dialect notes
- Common phrases or expressions

### Speech Examples
```latex
\say{\character}{"Example dialogue showing typical speech pattern"}

\say{\characterShort}{"Example showing casual or informal speech"}

% Formal dialogue with action
\say{\character}{"Your statement requires careful consideration." She tilted her head thoughtfully.}

% Informal dialogue with response
\say{\character}{"I understand your concern." Her voice softened. "Let me explain further."}

% Dialogue with interruption
\say{\character}{"We should—" She paused, considering her next words. "Perhaps a different approach."}

% Dialogue with modifier
\say{\character}[whispered]{I wonder if anyone hears me.}  

% Inner Thoughts: indicating who is thinking.
\thought{\character}{Maybe I shouldn't have said that...}

```

## Special Abilities/Skills
### Primary Abilities
- Main powers or capabilities
- Skill limitations
- Special techniques

### Equipment/Tools
- Standard equipment
- Special items
- Technological aids

## Character Arc
### Starting Point
- Initial worldview or flaw
- Beginning state of being
- Core belief to be challenged

### Transformation Triggers
- Key events that will change them
- Catalysts for growth
- Turning points in the story

### Ending Point (Intended)
- How they should evolve
- Resolution of internal conflicts
- Final state of being

## Relationships
### Key Connections
- Important relationships with other characters
- Group affiliations
- Professional networks

### Interaction Patterns
- How they relate to others
- Communication preferences
- Social dynamics

## Writing Guidelines
### Scene Integration
1. How to introduce the character
2. Typical behavior in scenes
3. Interaction patterns with others

### Error Prevention
- Common mistakes to avoid
- Character consistency notes
- Important limitations

## Visual Description
- Detailed description for illustration purposes
- Key visual elements that must be consistent
- Iconic poses or expressions
- Costume/clothing details
- Special effects or visual quirks
- Notable animation considerations

## Additional Notes
- Miscellaneous important information
- Future plot considerations
- Special requirements for writing the character
- Personality type indicators (MBTI, etc.)
- Cultural or social influences on behavior
- Secrets (what the character hides from others and/or themselves)
- Fears and phobias
- Theme connection (how this character embodies or challenges story themes)

## Usage Notes
1. All sections should be filled out as completely as possible for main characters
2. Secondary characters may have abbreviated profiles focusing on key elements
3. Update profile as character develops through the story
4. Ensure LaTeX commands match naming conventions
5. Include relevant cross-references to other character profiles
6. Add specific section examples from story when available
7. Always create a character profile as an external file
8. Body measurements are mandatory for female characters, recommended for male characters