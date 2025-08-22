# Xianxia Idioms Collection

JSON file with 100 Chinese cultivation idioms

## Basic Usage
```sh
# Print random idiom (requires jq)
jq -r '.[] | "\(.idiom) - \(.explanation)"' idioms.json | shuf -n 1

# Format for status bars
jq -r '.[3] | "\(.idiom) (\(.pinyin))"' idioms.json

# Count total idioms
jq 'length' *.json
