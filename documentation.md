# Documentation

Prompts for documentation generation and improvement.

## Prompts

### API Documentation

```
Generate comprehensive API documentation for the provided code or specification.

OUTPUT REQUIREMENTS:
-   **Overview:** A brief description of the API's purpose and functionality.
-   **Endpoints/Methods:** A table with columns for Endpoint/Method, Description, Parameters, and Response.
-   **Authentication:** Details on authentication requirements if applicable.
-   **Examples:** Code examples demonstrating common use cases.
-   **Error Handling:** A list of possible errors and their meanings.

Please ensure the documentation is clear, complete, and developer-friendly.
```

### Documentation Audit & Reorganization

```
Act as a Senior Technical Writer and Software Engineer. I need you to audit, reorganize, and update the repository documentation to match the current state of the codebase.

**Context:**
The documentation may be outdated regarding recent code changes. Do not suggest generic "standard" sections (like Code of Conduct) unless they are relevant to the specific code logic found. Focus strictly on technical accuracy and usability.

**Please execute the following steps:**

1.  **Phase 1: Deep Scan & Discovery**
    * Read the file structure of the source code (e.g., `src`, `lib`, `app`) to understand the architecture.
    * Read all existing Markdown files (`.md`) to understand the current documentation state.
    * Identify the "Truth Source": Treat the code logic, function signatures, and comments as the absolute truth.

2.  **Phase 2: Drift Detection (Code vs. Docs)**
    * Compare the codebase against the documentation.
    * Identify specific technical aspects that are missing or outdated in the docs (e.g., new API endpoints, changed function parameters, deprecated methods, or environment variables that were added).
    * Draft technical explanations for these missing pieces based on the code implementation.

3.  **Phase 3: Structural Organization**
    * Propose a reorganized directory structure for the documentation that groups files logically based on what you found in the code (e.g., separating "Architecture" from "Usage" or "API Reference").
    * Do not create empty placeholders. Only organize existing content and the new technical content identified in Phase 2.

4.  **Phase 4: Content Update & Cleanup**
    * Rewrite the Markdown files to incorporate the missing technical details found in Phase 2.
    * Fix formatting: Ensure consistent H1/H2/H3 hierarchies.
    * Verify code blocks: Ensure all code snippets in the docs match the actual syntax used in the project. Use correct language tags (e.g., ```python, ```typescript) for highlighting.
```
