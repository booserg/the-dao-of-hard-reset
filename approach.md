# The Dao of Hard Reset: Vibe Coding Workflow

*A pragmatic approach to iterative development with Claude, embracing the power of "reset and retry" for better outcomes.*

## Philosophy

The "hard reset" principle acknowledges that the first attempt isn't always the best. By committing early, testing thoroughly, and being willing to reset when needed, we maintain high code quality while preserving development velocity.

## Prerequisites

1. **GitHub Repository**: The developing project is hosted on GitHub
2. **Development Folder Structure**: Project has a `development/` folder in its root
3. **Prompt Template**: A reusable prompt template exists in the development folder
4. **Testing Setup**: Automated tests are configured and runnable

## Core Workflow: Iterative Development with Claude

### Phase 1: Planning & Prompt Creation
1. **Copy the prompt template** from the development folder
2. **Name the prompt** using the pattern: `N-{short-feature-name}.md`
   - `N` = iteration number (1, 2, 3...)
   - Example: `1-user-authentication.md`, `2-password-reset.md`
3. **Edit the prompt** to clearly describe the requirements
4. **Commit the prompt** to version control
   ```bash
   git add development/N-feature-name.md
   git commit -m "Add prompt for [feature name] - iteration N"
   ```

### Phase 2: Implementation
5. **Execute with Claude**: Provide the prompt to Claude for implementation
6. **Review Claude's changes**: Examine all modified/created files
7. **Run automated tests**: Ensure existing functionality isn't broken
8. **Manual testing**: Verify the feature works as expected

### Phase 3: Quality Gate
9. **Evaluate the implementation** across three dimensions:
   - **Architecture**: Does it fit well with existing codebase?
   - **Code Style**: Does it follow project conventions?
   - **Testing**: Is it properly tested and reliable?

### Phase 4: Decision Point
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
  2. **Update the prompt** with:
     - Lessons learned from previous attempt
     - More specific requirements
     - Clarified edge cases
     - Better examples
  3. **Return to step 4** (commit updated prompt)

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
