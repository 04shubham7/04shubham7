# GitHub Metrics Setup Instructions

Your profile has been updated with a comprehensive and attractive metrics display! 

## What's Changed

1. **README.md**: Enhanced with attractive header, profile badges, and organized sections
2. **GitHub Actions Workflow**: Updated `.github/workflows/main.yml` to automatically generate detailed metrics daily
3. **Enhanced Metrics**: Added multiple plugins for achievements, code activity, discussions, gists, and projects

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
   - `read:project` (Read access to projects)

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

The enhanced configuration now includes:
- **Achievements**: Displays ALL achievements (threshold set to X, no limit)
- **Activity and Contribution**: Extended to 30 days with more items
- **Programming Languages**: Shows up to 12 languages with 30-day analysis
- **Habits and Coding Patterns**: 30-day analysis from 500 commits
- **Code Activity**: Recent code snippets (3 days)
- **Starred Repositories**: Your top starred repos
- **Discussions**: GitHub Discussions activity
- **Gists**: Your public gists
- **Projects**: Active projects with descriptions
- **And many more plugins!**

## Customization

You can customize the metrics by editing `.github/workflows/main.yml`. 

Visit https://github.com/lowlighter/metrics for full documentation on available plugins and options.
