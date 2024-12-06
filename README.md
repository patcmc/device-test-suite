# Device Test Suite

## Development

Please install `patcmd` gem

```
gem install patcmd
```

### Git submodules

Fetch and checkout the latest commit for each submodule:

```bash
git submodule update --remote --merge
```

### Projects

1. Mastodon

```bash
patcmd exec project mastodon start --config=./.patcmd/config.yml
patcmd exec project mastodon setup --config=./.patcmd/config.yml
patcmd exec project mastodon dev --config=./.patcmd/config.yml
```

2. Chatwoot

```bash
patcmd exec project chatwoot build --config=./.patcmd/config.yml
patcmd exec project chatwoot start --config=./.patcmd/config.yml
```