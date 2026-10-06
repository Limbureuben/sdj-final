# SDG Interactive — Dokploy deployment

This project is a static website and is packaged as an Nginx Docker image.

## Dokploy settings

Create an **Application** in Dokploy and connect the Git repository:

- **Build type:** `Dockerfile`
- **Dockerfile path:** `Dockerfile`
- **Build context:** repository root
- **Container port:** `80`
- **Publish:** enable HTTPS for the domain in Dokploy

Deploy the application after saving the settings. The container serves `Index.html` and the `resources/` assets.

## Local verification

```bash
docker build -t sdg-interactive .
docker run --rm -p 8080:80 sdg-interactive
```

Open http://localhost:8080.
