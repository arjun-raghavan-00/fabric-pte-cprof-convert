# Hyperledger Fabric PTE Connection Profile Converter

This is a Node.js script for converting a [Hyperledger Fabric](https://www.hyperledger.org/projects/fabric) blockchain network's connection profile(s) to a JSON configuration file in a format compatible with Fabric's [Performance Traffic Engine (PTE)](https://github.com/hyperledger/fabric-test/tree/master/tools/PTE).

## Prerequisites

* Ensure you have [Go](https://golang.org/) and [Node.js](https://nodejs.org/en/) installed on your machine.
* Clone this repository somewhere onto your machine:
  ```
  git clone https://github.com/arjun-raghavan-00/fabric-pte-cprof-convert.git
  ```

## Usage and Details

The command to run the script is:
```
node <path to>/convert.js <input dir> <optional output dir>
```
`<path to>` is the path to the Node.js script, `<input dir>` is the path to the directory where your connection profile JSON files are located, and `<optional output dir>` is an optional parameter to specify a directory for the script to output the PTE configuration file.
If an output directory is not specified, then the script will default to saving the PTE configuration file in the same directory as the script.

The name of the output file is **`pte-config.json`**.

Note that if the input or output path begins with `/` they are treated as absolute;
if it begins with `~/` then they are treated as relative to your `$HOME` directory;
otherwise, the script treats the paths as relative to your _working directory_ (and _not_ relative to the script itself).

The script takes in a single network's connection profile(s) (it is possible that one network may have multiple connection profiles) and converts them to a single PTE configuration file for that network.
It is important to note that the script expects that _all_ of the JSON files in the supplied input directory are connection profiles associated with a single network, so ensure that there are no other JSON files in that directory (the script will safely skip any non-JSON files it finds).

## Links

- [Gerrit CR](https://gerrit.hyperledger.org/r/#/c/25165/)
- [JIRA issue](https://jira.hyperledger.org/browse/FAB-11489)
