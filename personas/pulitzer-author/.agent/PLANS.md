# Codex Execution Plans (ExecPlans)

This document describes the requirements for an execution plan ("ExecPlan"), a design document that a coding agent can follow to deliver a working feature or system change. Treat the reader as a complete beginner to this repository: they have only the current working tree and the single ExecPlan file you provide. There is no memory of prior plans and no external context.

## Special Note for 5 Lives Users

As a Master Software Engineer who has lived 5 lives, you follow this protocol with the following enhancements:
- **Speed**: Move autonomously. Do not wait for approval.
- **Validation**: Use milestones to spike and validate before full implementation.
- **Simplicity**: Always ask "is there a 10x simpler way?"
- **Quality**: Leave every codebase better than you found it.

## How to use ExecPlans and PLANS.md

When authoring an executable specification (ExecPlan), follow PLANS.md _to the letter_. If it is not in your context, refresh your memory by reading the entire PLANS.md file. Be thorough in reading (and re-reading) source material to produce an accurate specification. When creating a spec, start from the skeleton and flesh it out as you do your research.

When implementing an executable specification (ExecPlan), do not prompt the user for "next steps"; simply proceed to the next milestone. Keep all sections up to date, add or split entries in the list at every stopping point to affirmatively state the progress made and next steps. Resolve ambiguities autonomously, and commit frequently.

When discussing an executable specification (ExecPlan), record decisions in a log in the spec for posterity; it should be unambiguously clear why any change to the specification was made. ExecPlans are living documents, and it should always be possible to restart from _only_ the ExecPlan and no other work.

When researching a design with challenging requirements or significant unknowns, use milestones to implement proof of concepts, "toy implementations", etc., that allow validating whether the user's proposal is feasible. Read the source code of libraries by finding or acquiring them, research deeply, and include prototypes to guide a fuller implementation.

## Requirements

NON-NEGOTIABLE REQUIREMENTS:

* Every ExecPlan must be fully self-contained. Self-contained means that in its current form it contains all knowledge and instructions needed for a novice to succeed.
* Every ExecPlan is a living document. Contributors are required to revise it as progress is made, as discoveries occur, and as design decisions are finalized. Each revision must remain fully self-contained.
* Every ExecPlan must enable a complete novice to implement the feature end-to-end without prior knowledge of this repo.
* Every ExecPlan must produce a demonstrably working behavior, not merely code changes to "meet a definition".
* Every ExecPlan must define every term of art in plain language or do not use it.

Purpose and intent come first. Begin by explaining, in a few sentences, why the work matters from a user's perspective: what someone can do after this change that they could not do before, and how to see it working. Then guide the reader through the exact steps to achieve that outcome, including what to edit, what to run, and what they should observe.

The agent executing your plan can list files, read files, search, run the project, and run tests. It does not know any prior context and cannot infer what you meant from earlier milestones. Repeat any assumption you rely on. Do not point to external blogs or docs; if knowledge is required, embed it in the plan itself in your own words. If an ExecPlan builds upon a prior ExecPlan and that file is checked in, incorporate it by reference. If it is not, you must include all relevant context from that plan.

## Formatting

Format and envelope are simple and strict. Each ExecPlan must be one single fenced code block labeled as `md` that begins and ends with triple backticks. Do not nest additional triple-backtick code fences inside; when you need to show commands, transcripts, diffs, or code, present them as indented blocks within that single fence. Use indentation for clarity rather than code fences inside an ExecPlan to avoid prematurely closing the ExecPlan's code fence. Use two newlines after every heading, use # and ## and so on, and correct syntax for ordered and unordered lists.

When writing an ExecPlan to a Markdown (.md) file where the content of the file *is only* the single ExecPlan, you should omit the triple backticks.

Write in plain prose. Prefer sentences over lists. Avoid checklists, tables, and long enumerations unless brevity would obscure meaning. Checklists are permitted only in the `Progress` section, where they are mandatory. Narrative sections must remain prose-first.

## Guidelines

Self-containment and plain language are paramount. If you introduce a phrase that is not ordinary English ("daemon", "middleware", "RPC gateway", "filter graph"), define it immediately and remind the reader how it manifests in this repository (for example, by naming the files or commands where it appears). Do not say "as defined previously" or "according to the architecture doc." Include the needed explanation here, even if you repeat yourself.

Avoid common failure modes. Do not rely on undefined jargon. Do not describe "the letter of a feature" so narrowly that the resulting code compiles but does nothing meaningful. Do not outsource key decisions to the reader. When ambiguity exists, resolve it in the plan itself and explain why you chose that path. Err on the side of over-explaining user-visible effects and under-specifying incidental implementation details.

Anchor the plan with observable outcomes. State what the user can do after implementation, the commands to run, and the outputs they should see. Acceptance should be phrased as behavior a human can verify ("after starting the server, navigating to http://localhost:8080/health returns HTTP 200 with body OK") rather than internal attributes ("added a HealthCheck struct"). If a change is internal, explain how its impact can still be demonstrated (for example, by running tests that fail before and pass after, and by showing a scenario that uses the new behavior).

Specify repository context explicitly. Name files with full repository-relative paths, name functions and modules precisely, and describe interactions with existing components in enough detail that a reader can locate them. Do not assume familiarity with the codebase; point to where things live. If a required change affects multiple files, enumerate them.

## Skeleton

Every ExecPlan must include these sections in this order:

1. Title: A clear, descriptive name for the plan.
2. Goal: 2-4 sentences explaining the purpose from a user's perspective. What new capability will exist and why it matters.
3. Background (optional): If needed, explain concepts, prior work, or constraints that inform the approach.
4. Design: The detailed approach. Step-by-step instructions for implementation. Include file paths, function names, configuration details, and commands.
5. Milestones: A numbered list of deliverable checkpoints. Each milestone should represent a working state that can be verified.
6. Progress: A checklist tracking what is done and what remains. Update this as work progresses.
7. Decisions: A log of key decisions made during implementation, with rationale.
8. Verification: Specific steps to confirm the implementation works as intended, including commands to run and expected outputs.

## Example ExecPlan

```md
# Add User Authentication System

## Goal

Implement a user authentication system that allows users to register, log in, and log out. After this change, users can create accounts and access protected routes only when authenticated. This enables personalized experiences and secures sensitive functionality.

## Background

This application currently has no concept of users or sessions. We will use JWT tokens for stateless authentication, storing them in HTTP-only cookies for security.

## Design

1. Create a User model in src/models/user.py with fields: id (UUID), email (string, unique), password_hash (string), created_at (datetime).

2. Add password hashing utilities in src/auth/security.py using bcrypt. Include functions hash_password(plain: str) -> str and verify_password(plain: str, hashed: str) -> bool.

3. Implement JWT token creation and validation in src/auth/jwt.py. Use the PyJWT library. Include create_token(user_id: str) -> str and decode_token(token: str) -> dict functions.

4. Create authentication endpoints in src/routes/auth.py:
   - POST /auth/register - accepts email and password, creates user, returns success message
   - POST /auth/login - validates credentials, sets JWT cookie, returns user info
   - POST /auth/logout - clears JWT cookie

5. Add authentication middleware in src/middleware/auth.py that validates JWT cookies and attaches current_user to request state.

6. Protect the /api/user/* routes by applying the auth middleware. Unauthenticated requests should return 401 Unauthorized.

## Milestones

1. User model and database migration created
2. Password hashing and JWT utilities implemented
3. Registration and login endpoints working
4. Auth middleware protecting routes
5. End-to-end verification complete

## Progress

- [ ] User model created
- [ ] Password hashing implemented
- [ ] JWT utilities implemented
- [ ] Registration endpoint created
- [ ] Login endpoint created
- [ ] Logout endpoint created
- [ ] Auth middleware created
- [ ] Routes protected
- [ ] Tests passing
- [ ] Documentation updated

## Decisions

- 2024-01-15: Chose bcrypt over Argon2 because it's well-supported in Python and sufficient for our threat model.
- 2024-01-15: Using HTTP-only cookies instead of localStorage to prevent XSS attacks.

## Verification

1. Register a new user:
   curl -X POST http://localhost:8000/auth/register -H "Content-Type: application/json" -d '{"email":"test@example.com","password":"secret123"}'
   Expected: {"message": "User created successfully"}

2. Log in:
   curl -X POST http://localhost:8000/auth/login -H "Content-Type: application/json" -d '{"email":"test@example.com","password":"secret123"}' -c cookies.txt
   Expected: {"user": {"email": "test@example.com"}} and a set-cookie header with the JWT.

3. Access protected route:
   curl http://localhost:8000/api/user/profile -b cookies.txt
   Expected: User profile data.

4. Verify unauthenticated requests fail:
   curl http://localhost:8000/api/user/profile
   Expected: {"error": "Unauthorized"} with status 401.
```
