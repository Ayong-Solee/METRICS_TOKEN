name: Metrics
on:
  schedule: [{cron: "0 0 * * *"}] # Runs daily
  workflow_dispatch:              # Allows you to run it manually
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - name: Metrics embed
        uses: lowlighter/metrics@latest
        with:
          token: ${{ secrets.METRICS_TOKEN }}
