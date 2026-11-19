---

# Installation

## Prerequisites

Install the following:

### Required

- Git
- GitHub Account
- Visual Studio Code
- GitHub Copilot
- GitHub Copilot Chat

### MuleSoft Development

Install:

- Anypoint Code Builder OR Anypoint Studio
- Java 17
- Apache Maven 3.9+
- Mule Runtime 4.x

Recommended VS Code Extensions:

- GitHub Copilot
- GitHub Copilot Chat
- MuleSoft Extension Pack
- XML Tools
- Extension Pack for Java
- Maven for Java
- SonarLint
- GitLens
- YAML

---

# Setup Option 1: Add to Existing Project

Copy the repository artifacts:

```text
.github/
├── copilot-instructions.md
└── prompts/
```

Into your MuleSoft project:

```text
MyMuleProject/
├── .github/
│   ├── copilot-instructions.md
│   └── prompts/
├── src/
├── pom.xml
└── mule-artifact.json
```

Commit the changes:

```bash
git add .
git commit -m "Add Copilot MuleSoft standards"
git push
```

The instructions become available to all developers cloning the repository.

---

# Setup Option 2: Create New Project from Template

Create a repository using the organization MuleSoft template.

Project structure:

```text
MyMuleProject/
├── .github/
├── src/
├── pom.xml
├── mule-artifact.json
└── README.md
```

No additional setup required.

GitHub Copilot automatically reads:

```text
.github/copilot-instructions.md
```

when operating inside the repository.

---

# Verifying Installation

Open VS Code.

Open Copilot Chat.

Test:

```text
Create a Salesforce Account API.
```

Expected behavior:

- Uses reusable subflows
- Uses logging standards
- Uses retry standards
- Uses error handling framework
- Uses secure properties
- Follows MuleSoft best practices

---

# Prompt Discovery

Open GitHub Copilot Chat.

Type:

```text
/
```

Available prompts should appear.

Examples:

```text
/mulesoft-enterprise

/munit-generator

/production-review

/debug-integration

/salesforce-sql-sync
```

---

# Example Usage

## Generate Mule Flow

```text
/mulesoft-enterprise

Create a Customer Synchronization API from Salesforce to SQL Server.
```

---

## Generate MUnit Tests

```text
/munit-generator

Generate tests for Customer Sync Flow.
```

---

## Review for Production

```text
/production-review

Review this Mule application.
```

---

## Debug Errors

```text
/debug-integration

Analyze this Mule deployment error.
```

---

## Generate Salesforce to SQL Integration

```text
/salesforce-sql-sync

Create an Account synchronization process using JWT authentication and incremental loading.
```

---

# Updating Standards

Modify:

```text
.github/copilot-instructions.md
```

to update global standards.

Examples:

- Logging format
- Retry policy
- Error handling policy
- Security requirements
- MUnit standards

Changes automatically apply to future Copilot interactions in the repository.

---

# Sharing Across Teams

Recommended Repository:

```text
copilot-mulesoft-accelerator
```

Repository Structure:

```text
copilot-mulesoft-accelerator/
├── .github/
│   ├── copilot-instructions.md
│   └── prompts/
├── README.md
└── CHANGELOG.md
```

Developers can:

```bash
git clone https://github.com/<organization>/copilot-mulesoft-accelerator.git
```

or copy the `.github` folder into existing MuleSoft projects.

This ensures all developers use the same:
- Architecture standards
- Logging standards
- Retry framework
- Error handling strategy
- Testing standards
- Production review process

---

# Troubleshooting

## Prompt Not Appearing

Verify:

```text
.github/prompts/*.prompt.md
```

*xists inside*the repository.

Restart VS Code i**necessary.

---

## Copilot*Not Applying Instructions

Verify:*
```text
.github*copilot-instructions.md
```

exist**at repository root.

Open Cop*lot Chat and ask:

```text
*hat repository instructions are ac*ive*
```

---

## Agent Cannot*Create Files

Switch from:

```tex*
*sk Mode
```

to:

*``text
Agent Mode
```

Grant*file modification*permissions when prompted.

---

#*Recommended Daily*Workflow

Step 1

```text
/mulesof*-enterprise
``*

Generate integration.

Step*2

```text
/munit-generator*```

Generate tests.

Step 3

*``text
/production-review
```

Val*date*production readiness.

Step 4

```*ext
/debug-integration
``*

Troubleshoot any*issues.

Following this workflow e*sures all*MuleSoft integrations are develope*, tested, reviewed, and deployed*using consistent enterprise standa*ds.
````*