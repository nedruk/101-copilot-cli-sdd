# 101-copilot-cli-sdd

A quick guide to use copilot cli + a sample SDD project

## Workshop

The full workshop guide is available in [`docs/workshop/`](docs/workshop/00-index.md).

### Option 1: Run Directly

If you have Node.js 22+ installed, you can follow the workshop directly on your machine.

### Option 2: Run in Docker (Isolated Environment)

To try out the workshop without affecting your local environment, use Docker:

1. **Create the tryout folder** (if it doesn't exist):
   ```bash
   mkdir -p tryout
   ```

2. **Start the container:**
   ```bash
   docker run -it \
     --name copilot-workshop \
     -v "$(pwd)/tryout":/workspace \
     -w /workspace \
     ubuntu:24.04 \
     bash
   ```

3. **Inside the container**, install prerequisites:
   ```bash
   apt-get update && apt-get install -y curl git jq
   curl -fsSL https://deb.nodesource.com/setup_22.x | bash -
   apt-get install -y nodejs
   npm install -g @github/copilot
   ```

**Useful Docker commands:**

| Action | Command |
|--------|---------|
| Reconnect to stopped container | `docker start -ai copilot-workshop` |
| Open parallel shell | `docker exec -it copilot-workshop bash` |
| Remove container when done | `docker rm copilot-workshop` |
