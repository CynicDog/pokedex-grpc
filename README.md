# pokedex-grpc

A minimal Python gRPC app using [`buf`](https://buf.build) for proto management and [`uv`](https://github.com/astral-sh/uv) for Python packaging.

This project was heavily helped by [“Protobuf dependency management with Buf”](https://www.youtube.com/watch?v=OSdQlnoO0og), so big thanks to Mike for hosting the tutorial.

I also wrote an article in more detail here: [What Buf Did for My Protos, uv Did for My Python Soul](https://cynicdog.github.io/posts/what-buf-did-for-my-protos-uv-did-for-my-python-soul/)

## Run `main.py` script

> Don't forget to tell Python to treat `proto/gen` as the root of the import tree before running python files:

```bash
PYTHONPATH=proto/gen uv run main.py
````

## Run gRPC Server and Client

### Terminal 1 — Start server:

```bash
PYTHONPATH=proto/gen uv run grpc_server.py
```

### Terminal 2 — Run client:

```bash
PYTHONPATH=proto/gen uv run grpc_client.py
```