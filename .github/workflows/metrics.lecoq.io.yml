name: Metrics
on:
  # Schedule daily updates
  schedule: [{cron: "0 0 * * *"}]
  # (optional) Run workflow manually
  workflow_dispatch:
  # (optional) Run workflow when pushing on master/main
  push: {branches: ["master", "main"]}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - uses: Shea690901/metrics.lecoq.io@master
        with:
          token: ${{ secrets.METRICS_TOKEN }}

          # Options
          user: Shea690901
          template: classic
          base: header, activity, community, repositories, metadata
          base_indepth: yes
          config_octicon: yes
          config_timezone: Europe/Berlin
          plugin_achievements: yes
          plugin_achievements_display: detailed
          plugin_achievements_secrets: yes
          plugin_achievements_threshold: X
          plugin_followup: yes
          plugin_followup_archived: yes
          plugin_followup_sections: repositories
          plugin_gists: yes
          plugin_isocalendar: yes
          plugin_isocalendar_duration: full-year
          plugin_languages: yes
          plugin_languages_analysis_timeout: 15
          plugin_languages_analysis_timeout_repositories: 7.5
          plugin_languages_categories: markup, programming
          plugin_languages_colors: github
          plugin_languages_details: percentage
          plugin_languages_limit: 8
          plugin_languages_other: yes
          plugin_languages_recent_categories: markup, programming
          plugin_languages_recent_days: 14
          plugin_languages_recent_load: 300
          plugin_languages_sections: most-used, recently-used
          plugin_languages_threshold: 0%
          plugin_notable: yes
          plugin_notable_from: organization
          plugin_notable_repositories: yes
          plugin_notable_types: commit
          plugin_repositories: yes
          plugin_repositories_order: featured, pinned, starred, random
          plugin_repositories_pinned: 10
          plugin_repositories_random: 10
          plugin_repositories_starred: 10
