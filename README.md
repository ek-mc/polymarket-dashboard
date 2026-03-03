# polymarket-dashboard

Terminal dashboard for Polymarket events using `polymarket` CLI.

## Requirements

- `polymarket` CLI installed and authenticated
- `python3`
- Bash shell

## Install

```bash
chmod +x polymarket-dashboard
sudo cp polymarket-dashboard /usr/local/bin/polymarket-dashboard
```

## Help

```bash
polymarket-dashboard --help
```

## Common usage

```bash
# Default top volume
polymarket-dashboard

# Top 20 by volume
polymarket-dashboard --top 20

# Top 50 by volume
polymarket-dashboard --top 50 --fetch 120

# Newest 50
polymarket-dashboard --top 50 --newest --fetch 140

# Biggest movers
polymarket-dashboard --top 20 --movers

# Movers with volume filters
polymarket-dashboard --top 20 --movers --min-24h-vol 100k
polymarket-dashboard --top 20 --movers --min-24h-vol 1m

# Balanced (closest to 50¢)
polymarket-dashboard --top 20 --balanced

# Category filters
polymarket-dashboard --top 20 --category politics
polymarket-dashboard --top 20 --category crypto
polymarket-dashboard --top 20 --category sports
polymarket-dashboard --top 20 --category gaming
```

## Live refresh

```bash
watch -c -n 10 polymarket-dashboard --top 20
```

If colors are stripped by your terminal:

```bash
FORCE_COLOR=1 watch -c -n 10 polymarket-dashboard --top 20
```

## Notes

- `--top` = how many rows shown
- `--fetch` = how many events fetched before ranking/filtering
- `--min-24h-vol` accepts suffixes like `100k`, `1m`
- Category mode uses Polymarket tag filtering (`--tag`)

## License

MIT. See [LICENSE](LICENSE).

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

