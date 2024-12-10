# Device Test Suite

## Device Analysis

Estimate Linux server performance

```bash
curl -sL https://yabs.sh | bash
```

**Disable specific tests:**

Skip the disk test

```bash
curl -sL https://yabs.sh | bash -s -- -disk
```

Other options:

- `-net`: Skip the network test.
- `-ioping`: Skip the I/O latency test.

**Basic version (Non-Extended):**

```bash
curl -sL yabs.sh | bash -s -- -basic
```

## Development

Please install `patcmd` gem

```
gem install patcmd
```

### Git Submodules

Fetch and checkout the latest commit for each submodule:

```bash
patcmd exec git submodule update --config=./.patcmd/config.yml
```

### Container Collection

```bash
patcmd exec collection container start --config=./.patcmd/config.yml
patcmd exec collection container stop --config=./.patcmd/config.yml
```

### Projects

1. Mastodon

```bash
patcmd exec project mastodon start --config=./.patcmd/config.yml
patcmd exec project mastodon setup --config=./.patcmd/config.yml
patcmd exec project mastodon dev --config=./.patcmd/config.yml
patcmd exec project mastodon stop --config=./.patcmd/config.yml
```

2. Chatwoot

```bash
patcmd exec project chatwoot build --config=./.patcmd/config.yml
patcmd exec project chatwoot start --config=./.patcmd/config.yml
```

3. Discourse

```bash
# Run for the first time
patcmd exec project discourse init --config=./.patcmd/config.yml

patcmd exec project discourse boot --config=./.patcmd/config.yml
patcmd exec project discourse dev --config=./.patcmd/config.yml
patcmd exec project discourse cli --config=./.patcmd/config.yml
patcmd exec project discourse stop --config=./.patcmd/config.yml
```

4. Forem

```bash
patcmd exec project forem build --config=./.patcmd/config.yml
patcmd exec project forem start --config=./.patcmd/config.yml
```
