---
description: Create an Own Risk and Solvency Assessment (ORSA) report
globs: .arckit/templates/orsa-template.md
---
# arckit.orsa

This command generates an Own Risk and Solvency Assessment (ORSA) report structure.

## Usage

```bash
/arckit.orsa
```

## Description

The command generates an `orsa-report.md` file in the project directory. The ORSA is a key requirement of Solvency II Pillar 2, requiring insurers to assess their own solvency needs given their specific risk profile.

## Parameters

None. The command uses the template `.arckit/templates/orsa-template.md`.

## Example Output

```markdown
# Own Risk and Solvency Assessment (ORSA) Report

## Executive Summary
...

## 1. Business Strategy & Risk Profile
...
```
