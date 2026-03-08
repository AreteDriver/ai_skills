# Scoring Output Contract

Standard output shape for all composite scorers across BenchGoblins, Animus, marketing-engine, and any future project.

## Contract Shape

```json
{
  "score": 0-100,
  "grade": "A|B|C|D|F",
  "ready": true|false|"conditional",
  "categories": {
    "category_name": {
      "score": 0-100,
      "weight": 0.0-1.0,
      "weighted_score": 0-100,
      "issues": ["specific problem descriptions"],
      "warnings": ["non-blocking concerns"],
      "suggestions": ["optional improvements"]
    }
  },
  "priority_actions": [
    {
      "priority": "critical|high|medium",
      "action": "specific actionable fix",
      "impact": "what improves when this is done",
      "category": "which category this affects"
    }
  ],
  "summary": "1-2 sentence assessment"
}
```

## Rules

1. `score` = sum of all `weighted_score` values
2. All `weight` values must sum to 1.0
3. `weighted_score` = `score` * `weight` for each category
4. `ready` = false if ANY critical issue exists
5. `ready` = "conditional" if high-priority issues exist but no criticals
6. `priority_actions` sorted: all criticals first, then highs, then mediums
7. Maximum 10 priority actions (focus on highest impact)
8. Maximum 8 categories per scorer

## Grade Bands

| Grade | Range | Meaning |
|-------|-------|---------|
| A | 90-100 | Excellent — ship with confidence |
| B | 80-89 | Good — minor improvements optional |
| C | 70-79 | Acceptable — address high-priority items |
| D | 60-69 | Below standard — significant work needed |
| F | 0-59 | Failing — critical issues must be resolved |

## Domain Applications

### BenchGoblins — Player Quality Rater
| Category | Weight |
|----------|--------|
| Space Creation | 0.20 |
| Role Motion | 0.20 |
| Gravity Impact | 0.20 |
| Opportunity Delta | 0.20 |
| Matchup Fit | 0.20 |

### Animus — IntentNode Stability Scorer
| Category | Weight |
|----------|--------|
| Specificity | 0.25 |
| Evidence Quality | 0.25 |
| Constraint Clarity | 0.20 |
| Dependency Health | 0.15 |
| Staleness | 0.15 |

### Marketing Engine — Script Quality Scorer
| Category | Weight |
|----------|--------|
| Voice Match | 0.25 |
| Hook Strength | 0.20 |
| Specificity | 0.20 |
| Pacing | 0.20 |
| CTA Clarity | 0.15 |

### Code Quality
| Category | Weight |
|----------|--------|
| Correctness | 0.25 |
| Security | 0.20 |
| Maintainability | 0.20 |
| Performance | 0.15 |
| Testing | 0.10 |
| Documentation | 0.10 |

## Source

Derived from TheCraigHewitt/seomachine scoring modules (MIT License). Adapted for multi-domain use across AreteDriver projects.
