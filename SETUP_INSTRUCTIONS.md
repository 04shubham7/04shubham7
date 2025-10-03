# GitHub Metrics Setup Instructions

Your profile has been updated to match PerHac13's clean and professional style! 

## What's Changed

1. **README.md**: Simplified to display a single comprehensive metrics SVG image
2. **GitHub Actions Workflow**: Added `.github/workflows/main.yml` to automatically generate metrics

## Required Setup

To make the metrics work, you need to create a GitHub Personal Access Token:

### Steps to Create METRICS_TOKEN:

1. Go to GitHub Settings → Developer settings → Personal access tokens → Tokens (classic)
   - Or directly visit: https://github.com/settings/tokens

2. Click "Generate new token" → "Generate new token (classic)"

3. Give it a name like "GitHub Metrics"

4. Select the following scopes:
   - `repo` (Full control of private repositories)
   - `read:user` (Read user profile data)
   - `read:org` (Read org and team membership)

5. Click "Generate token" at the bottom

6. **Copy the token** (you won't be able to see it again!)

7. Go to your repository settings:
   - Navigate to: https://github.com/04shubham7/04shubham7/settings/secrets/actions
   
8. Click "New repository secret"

9. Name: `METRICS_TOKEN`
   Value: Paste your personal access token

10. Click "Add secret"

## Triggering the Workflow

The metrics will be generated automatically:
- Weekly (every Sunday at midnight)
- On every push to main/master branch
- Manually via Actions tab → Metrics workflow → Run workflow

After the first run, the `github-metrics.svg` file will be created and displayed in your README!

## Customization

You can customize the metrics by editing `.github/workflows/main.yml`. The current configuration includes:
- Activity and contribution history
- Programming languages
- Achievements
- Repositories information
- Habits and coding patterns
- And many more plugins!

Visit https://github.com/lowlighter/metrics for full documentation on available plugins and options.
