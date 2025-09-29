# New Workflow Usage Guide

## Quick Start

1. **Update roadmap** with short feature description
2. **Create draft** `N-{feature-name}-draft.md` with freeform description
3. **Refine with Claude** - iterate until requirements are clear
4. **Create final prompt** using the prompt template structure
5. **Implement** with Claude using the final prompt

## Workflow Phases Explained

### Phase 1: Roadmap Planning
- Add feature to roadmap.md with very brief description
- Focus on high-level capability, not implementation details
- Examples: "User Authentication", "File Upload", "Search Feature"

### Phase 2: Draft Creation
- Create `N-feature-name-draft.md` with freeform description
- Write like a user story or narrative
- Describe current vs desired behavior
- No structure required - just explain the need clearly

### Phase 3: Draft Refinement
- Ask Claude: "Please review this draft and identify unclear requirements"
- Answer Claude's questions to improve clarity
- Iterate multiple times until comprehensive
- Claude helps identify missing edge cases and requirements

### Phase 4: Final Prompt Creation
- Ask Claude: "Create a structured prompt using the prompt template"
- Claude fills in template sections based on refined draft
- May require iterations to complete all template sections
- Result should be implementation-ready prompt

## Tips for Better Drafts

### Write Narratively
❌ "Add authentication system"
✅ "Currently users can access all features without any login. We need users to create accounts and sign in to access personalized features. The flow should be: visit site → see login prompt → create account or sign in → access full functionality."

### Describe Current vs Desired State
- Explain how things work now (or don't work)
- Describe the desired user experience
- Include context about why the change is needed

### Think User-First
- Focus on user goals and pain points
- Describe the complete user journey
- Mention edge cases users might encounter

### Include Context
- Reference existing similar features
- Explain technical constraints you're aware of
- Mention integration points with current system

## Common Refinement Patterns

### Draft Refinement Iterations
**Round 1**: Claude identifies major missing pieces
- "What should happen when user forgets password?"
- "How should validation errors be displayed?"
- "What user roles need to be supported?"

**Round 2**: Claude asks about edge cases
- "What if user tries to register with existing email?"
- "Should there be session timeout?"
- "How to handle concurrent login attempts?"

**Round 3**: Claude clarifies technical details
- "Should this integrate with existing user table?"
- "What authentication library should be used?"
- "Are there specific security requirements?"

### Prompt Creation Iterations
**Round 1**: Basic template structure filled
- Core sections populated from draft
- May miss technical details

**Round 2**: Technical refinement
- Integration points clarified
- Performance requirements added
- Security considerations detailed

## Template Customization

### For Different Project Types
**Web API Projects:**
- Emphasize endpoint specifications
- Include authentication/authorization details
- Focus on request/response formats

**Frontend Projects:**
- Include UI/UX requirements
- Specify component architecture
- Define state management patterns

**Data Processing Projects:**
- Emphasize input/output formats
- Include performance requirements
- Define error handling strategies

### For Different Team Sizes
**Solo Development:**
- Simplified quality criteria
- Focus on functionality over process
- Flexible documentation requirements

**Team Development:**
- Stricter code style requirements
- Mandatory documentation updates
- Comprehensive testing requirements

## Troubleshooting Common Issues

### Claude Doesn't Follow Existing Patterns
- **Solution:** Add more specific examples of existing code
- **Prevention:** Include file paths for Claude to examine first

### Implementation Too Complex
- **Solution:** Break into smaller iterations
- **Prevention:** Start with simpler acceptance criteria

### Tests Don't Cover Edge Cases
- **Solution:** Be more specific about test scenarios
- **Prevention:** Include concrete test case examples

### Integration Issues
- **Solution:** Provide more context about existing architecture
- **Prevention:** Map out integration points clearly

## Example Draft Structure

```markdown
# Feature Draft: User Authentication

## Current State
Right now our app has no user system. Anyone can access all features without any identification. This makes it impossible to save user preferences or provide personalized experiences.

## Desired State
Users should be able to create accounts and sign in. Once logged in, they can access personalized features like saved preferences and user-specific data.

## User Journey
1. New user visits the app
2. Sees a sign-up form or login prompt
3. Creates account with email/password
4. Gets logged in automatically
5. Can access personalized features
6. Can log out and log back in later

## Technical Context
We're using [your framework] and have a database set up. Currently no user table exists. The app uses [your state management] for managing application state.

## Questions/Concerns
- Should we support social login (Google, GitHub)?
- What password requirements should we have?
- How long should sessions last?
```

## Quick Checklist

Before moving to prompt creation:
- [ ] Draft describes current vs desired state clearly
- [ ] User journey is explained
- [ ] Technical context is provided
- [ ] Claude has asked clarifying questions
- [ ] You've answered all unclear points
- [ ] Requirements feel comprehensive