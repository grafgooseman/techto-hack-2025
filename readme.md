# Techto Hack 2025

## Setup

### Install Cloudflare CLI (cloudflared)

**Option 1: Direct Download (Easiest)**
1. Go to: https://github.com/cloudflare/cloudflared/releases/latest
2. Download `cloudflared-windows-amd64.exe`
3. Rename it to `cloudflared.exe`
4. Put it in your project folder: `E:\techto-hack-2025\`

**Option 2: Using Chocolatey (if you have it)**
```bash
choco install cloudflared
```

**Option 3: Using Scoop (if you have it)**
```bash
scoop install cloudflared
```

**Option 4: Using PowerShell (Direct download)**
```powershell
# Download to your project folder
Invoke-WebRequest -Uri "https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-windows-amd64.exe" -OutFile "E:\techto-hack-2025\cloudflared.exe"
```

## Running the App

### Development with Tunnel
```bash
# Terminal 1: Start the Express server
pnpm run dev

# Terminal 2: Create tunnel to expose server
cloudflared tunnel --url http://localhost:3000
```

This will give you a public URL like `https://random-words-1234.trycloudflare.com` that forwards to your local server.