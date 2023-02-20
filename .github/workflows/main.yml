# Visit https://github.com/lowlighter/metrics#-documentation for full reference
name: Metrics
on:
  # Schedule updates (each hour)
  schedule: [{cron: "0 * * * *"}]
  # Lines below let you run workflow manually and on each commit
  workflow_dispatch:
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # Your GitHub token
          # The following scopes are required:
          #  - public_access (default scope)
          #  - repo
          #  - public_repo
          #  - read:project
          # The following additional scopes may be required:
          #  - read:org      (for organization related metrics)
          #  - read:user     (for user related data)
          #  - read:packages (for some packages related data)
          #  - repo          (optional, if you want to include private repositories)
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: blackhatethicalhacking
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Nicosia
          plugin_achievements: yes
          plugin_achievements_display: compact
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: C
          plugin_activity: yes
          plugin_activity_days: 14
          plugin_activity_filter: all
          plugin_activity_limit: 5
          plugin_activity_load: 300
          plugin_activity_visibility: all
          plugin_discussions: yes
          plugin_discussions_categories: yes
          plugin_habits: yes
          plugin_habits_charts: yes
          plugin_habits_charts_type: classic
          plugin_habits_days: 14
          plugin_habits_facts: yes
          plugin_habits_from: 200
          plugin_habits_languages_limit: 8
          plugin_habits_languages_threshold: 0%
          plugin_habits_trim: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: half-year
          plugin_lines: yes
          plugin_lines_history_limit: 2
          plugin_lines_repositories_limit: 4
          plugin_lines_sections: base
          plugin_notable: yes
          plugin_notable_from: organization
          plugin_notable_self: yes
          plugin_notable_types: commit
          plugin_projects: yes
          plugin_projects_limit: 4
          plugin_repositories: yes
          plugin_repositories_order: featured, pinned, starred, random
          plugin_stargazers: yes
          plugin_stargazers_charts: yes
          plugin_stargazers_charts_type: chartist
          plugin_stars: yes
          plugin_stars_limit: 2
          plugin_traffic: yes
