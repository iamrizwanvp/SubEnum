# SubEnum – automated subdomain enumeration

A small automation wrapper that runs multiple subdomain discovery tools and aggregates results.

## Features
- Runs: subfinder, assetfinder, findomain, gauplus, unfurl, github-subdomains, waybackurls, ctfr, BufferOver, haktrails
- Aggregates and deduplicates results into `recon/<domain>/allsubs.txt`
- Uses environment variables for secrets (no hard-coded API keys)

## Requirements
Install the following tools and ensure they are in your `PATH`:
`subfinder`, `assetfinder`, `findomain`, `gauplus`, `unfurl`, `github-subdomains`, `waybackurls`, `ctfr.py`, `jq`, `haktrails`, `curl`, `python3`.

## Usage
```bash
# make executable
chmod +x subenum.sh

# basic run (interactive)
./subenum.sh

# run with domain argument
./subenum.sh example.com

# provide optional environment variables:
export BUFFER_API_KEY="your_bufferover_key_here"
export GITHUB_TOKENS_FILE="/path/to/github_tokens.txt"   # newline separated tokens
./subenum.sh example.com
