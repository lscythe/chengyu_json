# Xianxia Idioms for Dotfiles

Minimal Chinese cultivation novel idioms for terminal text fillers. Simply pipe these JSON files to your CLI tools.

## Files
- `combat_idioms.json`: 20 fighting techniques
- `philosophy_idioms.json`: 80 wisdom phrases
- `enlightenment_idioms.json`: 20 transcendence concepts

## Basic Usage
```sh
# Print random idiom (requires jq)
jq -r '.[] | "\(.idiom) - \(.explanation)"' philosophy_idioms.json | shuf -n 1

# Format for status bars
jq -r '.[3] | "\(.idiom) (\(.pinyin))"' enlightenment_idioms.json

# Count total idioms
jq 'length' *.json
