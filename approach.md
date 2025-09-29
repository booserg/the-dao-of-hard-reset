# The Dao of Hard Reset: Vibe Coding Workflow

*A pragmatic approach to iterative development with Claude, embracing the power of "reset and retry" for better outcomes.*

## Philosophy

The "hard reset" principle acknowledges that the first attempt isn't always the best. By starting with roadmap planning, iteratively refining feature descriptions, and being willing to reset when needed, we maintain high code quality while preserving development velocity.

## Prerequisites

1. **GitHub Repository**: The developing project is hosted on GitHub
2. **Development Folder Structure**: Project has a `development/` folder in its root
3. **Roadmap File**: A roadmap file to track planned features
4. **Prompt Template**: A reusable prompt template that provides structure for final prompts
5. **Testing Setup**: Automated tests are configured and runnable

## Core Workflow: Feature Development with Claude

### Phase 1: Roadmap Planning
1. **Update the roadmap** with the new feature to implement
   - Add a very short description of the feature
   - No detailed specifications at this stage
   - Focus on the high-level goal or capability

### Phase 2: Draft Creation
2. **Create a freeform feature draft** in markdown
   - Name the file: `N-{short-feature-name}-draft.md`
   - No predefined structure - just plain explanation
   - Describe current flow vs desired flow
   - Write it as a user story or narrative
   - Include context about existing behavior and what needs to change

### Phase 3: Draft Refinement (Multi-iterational)
3. **Ask Claude to refine the draft**
   - Claude will identify unclear or missing requirements
   - Answer Claude's questions to improve clarity
   - Repeat this process multiple times until the draft is comprehensive
   - Each iteration makes the requirements clearer and more detailed
   - Continue until both you and Claude understand the full scope

### Phase 4: Final Prompt Creation (Multi-iterational)
4. **Ask Claude to create the final prompt** from the refined draft
   - Claude transforms the refined draft into a structured prompt using the prompt template
   - The prompt template provides the required structure and sections to fill
   - This may also require multiple iterations to get all sections complete
   - Refine the prompt until it contains all necessary technical details
   - The final prompt should follow the template structure and be ready for implementation

### Phase 5: Implementation
5. **Execute with Claude**: Provide the final prompt to Claude for implementation
6. **Review Claude's changes**: Examine all modified/created files
7. **Run automated tests**: Ensure existing functionality isn't broken
8. **Manual testing**: Verify the feature works as expected

### Phase 6: Quality Gate
9. **Evaluate the implementation** across three dimensions:
   - **Architecture**: Does it fit well with existing codebase?
   - **Code Style**: Does it follow project conventions?
   - **Testing**: Is it properly tested and reliable?

### Phase 7: Decision Point
- **If satisfactory**: Commit the changes and move to next feature
  ```bash
  git add .
  git commit -m "Implement [feature name] - iteration N"
  ```

- **If improvements needed**:
  1. **Hard reset** to clean state
     ```bash
     git reset --hard HEAD~1  # Reset to before Claude's changes
     ```
  2. **Go back to appropriate phase** depending on the issue:
     - If requirements were unclear: refine the draft further (Phase 3)
     - If prompt was incomplete: improve the final prompt (Phase 4)
  3. **Re-implement** with the improved specifications

## Playground Development

For exploring new APIs, libraries, or uncertain implementations:

### Setup
1. **Create playground projects** when working with unfamiliar APIs/libraries
2. **Location**: `playground/` folder in project root
3. **Treatment**: Follow the main development workflow (prompts, iterations, etc.)

### Structure
Every playground should include:
- **Implementation class**: The actual code being tested/explored. The class should be new and have no relations to the existing project functionality or codebase. Keep it library-specific and as far as possible from the current project scope.
- **Unit test project**: Comprehensive tests to validate behavior
- **Documentation**: Notes on findings, gotchas, and recommendations

### Integration Philosophy
- Playground discoveries should have nothing in common with the current project
- All discoveries should be reimplemented in the application from scratch
- Use playground as reference and learning material only
- Maintain complete separation between exploration and production code

---

**The dao of hard reset: Reset with purpose, iterate with intention, ship with confidence.**
