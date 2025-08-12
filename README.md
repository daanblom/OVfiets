# OV-Fiets Availability Script

A Bash script to search OV-fiets locations and display the number of available bikes.

It fetches live bike data from [ovfietsbeschikbaar.nl](https://ovfietsbeschikbaar.nl) and can be used in the terminal or integrated into status bars.

## Usage

```bash
./ovfiets.sh [OPTIONS] SEARCH_TERM
Options
Flag	Description
-c	Output only the bike count (no station name).
-s	Output bike count with a 🚲 icon (for status bar usage).
-h	Show the help menu and exit.
```

## Arguments
SEARCH_TERM — A case-insensitive string to search for in station names.

## Examples
```sh
# Show station name and bike count
./ovfiets.sh Utrecht

# Only bike count
./ovfiets.sh -c Amsterdam

# Bike count with 🚲 icon
./ovfiets.sh -s Rotterdam
```
## Output Examples

```sh
# Default
Utrecht Centraal 12 🚲

# Clean (-c)
12

# Status bar (-s)
12 🚲
```

## Requirements
```sh
bash
curl
grep
sed

Internet connection
```

### License
MIT — feel free to modify and share.
