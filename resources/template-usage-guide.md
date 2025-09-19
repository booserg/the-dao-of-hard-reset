# Prompt Template Usage Guide

## Quick Start

1. **Copy** `prompt-template.md`
2. **Rename** to `N-{feature-name}.md` (e.g., `1-user-login.md`)
3. **Fill in** all bracketed placeholders `[like this]`
4. **Remove** sections not applicable to your feature
5. **Commit** the prompt before asking Claude to implement

## Template Sections Explained

### Essential Sections (Never Skip)
- **Project Context** - Helps Claude understand your codebase
- **Feature Overview** - Clear problem/solution statement
- **Functional Requirements** - What the feature must do
- **Technical Requirements** - How it integrates with existing code
- **Quality Criteria** - Definition of done

### Optional Sections (Use When Relevant)
- **User Stories** - For user-facing features
- **Data Requirements** - For features requiring database changes
- **Performance Requirements** - For performance-critical features
- **Security Requirements** - For features handling sensitive data

## Tips for Better Prompts

### Be Specific
❌ "Add authentication"
✅ "Add JWT-based authentication with email/password login, including password reset functionality"

### Provide Context
- Always mention existing patterns Claude should follow
- Point to similar existing implementations
- Explain why certain constraints exist

### Set Clear Boundaries
- Specify what should NOT be changed
- List files that are off-limits
- Define scope limits clearly

### Include Examples
- Show expected input/output formats
- Provide example API calls or user interactions
- Include sample test cases

## Common Iteration Patterns

### Iteration 1: Core Functionality
- Focus on happy path implementation
- Basic functionality working
- Simple test coverage

### Iteration 2: Edge Cases & Validation
- Handle error scenarios
- Add input validation
- Improve error messages

### Iteration 3: Polish & Optimization
- Performance improvements
- Code cleanup and refactoring
- Comprehensive testing

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

## Example Quick Checklist

Before submitting prompt to Claude:
- [ ] Project context filled in
- [ ] Clear problem statement
- [ ] Specific functional requirements
- [ ] Integration points identified
- [ ] Quality criteria defined
- [ ] Existing files to examine listed
- [ ] Iteration learnings included (if applicable)
- [ ] Success criteria measurable