# Connection Profile PTE Conversion Tool

## Prerequisites

* Ensure you have [Node.js](https://nodejs.org/en/) installed on your machine.

## Setup

_Make sure you change your working directory to the root of this repository before you run the below commands or scripts; otherwise, they won't be able to find the scripts and other files they need)._
1. Clone this repository somewhere onto your machine and `cd` into the repo's root directory:
    1. `cd <working directory>`
    2. `git clone https://github.com/arjun-raghavan-00/fabric-pte-cprof-convert.git`
    3. `cd fabric-pte-cprof-convert`
2. Download your connection profile(s) as `.JSON` files and place them in `./config`, naming each of them `creds0.json`, `creds1.json`, etc.

## Command-Line Tool Usage

The script to run to use the tool is `./convert.sh`. 
(You can also run `node ./scripts/convert.js` for now, but a shell script wrapper has been written so that it is easier to add configuration options and other extensions in the future).
