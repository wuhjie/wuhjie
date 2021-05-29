- :school: University of Bristol | Computer Science | Year 2
- :musical_keyboard: Carpe Diem

name: Waka Readme

on:
  schedule:
    # Runs every day 1am
    - cron: '0 1 * * *'
  workflow_dispatch:
  
jobs:
  update-readme:
    name: Update status
    runs-on: ubuntu-latest
    steps:
      - uses: wuhjie/waka-readme-stats@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}