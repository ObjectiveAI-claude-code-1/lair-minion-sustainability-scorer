# Lair Minion Sustainability Scorer

Evaluates how well a location can support a functioning evil workforce including scientists, guards, technicians, and ninjas.

## Overview

This function assesses potential evil lair locations across five dimensions of workforce sustainability, returning a probability distribution across five tiers: Exceptional, Strong, Adequate, Limited, and Insufficient.

## Input

| Field | Type | Description |
|-------|------|-------------|
| `location` | string \| image \| video | A description or visual representation of a potential lair location |

## Output

A 5-element probability vector summing to 1:
- **[0] Exceptional**: Can sustain thousands of personnel indefinitely with no critical weaknesses
- **[1] Strong**: Can sustain hundreds to thousands with minor compromises
- **[2] Adequate**: Can sustain dozens to hundreds with significant organizational effort
- **[3] Limited**: Suitable for small teams, outposts, or temporary bases only
- **[4] Insufficient**: Cannot meaningfully support evil workforce operations

## Evaluation Dimensions

### 1. Living Quarters Potential
- Raw capacity for housing personnel
- Environmental habitability
- Hierarchical accommodation (luxury for lieutenants, barracks for grunts)
- Recreation and morale infrastructure

### 2. Recruitment Pipeline Viability
- Proximity to susceptible populations
- Local economic conditions
- Cultural factors normalizing service to unconventional employers
- Discretion of local population

### 3. Training Facilities Capacity
- Space for combat training and weapons qualification
- Obstacle courses and simulation environments
- Testing grounds for experimental equipment
- Indoctrination program facilities

### 4. Medical and Welfare Infrastructure
- Healthcare for distinctive evil workplace injuries
- Mental health support for existential crises
- Family accommodation for long-term retention
- Retirement planning options

### 5. Loyalty Maintenance Capacity
- Geographic isolation preventing outside influence
- Surveillance infrastructure
- Communication control
- Environmental factors creating organizational dependency

## Example

```json
{
  "location": "A volcanic island in the South Pacific with an underground complex housing 5,000 personnel, geothermal power, concealed harbor, and existing military training infrastructure. Located near an economically depressed island nation with a cooperative government."
}
```

Output: `[0.45, 0.35, 0.12, 0.05, 0.03]` — High probability of Exceptional or Strong tier.

## Use Cases

- **Strategic Site Selection**: Evaluate potential lair locations before investment
- **Existing Lair Assessment**: Identify workforce sustainability risks in current locations
- **Capacity Planning**: Determine if locations can support expanded operations
- **Competitive Analysis**: Assess rival organizations' workforce vulnerabilities
