# Scoring Algorithms

SuperGitSight uses two proprietary scoring algorithms to evaluate GitHub profiles and repositories: **KCRISMAG** for profiles and **ACID** for repositories.

## KCRISMAG Profile Scoring

The **KCRISMAG** algorithm evaluates GitHub profiles across eight key dimensions:

### K - Consistency
**Subtitle:** Reliability  
**Category:** SOFT  
**Description:** Sustained, continuous effort over time — showing up regularly and maintaining momentum.

### C - Contribution
**Subtitle:** Passion  
**Category:** SOFT  
**Description:** Meaningful participation in shared work, open-source involvement, and collaborative development.

### R - Reliability
**Subtitle:** Efficiency  
**Category:** HARD  
**Description:** Demonstrates strong logical thinking, producing reliable and maintainable code.

### I - Impact
**Subtitle:** Impact / Influence  
**Category:** SOFT  
**Description:** Influence and reach of work — adoption, recognition, and effect on the community or teams.

### S - Security
**Subtitle:** Robustness  
**Category:** HARD  
**Description:** Ability to produce secure and robust code without vulnerabilities or bugs.

### M - Maintainability
**Subtitle:** Cost  
**Category:** HARD  
**Description:** Ability to write clean, easy readable and maintainable code.

### A - Ambition
**Subtitle:** Builder Mindset  
**Category:** BUILDER  
**Description:** Ambition and creativity as a builder — originality, cross-domain depth, thoughtful systems, and the drive to create new things.

### G - Growth
**Subtitle:** Learning  
**Category:** SOFT  
**Description:** Learning velocity, adaptability, and expansion into new tools, languages, ideas, and problem spaces.

### Score Calculation

The KCRISMAG score is calculated as a weighted combination of these dimensions, resulting in a score from 0-100. The algorithm considers:

- Recency weighting (recent activity matters more)
- Quality over quantity
- Diversity of contributions
- Community engagement
- Long-term sustainability

## ACID Repository Scoring

The **ACID** framework evaluates repository health across four critical areas:

### A - Architecture & Structure
**Description:** Project organization, code structure, and technical foundation.

### C - Cross-Domain
**Description:** Technology diversity and cross-domain expertise demonstrated in the repository.

### I - Innovation
**Description:** Uniqueness, originality, and innovation signals in the repository.

### D - Documentation & Readability
**Description:** Documentation quality and community readiness.

### Score Calculation

The ACID score combines these four dimensions with equal weighting, producing a score from 0-100.

**Portfolio-Level ACID:**
For a developer's portfolio, the overall ACID score is the average of all analyzed repositories' ACID scores.

## Score Interpretation

### Profile Scores (KCRISMAG)
- **90-100**: Exceptional profile with outstanding contributions
- **75-89**: Strong profile with consistent, quality contributions
- **60-74**: Good profile with solid activity
- **45-59**: Developing profile with growing contributions
- **0-44**: New or inactive profile

### Repository Scores (ACID)
- **90-100**: Production-ready, well-maintained repository
- **75-89**: High-quality repository with minor improvements needed
- **60-74**: Good repository with some areas for improvement
- **45-59**: Basic repository needing significant improvements
- **0-44**: Early-stage or unmaintained repository

## Factors Not Included

To ensure fairness and privacy, our algorithms **do not** consider:
- Personal information
- Private repository data (unless explicitly authorized)
- Email addresses or contact information
- Sensitive metadata
- Non-public activity
- Repository content analysis (code is not read)
- Code comments (only documentation files are analyzed)

## Algorithm Updates

Our scoring algorithms are continuously refined based on:
- Industry best practices
- Community feedback
- GitHub platform updates
- Research findings
- User experience data

**Note:** Currently, algorithms are in Beta stage and may be adjusted based on feedback and testing.

## Transparency

While the exact implementation details are proprietary, we provide:
- High-level algorithm descriptions
- Score interpretation guides
- Example outputs
- Regular updates on improvements

## Example Scores

See our [examples](../examples/) folder for sample outputs:
- [KCRISMAG Sample](../examples/kcrismag-sample.json)
- [ACID Sample](../examples/acid-sample.json)
- [Profile Output](../examples/sample-profile-output.json)

---

**Questions about scoring?** Check our [FAQ](faq.md) or open a [GitHub Discussion](https://github.com/supergitsight/supergitsight/discussions).
