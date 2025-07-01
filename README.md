Here’s your updated `README.md` — combining your original **Project Description** and the new sections on **what’s included and how to preview**:

---

```md
# Mock Trial Task

**Goal:** Improve and extend the documentation for a fictional public API using an OpenAPI-compatible toolchain.

This project includes:

- ✅ OpenAPI 3.1 spec for TaskBoard API (`openapi/openapi.yaml`)
- ✅ A guide on how to use the `/tasks/search` endpoint (`docs/guides/search-tasks.md`)

---

## Project Description

You are contributing to a developer portal for a fictional service: **TaskBoard API** – a Trello-like task management platform.

The repository includes:

- An OpenAPI 3.1 spec (`openapi.yaml`)
- A basic docs site (Markdown + site config)
- A GitHub Actions CI config
- CLI tool setup

---

### Your Tasks

#### 1. Improve API Spec

Open `openapi.yaml`  
Add the following new endpoint:

```yaml
paths:
  /tasks/search:
    get:
      summary: Search tasks
      parameters:
        - in: query
          name: query
          schema:
            type: string
          required: true
          description: Search keyword
      responses:
        '200':
          description: Successful search
          content:
            application/json:
              schema:
                type: array
                items:
                  $ref: '#/components/schemas/Task'
```

Ensure this endpoint:

- Passes lint checks
- Includes operation-level summary and description
- Returns proper response schema

---

#### 2. Write a Markdown Guide

In `/docs/guides`, create a file: `search-tasks.md`  
Write a guide titled **“How to Search for Tasks”**

Include:

- Heading
- Brief intro
- `curl` example
- Expected response (mock JSON)
- A tip box

Bonus: Use custom markdown syntax for tips, code blocks, or tables if supported by your toolchain.

---

#### 3. Update Navigation

Update `siteConfig.yaml` or equivalent configuration  
Add the guide to the nav sidebar under “Guides”

---

#### 4. Polish and Commit

- Preview your changes locally
- Commit with clear messages (e.g., `feat: add search-tasks guide and endpoint`)
- Push your branch (e.g., `trial-taskboard`)
- Add a clear PR description:

> This PR adds a new `GET /tasks/search` endpoint to the spec, and a guide explaining how to use it. Validated and previewed locally.

---

### Evaluation Focus

| Area           | What They’ll Notice                                      |
| -------------- | -------------------------------------------------------- |
| API accuracy   | Does the endpoint follow OpenAPI rules and spec style?   |
| Docs clarity   | Is the guide concise, friendly, and technically correct? |
| Tool fluency   | Did you use linting and markdown syntax properly?        |
| Commit hygiene | Are messages meaningful and your work modular?           |
| Communication  | Is your PR description clear and professional?           |

---

## Preview Instructions

You can preview the OpenAPI spec locally using Redocly CLI:

```bash
npm install -g @redocly/cli
redocly preview-docs openapi/openapi.yaml
```

To lint and validate the spec:

```bash
redocly lint openapi/openapi.yaml
```

---

Let me know if you'd like this adapted for a specific documentation system like Docusaurus, GitBook, or Swagger UI.

```

---

