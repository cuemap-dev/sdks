# CueMap SDKs

**Redis for AI Agents** - Client libraries for CueMap.

## Available SDKs

### Python

```bash
pip install cuemap
```

[Documentation](./python/README.md) • [PyPI](https://pypi.org/project/cuemap/)

### TypeScript/JavaScript

```bash
npm install cuemap
```

[Documentation](./typescript/README.md) • [NPM](https://www.npmjs.com/package/cuemap)

## Quick Start

### Python

```python
from cuemap import CueMap

client = CueMap()
client.add("Server password is abc123", cues=["server", "password"])
results = client.recall(["server", "password"])
```

### TypeScript

```typescript
import CueMap from 'cuemap';

const client = new CueMap();
await client.add("Server password is abc123", ["server", "password"]);
const results = await client.recall(["server", "password"]);
```

## Running the Engine

All SDKs require a running CueMap engine:

```bash
docker run -p 8080:8080 cuemap/engine:latest
```

Or from source:

```bash
git clone https://github.com/cuemap-dev/engine
cd engine
cargo build --release
./target/release/cuemap-rust --port 8080
```

## Links

- [Engine Repository](https://github.com/cuemap-dev/engine)

## License

MIT
