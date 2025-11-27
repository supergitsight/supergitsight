# Frequently Asked Questions

## General Questions

### What is SuperGitSight?
SuperGitSight is a data-driven platform that analyzes GitHub profiles and repositories to provide objective insights about developer contributions, code quality, and repository health using proprietary KCRISMAG and ACID scoring algorithms.

### How does SuperGitSight work?
Simply enter a GitHub username on our website, and our system will:
1. Fetch public data from the GitHub API
2. Process it through our scoring algorithms
3. Generate comprehensive insights and scores
4. Display results in an easy-to-understand dashboard

### Is SuperGitSight free?
Yes! SuperGitSight is currently free to use. We analyze public GitHub data at no cost.

### Do I need a GitHub account?
No, you don't need a GitHub account to analyze profiles. However, if you want to analyze private repositories in the future, you'll need to authenticate with GitHub.

## Scoring Questions

### What is KCRISMAG?
KCRISMAG is our proprietary 8-dimension scoring system for GitHub profiles:
- **K** - Consistency (Reliability)
- **C** - Contribution (Passion)
- **R** - Reliability (Efficiency)
- **I** - Impact (Influence)
- **S** - Security (Robustness)
- **M** - Maintainability (Cost)
- **A** - Ambition (Builder Mindset)
- **G** - Growth (Learning)

### What is ACID?
ACID is our repository scoring framework evaluating:
- **A** - Architecture & Structure
- **C** - Cross-Domain
- **I** - Innovation
- **D** - Documentation & Readability

### How are scores calculated?
Scores are calculated using proprietary algorithms that analyze multiple factors including:
- Contribution patterns and consistency
- Repository quality and structure
- Technology stack diversity
- Community engagement
- Code quality indicators

Exact calculation formulas are proprietary, but we provide high-level explanations in our [scoring documentation](scoring.md).

### What does my score mean?
- **90-100**: Exceptional profile with outstanding contributions
- **75-89**: Strong profile with consistent, quality contributions
- **60-74**: Good profile with solid activity
- **45-59**: Developing profile with growing contributions
- **0-44**: New or inactive profile

### Can I improve my score?
Yes! Focus on:
- Consistent contributions over time
- Quality code and documentation
- Active open-source participation
- Diverse technology usage
- Maintaining your projects

## Privacy & Security

### What data does SuperGitSight access?
We only access public GitHub data through the GitHub API. We do not:
- Access private repositories (unless you explicitly authorize)
- Store your personal information
- Read your code content
- Access sensitive data

### Is my data stored?
No, we don't permanently store your GitHub data. Analysis results are cached temporarily for performance, but your raw data is not stored.

### Is SuperGitSight secure?
Yes! We use:
- HTTPS encryption for all data transmission
- Secure API integrations
- No permanent data storage
- Privacy-first approach

### Can I delete my data?
Since we don't permanently store your data, there's nothing to delete. Cached results expire automatically.

## Technical Questions

### Which GitHub data is analyzed?
We analyze:
- Public repositories
- Contribution history
- Repository metadata (stars, forks, languages)
- Repository structure and files
- Issue and PR activity (public only)

### How accurate are the scores?
Our algorithms are continuously refined based on industry best practices and community feedback. Scores provide objective metrics based on available public data.

### Why is my score different from what I expected?
Scores are based on objective metrics. Factors that might affect your score:
- Recent activity vs. historical activity
- Quality of contributions vs. quantity
- Repository maintenance status
- Documentation and code quality
- Community engagement

### Can I analyze private repositories?
Currently, we only analyze public repositories. Private repository analysis is planned for the future and will require GitHub authentication.

## Comparison Feature

### How does profile comparison work?
Enter two GitHub usernames to compare:
- Side-by-side score breakdowns
- Strengths and concerns for each profile
- Ranking based on composite scores
- Hiring recommendations

### What factors are considered in comparison?
Comparisons consider:
- Overall KCRISMAG scores
- Individual dimension scores
- Contribution patterns
- Repository quality
- Community engagement

## Usage Questions

### How often can I analyze a profile?
You can analyze profiles as often as you like. Results are cached for performance, but you can refresh to get the latest data.

### Can I export my results?
Yes! You can:
- Export PDF reports for profiles and comparisons
- Share links to results
- Screenshot visualizations

### Is there an API?
A public API is planned for the future. Currently, the platform is web-based only.

### Can I use SuperGitSight for hiring?
Yes! SuperGitSight is designed to help with:
- Candidate evaluation
- Objective profile assessment
- Side-by-side candidate comparison
- Skill verification

However, scores should be used as one data point among many in the hiring process.

## Troubleshooting

### The analysis is taking too long
Analysis typically completes within seconds. If it's taking longer:
- Check your internet connection
- The profile might have many repositories
- GitHub API rate limits might be affecting the request

### I'm getting an error
Common issues:
- **User not found**: Check the GitHub username spelling
- **Rate limit**: Wait a few minutes and try again
- **Network error**: Check your internet connection

If issues persist, contact support at supergitsight@gmail.com.

### My profile isn't showing up
Make sure:
- The GitHub username is correct
- The profile is public
- The profile has some activity

### The scores seem incorrect
Scores are calculated based on available public data. If you believe there's an error:
- Check that all your repositories are public
- Verify your contribution history is visible
- Contact support with specific concerns

## Future Features

### What's coming next?
See our [Roadmap](../roadmap/roadmap.md) for planned features including:
- GitHub token integration for private repos
- AI-driven recommendations
- Enhanced visualizations
- Public API

### How can I request a feature?
Open a [Feature Request](https://github.com/supergitsight/supergitsight/issues/new?template=feature_request.md) on GitHub!

## Support

### How can I get help?
- **Documentation**: Check our [docs](../docs/)
- **GitHub Issues**: Open an issue for bugs or questions
- **Discord**: Join our [Discord community](https://discord.gg/RdMYBFzQQn)
- **Email**: Contact support at supergitsight@gmail.com

### How can I contribute?
We welcome contributions! See our [Contributing Guide](../CONTRIBUTING.md) for details.

---

**Still have questions?** Open a [GitHub Discussion](https://github.com/supergitsight/supergitsight/discussions) or contact us at supergitsight@gmail.com.

