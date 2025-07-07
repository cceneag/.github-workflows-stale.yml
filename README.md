# .github-workflows-stale.yml
name: Close Stale Issues
on:
  schedule:
    - cron: '0 12 * * *' # 每天晚上 8:00 (台灣時間)
jobs:
  stale:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/stale@v9.1.0
        with:
          stale-issue-message: 'Old issue!'
          days-before-stale: 30
          days-before-close: 7
