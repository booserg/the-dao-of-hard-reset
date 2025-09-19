# Software Development Prompt Template

## Project Context
**Project Name:** [Project Name]
**Technology Stack:** [Languages, frameworks, databases, etc.]
**Current Version/Branch:** [Branch name or commit hash]
**Architecture Pattern:** [MVC, microservices, monolith, etc.]

## Feature Overview
**Feature Name:** [Clear, descriptive name]
**Priority:** [High/Medium/Low]
**Estimated Complexity:** [Simple/Medium/Complex]

### Problem Statement
[Describe the problem this feature solves. What pain point are users experiencing?]

### Solution Summary
[Brief description of the proposed solution]

## Functional Requirements

### Core Functionality
[List the main functions this feature must perform]
- [ ] Requirement 1
- [ ] Requirement 2
- [ ] Requirement 3

### User Stories
[If applicable, provide user stories in the format: "As a [user type], I want [goal] so that [benefit]"]

### Input/Output Specifications
**Inputs:**
- [Describe expected inputs, formats, validation rules]

**Outputs:**
- [Describe expected outputs, formats, success/error responses]

### Business Rules
[Any business logic, validation rules, or constraints]

## Technical Requirements

### Integration Points
**Existing Components to Modify:**
- [List files, classes, or modules that need changes]

**New Components to Create:**
- [List new files, classes, or modules to be created]

**External Dependencies:**
- [APIs, libraries, services this feature depends on]

### Data Requirements
**Database Changes:**
- [New tables, columns, indexes, migrations needed]

**Data Flow:**
- [How data moves through the system for this feature]

### Performance Requirements
- [Response time expectations, throughput requirements, resource constraints]

### Security Requirements
- [Authentication, authorization, data protection, input validation]

## Technical Constraints

### Code Style & Patterns
- [Specific coding standards, design patterns to follow]
- [Existing conventions to maintain]

### Technology Constraints
- [Required libraries, forbidden libraries, version constraints]

### Architecture Constraints
- [Architectural decisions that must be respected]

## Quality Criteria

### Definition of Done
- [ ] Feature works as specified
- [ ] All tests pass (existing + new)
- [ ] Code follows project conventions
- [ ] No security vulnerabilities introduced
- [ ] Performance requirements met
- [ ] Documentation updated (if applicable)

### Testing Requirements
**Unit Tests:**
- [Specific test cases to cover]

**Integration Tests:**
- [Integration scenarios to test]

**Manual Testing:**
- [Manual test scenarios to verify]

### Code Quality Standards
- [Coverage requirements, linting rules, review criteria]

## Implementation Guidance

### Suggested Approach
[High-level implementation strategy or sequence]

### Key Considerations
[Important design decisions, trade-offs, or gotchas to consider]

### Files to Examine First
[Suggest which existing files Claude should read to understand current patterns]

## Acceptance Criteria

### Must Have
- [ ] [Critical functionality that must work]

### Should Have
- [ ] [Important functionality for good user experience]

### Could Have
- [ ] [Nice-to-have features for future iterations]

## Context for Claude

### Iteration Information
**Iteration Number:** [1, 2, 3...]
**Previous Iteration Learnings:**
[If this is iteration 2+, describe what was learned from previous attempts]

### Specific Focus Areas
[What aspects need special attention in this iteration]

### Known Challenges
[Technical challenges or edge cases to be aware of]

---

## Instructions for Claude

1. **Read existing code** in the files mentioned above to understand current patterns
2. **Follow existing conventions** for naming, structure, and style
3. **Implement incrementally** - start with core functionality, add features progressively
4. **Write tests first** or alongside implementation
5. **Document as you go** - add comments for complex logic
6. **Consider edge cases** mentioned in requirements
7. **Ask clarifying questions** if requirements are ambiguous

### Success Criteria for This Implementation
[Clear, measurable criteria for when this iteration is considered successful]