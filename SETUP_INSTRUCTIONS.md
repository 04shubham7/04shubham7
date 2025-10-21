# GitHub Metrics Setup Instructions

Your profile has been updated with a comprehensive and attractive display! 

## What's Changed

1. **README.md**: Completely revamped with:
   - Enhanced "About Me" section
   - Comprehensive Tech Stack with badges
   - GitHub Stats cards (statistics, streak, top languages)
   - Improved achievements and trophies section
   - Better organized sections with modern styling
   
2. **GitHub Actions Workflow**: Fixed `.github/workflows/main.yml` to:
   - Remove plugins causing "Unexpected error" messages
   - Keep only working and reliable plugins
   - Ensure daily automatic updates at midnight UTC
   
3. **Fixed Issues**: Removed problematic plugins (projects, habits, activity duplicates, achievements) that were showing errors

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
   - `read:org` (Read org and team membership, team discussions)
   - `read:discussion` (Read team discussions)

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
- **Daily** (every day at midnight UTC) - ensures your data is always up to date!
- On every push to main/master branch
- Manually via Actions tab → Metrics workflow → Run workflow

After the first run, the `github-metrics.svg` file will be created and displayed in your README!

## Features Included

The current working configuration includes:
- **Base Metrics**: Header, isocalendar, activity, community stats, repositories, metadata
- **Programming Languages**: Shows up to 12 languages with 30-day analysis and detailed breakdown
- **Calendar**: Contribution calendar (isocalendar and regular calendar)
- **Code Activity**: Recent code snippets from last 3 days
- **Starred Repositories**: Your top 4 starred repos
- **Topics**: Top 15 topics you work with
- **Traffic**: Repository traffic statistics
- **Discussions**: GitHub Discussions activity with categories
- **Gists**: Your public gists
- **Followup**: Follow-up on issues and PRs in repositories
- **Notable Contributions**: Notable commits and contributions from organizations
- **Lines of Code**: Code additions and deletions statistics

### Disabled Plugins (Were Causing Errors)
The following plugins have been disabled to remove "Unexpected error" messages:
- ~~**Achievements**~~ - Causing API errors
- ~~**Projects**~~ - Causing permissions errors
- ~~**Habits**~~ - Causing data collection errors  
- ~~**Activity plugin**~~ - Conflicting with base activity

## Customization

You can customize the metrics by editing `.github/workflows/main.yml`. 

Visit https://github.com/lowlighter/metrics for full documentation on available plugins and options.
