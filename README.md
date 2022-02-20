# MEDDL IHR WERNER!!!
<img src="http://188.195.184.221/electrospoon.png" width="300">

### ROBOTS SIND TOLL
<img src="http://188.195.184.221/plume.jpg" width="200">

name: gitartwork from a contribution graph
on: 
  push:
  schedule:
    - cron: '* */24 * * *'
workflow_dispatch:
jobs:
  build:
    name: Make gitartwork SVG
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: jasineri/gitartwork@v1
        with:
           # Use this username's contribution graph  
           user_name: jasineri
           # Text on contribution graph 
           text: snaens
      - uses: jasineri/simple-push-action@v1
